Docker container running the Stationeers dedicated server.

### Usage
```console
$ docker run /
	-it --rm / 
	-p 27500:27500 -p 27500:27500/udp -p 27015:27015/udp /
	-v $pwd/default.ini:/data/default.ini /
	-v $pwd/saves:/data/saves /
	biseque/stationeers /
	-batchmode -nographics -autostart -autosaveinterval=300 -clearallinterval=900
```

### Default settings and save games
Creating a default.ini before run in the working directory will include it when starting the server. Put your savegames in the saves folder under the working directory to make those available to the container and run from existing save games using the "-loadworld=<game>" tag.