# Directions Widget Print Page

## About

This example application can be used to create a custom printing page for directions generated from the directions widget.

## Requirements

    ArcGIS JavaScript Directions Widget from API 3.6 or above.
    Print page must be stored on the same domain as the page using the ArcGIS directions widget.
    This example uses Mustache.js to render a HTML template showing the list of directions.

## Setup Instructions

    Add the URL to the custom page (index.html in this folder) as the "printPage" options property of the directions widget.
        
            var myWidget = new Directions({
                map: this.map,
                printPage: 'http://myurl.com/print-directions/',
            }, 'directions');

## How it works
 
    The directions widget will call the URL that you define in the "printPage" option and you will have access to the directions response object returned from the route service.
    
    You can access the variable using "window.opener.directions".
    
    If the page is opened by itself and the window.opener has no "directions" property, then an error message is displayed.
    
    You can customize the template and CSS included in the "tpl" folder and do things like adding a map to the print directions page. See Mustache.js for more information on how to write Mustache templates. https://github.com/janl/mustache.js/
    

[](Esri Tags: ArcGIS JavaScript API 3.6 Directions Widget JS API Esri Printing Print Directions)
[](Esri Language: JS)
