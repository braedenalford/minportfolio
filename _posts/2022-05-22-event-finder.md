---
title: "Event Finder"
date: 2022-05-22T15:34:30-04:00
categories:
  - project
tags:
  - Events
  - JavaScript
  - Ticketmaster
---

<!-- Latest compiled and minified JavaScript -->
<!-- First include jquery js -->
<script src="//code.jquery.com/jquery-1.12.0.min.js"></script>
<script src="//code.jquery.com/jquery-migrate-1.2.1.min.js"></script>

<!-- Then include bootstrap js -->
<script src="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.6/js/bootstrap.min.js" integrity="sha384-0mSbJDEHialfmuBBQP6A4Qrprq5OVfW37PRR3j5ELqxss1yVqOtnepnHVP9aJ7xS" crossorigin="anonymous"></script>

<style>
	form {
	    margin: 0 0 5px 0;
	    padding: 1em;
	    background-color: #f3f6f6;
	}
	.elementor-widget-text-editor {
		color: #212529;
		font-family: var( --e-global-typography-text-font-family ), Sans-serif;
		font-weight: var( --e-global-typography-text-font-weight );
	}
	
	label {
		display: initial !important;
		font-family: var( --e-global-typography-text-font-family ), Sans-serif;
		margin-bottom: 5px;
	}
	
	.form-group.callbackFamily {
		padding-bottom: 30.39px;
	}
	
	label.col-sm-2.control-label {font-family: var( --e-global-typography-text-font-family ), Sans-serif;
	font-weight: bold;font-size: 18px;margin-bottom: 10px;}
	.well {
	color: #212529;
	border-radius: 0.25rem;
	font-family: var( --e-global-typography-text-font-family ), Sans-serif;
	font-weight: var( --e-global-typography-text-font-weight );
	min-height: 20px;
	padding: 19px;
	margin-bottom: 20px;
	background-color: #f1f1f1;
	border: 1px solid #ced4da;
	border-radius: 4px
	px
	;
	-webkit-box-shadow: inset 0 1px 1px rgb(0 0 0 / 5%);
	box-shadow: inset 0 1px 1px rgb(0 0 0 / 5%);
	}
	.hidden {
	display: none;
	}

	.pagination>li>a, .pagination>li>span {position: relative;
	float: left;
	padding: 6px 12px;
	line-height: 1.5;
	color: #000;
	text-transform: uppercase;text-align: center;text-decoration: none;
	background-color: #F7BF50;
	border: 1px solid #ddd;font-weight: 600;font-size: 1rem;font-family: Montserrat,sans-serif;
    border-top-left-radius: 4px;
    border-bottom-left-radius: 4px;}

	.pagination>li:last-child>a, .pagination>li:last-child>span {border-top-right-radius: 0.25rem;
    border-bottom-right-radius: 0.25rem;
    border-top-left-radius: 0 !important;
    border-bottom-left-radius: 0 !important;}

	.pagination>li:last-child>a, .pagination>li:last-child>span {border-top-right-radius: 4px;
	border-bottom-right-radius: 4px;}

	li.page-item {}

	.pagination>li {display: inline;}

	li.page-item {}

	.pagination>li:first-child>a, .pagination>li:first-child>span {margin-left: 0;
	border-top-left-radius: 4px;
	border-bottom-left-radius: 4px;margin-left: -18px;}

	.pagination>li>a:hover {color: #fff;}
	.btn {
	font-weight: 600;
	font-size: 16px;
	display: inline-block;
	color: #212529;
	background-color: #545b62;
	text-align: center;
	vertical-align: middle;
	-webkit-user-select: none;
	-moz-user-select: none;
	-ms-user-select: none;
	user-select: none;
	background-color: transparent;
	border: 1px solid transparent;
	padding: 0.375rem 0.75rem;
	font-size: 1rem;
	line-height: 1.5;
	border-radius: 0.25rem;
	transition: color .15s ease-in-out,background-color .15s ease-in-out,border-color .15s ease-in-out,box-shadow .15s
	ease-in-out;
	}
	.btn-secondary, .btn-secondary:focus, .btn-secondary:active {
	color: #000;
	background-color: #F7BF50 !important;
	border-color: #F7BF50 !important;
	box-shadow: none;
	}
	body {
	padding-top: 50px;
	overflow: hidden;
	font-family: Calibri, "Times new roman", Serif;
	}
	.form-control {display: block;
	width: 100%;
	height: 34px;
	padding: 6px 12px;
	font-size: 16px;
	line-height: 1.42857143;
	color: #555;
	
	background-image: none;
	border: 1px solid #ccc;
	left: 100px;border-radius: 4px;
	-webkit-box-shadow: inset 0 1px 1px rgb(0 0 0 / 8%);
	box-shadow: inset 0 1px 1px rgb(0 0 0 / 8%);
	-webkit-transition: border-color ease-in-out .15s,-webkit-box-shadow ease-in-out .15s;
	-o-transition: border-color ease-in-out .15s,box-shadow ease-in-out .15s;
	transition: border-color ease-in-out .15s,box-shadow ease-in-out .15s;}

	input[type=text] {background-color: #f1f1f1;width: 100%;}

	.btn-block {width: 100%;}

	.form-group {}

	.rowClear {
	display: flex;
	flex-wrap: none;
	margin-right: -15px;
	margin-left: 0px;
	margin-top: -38px;
	}

	.btn-secondary:hover {color: #fff;}

	.btn-default:hover {color: #fff;}

	.btn-default {color: #fff;background: #32373C;}

	.btn-default:hover {border-color: #F7BF50;color: #000;background: #F7BF50;}

	.row {
	display: flex;
	flex-wrap: wrap;
	margin-right: 0px;
	margin-left: 713px;
	margin-top: 0px;}

	#wrapper {
	min-height: 100%;
	height: 100%;
	width: 100%;
	position: absolute;
	top: 0px;
	left: 0;
	display: inline-block;
	}
	#main-wrapper {
	height: 100%;
	overflow-y: auto;
	padding: 50px 0 0px 0;
	}

	#main {
	position: relative;
	height: 100%;
	overflow-y: auto;
	padding: 0 15px;
	}

	#sidebar-wrapper {
	height: 100%;
	padding: 50px 0 0px 0;
	position: fixed;
	border-right: 1px solid gray;
	}

	#sidebar {
	position: relative;
	height: 100%;
	overflow-y: auto;
	}

	#sidebar .list-group-item {
	border-radius: 0;
	border-left: 0;
	border-right: 0;
	border-top: 0;
	}

	.headline {
	width: 100%;
	height: 40px;
	background: #eee;
	margin-bottom: 20px;
	border-top: solid 1px #ccc;
	border-bottom: solid 1px #ccc;
	}

	.headline p {
	position: relative;
	top: 10px;
	left: 150px;
	font-weight: 700;
	}

	.btn {
	display: inline-block;
	}

	@media (max-width: 992px) {
	body {
	padding-top: 0px;
	}
	}

	@media (min-width: 992px) {
	#main-wrapper {
	float: right;
	}
	}

	@media (max-width: 992px) {
	#main-wrapper {
	padding-top: 0px;
	}
	}

	@media (max-width: 992px) {
	#sidebar-wrapper {
	position: static;
	height: auto;
	max-height: 300px;
	border-right: 0;
	}
	}
	.callback{

	}
	.callbackMusic{
	display:none;
	}
	.callbackSport{
	display:none;
	}
	.callbackArt{
	display:none;
	}
	.callbackFamily{
	display:none;
	}
	body{
	overflow:scroll
	}
	summary {
	display: list-item
	}
	
	
</style>

<form class="form-horizontal">
	<div class="form-group">
		<label for="state" class="col-sm-2 control-label">State</label>
		<div class="col-sm-4">
			<select class="selectpicker form-control" name="state">
				<option>All</option>
				<option>New South Wales</option>
				<option>Victoria</option>
				<option>Queensland</option>
				<option>South Australia</option>
				<option>Western Australia</option>
				<option>Tasmania</option>
				<option>Northern Territory</option>
				<option>Australian Capital Territory</option>
			</select>
		</div>
		<br>
	</div>

	<div class="form-group">
		<label for="eventTypes" class="col-sm-2 control-label">Event Type</label>
		<div class="col-sm-4">
            <div id="eventTypes">
                <div class="form-check">
                    <input class="form-check-input" type="radio" value="All" name="flexRadioDefault" id="flexRadioAll" checked onclick="changeType()">
                    <label class="form-check-label" for="flexRadioAll">
                        All
                    </label>
                </div>
                <div class="form-check">
                    <input class="form-check-input" type="radio" value="Music" name="flexRadioDefault" id="flexRadioMusic" onclick="changeType()">
                    <label class="form-check-label" for="flexRadioMusic">
                        Music
                    </label>
                </div>
                <div class="form-check">
                    <input class="form-check-input" type="radio" value="Sport" name="flexRadioDefault" id="flexRadioSport" onclick="changeType()">
                    <label class="form-check-label" for="flexRadioSport">
                        Sport
                    </label>
                </div>
                <div class="form-check">
                    <input class="form-check-input" type="radio" value="Art" name="flexRadioDefault" id="flexRadioArts" onclick="changeType()">
                    <label class="form-check-label" for="flexRadioArts">
                        Arts, Theatre & Comedy
                    </label>
                </div>
                <div class="form-check">
                    <input class="form-check-input" type="radio" value="Family" name="flexRadioDefault" id="flexRadioFamily" onclick="changeType()">
                    <label class="form-check-label" for="flexRadioFamily">
                        Family & Attractions
                    </label>
                </div>
            </div>
		</div>
		<br>
	</div>
   

	<div class="form-group callback">
		<label for="crops" class="col-sm-2 control-label">Event Subtype</label>
		<div class="col-sm-4">
			<select class="subselectpickerall form-control" name="default">
				<option>All</option>
			</select>
		</div>
		<br>
	</div>

	<div class="form-group callbackMusic">
		<label for="crops" class="col-sm-2 control-label">Event Subtype</label>
		<div class="col-sm-4">
			<select class="subselectpickermusic form-control" name="music">
				<option>All</option>
				<option>Alternative Rock</option>
				<option>Cabaret</option>
				<option>Country and Folk</option>
				<option>Dance/Electronic</option>
				<option>Festivals</option>
				<option>Hard Rock/Metal</option>
				<option>Jazz and Blues</option>
				<option>Miscellaneous</option>
				<option>New Age and Spiritual</option>
				<option>R&B/Urban Soul</option>
				<option>Rap and Hip-Hop</option>
				<option>Pop Rock</option>
				<option>Pop</option>
				<option>World Music</option>
				<option>Other</option>
			</select>
		</div>
		<br>
	</div>

	<div class="form-group callbackSport">
		<label for="crops" class="col-sm-2 control-label">Event Subtype</label>
		<div class="col-sm-4">
			<select class="subselectpickersport form-control" name="sport">
				<option>All</option>
				<option>AFL</option>
				<option>Basketball</option>
				<option>Boxing</option>
				<option>Competitions</option>
				<option>Cricket</option>
				<option>Field Sport</option>
				<option>Golf</option>
				<option>Handball</option>
				<option>Hockey</option>
				<option>Horse Racing</option>
				<option>MMA</option>
				<option>Motorsport</option>
				<option>Netball</option>
				<option>Rugby League</option>
				<option>Rugby Union</option>
				<option>Soccer</option>
				<option>Tennis</option>
				<option>Wrestling</option>
				<option>Other</option>
			</select>
		</div>
		<br>
	</div>

	<div class="form-group callbackArt">
		<label for="crops" class="col-sm-2 control-label">Event Subtype</label>
		<div class="col-sm-4">
			<select class="subselectpickerart form-control" name="art">
				<option>All</option>
				<option>Ballet and Dance</option>
				<option>Classical</option>
				<option>Comedy</option>
				<option>Fashion</option>
				<option>Museums and Exhibits</option>
				<option>Musicals</option>
				<option>Opera</option>
				<option>Plays</option>
				<option>Other</option>
			</select>
		</div>
		<br>
	</div>

	<div class="form-group callbackFamily">
		<label for="crops" class="col-sm-2 control-label">Event Subtype</label>
		<div class="col-sm-4">
			<select class="subselectpickerfamily form-control" name="family">
				<option>All</option>
				<option>Children's Music and Theatre</option>
				<option>Circus</option>
				<option>Fairs and Festivals</option>
				<option>Family Attractions</option>
				<option>Ice Shows</option>
				<option>Magic Shows</option>
				<option>Other</option>
			</select>
		</div>
	</div>
<div class="row">
		<div class="col-sm-offset-1 col-sm-10">
			<button type="button" class="btn btn-secondary" onclick="onSearchResultsClick()">Search Results</button>
		</div>
	</div>
	

	
	<div id="searchResults">
	</div>
	<nav aria-label="Page navigation example">
		<ul class="pagination">
			<br>
			<li class="page-item hidden"><a class="page-link hidden" onclick="previousPageData()">Previous</a></li>
			<li class="page-item hidden"><a class="page-link hidden" onclick="nextPageData()">Next</a></li>
		</ul>
	</nav>

<script>
	var currentQuery;

	$('input[type=radio]').on('change', function () {
		if ($(this).val() == "Music") {
			$('.upload').hide();
			$('.callback').hide();
			$('.callbackSport').hide();
			$('.callbackArt').hide();
			$('.callbackFamily').hide();
			$('.callbackMusic').show();
		} else if ($(this).val() == "Sport") {
			$('.upload').hide();
			$('.callback').hide();
			$('.callbackSport').show();
			$('.callbackArt').hide();
			$('.callbackFamily').hide();
			$('.callbackMusic').hide();
		} else if ($(this).val() == "Art") {
			$('.upload').hide();
			$('.callback').hide();
			$('.callbackSport').hide();
			$('.callbackArt').show();
			$('.callbackFamily').hide();
			$('.callbackMusic').hide();
		} else if ($(this).val() == "Family") {
			$('.upload').hide();
			$('.callback').hide();
			$('.callbackSport').hide();
			$('.callbackArt').hide();
			$('.callbackFamily').show();
			$('.callbackMusic').hide();
		} else if ($(this).val() == "All") {
			$('.upload').hide();
			$('.callback').show();
			$('.callbackSport').hide();
			$('.callbackArt').hide();
			$('.callbackFamily').hide();
			$('.callbackMusic').hide();
		}
	});


	stateDict = {
		"All": "All",
		"New South Wales": "NSW",
		"Victoria": "VIC",
		"Queensland": "QLD",
		"South Australia": "SA",
		"Western Australia": "WA",
		"Tasmania": "TAS",
		"Northern Territory": "NT",
		"Australian Capital Territory": "ACT"
	}

	async function getEventData(state, keyword) {

		const loadingOverlay = document.getElementsByClassName('loading-overlay')?.[0];

		var res;
		if (state == "All") {
			currentQuery =
				`https://app.ticketmaster.com/discovery/v2/events.json?keyword=${keyword}&countryCode=AU&apikey=KiqhEiBfJaj2xsSb0iNNO8rp7zislaiC&countryCode=AU&sort=date,asc&size=10`
			res = await
			fetch(`https://app.ticketmaster.com/discovery/v2/events.json?keyword=${keyword}&countryCode=AU&apikey=KiqhEiBfJaj2xsSb0iNNO8rp7zislaiC&countryCode=AU&sort=date,asc&size=10`);
		} else if (state == undefined) {
			currentQuery =
				`https://app.ticketmaster.com/discovery/v2/events.json?keyword=${keyword}&countryCode=AU&apikey=KiqhEiBfJaj2xsSb0iNNO8rp7zislaiC&countryCode=AU&sort=date,asc&size=10`
			res = await
			fetch(`https://app.ticketmaster.com/discovery/v2/events.json?keyword=${keyword}&countryCode=AU&apikey=KiqhEiBfJaj2xsSb0iNNO8rp7zislaiC&countryCode=AU&sort=date,asc&size=10`);
		} else {
			currentQuery =
				`https://app.ticketmaster.com/discovery/v2/events.json?keyword=${keyword}&countryCode=AU&apikey=KiqhEiBfJaj2xsSb0iNNO8rp7zislaiC&stateCode=${state}&sort=date,asc&size=10`
			res = await
			fetch(`https://app.ticketmaster.com/discovery/v2/events.json?keyword=${keyword}&countryCode=AU&apikey=KiqhEiBfJaj2xsSb0iNNO8rp7zislaiC&stateCode=${state}&sort=date,asc&size=10`);
		}
		const json = await res.json();

		var element = document.getElementsByClassName("page-item hidden");
		for (i = 0; i < element.length; i++) {
			element[i].classList.remove("hidden");
		}
		var
			element = document.getElementsByClassName("page-item hidden");
		for (i = 0; i < element.length; i++) {
			element[i].classList.remove("hidden");
		}
		var element = document.getElementsByClassName("page-link hidden");
		for (i = 0; i < element.length; i++) {
			element[i].classList.remove("hidden");
		}
		var
			element = document.getElementsByClassName("page-link hidden");
		for (i = 0; i < element.length; i++) {
			element[i].classList.remove("hidden");
		}
		return json;
	}
	async function youGotNextMarty(url) {
		const
			loadingOverlay = document.getElementsByClassName('loading-overlay')?.[0];
		var res;
		res = await fetch(url);
		const
			json = await res.json();
		return json;
	}
	var selectedItemState, selectedItemType, selectedItemSubtypeAll, selectedItemSubtypeMusic, selectedItemSubtypeSport, selectedItemSubtypeArt, selectedItemSubtypeFamily;
	var subtypeActive = -1;
	$('.selectpicker').change(function () {
		selectedItemState = $('.selectpicker').val();
	});
	
    function changeType(){
        selectedItemType = document.querySelector('input[type=radio]:checked').value;
        console.log(selectedItemType)
    }



	$('.subselectpickerall').change(function () {
		selectedItemSubtypeAll = $('.subselectpickerall').val();
		subtypeActive = 0;
	});
	$('.subselectpickermusic').change(function () {
		selectedItemSubtypeMusic = $('.subselectpickermusic').val();
		subtypeActive = 1;
	});
	$('.subselectpickersport').change(function () {
		selectedItemSubtypeSport = $('.subselectpickersport').val();
		subtypeActive = 2;
	});
	$('.subselectpickerart').change(function () {
		selectedItemSubtypeArt = $('.subselectpickerart').val();
		subtypeActive = 3;
	});
	$('.subselectpickerfamily').change(function () {
		selectedItemSubtypeFamily = $('.subselectpickerfamily').val();
		subtypeActive = 4;
	});
	$("#clear :button").click(function () {
		$('select[name=state]').val('All');
		$('select[name=eventTypes]').val('All');
		$('select[name=default]').val('All');
		$('select[name=music]').val('All');
		$('select[name=sport]').val('All');
		$('select[name=art]').val('All');
		$('select[name=family]').val('All');
	});
	var
		currentQuery;
	var pageNo;

	function onSearchResultsClick() {
		state = selectedItemState 
		category = selectedItemType

		if (subtypeActive == -1) {
			keyword = category
		}
		if (subtypeActive == 0) {
			keyword = ''
		} else if (subtypeActive == 1) {
			if (selectedItemSubtypeMusic == 'All') {
				keyword = category
			} else {
				if (selectedItemSubtypeMusic == 'All') {
					keyword = category
				} else {
					keyword = selectedItemSubtypeMusic
				}
			}
		} else if (subtypeActive == 2) {
			if (selectedItemSubtypeSport == 'All') {
				keyword = category
			} else {
				if (selectedItemSubtypeSport == undefined) {
					keyword = category
				} else {
					keyword = selectedItemSubtypeSport
				}
			}
		} else if (subtypeActive == 3) {
			if (selectedItemSubtypeArt == 'All') {
				keyword = category
			} else {
				if (selectedItemSubtypeArt == undefined) {
					keyword = category
				} else {
					keyword = selectedItemSubtypeArt
				}
			}
		} else if (subtypeActive == 4) {
			if (selectedItemSubtypeFamily == 'All') {
				keyword = category
			} else {
				if (selectedItemSubtypeFamily == undefined) {
					keyword = category
				} else {
					keyword = selectedItemSubtypeFamily
				}
			}
		}
		eventData = getEventData(stateDict[state], keyword)
		eventData.then(function (result) {
			pageNo = result.page.number
            if (result.page.totalElements == 0) {
				document.getElementById("searchResults").innerHTML += "<div class='well'>" + "<br>" + "<b>No Results Found...</b>" +
					"</div>"
			}
            else{
                eventData = result._embedded.events
                for (i = 0; i < eventData.length; i++) {

                    eventCity = result._embedded.events[i]._embedded.venues[0].city.name
                    eventState = result._embedded.events[i]._embedded.venues[0].state.name

                    timeString = eventData[i].dates.start.localTime // Prepend any date. Use your birthday. 
                    const timeString12hr=new Date('1970-01-01T' + timeString + 'Z').toLocaleTimeString('en-US', {
                        timeZone: 'UTC',
                        hour12: true,
                        hour: 'numeric',
                        minute: 'numeric'
                    });
                    if (eventData[i].info == '.') {
                        var
                            eventInfo = 'No additional Information'
                    } else {
                        var eventInfo = eventData[i].info
                    }
                    if (parseInt(eventData[i].dates.start.localDate) < 2022) {} else if (parseInt(eventData[i].dates.start.localDate) > 2025) {} else {
                        eventDate = eventData[i].dates.start.localDate.split('-')[2] + "/" + eventData[i].dates.start.localDate.split('-')[1] + "/" + eventData[i].dates.start.localDate.split('-')[0]

                        
                        document.getElementById('searchResults').innerHTML += "<div class='well' id='result'><p style = 'font-size:18px' >" + " <b> " + eventData[i].name + " </b>" + "<br></p> <b> Date: </b>" + eventDate + "<br><b>Time:</b> " +
                            timeString12hr + "<br><b>Location:</b> " + (eventData[i]._embedded.venues[0].name).split(',')[0] + " - " + eventCity + ", " + eventState + "<br> <a href = " + eventData[i].url + " target ='_blank'> <b> Buy Tickets </b></a> " +
                            "<br> <details><summary> <b> Information </b></summary><p> " + eventInfo + " </p> </details>" + " </div>"
                    }
                }
            }
		})


		document.getElementById("searchResults").innerHTML = "<br>"

	}


	function nextPageData() {

		state = selectedItemState
		category = selectedItemType

		if (subtypeActive == -1) {
			keyword = category
		}

		if (subtypeActive == 0) {
			keyword = ''
		} else if (subtypeActive == 1) {
			if (selectedItemSubtypeMusic == 'All') {
				keyword = category
			} else {
				if (selectedItemSubtypeMusic == 'All') {
					keyword = category
				} else {
					keyword = selectedItemSubtypeMusic
				}
			}

		} else if (subtypeActive == 2) {
			if (selectedItemSubtypeSport == 'All') {
				keyword = category
			} else {
				if (selectedItemSubtypeSport == undefined) {
					keyword = category
				} else {
					keyword = selectedItemSubtypeSport
				}
			}
		} else if (subtypeActive == 3) {
			if (selectedItemSubtypeArt == 'All') {
				keyword = category
			} else {
				if (selectedItemSubtypeArt == undefined) {
					keyword = category
				} else {
					keyword = selectedItemSubtypeArt
				}
			}
		} else if (subtypeActive == 4) {
			if (selectedItemSubtypeFamily == 'All') {
				keyword = category
			} else {
				if (selectedItemSubtypeFamily == undefined) {
					keyword = category
				} else {
					keyword = selectedItemSubtypeFamily
				}
			}
		}

		if (pageNo = 0) {
			if (state == "All") {
				currentQuery =
					`https://app.ticketmaster.com/discovery/v2/events.json?keyword=${keyword}&countryCode=AU&apikey=KiqhEiBfJaj2xsSb0iNNO8rp7zislaiC&countryCode=AU&sort=date,asc&size=10`
			} else if (state == undefined) {
				currentQuery =
					`https://app.ticketmaster.com/discovery/v2/events.json?keyword=${keyword}&countryCode=AU&apikey=KiqhEiBfJaj2xsSb0iNNO8rp7zislaiC&countryCode=AU&sort=date,asc&size=10`
			} else {
				currentQuery =
					`https://app.ticketmaster.com/discovery/v2/events.json?keyword=${keyword}&countryCode=AU&apikey=KiqhEiBfJaj2xsSb0iNNO8rp7zislaiC&stateCode=${stateDict[state]}&sort=date,asc&size=10`
			}
		}



		eventData = youGotNextMarty(currentQuery)

		eventData.then(function (result) {



			pageNo = result.page.number + 1
			if (result.page.totalElements == 0) {
				document.getElementById("searchResults").innerHTML += "<div class='well'>" + "<b>No Results Found...</b>" +
					"</div>"
			}
			eventData = result._embedded.events
			try {
				nextQuery = "https://app.ticketmaster.com" + result._links.next.href + "&apikey=KiqhEiBfJaj2xsSb0iNNO8rp7zislaiC"
				
							currentQuery = nextQuery
			eventData = youGotNextMarty(nextQuery)


			eventData.then(function (result) {

				eventData = result._embedded.events

				if (result.page.totalElements == 0) {
					document.getElementById("searchResults").innerHTML = "<div class='well'>" + "<br>" + "<b>No Results Found.</b>" + " </div>"
				}

				for (i = 0; i < eventData.length; i++) {

                    eventCity = result._embedded.events[i]._embedded.venues[0].city.name
                    eventState = result._embedded.events[i]._embedded.venues[0].state.name

					timeString = eventData[i].dates.start.localTime // Prepend any date. Use your birthday.
					const timeString12hr = new Date('1970-01-01T' + timeString + 'Z').toLocaleTimeString('en-US', {
						timeZone: 'UTC',
						hour12: true,
						hour: 'numeric',
						minute: 'numeric'
					});
					if (eventData[i].info == '.') {
						var
							eventInfo = 'No additional Information'
					} else {
						var eventInfo = eventData[i].info
					}
					if (parseInt(eventData[i].dates.start.localDate) < 2022) {} else if (parseInt(eventData[i].dates.start.localDate) >
						2025) {} else {
						eventDate = eventData[i].dates.start.localDate.split('-')[2] + "/" + eventData[i].dates.start.localDate.split('-')[1] + "/" + eventData[i].dates.start.localDate.split('-')[0]

                        document.getElementById('searchResults').innerHTML += "<div class='well' id='result'><p style = 'font-size:18px' >" + " <b> " + eventData[i].name + " </b>" + "<br></p> <b> Date: </b>" + eventDate + "<br><b>Time:</b> " +
                            timeString12hr + "<br><b>Location:</b> " + (eventData[i]._embedded.venues[0].name).split(',')[0] + " - " + eventCity + ", " + eventState + "<br> <a href = " + eventData[i].url + " target ='_blank'> <b> Buy Tickets </b></a> " +
                            "<br> <details><summary> <b> Information </b></summary><p> " + eventInfo + " </p> </details>" + " </div>"
                        }
				}

			})
			} catch {
				document.getElementById("searchResults").innerHTML += "<div class='well'>" + "<b>No More Results...</b>" +
					"</div>"
			}




		})


		document.getElementById("searchResults").innerHTML = "<br>"

	}

	function previousPageData() {

		state = selectedItemState
		category = selectedItemType

		if (subtypeActive == -1) {
			keyword = category
		}

		if (subtypeActive == 0) {
			keyword = ''
		} else if (subtypeActive == 1) {
			if (selectedItemSubtypeMusic == 'All') {
				keyword = category
			} else {
				if (selectedItemSubtypeMusic == 'All') {
					keyword = category
				} else {
					keyword = selectedItemSubtypeMusic
				}
			}

		} else if (subtypeActive == 2) {
			if (selectedItemSubtypeSport == 'All') {
				keyword = category
			} else {
				if (selectedItemSubtypeSport == undefined) {
					keyword = category
				} else {
					keyword = selectedItemSubtypeSport
				}
			}
		} else if (subtypeActive == 3) {
			if (selectedItemSubtypeArt == 'All') {
				keyword = category
			} else {
				if (selectedItemSubtypeArt == undefined) {
					keyword = category
				} else {
					keyword = selectedItemSubtypeArt
				}
			}
		} else if (subtypeActive == 4) {
			if (selectedItemSubtypeFamily == 'All') {
				keyword = category
			} else {
				if (selectedItemSubtypeFamily == undefined) {
					keyword = category
				} else {
					keyword = selectedItemSubtypeFamily
				}
			}
		}

		console.log(pageNo)
		if (pageNo != 0) {
			if (state == "All") {
				previousQuery =
					`https://app.ticketmaster.com/discovery/v2/events.json?keyword=${keyword}&countryCode=AU&apikey=KiqhEiBfJaj2xsSb0iNNO8rp7zislaiC&countryCode=AU&sort=date,asc&size=10&page=${pageNo-1}`
			} else if (state == undefined) {
				previousQuery =
					`https://app.ticketmaster.com/discovery/v2/events.json?keyword=${keyword}&countryCode=AU&apikey=KiqhEiBfJaj2xsSb0iNNO8rp7zislaiC&countryCode=AU&sort=date,asc&size=10&page=${pageNo-1}`
			} else {
				previousQuery =
					`https://app.ticketmaster.com/discovery/v2/events.json?keyword=${keyword}&countryCode=AU&apikey=KiqhEiBfJaj2xsSb0iNNO8rp7zislaiC&stateCode=${stateDict[state]}&sort=date,asc&size=10&page=${pageNo-1}`
			}
		} else {
			if (state == "All") {
				previousQuery =
					`https://app.ticketmaster.com/discovery/v2/events.json?keyword=${keyword}&countryCode=AU&apikey=KiqhEiBfJaj2xsSb0iNNO8rp7zislaiC&countryCode=AU&sort=date,asc&size=10&page=0`
			} else if (state == undefined) {
				previousQuery =
					`https://app.ticketmaster.com/discovery/v2/events.json?keyword=${keyword}&countryCode=AU&apikey=KiqhEiBfJaj2xsSb0iNNO8rp7zislaiC&countryCode=AU&sort=date,asc&size=10&page=0`
			} else {
				previousQuery =
					`https://app.ticketmaster.com/discovery/v2/events.json?keyword=${keyword}&countryCode=AU&apikey=KiqhEiBfJaj2xsSb0iNNO8rp7zislaiC&stateCode=${stateDict[state]}&sort=date,asc&size=10&page=0`
			}
		}

		currentQuery = previousQuery
		eventData = youGotNextMarty(previousQuery)


		eventData.then(function (result) {
			pageNo = result.page.number
			eventData = result._embedded.events

			if (result.page.totalElements == 0) {
				document.getElementById("searchResults").innerHTML = "<div class='well'>" + "<br>" + "<b>No Results Found... < /b>" + "</div>"
			}

			for (i = 0; i < eventData.length; i++) {

                eventCity = result._embedded.events[i]._embedded.venues[0].city.name
                eventState = result._embedded.events[i]._embedded.venues[0].state.name

				timeString = eventData[i].dates.start.localTime // Prepend any date. Use your birthday.
				const timeString12hr = new Date('1970-01-01T' + timeString + 'Z').toLocaleTimeString('en-US', {
					timeZone: 'UTC',
					hour12: true,
					hour: 'numeric',
					minute: 'numeric'
				});
				if (eventData[i].info == '.') {
					var
						eventInfo = 'No additional Information'
				} else {
					var eventInfo = eventData[i].info
				}
				if (parseInt(eventData[i].dates.start.localDate) < 2022) {} else
				if (parseInt(eventData[i].dates.start.localDate) > 2025) {} else {
					eventDate = eventData[i].dates.start.localDate.split('-')[2] + "/" + eventData[i].dates.start.localDate.split('-')[1] + "/" + eventData[i].dates.start.localDate.split('-')[0]

                    document.getElementById('searchResults').innerHTML += "<div class='well' id='result'><p style = 'font-size:18px' >" + " <b> " + eventData[i].name + " </b>" + "<br></p> <b> Date: </b>" + eventDate + "<br><b>Time:</b> " +
                            timeString12hr + "<br><b>Location:</b> " + (eventData[i]._embedded.venues[0].name).split(',')[0] + " - " + eventCity + ", " + eventState + "<br> <a href = " + eventData[i].url + " target ='_blank'> <b> Buy Tickets </b></a> " +
                            "<br> <details><summary> <b> Information </b></summary><p> " + eventInfo + " </p> </details>" + " </div>"
				}

			}
		})

		document.getElementById("searchResults").innerHTML = "<br>"

	}
</script>
</form>
