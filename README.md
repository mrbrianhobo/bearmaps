# bearmaps

BearMaps is web mapping application (inspired by Google Maps) of Berkeley built using map data and images from [OpenStreetMaps](https://www.openstreetmap.org/). The backend web server uses [Apache Maven](https://maven.apache.org/).

## Features ##
* Map scrolling/zooming 
![](rastering.gif)
* Location search and autocomplete
![](autocomplete.gif)
* Routing and path finding
![](a*%20star.gif)

## Implementation ##
The scroll and zoom functions are done by map rastering (converting user's viewing frame into desired image/bitmap). We do this by using a QuadTree data structure to contruct overall map images from smaller component "pixels."

Location search is possible through the [OpenStreetMaps](https://www.openstreetmap.org/) metadata that we import. Using a Trie data structure, we can reliable include autocomplete our search bar.

We implement routing and path finding by constructing a Graph using all the location data that we import. We then run A* search to find the shortest path between any two abitrary points ( A ⇒  B ).