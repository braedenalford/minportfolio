---
title: "The Network of The Lord of the Rings"
date: 2021-05-21T15:34:30-04:00
categories:
  - project
tags:
  - Visualisations
  - Film
  - JavaScript
  - D3
---

<!DOCTYPE html>
<html>

<head>
	<title>The Network of The Lord of the Rings</title>
	<!-- Import pure.css -->
	<link rel="stylesheet" href="https://unpkg.com/purecss@2.0.3/build/pure-min.css" integrity="sha384-cg6SkqEOCV1NbJoCu11+bm0NvBRc8IYLRGXkmNrqUBfTjmMYwNKPWBTIKyw9mHNJ" crossorigin="anonymous">
	<meta name="viewport" content="width=device-width, initial-scale=1">
	<!-- Google font -->
	<link href="https://fonts.googleapis.com/css2?family=Source+Sans+Pro:wght@400;700;900&display=swap" rel="stylesheet">
	<!-- import d3 -->
	<script src="https://d3js.org/d3.v4.min.js"></script>
	<script src="https://d3js.org/d3-geo-projection.v3.min.js"></script>
	<!--
- FIT5147 Data Exploration and Visualisation
- Programming Exercise 3 D3 Template
- Created by: Kadek Satriadi
- Last update by Kadek Satriadi (27/04/2021)
-->
	<!-- custom style -->
	<style>
	* {
		font-family: 'Source Sans Pro', sans-serif;
	}
	
	h1 {
		font-weight: 900;
	}
	
	body {
		background-color: lightgray;
	}
	
	.page {
		width: 1200px;
		background-color: white;
		padding-left: 20px;
		padding-right: 20px;
		margin: auto;
	}
	
	.highlight-text {
		fill: #ff009d;
		font-size: 14px;
		font-weight: bold;
	}
	
	.normal-text {
		fill: #555;
		font-size: 12px;
		font-weight: bold;
	}
	
	svg {
		cursor: pointer;
	}
	
	.hover-link {
		stroke: greenyellow;
	}
	
	.highlight-link {
		stroke: #ff7f00;
	}
	
	.normal-link {
		stroke: #bbb;
		cursor: default;
	}
	
	#tooltip-container {
		position: absolute;
		background-color: white;
		padding: 2px 10px 2px 10px;
		visibility: hidden;
		border: 1px solid #555;
	}
	
	#tooltip-text {
		font-weight: bold;
	}
	</style>
</head>

<body>
	<!-- tooltip -->
	<div id="tooltip-container">
		<p id="tooltip-text">Tooltip text</p>
	</div>
	<div class="page">
		<!-- pure grid group -->
		<div class="pure-g">
			<div class="pure-u-2-3">
				<svg id="chart"></svg>
			</div>
			<div class="pure-u-1-3">
				<h1>The Network of <br /> The Lord of the Rings</h1>
				<p>This visualisation depicts the interactions among characters in The Lord of the Rings: The Return of The King movie.</p>
				<h2>Two Dominating Couples</h2>
				<p>Despite the fact that Sam and Frodo are (arguablly) the two key roles in the last movie of the The Lord of the Rings trilogy, their number of interaction is only slighly higher than the interaction between Gandalf and Pippin. Gandalf and Pippin played significant roles in the siege of Minas Tirith scenes. </p>
				<h2>Two Parallel Stories</h2>
				<p>Two node clusters are apparent in the network. These clusters are facinating depictions of the two parallel stories in the movie. One story is about the journey to the Mount Doom that Frodo, Sam, and Gollum undertook, while the other story is about the wars that took place in Minas Tirith and Mordor.</p>
			</div>
		</div>
		<!-- end pure grid group -->
		<div class="pure-g">
			<div class="pure-u-1-1 small-font">
				<p><strong>Data source: </strong>Kaminski, Jermain; Schober, Michael; Albaladejo, Raymond; Zastupailo, Oleksandr; Hidalgo, C
					<U+00E9>sar, 2018, Moviegalaxies - Social Networks in Movies, https://doi.org/10.7910/DVN/T4HBA3, Harvard Dataverse, V3 </p>
			</div>
		</div>
		<!-- end pure grid group -->
	</div>
	<!-- end page -->
	<script type="text/javascript">
	var width = 750;
	var height = 700;
	// the data is stored online, use this path to load the data
	var dataPath = "https://raw.githubusercontent.com/KadekSatriadi/TheLordOfTheRingsNetworkData/main/LOTR_3.json";
	// select the svg element
	var svg = d3.select("#chart").attr("width", width).attr("height", height);
	// your script goes here
	// https://bl.ocks.org/heybignick/3faf257bbbbc7743bb72310d03b86ee8 was used to help act as a basis for my learning. 
	// establishing tooltip container and text 
	var toolTipContainer = d3.select("#tooltip-container").style("class", "#tooltip-container");
	var toolTipText = d3.select("tooltip-text").style("class", "#tooltip-text");
	// creating the force we apply to the network graph. Link applies to the links between nodes. Charge applies to the force repulsing each node from one another. 
	// Center relates to the nodes being attracted to the center of the svg canvas.
	var simulation = d3.forceSimulation().force("link", d3.forceLink().id(function(d) {
		return d.id;
	})).force("charge", d3.forceManyBody().strength(-200)).force("center", d3.forceCenter(width / 2, height / 2));
	d3.json(dataPath, function(data) {
		// https://www.d3-graph-gallery.com/graph/interactivity_tooltip.html#customContent was used in aid of creating the tooltip.
		// creating the links.
		var link = svg.append("g").selectAll("line").data(data.links).enter().append("line")
			// if statement to check if the link should be highlighted, otherwise keep as a normal-link class. This approach does not rely on checking the data first to find the index of the target links and nodes
			.attr("class", function(d) {
				if(((d.to == "GANDALF") || (d.from == "GANDALF")) && ((d.to == "PIPPIN") || (d.from == "PIPPIN")) || ((d.to == "FRODO") || (d.from == "FRODO")) && ((d.to == "SAM") || (d.from == "SAM"))) {
					return "highlight-link"
				} else {
					return "normal-link"
				}
			})
			// setting the width based on the weight
			.attr("stroke-width", function(d) {
				return d.weight;
			})
			// on mouseover we change the link class to hover-link which changes the colour. 
			// we also make the tooltip visible and set the location near the link/pointer location.
			// for the text in the tooltip, we want to output a set message, however this is slightly different if the link weight is 1, as no plural.
			.on("mouseover", function(d) {
				d3.select(this).attr("class", "hover-link")
				toolTipContainer.style("visibility", "visible").style("left", d3.event.pageX + 50 + "px").style("top", d3.event.pageY - 70 + "px")
				if(d.weight != 1) {
					document.getElementById("tooltip-text").innerHTML = d.from + " interacted with " + d.to + " " + d.weight + " times.";
				} else {
					document.getElementById("tooltip-text").innerHTML = d.from + " interacted with " + d.to + " " + d.weight + " time.";
				}
			})
			// on mouseout, we want to change our class for the link back to what it previously was, as well as set the tooltip to be hidden.
			.on("mouseout", function(d) {
				d3.select(this).attr("class", function(d) {
					if(((d.to == "GANDALF") || (d.from == "GANDALF")) && ((d.to == "PIPPIN") || (d.from == "PIPPIN")) || ((d.to == "FRODO") || (d.from == "FRODO")) && ((d.to == "SAM") || (d.from == "SAM"))) {
						return "highlight-link"
					} else {
						return "normal-link"
					}
				})
				toolTipContainer.style("visibility", "hidden");
			});
		// creating the nodes for the network based on the data given.
		var node = svg.append("g").attr("class", "nodes").selectAll("g").data(data.nodes).enter().append("g")
			// appending circles to these nodes.
		var circles = node.append("circle").attr("r", 8).attr("stroke", "#FFFFFF").attr("fill", "#8B45DF")
			// adding some interactivity with the nodes and circles to add a bit of life into the graph. Help to create this was using the above links.
			.call(d3.drag().on("start", dragstarted).on("drag", dragged).on("end", dragended));
		// adding text for each of the nodes. The text is set as the node's name.
		// we also want to highlight certain nodes from the given links and nodes to highlight, so we change the class for these.
		var labels = node.append("text").text(function(d) {
			return d.name;
		}).attr("class", function(d) {
			if(["GANDALF", "PIPPIN", "FRODO", "SAM"].includes(d.name)) {
				return "highlight-text"
			} else {
				return "normal-text"
			}
		}).attr('x', -20).attr('y', -10);
		simulation.nodes(data.nodes).on("tick", ticked);
		simulation.force("link").links(data.links);

		function ticked() {
			link.attr("x1", function(d) {
				return d.source.x;
			}).attr("y1", function(d) {
				return d.source.y;
			}).attr("x2", function(d) {
				return d.target.x;
			}).attr("y2", function(d) {
				return d.target.y;
			});
			node.attr("transform", function(d) {
				return "translate(" + d.x + "," + d.y + ")";
			})
		}
	});

	function dragstarted(d) {
		if(!d3.event.active) simulation.alphaTarget(0.1).restart();
		d.fx = d.x;
		d.fy = d.y;
	}

	function dragged(d) {
		d.fx = d3.event.x;
		d.fy = d3.event.y;
	}

	function dragended(d) {
		if(!d3.event.active) simulation.alphaTarget(0);
		d.fx = null;
		d.fy = null;
	}
	</script>
</body>

</html>
