# Analyzing the "Johny Cash Has Been Everywhere" Web Map

![](img/website_screenshot.png)

The project can be found at http://www.johnnycashhasbeeneverywhere.com/

## Introduction
The goal of the project is to provide a chronological guide to the places Johny Cash mentiones in the "I've Been Everywhere" song. The project was created by Iain Mullan for Music Hack Day London 2012.

## Major Functions
* Displays the lyrics to the "I've Been Everywhere" song in realtime on the top of the page. Everytime Jonhny Cash mentions a place it is highlighted in green.
* Play, Pause, Hurry up!, and Skip to End interactive buttons.
* Distanced traveled is displayed on the bottom right of the page.

## Target Audience
Since this project is meant for entertainment purposes, it can be enjoyed by pretty much anyone. Especially fans of Johny Cash or music fans in general.

## Project Author
The project was created by Iain Mullan, a London based software developer.

## Systematic Architecture
This project is hosted on an external network, meaning it can be accessed by anyone using a web browser. Each user has access to their own web client. The web client then pulls information from the internal network, which consists of a web server and a file server. For this project, the web server stores the HTML, JavaScript, and CSS files that are used by the web client. For example, some of the files stored by the web server in this project are the index.html, lyrics.js, and style.css files.
![](img/webserver.png)

## Inspecting the Code
### Data Flow
If we take a look at the Network tab in the Google Chrome Inspector tool we can see that the majority of the data that is being flowed between the client and the server is the google maps service data.
![](img/networktab.png)

It appears as though each time the the map moves, the client is calling upon the google map service in order to recieve tile information on that particular section of the map.
![](img/googlemaptile.png)

It's also worth noting that data is only called upon once in order to increase performace. For example, the image of Johny Cash's face is fetched in the begininng, but never fetched again even though it pops up on the map over and over again throughout the duration of the song.

### Major Libraries and APIs in Use
| Library/API     | Function                                                                                                |
|-----------------|---------------------------------------------------------------------------------------------------------|
| JQuery          | Simplifys HTML DOM tree traversal and manipulation, as well as event handling, CSS animation, and Ajax. |
| Google Maps API | Allows for use of the google map basemap with the ability to add layers, styles, events, and controls. |
| Musixmatch API  | Allows the lyrics to be displayed and synchronized with the song.                                       |
| Tomahk API      | Fetches and plays the audio of the song.                                                                |

### Responsive Design Support
Using the device toolbar in the Chrome Inspector tool we can see that the web map does support responsive design:
![](img/responsivedesigntest.gif)

## Data Sources
* **Vector:** `america_keyed.json` contains the names and coordinates of all the places Johny Cash mentions in the song. Mapped as point vectors using the google maps API.
* **Raster:** `google maps basic maps` consiting of roadmap, satellite, hybrid, and terrain basemap tiles provided by the Google Maps API. 

## Web Map Design

### UI/UX

### Basemap

### Thematic Layer

## Social Implications

## Summary

## References
