
#																					   	
#																						
#							PcapChecker v4												
#						Writer: Omar FARISS																




1- Project composition:
The poject has two main clases: mainPcapAnalyser and PcapAnalyser

	- PcapAnalyser:
		This class implement all the function of the project. This class has the following funcitons:
		- parseTrace(String path): This function parse the pcap file and generate a "tmptrace.txt" file with Hexa content. 
			This file is used by other funcitons to extrat information for specific purposes.
			
		- loadParsedfile(String path): This function reads frim the tmptrace.txt file to return an array of the file content.
		
		- getGlobalHeader(String[] array): This function is used to extrat the global header of the Pcap file.
		
		- convertBytesToInt (String[] array): This function is used to convert Bytes to int.
		
		- getIpPacketSize (String[] array): This funciton is used to get the size of an given IP packet of the pcap file.
		
		- getIpPacket (String[] array, int offset): This function gets an IP packets in a specific position "offset" of the pcap file.
		
		- getPacketSrcIp (String[] array): this function provide the source IP of a given IP packet.
		
		- getPacketDstIp (String[] array): this function provide the destination IP of a given IP packet.
		
		- getPacketTrptProtocol (String[] array): This funciton provide the transport protocol (level 4 of OSI model) of a given IP packet.
		
		- getPacketSrcPort (String[] array): this function provide the source port of a given packet
		
		- getPacketDstPort (String[] array): this function provide the destination port of a given packet
		
		- getPacketAppProtocol (String[] array): this funciton get the applicaiton protocol of a given packet (level 7 of OSI model)
		
		- getFilteredPacketArrayList (List<String[]> arrayList, String protocol): This function gets the filtered IP packet based on the application protocol
		
		-ExportPcapFile (List<String[]> arrayList, String[] globalHeader, String protocol): This function export the filtered pcap file based on the chosen applicaiton protocol.
		
		- buildPacketsList (String[] array): This function is used to buil an arrayList of the arrays, each array is an IP packet.
		
		- printPackets (List<String[]> arrayList) : this fucntion prints IP packets.
	
	
	- The mainPcapAnalyser: this class is the main class. It's manage the menu provided to the user.

2- Program execution

	To execute the program you need:
		- upload the mainPcapAnalyser and PcapAnalyser clased in an IDE.
		- pcap trace: you can use the pcap trace provided for testing.
		- Launch the program in linux envirenement only.


3- Implemented Funtionalities:
	- PArse the PCAP file
	-retrieve from pcap file:
		- Global Header
		- IP packets
		- Source and destination IP addresses
		- ConvertBytes
		- Get transport protocol
		- packets size
		- Packets ports: source and destination
		- Application protocol of each IP packet
	
	- Export filtered IP packets to a pcap file.
	- Print IP packet in the console.
	- interactive menu for the user with multiple choices.
	- this program support the folowing protocols:
		- HTTP
		- HTTPS
		- DNS
		- DHCP
		- NTP
		- SNMP
		- FTP
		- SSH
		- TELNET
	
	
	
