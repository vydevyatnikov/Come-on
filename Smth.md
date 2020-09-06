---
title: "Just another assignment"
author: "vydevyatnikov"
date: "06 09 2020"
output: 
  html_document:
    keep_md: true
---



# MAP 


```r
library(leaflet)
df <- data.frame(lat = c(29.9795, 32.5348, 37.9498, 37.6383, 37.0378, 36.4513, 31.2143), 
                 lng = c(31.1341, 44.4308, 27.3638, 21.6300, 27.4241, 28.2278, 29.8850))
iconSet <- iconList(Pyramid = makeIcon("https://img.wallpapersafari.com/desktop/1920/1080/7/4/96Aoyc.jpg", iconWidth = 50, iconHeight = 25), 
                    Hanging_Gardens = makeIcon("https://img.wallpapersafari.com/desktop/1920/1080/57/58/pN1A7j.jpg", iconWidth = 50, iconHeight = 25),
                    Temple_of_Artemis = makeIcon("https://upload.wikimedia.org/wikipedia/commons/thumb/f/f3/Templo-Artemisa-Efeso-2017.jpg/1280px-Templo-Artemisa-Efeso-2017.jpg", iconWidth = 50, iconHeight = 25),
                    Statue_of_Zeus = makeIcon("https://upload.wikimedia.org/wikipedia/commons/6/66/Le_Jupiter_Olympien_ou_l%27art_de_la_sculpture_antique.jpg", iconWidth = 50, iconHeight = 25),
                    Mausoleum_at_Halicarnassus = makeIcon("https://www.wallpaperup.com/uploads/wallpapers/2015/05/28/701339/7cc6c5f860c55ebd46c2f839d1c2e3dc.jpg", iconWidth = 50, iconHeight = 25),
                    Colossus_of_Rhodes = makeIcon("https://upload.wikimedia.org/wikipedia/commons/thumb/5/5f/Colosse_de_Rhodes_%28Barclay%29.jpg/800px-Colosse_de_Rhodes_%28Barclay%29.jpg", iconWidth = 50, iconHeight = 25),
                    Lighthouse_of_Alexandria = makeIcon("https://upload.wikimedia.org/wikipedia/commons/thumb/2/22/Lighthouse_-_Thiersch.png/1280px-Lighthouse_-_Thiersch.png", iconWidth = 50, iconHeight = 25))
df %>% leaflet() %>% addTiles(attribution = "06.09.2020") %>% addMarkers(icon = iconSet, popup = names(iconSet))
```

<!--html_preserve--><div id="htmlwidget-2f80fd16af7d8fd76eba" style="width:672px;height:480px;" class="leaflet html-widget"></div>
<script type="application/json" data-for="htmlwidget-2f80fd16af7d8fd76eba">{"x":{"options":{"crs":{"crsClass":"L.CRS.EPSG3857","code":null,"proj4def":null,"projectedBounds":null,"options":{}}},"calls":[{"method":"addTiles","args":["//{s}.tile.openstreetmap.org/{z}/{x}/{y}.png",null,null,{"minZoom":0,"maxZoom":18,"tileSize":256,"subdomains":"abc","errorTileUrl":"","tms":false,"noWrap":false,"zoomOffset":0,"zoomReverse":false,"opacity":1,"zIndex":1,"detectRetina":false,"attribution":"06.09.2020"}]},{"method":"addMarkers","args":[[29.9795,32.5348,37.9498,37.6383,37.0378,36.4513,31.2143],[31.1341,44.4308,27.3638,21.63,27.4241,28.2278,29.885],{"iconUrl":{"data":["https://img.wallpapersafari.com/desktop/1920/1080/7/4/96Aoyc.jpg","https://img.wallpapersafari.com/desktop/1920/1080/57/58/pN1A7j.jpg","https://upload.wikimedia.org/wikipedia/commons/thumb/f/f3/Templo-Artemisa-Efeso-2017.jpg/1280px-Templo-Artemisa-Efeso-2017.jpg","https://upload.wikimedia.org/wikipedia/commons/6/66/Le_Jupiter_Olympien_ou_l%27art_de_la_sculpture_antique.jpg","https://www.wallpaperup.com/uploads/wallpapers/2015/05/28/701339/7cc6c5f860c55ebd46c2f839d1c2e3dc.jpg","https://upload.wikimedia.org/wikipedia/commons/thumb/5/5f/Colosse_de_Rhodes_%28Barclay%29.jpg/800px-Colosse_de_Rhodes_%28Barclay%29.jpg","https://upload.wikimedia.org/wikipedia/commons/thumb/2/22/Lighthouse_-_Thiersch.png/1280px-Lighthouse_-_Thiersch.png"],"index":[0,1,2,3,4,5,6]},"iconWidth":50,"iconHeight":25},null,null,{"interactive":true,"draggable":false,"keyboard":true,"title":"","alt":"","zIndexOffset":0,"opacity":1,"riseOnHover":false,"riseOffset":250},["Pyramid","Hanging_Gardens","Temple_of_Artemis","Statue_of_Zeus","Mausoleum_at_Halicarnassus","Colossus_of_Rhodes","Lighthouse_of_Alexandria"],null,null,null,null,{"interactive":false,"permanent":false,"direction":"auto","opacity":1,"offset":[0,0],"textsize":"10px","textOnly":false,"className":"","sticky":true},null]}],"limits":{"lat":[29.9795,37.9498],"lng":[21.63,44.4308]}},"evals":[],"jsHooks":[]}</script><!--/html_preserve-->
