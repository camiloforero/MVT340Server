MVT340Server v 0.1.1
A Meitrack MVT340 TCP server for OpenGTS

Changelog:
* 15/03/2015 - v. 0.1: Created the mvt340 server based on the OpenGTS template, it works.
* 16/03/2015 - v. 0.1.1: Added the readme, notice, build_mod and dcservers_mod files for easier implementation

As the description says, this is a custom dcserver that allows OpenGTS to communicate with a Meitrack MVT340 device
This code is based off the "template" server included.

This code works for v. 2.5.8 of OpenGTS

Functionality:
1 Detect and log gps events for
  - SOS button
  - Timed events
  - GPS signal lost
  - GPS signal recovered
    
Installation steps:
1) Modify the dcservers.xml in OpenGTS' root directory to include the snippet in dcservers_mod.xml. Remember to replace the TCP and UDP ports by those you want to use, by default I put port 27868 for both of them.
2) Modify the dcservers.xml in OpenGTS' root directory to include the snippet in dcservers_mod.xml.
3) Modify the source in org/opengts/db/DCServerFactory to include the constant public static final String  MVT_340_NAME                       = "mvt340";           // [27838]
4) Put the mvt340 package source inside the org/opengts/servers directory of the OpenGTS source
5) Use ant all to rebuild the project
6) Use ant mvt340 to build the new server
7) It's done. You can start the new server using the command $GTS_HOME/bin/runserver.pl -s mvt340



Useful links:
OpenGTS installation and configuration manual: http://opengts.sourceforge.net/OpenGTS_Config.pdf
Meitrack MVT340 GPRS protocol: http://www.meitrack.net/meitrack-support/protocol/MEITRACK_GPRS_Protocol.pdf



