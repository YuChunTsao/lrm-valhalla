Leaflet Routing Machine / Valhalla by Mapzen
=====================================


     ██▒   █▓ ▄▄▄       ██▓     ██░ ██  ▄▄▄       ██▓     ██▓    ▄▄▄      
    ▓██░   █▒▒████▄    ▓██▒    ▓██░ ██▒▒████▄    ▓██▒    ▓██▒   ▒████▄    
     ▓██  █▒░▒██  ▀█▄  ▒██░    ▒██▀▀██░▒██  ▀█▄  ▒██░    ▒██░   ▒██  ▀█▄  
      ▒██ █░░░██▄▄▄▄██ ▒██░    ░▓█ ░██ ░██▄▄▄▄██ ▒██░    ▒██░   ░██▄▄▄▄██ 
       ▒▀█░   ▓█   ▓██▒░██████▒░▓█▒░██▓ ▓█   ▓██▒░██████▒░██████▒▓█   ▓██▒
       ░ ▐░   ▒▒   ▓▒█░░ ▒░▓  ░ ▒ ░░▒░▒ ▒▒   ▓▒█░░ ▒░▓  ░░ ▒░▓  ░▒▒   ▓▒█░
       ░ ░░    ▒   ▒▒ ░░ ░ ▒  ░ ▒ ░▒░ ░  ▒   ▒▒ ░░ ░ ▒  ░░ ░ ▒  ░ ▒   ▒▒ ░
         ░░    ░   ▒     ░ ░    ░  ░░ ░  ░   ▒     ░ ░     ░ ░    ░   ▒   
          ░        ░  ░    ░  ░ ░  ░  ░      ░  ░    ░  ░    ░  ░     ░  ░
         ░                                                                    


Extends [Leaflet Routing Machine](https://github.com/perliedman/leaflet-routing-machine) with support for [Valhalla](https://mapzen.com/projects/valhalla).

## Installing

Go to the [download page](http://www.liedman.net/lrm-graphhopper/download/) to get the script to include in your page. Put the script after Leaflet and Leaflet Routing Machine has been loaded.


## Using

You can use Valhalla routing machine with Leaflet Routing Machine plugin by replacing Router and Formatter instance. 

    var rr = L.Routing.control({
      // you can get api key from Mapzen developer (https://mapzen.com/developers)
      router: L.Routing.valhalla('valhalla-nsDITYA','auto'),
      formatter: new L.Routing.Valhalla.Formatter()
    }).addTo(map);


You can change transitmode for routing later by passing the options.
Currently (June 2015), Valhalla supports auto, bicycle, and pedestrian mode for routing.

     rr.route({transitmode: 'auto'});