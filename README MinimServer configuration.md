A brief guide to configuring MinimServer/MinimStreamer to stream internet radios

This guide is based on the giude provide by https://melius.club/ user stefano-mbp (in ITALIAN) tha can be found at https://drive.google.com/file/d/19qe4iB8l_Bbh385TG4cqP59A8UJtxg05/view?usp=sharing)

It is possible to define playlists containing references to internet streams in order to listen to internet radio through MinimServer.

In first place, if you have not done that already, you need to install MinimStreamer module.
Go to MinimServer properties, select the Packages panel, then select MinimStreamer in the left panel and install it.

At this point you need to configure all the radio playlists in the folder that contains the musical archive defined for MinimServer.
As an example, I'm assuming you will create a "Radio" subfolder in MinimServer music folder.

You wil need to create a different folder for each radio station.
In each of these radio folders, you will put the image to be used as rasdio logo and the playlist descriptor, with extension ".m3u".
In creating the m3u playlist descriptor you need to follow the correct syntax, otehrwise the playlist will not be interpreted correctly, as in the following example:

 
#EXTM3U  
#EXTINF:-1,[*;mp3] Audiophile Classical 
http://94.23.201.38:8010/stream 

• The value in the first row is fixed

• The second row include the stream type (mp3 in the example) and the stream name (Audiophile Classical) in the example

• The third row contains the strema URL

It is reccommended to name the ".m3u" file with the same name configured in the playlist descriptor.

Please see below two other examples for an AAC and for a FLAC file.
 
#EXTM3U  
#EXTINF:-1,[*;aac] Jazz24.org 
https://live.wostreaming.net/direct/ppm-jazz24aac256-ibc1 

#EXTM3U  
#EXTINF:-1,[*;flac] Radio Paradise Main Mix 
http://stream.radioparadise.com/flac 

Once the folder structure with all the playlist is complete you will need to launch the rescan of the library in MinimServer.

In your controlpoint application (for example Lumin App) you fill wind a new folder labelled as "<n> playlists", where <n> is the number of playlists you have actually configured.
Selecting the folder of the desired playlist you will start its audio reproduction! 
