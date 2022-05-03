# multicraft-confs
Multicraft jar.conf files for simplifying server setups

# Installation Instructions

The best way to use this repo is to download the zip for the archive and upload to the jar folder
 of your server and unzip into the jar folder, this will put the conf files where you want them
 and put the forge_store folder with the libraries in the right place.
 
 
 Then you need to go into multicraft settings and update the files for the version you want to use,
  then create you server, set your server base dir to a memorable name and start your server, the server
  will crash but thats ok. Stop your server.
  
  Now copy the relevant library and server from forge_stores into your servers base directory, then chown
  the copied libraries folder recursively to the server user i.e.
            
            chown -R mc3:mc3 libraries
            
   Now do the same for the minecraft_server-1.11.2.jar whatever.
   
Now the last thing you need to do is to copy the minecraft-forge-1.11.2.jar file
also to your server base directory and chown that too.

And thats it you can start the server it it will load.

The conf files are set to run the forge jar from your server base directory, this
way we can have multiple forge servers on a multicraft panel.


# Helper

There is now a helper file called mover, after extracting the archive to your jar folder, use

        chmod +x mover
        
Now when you need to setup a server, just use

        ./mover 1.11.2 myserver
        
and it will move all the files automatically, however you do have to have been into multicraft and updated the jar and conf in settings >> update minecraft first 
or it wont find the correct jar file to copy for forge.
