
### How to implement Reactom API


1. Include the fireworks javascript dependency in you HTML header

```
    <script type="text/javascript" language="javascript" src="https://reactome.org/FireworksJs/fireworks/fireworks.nocache.js"></script>
```  
------------------------------    
        
2. Add a place holder in the body of your web page
```
    <div id="fireworksHolder"></div>
```    
----------------------------------------
        
3. Set a proxy in your server under "/reactome" pointing to "https://reactome.org"

---------------------------------------------------

4. Create and initialise the pathways overview from your javascript code
```
    //Creating the Reactome pathways overview widget
    function onReactomeFireworksReady(){  //This function is automatically called when the widget code is ready to be used
        var fireworks = Reactome.Fireworks.create({
            "placeHolder" : "fireworksHolder",
            "width" : 930,
            "height" : 500
        });

        //Adding different listeners

        fireworks.onFireworksLoaded(function (loaded) {
            console.info("Loaded ", loaded);
        });

        fireworks.onNodeHovered(function (hovered){
            console.info("Hovered ", hovered);
        });

        fireworks.onNodeSelected(function (selected){
            console.info("Selected ", selected);
        });
    }
 ```       
  -------------------------
  ### References:
  1. These instructions are obtained from Reactom Website (https://reactome.org/dev/pathways-overview/js)
