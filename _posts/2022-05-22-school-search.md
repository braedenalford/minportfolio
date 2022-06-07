---
title: "School Search"
date: 2022-05-22T15:34:30-04:00
categories:
  - project
tags:
  - School
  - JavaScript
  - Leaflet
  - Education
  - D3
  - Visualisations
---

<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<meta http-equiv="X-UA-Compatible" content="IE=edge">
<title>Document</title>
<link rel="stylesheet" href="https://unpkg.com/leaflet@1.2.0/dist/leaflet.css">
<script src="https://unpkg.com/leaflet@1.2.0/dist/leaflet-src.js"></script>

<link rel="stylesheet" href="https://pro.fontawesome.com/releases/v5.11.2/css/all.css">
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/Leaflet.awesome-markers/2.0.2/leaflet.awesome-markers.css">
<script src="https://cdnjs.cloudflare.com/ajax/libs/Leaflet.awesome-markers/2.0.2/leaflet.awesome-markers.js"></script>

<script src="https://cdn.jsdelivr.net/npm/popper.js@1.14.7/dist/umd/popper.min.js" integrity="sha384-UO2eT0CpHqdSJQ6hJty5KVphtPhzWj9WO1clHTMGa3JDZwrnQq4sF86dIHNDz0W1" crossorigin="anonymous"></script>
<script src="https://cdn.jsdelivr.net/npm/bootstrap@4.3.1/dist/js/bootstrap.min.js" integrity="sha384-JjSmVgyd0p3pXB1rRibZUAYoIIy6OrQ6VrjIEaFf/nJGzIxFDsf4x0xIM+B07jRM" crossorigin="anonymous"></script>

<link rel="stylesheet" href="https://pro.fontawesome.com/releases/v5.11.2/css/all.css">
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/Leaflet.awesome-markers/2.0.2/leaflet.awesome-markers.css">
<script src="https://cdnjs.cloudflare.com/ajax/libs/Leaflet.awesome-markers/2.0.2/leaflet.awesome-markers.js"></script>

<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap@5.0.0-alpha1/dist/css/bootstrap.min.css">
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/4.7.0/css/font-awesome.min.css">

<script src="https://cdn.jsdelivr.net/npm/bootstrap@5.0.0-alpha1/dist/js/bootstrap.bundle.min.js"></script>
<script src="https://d3js.org/d3.v4.js"></script>

<script src="https://cdnjs.cloudflare.com/ajax/libs/d3/4.6.0/d3.min.js"></script>

<link rel="stylesheet" href="https://code.jquery.com/ui/1.12.1/themes/base/jquery-ui.css">

<script src="https://cdnjs.cloudflare.com/ajax/libs/jquery/3.3.1/jquery.min.js"></script>

<script src="https://cdnjs.cloudflare.com/ajax/libs/jquery/3.2.1/jquery.min.js"></script>

<script src="https://cdnjs.cloudflare.com/ajax/libs/jqueryui/1.12.1/jquery-ui.min.js"></script>


<style>

.form-check-input:checked {
    background-color: #F7BF50;
    border-color: #F7BF50;
}
	.form-override {
		appearance: auto !important;
	}
	
	.navbar {
    position: relative;
    z-index: 200;
    color: #fff;
    background: #101010;
    padding: 18px 0;
    transition: all .5s ease-in-out;
}
	@media screen and (min-width:48em).admin-bar:not(.side-nav-open) .headroom{
		top: 32px;
	}
	@media screen and (min-width:48em).site-header.headroom--not-top{
		position: fixed;
    	top: 0;
    	border: none;
	}
	.collapse:not(.show){
		display: block !important
	}
	
	a{
		text-decoration:none;
	}
	
	.navbar-nav {
		position: relative !important;
		z-index: 200 !important;
		color: #fff !important;
		padding: 18px 0 !important;
		transition: all .5s ease-in-out !important;
		display: flex;
		flex-direction: inherit;
		margin-bottom: 0;
		list-style: none;
}
	.entry-content h5{
		margin-bottom:0px !important
	}
@-webkit-keyframes spinner-border {
  to {
    -webkit-transform: rotate(360deg);
    transform: rotate(360deg);
  }
}

@keyframes spinner-border {
  to {
    -webkit-transform: rotate(360deg);
    transform: rotate(360deg);
  }
}
a {
    color: #f7bf50;
}

a:hover{
    color: #50380a;
}
	
	.navbar-nav {
		font-weight:400
		flex-wrap:wrap
		justify-content:flex-end
	}

.spinner-border {
  display: inline-block;
  width: 2rem;
  height: 2rem;
  vertical-align: -0.125em;
  border: 0.25em solid currentColor;
  border-right-color: transparent;
  border-radius: 50%;
  -webkit-animation: .75s linear infinite spinner-border;
  animation: .75s linear infinite spinner-border;
}

.spinner-border-sm {
  width: 1rem;
  height: 1rem;
  border-width: 0.2em;
}
	
.sr-only {
    position: absolute;
    width: 1px;
    height: 1px;
    padding: 0;
    margin: -1px;
    overflow: hidden;
    clip: rect(0,0,0,0);
    white-space: nowrap;
    border: 0;
}
	
.spinner-border {
    display: inline-block;
    width: 2rem;
    height: 2rem;
    vertical-align: -0.125em;
    border: 0.25em solid currentColor;
    border-right-color: transparent;
    border-radius: 50%;
    -webkit-animation: .75s linear infinite spinner-border;
    animation: .75s linear infinite spinner-border;
}
.entry-content a {
    text-decoration: none;
}
.dropdown-menu.show {
    right: 0;
    display: inline-block;
}
	
.entry-content h1, .entry-content h2, .entry-content h3, .entry-content h4, .entry-content h5, .entry-content h6 {
    margin-bottom: 20px;
    line-height: 1.3;
    font-weight: 700;
    margin-top: auto;
}
	
.entry-header .entry-title {
    margin-bottom: -50px;
    margin-top: 0;
}
	
.form-control {
    left: 100px;
    display: block;
    width: 100%;
    height: calc(1.5em + 0.75rem + 2px);
    padding: 0.375rem 0.75rem;
    font-size: 1rem;
    font-weight: 400;
    line-height: 1.5;
    color: #495057;
    background-color: #fff;
    background-clip: padding-box;
    border: 1px solid #ced4da;
    border-radius: 0.25rem;
    transition: border-color .15s ease-in-out,box-shadow .15s ease-in-out;
}

.row {display: flex;flex-wrap: wrap;margin-right: -15px;margin-left:  -15px;}

.mt-2, .my-2 {margin-top: 0.5rem!important;}

.card {position: relative;display: flex;flex-direction: column;min-width: 0;word-break: break-word;background-color: #FFF;background-clip: border-box;border: 1px solid rgba(0,0,0,.125);border-radius: 0.25em;}

h5 {font-size: 1.25rem;}

.mt-5, .my-5 {margin-top: auto;}

.d-flex {display: flex!important;}

.col-md-10 {flex: 0 0 83.333333%;max-width: 83.333333%;}

.col, .col-1, .col-10, .col-11, .col-12, .col-2, .col-3, .col-4, .col-5, .col-6, .col-7, .col-8, .col-9, .col-auto, .col-lg, .col-lg-1, .col-lg-10, .col-lg-11, .col-lg-12, .col-lg-2, .col-lg-3, .col-lg-4, .col-lg-5, .col-lg-6, .col-lg-7, .col-lg-8, .col-lg-9, .col-lg-auto, .col-md, .col-md-1, .col-md-10, .col-md-11, .col-md-12, .col-md-2, .col-md-3, .col-md-4, .col-md-5, .col-md-6, .col-md-7, .col-md-8, .col-md-9, .col-md-auto, .col-sm, .col-sm-1, .col-sm-10, .col-sm-11, .col-sm-12, .col-sm-2, .col-sm-3, .col-sm-4, .col-sm-5, .col-sm-6, .col-sm-7, .col-sm-8, .col-sm-9, .col-sm-auto, .col-xl, .col-xl-1, .col-xl-10, .col-xl-11, .col-xl-12, .col-xl-2, .col-xl-3, .col-xl-4, .col-xl-5, .col-xl-6, .col-xl-7, .col-xl-8, .col-xl-9, .col-xl-auto {position: relative;
    
    padding-right: 15px;
    padding-left: 15px;}

.pb-4, .py-4 {padding-bottom: 1.5rem!important;}

.pt-4, .py-4 {padding-top: 1.5rem!important;}

.p-3 {padding: 1rem!important;}

.col-md-4 {flex: 0 0 33.333333%;
    max-width: 33.333333%;}

.dropdown, .dropleft, .dropright, .dropup {position: relative;}

.btn:not(:disabled):not(.disabled) {cursor: pointer;}

button:focus:not(:focus-visible) {outline: 0;}

.dropdown-toggle {white-space:  nowrap;}
	
element.style {
	position: inherit !important
    transform: translate3d(0px, 38px, 0px);
    top: 0px;
    left: 0px;
    will-change: transform;
}
	
.btn-block {display: block;
    width: 100%;}

[type=button], [type=reset], [type=submit], button {-webkit-appearance: button;}

.dropdown-menu {position: absolute;
    top: 100%;
    left: 0;
    z-index: 1000;
    display: none;
    float: left;
    min-width: 10rem;
    padding: 0.5rem 0;
    margin: 0.125rem 0 0;
    font-size: 1rem;
    color: #212529;
    text-align: left;
    list-style: none;
    background-color: #fff;
    background-clip: padding-box;
    border: 1px solid rgba(0,0,0,.15);
    border-radius: 0.25rem;}

.btn-secondary:not(:disabled):not(.disabled).active:focus, .btn-secondary:not(:disabled):not(.disabled):active:focus, .show>.btn-secondary.dropdown-toggle:focus {box-shadow: 0 0 0 0.2rem rgb(130 138 145 / 50%);}

.btn-secondary:not(:disabled):not(.disabled).active, .btn-secondary:not(:disabled):not(.disabled):active, .show>.btn-secondary.dropdown-toggle {color: #fff;
    background-color: #545b62;
    border-color: #4e555b;}

.dropdown-toggle::after {display: inline-block;}

.dropdown-toggle::after {;display: inline-block;margin-left: 0.255em;}

.dropdown, .dropleft, .dropright, .dropup {
    position: relative;
}
	
	b, strong {
    font-weight: 800;
	font-size:16px;
	margin-left: 15px;
}
	
	.dropdown-menu > li > a:hover {
    background-image: none;
    background-color: F7BF50!important;
}
	
.dropdown-item {display: block;
    width: 100%;
    padding: 0.25rem 1.5rem;
    clear: both;
    font-weight: 400;
    color: #212529;
    text-align: inherit;
    white-space: nowrap;
    background-color: transparent;
    border: 0;}

.form-check-input {position: absolute;
    margin-top: 0.5rem;
    margin-left: -1.25rem;}

.form-check-label {margin-bottom: 0;}

.col-md-5 {flex: 0 0 41.666667%;max-width: 41.666667%;}

.col-md-3 {flex: 0 0 25%;
    max-width: 25%;}

	.btn, .btn:hover {
    font-weight: 600;
    font-size: 16px;
    display: inline-block;
    font-weight: 400;
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
    transition: color .15s ease-in-out,background-color .15s ease-in-out,border-color .15s ease-in-out,box-shadow .15s ease-in-out;
}
	
html {
    box-sizing: border-box;
    -webkit-tap-highlight-color: transparent !important;
}



    * {
        box-sizing: inherit;
    }

    .autocomplete {
        /*the container must be positioned relative:*/
        position: relative;
        display: inline-block;

    }

    input {
        border: 1px solid transparent;
        background-color: #f1f1f1;
        padding: 10px;
        font-size: 16px;
    }

	.dropdown-menu{
    	transform: translate3d(5px, 35px, 0px)!important;
	}
	
    input[type=text] {
        background-color: #f1f1f1;
        width: 100%;
    }

    input[type=submit] {
        background-color: DodgerBlue;
        color: #fff;
    }

    .autocomplete-items {
        position: absolute;
        border: 1px solid #d4d4d4;
        border-bottom: none;
        border-top: none;
        z-index: 2;
        /*position the autocomplete items to be the same width as the container:*/
        top: 100%;
        left: 15px;
        right: 15px;
    }

    .autocomplete-items div {
        padding: 10px;
        cursor: pointer;
        background-color: #fff;
        border-bottom: 1px solid #d4d4d4;
    }

    .autocomplete-items div:hover {
        /*when hovering an item:*/
        background-color: #e9e9e9;
    }

    .autocomplete-active {
        /*when navigating through the items using the arrow keys:*/
        background-color: DodgerBlue !important;
        color: #ffffff;
    }

    .container {
        width: 170%;
        z-index: -1;
        padding-right: 0px;
        padding-left: 0px;
    }
.justify-content-center {
    justify-content: left!important;
}
    body {
        background-color: #FFFFFF;
        text-transform: none;

    }

    .advanced {
        text-decoration: none;
        font-size: 15px;
        font-weight: 1000
    }

    .btn-secondary,
    .btn-secondary:focus,
    .btn-secondary:active{
        color: #000;
        background-color: #F7BF50 !important;
        border-color: #F7BF50 !important;
        box-shadow: none;
		margin-top:5px !important;
    }
	
	.btn-secondary:hover{
        color: #FFF;
        background-color: #F7BF50 !important;
        border-color: #F7BF50 !important;
        box-shadow: none
    }

    .advanced {
        color: #F7BF50 !important
		hover: #F7BF50
    }

    .form-control:focus {
        box-shadow: none;
        border: 1px solid #F7BF50
    }
    .form-control{
        left:100px;
    }

    body {
        margin: 0;
        padding: 0;
    }

    #map {
        width: 100%;
        height: 60vh;
        z-index: 1;
    }

    span {
        text-transform: none;
    }

    .loading-overlay {
        width: 96.6%;
        height: 60vh;
        background-color: #d4d4d4;
        opacity: 0.7;
        z-index: 2;
        position: absolute;
        margin: auto;
        top:122px;
        bottom: 0;
        left: 0;
        right: 0;
        }

    .hidden {
        display: none;
    }

    .dropdown-menu.show {
    right: 0;
  }
    .btn, .btn:hover {
        font-weight: 600;
        font-size:16px;
    }

    .spinner-border{
        position: absolute;
        margin: auto;
        top:0;
        bottom: 0;
        left: 0;
        right: 0;
    }
    .mh, .dropdown-menu {
    max-height: 50px;
    overflow: hidden;
    }

	.well {
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
    
    div.tooltip-donut {
     position: absolute;
     text-align: center;
     padding: .5rem;
     padding-top: 0.25rem;
     padding-bottom: 0.25rem;
     background: #FFFFFF;
     color: #313639;
     border: 1px solid #ced4da;
     border-radius: 8px;
     pointer-events: none;
     font-size: 1.3rem;
     font-size: 16px;
     font-family: var( --e-global-typography-text-font-family ), Sans-serif;
    }

    .grid line {stroke: lightgrey;stroke-opacity: 0.7;shape-rendering: crispEdges;}
    .grid path {stroke-width: 0;}
.form-control-search {left: 100px;
    display: block;
    width: 100%;
    height: calc(1.5em + 0.75rem + 2px);
    padding: 0.375rem 0.75rem;
    font-size: 1rem;
    font-weight: 400;
    line-height: 1.5;
    color: #495057;
    background-color: #fff;
    background-clip: padding-box;
    border: 1px solid #ced4da;
    border-radius: 0.25rem;
    transition: border-color .15s ease-in-out,box-shadow .15s ease-in-out;margin-top: 5px;}

    .collapse-list {
        background-color: white;
        max-height: 0;
        overflow: hidden;
        transition: max-height 0.2s ease-out;
    }
	select::-ms-expand { display: block; }

    





















    .selector {
    position: relative;
    padding: 20px;
    width: 200px;
    color: #7e7e7e;
}

.selector ul {
    position: relative;
    display: block;
    overflow: auto;
    min-width: 138px;
    max-height: 200px;
    background: #fff;
    list-style: none;
    white-space: inherit;
    padding-right: 17px;
    width: calc(100% + 17px)
}

.selector li {
    position: relative;
    padding: 3px 20px 3px 25px;
    cursor: pointer
}

.selector li:before {
    position: absolute;
    top: 50%;
    left: 0;
    top: 4px;
    display: inline-block;
    margin-right: 9px;
    width: 17px;
    height: 17px;
    background-color: #f4f4f4;
    border: 1px solid #d5d5d5;
    content: ""
}

.selector li[data-selected="1"]:before {
    border: 1px solid #d7d7d7;
    background-color: #fff
}

.selector li[data-selected="1"]:after {
    position: absolute;
    top: 50%;
    left: 3px;
    top: 11px;
    display: inline-block;
    width: 4px;
    height: 10px;
    border-right: 2px solid;
    border-bottom: 2px solid;
    background: none;
    color: #39c9a9;
    content: "";
    -webkit-transform: rotate(40deg) translateY(-50%);
    transform: rotate(40deg) translateY(-50%)
}

.selector li:hover {
    color: #aaa
}

.selector li .total {
    position: absolute;
    right: 0;
    color: #d7d7d7
}

.selector .price-slider {
    text-align: center;
    display: -webkit-box;
    display: -ms-flexbox;
    display: flex;
    -ms-flex-wrap: wrap;
    flex-wrap: wrap;
    -webkit-box-pack: justify;
    -ms-flex-pack: justify;
    justify-content: space-between;
    -webkit-box-align: center;
    -ms-flex-align: center;
    align-items: center;
    position: relative;
    padding-top: 17px
}

@media (min-width: 768px) {
    .selector .price-slider {
        padding-top:8px
    }
}

.selector .price-slider:before {
    position: absolute;
    top: 50%;
    left: 0;
    margin-top: 0;
    color: #39c9a9;
    content: attr(data-currency);
    -webkit-transform: translateY(-50%);
    transform: translateY(-50%)
}

.selector #distance-slider {
    width: 90%;
    margin-bottom: 20px;
    border: none;
    background: #f1f1f1;
    height: 3px;
    margin-left: -10px;
    margin-right: 0px
}

.selector #education-slider {
    width: 90%;
    margin-bottom: 20px;
    border: none;
    background: #f1f1f1;
    height: 3px;
    margin-left: -10px;
    margin-right: 0px
}

@media (min-width: 768px) {
     .selector #distance-slider {
        width:100%
    }
}

@media (min-width: 768px) {
     .selector #education-slider {
        width:100%
    }
}

.selector .ui-slider-handle {
	z-index:1;
    border-radius: 50%;
    background-color: #F7BF50;
    border: none;
    top: -14px;
    width: 28px;
    height: 28px;
    outline: none
}

@media (min-width: 768px) {
    .selector .ui-slider-handle {
        top:-7px;
        width: 16px;
        height: 16px
    }
}

.selector .ui-education-slider {
    background-color: #000
}

.selector .ui-distance-slider {
    background-color: #d7d7d7
}

.selector .slider-price {
    position: relative;
    display: inline-block;
    padding: 0px 0px;
    font-size:12px;

    text-align: center
}

.selector .slider-price:before {
    position: absolute;
    top: 50%;
    left: 13px;
    margin-top: 0;
    color: #39c9a9;
    content: attr(data-currency);
    -webkit-transform: translateY(-50%);
    transform: translateY(-50%)
}

.selector .show-all {
    position: relative;
    padding-left: 25px;
    color: #39c9a9;
    cursor: pointer;
    line-height: 28px
}

.selector .show-all:after, .selector .show-all:before {
    content: "";
    position: absolute;
    top: 50%;
    left: 4px;
    margin-top: -1px;
    color: #39c9a9;
    width: 10px;
    border-bottom: 1px solid
}

.selector .show-all:after {
    -webkit-transform: rotate(90deg);
    transform: rotate(90deg)
}

.selector.open ul {
    max-height: none
}

.selector.open .show-all:after {
    display: none
}


* {
    -webkit-box-sizing: border-box;
    -ms-box-sizing: border-box;
    box-sizing: border-box;
}

.ui-widget-header {
    border: 1px solid #dddddd;
    background: #F7BF50;
    color: #333333;
    /* font-weight: bold; */
}

.hidden{
    display:none
}

label.col-sm-2.control-label {font-family: var( --e-global-typography-text-font-family ), Sans-serif;
	font-weight: bold;font-size: 18px;margin-bottom: 10px;}
	.well {
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

	li.page-item {}

	.pagination>li {display: inline;}

	li.page-item {}

	.pagination>li:first-child>a, .pagination>li:first-child>span {border-top-left-radius: 4px;
	border-bottom-left-radius: 4px;}

	.pagination>li>a:hover {color: #fff;}
	.btn {
	font-weight: 600;
	font-size: 16px;
	display: inline-block;
	color: #212529;
	background-color: #F7BF50;
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

    a.page-link:hover {
    background-color: #f7bf50;
}

</style>



<body>
    <div>
        <div class="container mt-5">
            <div class="row d-flex justify-content-center">
                <div class="col-md-10">
                    <div class="card p-3 py-4">
                        <h5>Find The Most Suitable School For Your Children</h5>
                        <div class="row g-3 mt-2">
                            <div class="col-md-3">
                                <label for="country" class="control-label" aria-expanded="false">Country To Sort By</label>
                                <select class="country form-control mh selectpicker form-override"  data-live-search="true"  data-width="100%" aria-expanded="false">
                                    <option value="all">All</option>
                                    <option value="afghanistan">Afghanistan</option>
                                    <option value="australia">Australia</option>
                                    <option value="bangladesh">Bangladesh</option>
                                    <option value="bosnia_and_herzegovina">Bosnia & Herzegovina</option>
                                    <option value="cambodia">Cambodia</option>
                                    <option value="canada">Canada</option>
                                    <option value="chile">Chile</option>
                                    <option value="china">China</option>
                                    <option value="croatia">Croatia</option>
                                    <option value="egypt">Egypt</option>
                                    <option value="england">England</option>
                                    <option value="fiji">Fiji</option>
                                    <option value="france">France</option>
                                    <option value="germany">Germany</option>
                                    <option value="greece">Greece</option>
                                    <option value="hong_kong">Hong Kong</option>
                                    <option value="india">India</option>
                                    <option value="indonesia">Indonesia</option>
                                    <option value="iran">Iran</option>
                                    <option value="iraq">Iraq</option>
                                    <option value="ireland">Ireland</option>
                                    <option value="italy">Italy</option>
                                    <option value="japan">Japan</option>
                                    <option value="lebanon">Lebanon</option>
                                    <option value="malaysia">Malaysia</option>
                                    <option value="malta">Malta</option>
                                    <option value="mauritius">Mauritius</option>
                                    <option value="myanmar">Myanmar</option>
                                    <option value="nepal">Nepal</option>
                                    <option value="netherlands">Netherlands</option>
                                    <option value="new_zealand">New Zealand</option>
                                    <option value="northern_ireland">Northern Ireland</option>
                                    <option value="pakistan">Pakistan</option>
                                    <option value="papua_new_guinea">Papua New Guinea</option>
                                    <option value="philippines">Philippines</option>
                                    <option value="poland">Poland</option>
                                    <option value="scotland">Scotland</option>
                                    <option value="singapore">Singapore</option>
                                    <option value="south_africa">South Africa</option>
                                    <option value="south_eastern_europe">South Eastern Europe</option>
                                    <option value="south_korea">South Korea</option>
                                    <option value="sri_lanka">Sri Lanka</option>
                                    <option value="taiwan">Taiwan</option>
                                    <option value="thailand">Thailand</option>
                                    <option value="north_macedonia">North Macedonia</option>
                                    <option value="turkey">Turkey</option>
                                    <option value="usa">USA</option>
                                    <option value="vietnam">Vietnam</option>
                                    <option value="wales">Wales</option>
                                    <option value="zimbabwe">Zimbabwe</option>
                                </select>
                            </div>
                            <div class="col-md-6">
                                <br>
                                <input type="text" id="myInput" class="form-control-search" autocomplete="off" placeholder="Enter suburb..."> 
                            </div>
                                
                                <div class="col-md-3">
                                    <br>
                                    <button class="btn btn-secondary btn-block" id="searchButton" onclick="onSearchResultsClick()">Search Results</button>
                                </div>
                            </div>
                            <br>
                            <div class="row">
                                    <div class="col-md-3">
                                        <label class="control-label">School Sector</label>
                                        <div id = "sector">
                                            <div class="form-check">
                                                <input class="form-check-input" type="checkbox" value="" id="flexCheckGovernment" checked onclick="updateSectorChecks('flexCheckGovernment')">
                                                <label class="form-check-label" for="flexCheckChecked">
                                                    Government
                                                </label>
                                            </div>
                                            <div class="form-check">
                                                <input class="form-check-input" type="checkbox" value="" id="flexCheckIndependent" checked onclick="updateSectorChecks('flexCheckIndependent')">
                                                <label class="form-check-label" for="flexCheckChecked">
                                                    Independent
                                                </label>
                                            </div>
                                            <div class="form-check">
                                                <input class="form-check-input" type="checkbox" value="" id="flexCheckCatholic" checked onclick="updateSectorChecks('flexCheckCatholic')">
                                                <label class="form-check-label" for="flexCheckChecked">
                                                    Catholic
                                                </label>
                                            </div>
                                        </div>
                                    </div>
                                    <div class="col-md-3">
                                        <div id="type">
                                            <label id= "ting" class="control-label">School Type</label>
                                            <div class="form-check">
                                                <input class="form-check-input" type="checkbox" value="" id="flexCheckPrimary" checked onclick="updateTypeChecks()">
                                                <label class="form-check-label" for="flexCheckChecked">
                                                    Primary
                                                </label>
                                            </div>
                                            <div class="form-check">
                                                <input class="form-check-input" type="checkbox" value="" id="flexCheckSecondary" checked onclick="updateTypeChecks()">
                                                <label class="form-check-label" for="flexCheckChecked">
                                                    Secondary
                                                </label>
                                            </div>
                                            <div class="form-check">
                                                <input class="form-check-input" type="checkbox" value="" id="flexCheckCombined" checked onclick="updateTypeChecks()">
                                                <label class="form-check-label" for="flexCheckChecked">
                                                    Combined
                                                </label>
                                            </div>
                                            <div class="form-check">
                                                <input class="form-check-input" type="checkbox" value="" id="flexCheckSpecial" checked onclick="updateTypeChecks()">
                                                <label class="form-check-label" for="flexCheckChecked">
                                                    Special
                                                </label>
                                            </div>
                                        </div>
                                    </div>
                                    
                                    <div class="col-md-3">
                                        <label for="education" class="control-label">School Education Quality</label>
                                        <div class="selector">
                                            <div class="price-slider">
                                                <div id="education-slider" class="ui-slider ui-corner-all ui-slider-horizontal ui-widget ui-widget-content">
                                                    <div class="ui-education-slider ui-corner-all"></div>
                                                    <span tabindex="0" class="ui-slider-handle ui-corner-all ui-state-default" style = "left:100%"></span><span tabindex="0" class="ui-slider-handle ui-corner-all ui-state-default" ></span>
                                                </div>
                                                <span id="education-value" data-max="50"  class="slider-price">Top 100% of schools</span>
                                            </div> 
                                        </div>
                                    </div>

                                    <div class="col-md-3">
                                        <label for="radius" class="control-label">School Distance</label>
                                        <div class="selector">
                                            <div class="price-slider">
                                                <div id="distance-slider" class="ui-slider ui-corner-all ui-slider-horizontal ui-widget ui-widget-content">
                                                    <div class="ui-distance-slider ui-corner-all"></div>
                                                    <div class="inputWrap hidden"><input class="inputNumber" type="text" value="5"></div>
                                                    <span tabindex="0" class="ui-slider-handle ui-corner-all ui-state-default"></span><span tabindex="0" class="ui-slider-handle ui-corner-all ui-state-default"></span>
                                                </div>
                                                <span id="distance-value" data-max="50" class="slider-price">Up to 10km away</span>
                                            </div> 
                                        </div>
                                        
                                    </div>
                                </div>
                        </div>
                        <br>
                        <div id="searchResults"></div>
                        <nav aria-label="Page navigation example">
                            <ul class="pagination">
                                <br>
                                <li class="page-item hidden"><a class="page-link hidden" onclick="previousPage()">Previous</a></li>
                                <li class="page-item hidden"><a class="page-link hidden" onclick="nextPage()">Next</a></li>
                            </ul>
                        </nav>
                    </div>
                </div>
            </div>
            <ul id="postcodeList"></ul>
        </div>
</body>

<script>

    var educationVal = 0
    var distanceVal = 10;

    jQuery(document).ready(function($){
        $("#education-slider").slider({
            range: "max", 
            min: 0,
            max: 90,
            step: 10,
            slide: function( event, ui ) {
                
                $( "#education-value").html('Top ' + (100-ui.value) + '% of schools')
                educationVal = ui.value
            }
        })

        $("#distance-slider").slider({
            range: "min", 
            value:10,
            min: 5,
            max: 50,
            step: 5,
            slide: function( event, ui ) {
                $( "#distance-value").html('Up to ' + ui.value + 'km away')
                distanceVal = ui.value
            }
        })
        
    })

    var sectorList = ["Government","Independent","Catholic"];
    var typeList = ["Primary","Secondary","Combined","Special"];

    function updateSectorChecks(id){    
        console.log(document.getElementById(id).checked)

        
        sectorList = []
        sectorCheck = ["Government","Independent","Catholic"]

        for (i = 0; i < sectorCheck.length; i++) {

            if (document.getElementById("flexCheck" + sectorCheck[i]).checked) {
                sectorList.push(sectorCheck[i])
            }
        }

    }

    function updateTypeChecks(id){    
        typeList = []
        typeCheck = ["Primary","Secondary","Combined","Special"]
        for (i = 1; i < typeCheck.length; i++) {
            if (document.getElementById("flexCheck" + typeCheck[i]).checked) {
                typeList.push(typeCheck[i])
            }
        }

    }

    var acc = document.getElementsByClassName("advanced");
    var i;

    for (i = 0; i < acc.length; i++) {
    acc[i].addEventListener("click", function() {
        this.classList.toggle("active");
        var collapse = this.nextElementSibling;
        if (collapse.style.maxHeight) {
            collapse.style.maxHeight = null;
        } else {
            collapse.style.maxHeight = collapse.scrollHeight + "px";
        } 
    });
    }

    var postcodeData;

    var selectedCountry = 'all';
    var selectedType = 'all';
    var selectedSector = 'all';
    var selectedEducation = 'all';
    var selectedRadius = '10';

    jQuery(document).ready(function($){
        $('.country').change(function () {
            selectedCountry = $('.country').val();
        });
        $('.type').change(function () {
            selectedType = $('.type').val();
        });
        $('.sector').change(function () {
            selectedSector = $('.sector').val();

        });
        $('.education').change(function () {
            selectedEducation = $('.education').val();

        });
        $('.radius').change(function () {
            selectedRadius = $('.radius').val();
        });
    });
    

    async function getPostcodeData(locality) {

        const loadingOverlay = document.getElementsByClassName('loading-overlay')?.[0];

        const res = await fetch(
            `https://cjrfnta8ve.execute-api.ap-southeast-2.amazonaws.com/default/mysql_postcode_query?locality=${locality}`
            );
        const json = await res.json();

        return json;
    }

    async function getSchoolData(north,south,east,west,country,type,sector,education) {

    const loadingOverlay = document.getElementsByClassName('loading-overlay')?.[0];

    url = `https://46987lgfvh.execute-api.ap-southeast-2.amazonaws.com/default/schoolQuery?north=${north}&south=${south}&east=${east}&west=${west}&country=${country}&education=${education}`
    

    types = {
        type0:"none",
        type1:"none",
        type2:"none",
        type3:"none"
    }

    sectors = {
        sector0:"none",
        sector1:"none",
        sector2:"none"
    }

    for (i = 0; i < type.length; i++){
        types["type" + i] = type[i]
    }

    for (i = 0; i < sector.length; i++){
        sectors["sector" + i] = sector[i]
    }

    for (const [key, value] of Object.entries(types)) {
        url += "&" + key + "=" + value
    }
    
    for (const [key, value] of Object.entries(sectors)) {
        url += "&" + key + "=" + value
    }

    const res = await fetch(
        url
        );
    const json = await res.json();

    var element = document.getElementsByClassName("page-item hidden");
    for (i = 0; i < element.length; i++) {
        element[i].classList.remove("hidden");
    }
    var element = document.getElementsByClassName("page-item hidden");
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
    console.log(json)
    return json;
    }

    async function getSchoolTimeSeriesData(schoolId) {

    const loadingOverlay = document.getElementsByClassName('loading-overlay')?.[0];

    url = `https://ev1bb9k557.execute-api.ap-southeast-2.amazonaws.com/default/schoolTimeSeries?acara_sml_id=${schoolId}`


    const res = await fetch(
        url
        );

    const json = await res.json();

    var element = document.getElementsByClassName("page-item hidden");
    for (i = 0; i < element.length; i++) {
        element[i].classList.remove("hidden");
    }
    var element = document.getElementsByClassName("page-item hidden");
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


    // search functionality based on 
    function searchFunction() {
        var postcodes;

        function autocomplete(input, arr) {
            arr = {};

            /*the autocomplete function takes two arguments,
            the text field element and an array of possible autocompleted values:*/
            var currentFocus;
            /*execute a function when someone writes in the text field:*/
            input.addEventListener("input", function (e) {

                arr = {};
                var count = 0;
                var a, b, i, val = this.value;


                if (val.length >= 3) {
                    postcodeDict = getPostcodeData(val)
                } else {
                    postcodeDict = getPostcodeData('madting')
                }


                postcodeDict.then(function (result) {
                    postcodeDict = result

                    for (var i = 0; i < postcodeDict.length; i++) {
                        arr[postcodeDict[i].locality.toString() + ', ' + postcodeDict[i].state
                        .toString() + ', ' + postcodeDict[i].postcode.toString()] = [postcodeDict[i]
                            .lon, postcodeDict[i].lat
                        ];

                    }


                    return arr
                }).then(arr => {
                    /*close any already open lists of autocompleted values*/
                    closeAllLists();
                    if (!val) {
                        return false;
                    }
                    currentFocus = -1;
                    /*create a DIV element that will contain the items (values):*/
                    a = document.createElement("DIV");
                    a.setAttribute("id", this.id + "autocomplete-list");
                    a.setAttribute("class", "autocomplete-items");
                    /*append the DIV element as a child of the autocomplete container:*/
                    this.parentNode.appendChild(a);
                    /*for each item in the array...*/



                    Object.entries(arr).forEach(([key, value]) => {
                        /*check if the item starts with the same letters as the text field value:*/
                        if (count < 11) {
                            if (key.substr(0, val.length).toUpperCase() == val.toUpperCase()) {
                                count += 1
                                /*create a DIV element for each matching element:*/
                                b = document.createElement("DIV");
                                b.className = 'form-control';

                                /*make the matching letters bold:*/
                                b.innerHTML = "<strong>" + key.substr(0, val.length) +
                                    "</strong>";
                                b.innerHTML += key.substr(val.length);
                                /*insert a input field that will hold the current array item's value:*/
                                b.innerHTML += "<input type='hidden' value='" + key + "'>";
                                /*execute a function when someone clicks on the item value (DIV element):*/
                                b.addEventListener("click", function (e) {
                                    /*insert the value for the autocomplete text field:*/
                                    input.value = this.getElementsByTagName("input")[0]
                                        .value;
                                    /*close the list of autocompleted values,
                                    (or any other open lists of autocompleted values:*/
                                    closeAllLists();
                                });
                                a.appendChild(b);
                            }
                        }

                        if (i == arr.length - 1) {
                            if (count == 0) {

                                count += 1
                                /*create a DIV element for each matching element:*/
                                b = document.createElement("DIV");
                                b.className = 'form-control';

                                /*make the matching letters bold:*/
                                b.innerHTML = "No results found";

                                /*execute a function when someone clicks on the item value (DIV element):*/
                                b.addEventListener("click", function (e) {
                                    /*insert the value for the autocomplete text field:*/
                                    input.value = this.getElementsByTagName("input")[0]
                                        .value;
                                    /*close the list of autocompleted values,
                                    (or any other open lists of autocompleted values:*/
                                    closeAllLists();
                                });
                                a.appendChild(b);
                            }
                        }
                    });
                })


            });

            /*execute a function presses a key on the keyboard:*/
            input.addEventListener("keydown", function (e) {
                if (e.key === "Enter") {  
                    val = document.getElementById("myInput").value

                    if (val.length >= 3) {
                        postcodeDict = getPostcodeData(val)
                    } else {
                        postcodeDict = getPostcodeData('madting')
                    }


                    postcodeDict.then(function (result) {

                        postcodeDict = result

                        onSearchResultsClick()
    


                    })
                }
                
            });

            input.addEventListener("keydown", function (e) {
                var x = document.getElementById(this.id + "autocomplete-list");
                        if (x) x = x.getElementsByTagName("div");
                        if (e.keyCode == 40) {
                            /*If the arrow DOWN key is pressed,
                            increase the currentFocus variable:*/
                            currentFocus++;
                            /*and and make the current item more visible:*/
                            addActive(x);
                            
                        } else if (e.keyCode == 38) { //up
                            /*If the arrow UP key is pressed,
                            decrease the currentFocus variable:*/
                            currentFocus--;
                            /*and and make the current item more visible:*/
                            addActive(x);
                        } else if (e.keyCode == 13) {
                            /*If the ENTER key is pressed, prevent the form from being submitted,*/
                            e.preventDefault();
                            if (currentFocus > -1) {
                                /*and simulate a click on the "active" item:*/
                                if (x) x[currentFocus].click();
                            }
                        }
                    })

            function addActive(x) {
                /*a function to classify an item as "active":*/
                if (!x) return false;
                /*start by removing the "active" class on all items:*/
                removeActive(x);
                if (currentFocus >= x.length) currentFocus = 0;
                if (currentFocus < 0) currentFocus = (x.length - 1);
                /*add class "autocomplete-active":*/
                x[currentFocus].classList.add("autocomplete-active");
                
            }

            function removeActive(x) {
                /*a function to remove the "active" class from all autocomplete items:*/
                for (var i = 0; i < x.length; i++) {
                    x[i].classList.remove("autocomplete-active");
                }
            }
            
            function closeAllLists(elmnt) {
                /*close all autocomplete lists in the document,
                except the one passed as an argument:*/
                var x = document.getElementsByClassName("autocomplete-items");
                for (var i = 0; i < x.length; i++) {
                    if (elmnt != x[i]) {
                        if (elmnt != input) {
                            x[i].parentNode.removeChild(x[i]);
                        }
                    }
                }
            }
            /*execute a function when someone clicks in the document:*/
            document.addEventListener("click", function (e) {
                closeAllLists(e.target);
            });
        }


        autocomplete(document.getElementById("myInput"), postcodes);

    }

    searchFunction()

    var pageNo = 0;

    var maxPageNo;

    function nextPage(){

        if (pageNo == maxPageNo) {
            pageNo == maxPageNo;
        }
        else {
            pageNo += 1;
        }

        onSearchResultsClick()
        document.body.scrollTop = document.documentElement.scrollTop = 0;
    }

    function previousPage(){

        if (pageNo >0){
            pageNo -= 1;
        }
        onSearchResultsClick()
        document.body.scrollTop = document.documentElement.scrollTop = 0;
    }


    costMap = {
        Government: "500 approximately",
        Catholic: "1375 approximately",
        Independent: "22473 approximately"
    }

    function separator(num) {
        var str = num.toString().split(".");
        str[0] = str[0].replace(/\B(?=(\d{3})+(?!\d))/g, ",");
        return str.join(".");
    }


    function onSearchResultsClick() {
        arr = {};

        val = document.getElementById("myInput").value.split(', ')[0]

        if (val.length >= 3) {
            postcodeDict = getPostcodeData(val)
        } else {
            postcodeDict = getPostcodeData('madting')
        }

        postcodeDict.then(function (result) {

            postcodeDict = result

            suburb_lat = postcodeDict[0].lat
            suburb_lon = postcodeDict[0].lon

            radius = distanceVal/111

            north_bound = suburb_lat+radius
            south_bound = suburb_lat-radius
            east_bound = suburb_lon+radius
            west_bound = suburb_lon-radius

            country = selectedCountry
            type = typeList
            sector = sectorList
            education = educationVal
            
            
            schoolData = getSchoolData(north_bound,south_bound,east_bound,west_bound,country,type,sector,education)

            schoolData.then(function (result) {
                schoolData = result
				if (schoolData.length == 0){
					document.getElementById("searchResults").innerHTML = "<div class='well'>" + "<br>" + "<b>No Results Found... </b>" + "</div>"
				}
				else{

                
                
                var elementCounter = 0;
				
				if(schoolData[0].country != "None"){
					
                    
					function titleCase(string){
						return string[0].toUpperCase() + string.slice(1).toLowerCase();
					}
					
					country = titleCase(selectedCountry)
					
					document.getElementById('searchResults').innerHTML = ""

                    maxPageNo = Math.ceil(schoolData.length)

					for (i = pageNo*10; i < schoolData.length; i++) {

                        if(schoolData[i].school_cost == null){
                            var cost = costMap[schoolData[i].school_sector]
                        }
                        else{
                            var cost = schoolData[i].school_cost
                        }
                        elementCounter += 1

						document.getElementById('searchResults').innerHTML += "<div class='well' id='result'><p style = 'font-size:18px' >" + " <b> " + schoolData[i].school_name + " </b>" + 
							"<br></p> <b>Location: </b>" + schoolData[i].suburb + ", " + schoolData[i].state + ", " + schoolData[i].postcode + "<br><b>School Type: </b>" + schoolData[i].school_type + "<br><b>School Sector: </b>" 
							+ schoolData[i].school_sector + "<br><b>Year Level Range: </b>" + schoolData[i].school_range 
							+ "<details ><summary onclick='showPlots(" + i + ")'> <b> More School Information </b></summary><p>" + "<div id='my_dataviz" + i + "'></div>" + "<br><b>This school ranks in the top " + (100-schoolData[i].education_percentile) + "% of schools in Australia" + "<br><b>Local Area From " + country + ": </b>" + schoolData[i].country.toFixed(2) + "%"
                            + "<br><b>Annual Year 12 School Fees: </b>$" + separator(cost)+ "<br><b>Total Teaching Staff: </b>" + schoolData[i].teaching_staff + "<br><b>Total Students: </b>" + schoolData[i].total_enrolments + "<br><b> School URL: </b> <a href = " + schoolData[i].school_url 
							+ " target ='_blank'>" + schoolData[i].school_url + "</p></details></a>" + "<details ><summary onclick='schoolMap(" + i + ")'>  Show School Location</summary><p>" + "<div id='map" + schoolData[i].acara_sml_id + "' style='width: 600px; height: 400px;'></div></details>" + "</div>"

                        if (elementCounter == 10){
                            break;
                        }
					}
				}
				else{
					document.getElementById('searchResults').innerHTML = ""

                    maxPageNo = Math.ceil(schoolData.length)

                    for (i = pageNo*10; i < schoolData.length; i++) {

                        if(schoolData[i].school_cost == null){
                            var cost = costMap[schoolData[i].school_sector]
                        }
                        else{
                            var cost = schoolData[i].school_cost
                        }

                        elementCounter += 1

                        document.getElementById('searchResults').innerHTML += "<div class='well' id='result'><p style = 'font-size:18px' >" + " <b> " + schoolData[i].school_name + " </b>" + 
							"<br></p> <b>Location: </b>" + schoolData[i].suburb + ", " + schoolData[i].state + ", " + schoolData[i].postcode + "<br><b>School Type: </b>" + schoolData[i].school_type + "<br><b>School Sector: </b>" 
							+ schoolData[i].school_sector + "<br><b>Year Level Range: </b>" + schoolData[i].school_range 
							+ "<details ><summary onclick='showPlots(" + i + ")'> <b> More School Information </b></summary><p>" + "<div id='my_dataviz" + i + "'></div>" + "<br><b>This school ranks in the top " + (100-schoolData[i].education_percentile) + "% of schools in Australia</b>"
                            + "<br><b>Annual Year 12 School Fees: </b>$" + separator(cost)+ "<br><b>Total Teaching Staff: </b>" + schoolData[i].teaching_staff + "<br><b>Total Students: </b>" + schoolData[i].total_enrolments + "<br><b> School URL: </b> <a href = " + schoolData[i].school_url 
							+ " target ='_blank'>" + schoolData[i].school_url + "</p></details></a>" + "<details ><summary onclick='schoolMap(" + i + ")'> <b> Show School Location</b></summary><p>" + "<div id='map" + schoolData[i].acara_sml_id + "' style='width: 600px; height: 400px;'></div></details>" + "</div>"
                        
                        if (elementCounter == 10){
                            break;
                        }
                    
                    }
                        

                }
				}
            })

        })
    }
  
    function buildSexDonut(i){
        // define data
        var totals = [
            {
                title:'Boys Enrolment', 
                value: schoolData[i].boys_enrolments, 
                all: schoolData[i].total_enrolments}, 
            {
                title:'Girls Enrolment', 
                value: schoolData[i].girls_enrolments, 
                all: schoolData[i].total_enrolments
            }];

        var width = 250;
        var height = 280;
        var radius = 100;
        var donutWidth = 35;
        var color = d3.scaleOrdinal()
            .range(["#b7b7b7", "#F7BF50"]);

        var svg = d3.select("#my_dataviz" + i)
            .append('svg')
            .attr('width', width)
            .attr('height', height)
            .append('g')
            .attr('transform', 'translate(' + (width / 2) +
                ',140)');

                
        var arc = d3.arc()
            .innerRadius(radius - donutWidth)
            .outerRadius(radius);

            

        var pie = d3.pie()
            .padAngle(.01)
            .value(function (d) {
                return d.value;
            })
            .sort(null);

        var legendRectSize = 17;
        var legendSpacing = 10;

        var donutTip = d3.select("body").append("div")
            .attr("class", "donut-tip")
            .style("opacity", 0);

            var div = d3.select("body").append("div")
            .attr("class", "tooltip-donut")
            .style("opacity", 0);


        var path = svg.selectAll('path')
            .data(pie(totals))
            .enter()
            .append('path')
            .attr('d', arc)
            .attr('fill', function (d, i) {
                return color(d.data.title);
            })
            .attr('transform', 'translate(0, 0)')
            .on('mouseover', function (d, i) {
                d3.select(this).transition()
                    .duration('50')
                    .attr('opacity', '.7');
                div.transition()
                    .duration(50)
                    .style("opacity", 1);
                let num = (Math.round((d.value / d.data.all) * 100)).toString() + '%';
                div.html(num)
                    .style("left", (d3.event.pageX + 10) + "px")
                    .style("top", (d3.event.pageY - 15) + "px");
            })
            .on('mousemove', function (d, i) {
                d3.select(this).transition()
                    .duration('50')
                    .attr('opacity', '.7');
                div.transition()
                    .duration(50)
                    .style("opacity", 1);
                let num = (Math.round((d.value / d.data.all) * 100)).toString() + '%';
                div.html(num)
                    .style("left", (d3.event.pageX + 10) + "px")
                    .style("top", (d3.event.pageY - 15) + "px");
            })
            .on('mouseout', function (d, i) {
                d3.select(this).transition()
                    .duration('50')
                    .attr('opacity', '1');
                div.transition()
                    .duration('50')
                    .style("opacity", 0);
            })


        var legend = svg.selectAll('.legend')
            .data(color.domain())
            .enter()
            .append('g')
            .attr('class', 'circle-legend')
            .attr('transform', function (d, i) {
                var height = legendRectSize + legendSpacing;
                var offset = height * color.domain().length / 2;
                var horz = -2 * legendRectSize - 13;
                var vert = i * height - offset;
                return 'translate(' + horz + ',' + vert + ')';
            });

        legend.append('circle')
            .style('fill', color)
            .style('stroke', color)
            .attr('cx', 0)
            .attr('cy', 15)
            .attr('r', '.3rem');

        legend.append('text')
            .attr('x', 10)
            .attr('y', 20)
            .style("font-size", "12px")
            .text(function (d) {
                return d;
            });


        svg.append("text")
            .attr("x", 0)             
            .attr("y", -115)
            .attr("text-anchor", "middle")  
            .style("font-size", "16px") 
            .text("Gender Distribution");


    }

    function buildEthnicDonut(i){

        allBackground = schoolData[i].english_background + schoolData[i].non_english_background

        // define data
        var totals = [
            {
                title:'English', 
                value: schoolData[i].english_background, 
                all: allBackground}, 
            {
                title:'Non-English', 
                value: schoolData[i].non_english_background, 
                all: allBackground
            }];





        var width = 250;
        var height = 280;
        var radius = 100;
        var donutWidth = 35;
        var color = d3.scaleOrdinal()
            .range(["#b7b7b7", "#F7BF50"]);

        var svg = d3.select("#my_dataviz" + i)
            .append('svg')
            .attr('width', width)
            .attr('height', height)
            .append('g')
            .attr('transform', 'translate(' + (width / 1.9) +
                ',140)');

        var arc = d3.arc()
            .innerRadius(radius - donutWidth)
            .outerRadius(radius);

        var pie = d3.pie()
            .padAngle(.01)
            .value(function (d) {
                return d.value;
            })
            .sort(null);

        var legendRectSize = 17;
        var legendSpacing = 10;

        var donutTip = d3.select("body").append("div")
            .attr("class", "donut-tip")
            .style("opacity", 0);

            var div = d3.select("body").append("div")
            .attr("class", "tooltip-donut")
            .style("opacity", 0);
        var path = svg.selectAll('path')
            .data(pie(totals))
            .enter()
            .append('path')
            .attr('d', arc)
            .attr('fill', function (d, i) {
                return color(d.data.title);
            })
            .attr('transform', 'translate(0, 0)')
            .on('mouseover', function (d, i) {
                d3.select(this).transition()
                    .duration('50')
                    .attr('opacity', '.7');
                div.transition()
                    .duration(50)
                    .style("opacity", 1);
                let num = (Math.round((d.value / d.data.all) * 100)).toString() + '%';
                div.html(num)
                    .style("left", (d3.event.pageX + 10) + "px")
                    .style("top", (d3.event.pageY - 15) + "px");
            })
            .on('mousemove', function (d, i) {
                d3.select(this).transition()
                    .duration('50')
                    .attr('opacity', '.7');
                div.transition()
                    .duration(50)
                    .style("opacity", 1);
                let num = (Math.round((d.value / d.data.all) * 100)).toString() + '%';
                div.html(num)
                    .style("left", (d3.event.pageX + 10) + "px")
                    .style("top", (d3.event.pageY - 15) + "px");
            })
            .on('mouseout', function (d, i) {
                d3.select(this).transition()
                    .duration('50')
                    .attr('opacity', '1');
                div.transition()
                    .duration('50')
                    .style("opacity", 0);
            });


        var legend = svg.selectAll('.legend')
            .data(color.domain())
            .enter()
            .append('g')
            .attr('class', 'circle-legend')
            .attr('transform', function (d, i) {
                var height = legendRectSize + legendSpacing;
                var offset = height * color.domain().length / 2;
                var horz = -2 * legendRectSize - 13;
                var vert = i * height - offset;
                return 'translate(' + horz + ',' + vert + ')';
            });

        legend.append('circle')
            .style('fill', color)
            .style('stroke', color)
            .attr('cx', 8)
            .attr('cy', 15)
            .attr('r', '.3rem');

        legend.append('text')
            .attr('x', 18)
            .attr('y', 20)
            .style("font-size", "12px")
            .text(function (d) {
                return d;
            });



        svg.append("text")
            .attr("x", 0)             
            .attr("y", -115)
            .attr("text-anchor", "middle")  
            .style("font-size", "16px") 
            .text("Background Of Students");

    }

    function buildBarChart(i){
        
        allData = schoolData[i].bottom_percentile + schoolData[i].lower_middle_percentile + schoolData[i].upper_middle_percentile + schoolData[i].top_percentile
		
        var data = [
            {
                title:'Bottom Quartile', 
                value: schoolData[i].bottom_percentile, 
                all: allData}, 
            {
                title:'Lower Middle Quartile', 
                value: schoolData[i].lower_middle_percentile, 
                all: allData},
            {
                title:'Upper Middle Quartile', 
                value: schoolData[i].upper_middle_percentile, 
                all: allData}, 
            {
                title:'Top Quartile', 
                value: schoolData[i].top_percentile, 
                all: allData
            }];
        // set the dimensions and margins of the graph
        var margin = {top: 50, right: 30, bottom: 90, left: 50},
            width = 300,
            height = 190 - margin.top;
        
        // append the svg object to the body of the page
        var svg = d3.select("#my_dataviz" + i)
        .append("svg")
            .attr("width", width + margin.left + margin.right)
            .attr("height", height + margin.top + margin.bottom)
        .append("g")
            .attr("transform",
                "translate(" + margin.left + "," + margin.top + ")");
        
        // Parse the Data
        
        
        // X axis
        var x = d3.scaleBand()
        .range([ 0, width ])
        .domain(data.map(function(d) { return d.title; }))
        .padding(0.2);
        svg.append("g")
        .attr("transform", "translate(0," + height + ")")
        .call(d3.axisBottom(x))
        .selectAll("text")
            .attr("transform", "translate(-10,0)rotate(-30)")
            .style("text-anchor", "end");

        // Add Y axis
        var y = d3.scaleLinear()
        .domain([0, 100])
        .range([ height, 0]);
        svg.append("g")
        .call(d3.axisLeft(y));
        
        // Add Gridlines
        svg.append("g")
            .attr("class", "grid")
            .call(d3.axisLeft(y)
                    .tickSize(-width)
                    .tickFormat("")
            );





        var div = d3.select("body").append("div")
                .attr("class", "tooltip-donut")
                .style("opacity", 0);

        // Bars
        svg.selectAll("mybar")
        .data(data)
        .enter()
        .append("rect")
            .attr("x", function(d) { return x(d.title); })
            .attr("width", x.bandwidth())
            .attr("fill", "#F7BF50")
            // no bar at the beginning thus:
            .attr("height", function(d) { return height - y(0); }) // always equal to 0
            .attr("y", function(d) { return y(0); })
            .on('mouseover', function (d, i) {
                    d3.select(this).transition()
                        .duration('50')
                        .attr('opacity', '.7');
                    div.transition()
                        .duration(50)
                        .style("opacity", 1);
                    let num = (Math.round((d.value / d.all) * 100)).toString() + '%';
                    div.html(num)
                        .style("left", (d3.event.pageX + 10) + "px")
                        .style("top", (d3.event.pageY - 15) + "px");
                })
                .on('mousemove', function (d, i) {
                    d3.select(this).transition()
                        .duration('50')
                        .attr('opacity', '.7');
                    div.transition()
                        .duration(50)
                        .style("opacity", 1);
                    let num = (Math.round((d.value / d.all) * 100)).toString() + '%';
                    div.html(num)
                        .style("left", (d3.event.pageX + 10) + "px")
                        .style("top", (d3.event.pageY - 15) + "px");
                })
                .on('mouseout', function (d, i) {
                    d3.select(this).transition()
                        .duration('50')
                        .attr('opacity', '1');
                    div.transition()
                        .duration('50')
                        .style("opacity", 0);
                });

                        // Animation
        svg.selectAll("rect")
        .transition()
        .duration(800)
        .attr("y", function(d) { return y(d.value); })
        .attr("height", function(d) { return height - y(d.value); })
        .delay(function(d,i){ return(i*100)})

        svg.append("g")
            .attr("transform", "translate(0, 106)")
            .append("line")
            .attr("x2", width)
            .style("stroke", "#855F12")
            .style("stroke-width", "2px");
        
		svg.append("text")
			.attr("x", (width / 2))             
			.attr("y", 0 - (margin.top / 2))
			.attr("text-anchor", "middle")  
			.style("font-size", "16px") 
			.text("Socio-Educational Distribution");
    
    }

    function buildTimeSeries(i){
        schoolId = schoolData[i].acara_sml_id
        timeSeriesData = getSchoolTimeSeriesData(schoolId)






        timeSeriesData.then(function (result) {

                var data = result;
                if(data.length>0){
                    minYear = data[0].calendar_year
                maxYear = data.slice(-1)[0].calendar_year
                
                var margin = {top: 60, right: 330, bottom: 30, left: 60},
                    width = 800 - margin.left - margin.right,
                    height = 310 - margin.top - margin.bottom;


                var color = d3.scaleOrdinal()
                    .range(["#b7b7b7", "#F7BF50"]);

                // append the svg object to the body of the page
                var svg = d3.select("#my_dataviz" + i)
                .append("svg")
                    .attr("width", width + margin.left + margin.right)
                    .attr("height", height + margin.top + margin.bottom)
                .append("g")
                    .attr("transform",
                        "translate(" + margin.left + "," + margin.top + ")");

                var allGroup = ["icsea_percentile", "language_background_other_than_english_yes"]

                
                var dataReady = allGroup.map( function(grpName) { // .map allows to do something for each element of the list
                return {
                    name: grpName,
                    values: data.map(function(d) {
                    return {time: d.calendar_year, value: +d[grpName]};
                    })
                };
                });
                

                var myColor = d3.scaleOrdinal()
                .domain(allGroup)
                .range(["#b7b7b7", "#F7BF50"]);

                // Add X axis --> it is a date format
                var x = d3.scaleLinear()
                    .domain([minYear,maxYear])
                    .range([ 0, width ]);
                svg.append("g")
                    .attr("transform", "translate(0," + height + ")")
                    .call(d3.axisBottom(x).ticks(10).tickFormat(d3.format("d")));

                // Add Y axis
                var y = d3.scaleLinear()
                    .domain([0,100])
                    .range([ height, 0 ]);
                svg.append("g")
                    .call(d3.axisLeft(y));

                    // Add Gridlines
                svg.append("g")
                    .attr("class", "grid")
                    .call(d3.axisLeft(y)
                            .tickSize(-width)
                            .tickFormat("")
                    );


                // Add the lines
                var line = d3.line()
                .x(function(d) { return x(+d.time) })
                .y(function(d) { return y(+d.value) })
                svg.selectAll("myLines")
                .data(dataReady)
                .enter()
                .append("path")
                    .attr("class", function(d){ return d.name })
                    .attr("d", function(d){ return line(d.values) } )
                    .attr("stroke", function(d){ return myColor(d.name) })
                    .style("stroke-width", 4)
                    .style("fill", "none")

                var donutTip = d3.select("body").append("div")
                .attr("class", "donut-tip")
                .style("opacity", 0);

                var div = d3.select("body").append("div")
                .attr("class", "tooltip-donut")
                .style("opacity", 0);

                // Add the points
                svg
                .selectAll("myDots")
                .data(dataReady)
                .enter()
                    .append('g')
                    .style("fill", function(d){ return myColor(d.name) })
                    .attr("class", function(d){ return d.name })
                // Second we need to enter in the 'values' part of this group
                .selectAll("myPoints")
                .data(function(d){ return d.values })
                .enter()
                .append("circle")
                    .attr("cx", function(d) { return x(d.time) } )
                    .attr("cy", function(d) { return y(d.value) } )
                    .attr("r", 5)
                    
                .on('mouseover', function (d, i) {
                    d3.select(this).transition()
                        .duration('50')
                        .attr('opacity', '.7')
                        .attr("r", 8);
                    div.transition()
                        .duration(50)
                        .style("opacity", 1);
                    let num = (d.value.toString());
                    div.html(num)
                        .style("left", (d3.event.pageX + 10) + "px")
                        .style("top", (d3.event.pageY - 15) + "px");
                })
                .on('mousemove', function (d, i) {
                    d3.select(this).transition()
                        .duration('50')
                        .attr('opacity', '.7')
                        .attr("r", 8);
                    div.transition()
                        .duration(50)
                        .style("opacity", 1);
                    let num = (d.value.toString());
                    div.html(num)
                        .style("left", (d3.event.pageX + 10) + "px")
                        .style("top", (d3.event.pageY - 15) + "px");
                })
                .on('mouseout', function (d, i) {
                    d3.select(this).transition()
                        .duration('50')
                        .attr('opacity', '1')
                        .attr("r", 5);
                    div.transition()
                        .duration('50')
                        .style("opacity", 0);
                })

                var legend = svg.selectAll('.legend')
                    .data(color.domain())
                    .enter()
                    .append('g')
                    .attr('class', 'circle-legend')
                    .attr('transform', function (d, i) {
                        var height = legendRectSize + legendSpacing;
                        var offset = height * color.domain().length / 2;
                        var horz = -2 * legendRectSize - 13;
                        var vert = i * height - offset;
                        return 'translate(' + horz + ',' + vert + ')';
                    });

                svg.append("circle").attr("cx",450).attr("cy",20).attr("r", 6).style("fill", "#b7b7b7")
                svg.append("circle").attr("cx",450).attr("cy",50).attr("r", 6).style("fill", "#F7BF50")
                svg.append("text").attr("x", 470).attr("y", 20).text("Australian School Educational Ranking").style("font-size", "15px").attr("alignment-baseline","middle").style("font-size", "12px")
                svg.append("text").attr("x", 470).attr("y", 50).text("Students With A Non-English").style("font-size", "15px").attr("alignment-baseline","middle").style("font-size", "12px")
				svg.append("text").attr("x", 470).attr("y", 70).text("Speaking Background (%)").style("font-size", "15px").attr("alignment-baseline","middle").style("font-size", "12px")

                legend.append('text')
                    .attr('x', 10)
                    .attr('y', 20)
                    .style("font-size", "12px")
                    .text(function (d) {
                        return d;
                    });


                svg.append("text")
                    .attr("x", 200)             
                    .attr("y", -20)
                    .attr("text-anchor", "middle")  
                    .style("font-size", "16px") 
                    .text("School Demographic Changes Over Time");
                }
                
                
        })
    }

    var schoolMarker = L.AwesomeMarkers.icon({
        iconColor: 'darkred',
        prefix: 'fa',
        markerColor: 'red'
    });


    function schoolMap(i){

        
        

        lat = schoolData[i].latitude
        lon = schoolData[i].longitude

        window['map'+schoolData[i].acara_sml_id] = L.map(window['map'+schoolData[i].acara_sml_id],{ zoomControl: false }).setView([lat, lon], 12);

        L.tileLayer('https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png', {
        attribution: '&copy; <a href="http://www.openstreetmap.org/copyright">OpenStreetMap</a>',
        minZoom: 13,
        maxZoom: 13
    }).addTo(window['map'+schoolData[i].acara_sml_id]);

        marker = L.marker([lat, lon], {
            icon: schoolMarker
            }).addTo(window['map'+schoolData[i].acara_sml_id]);


        var popup = marker.bindPopup(schoolData[i].school_name);

        popup.openPopup();

        window['map'+schoolData[i].acara_sml_id].dragging.disable();
    }


    function showPlots(i){

        arr = {};

            val = document.getElementById("myInput").value.split(', ')[0]

            if (val.length >= 3) {
                postcodeDict = getPostcodeData(val)
            } else {
                postcodeDict = getPostcodeData('madting')
            }

            postcodeDict.then(function (result) {

                postcodeDict = result

                suburb_lat = postcodeDict[0].lat
                suburb_lon = postcodeDict[0].lon

                radius = distanceVal/111

                north_bound = suburb_lat+radius
                south_bound = suburb_lat-radius
                east_bound = suburb_lon+radius
                west_bound = suburb_lon-radius

                country = selectedCountry
                type = typeList
                sector = sectorList
                education = educationVal
            
            
            schoolData = getSchoolData(north_bound,south_bound,east_bound,west_bound,country,type,sector,education)

                schoolData.then(function (result) {

                    schoolData = result
                    document.getElementById('my_dataviz' + i).innerHTML = ""
                    buildSexDonut(i)

                    buildEthnicDonut(i)

                    buildTimeSeries(i)
                })
                
            })

    }
</script>
