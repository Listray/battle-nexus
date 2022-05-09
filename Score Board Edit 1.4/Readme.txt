Score Board Edit v1.4 by Zou
2014 (C) Zou

Requirements :
==============
  - Windows Vista / 7 / 8 (x86/x64)
  - Microsoft .NET Framework 4 (or newer)


What it does ?
==============
	Simple, it edit (or creat if doesn't exist) the content of a simple xml/text file in real time. Why? To live edit a text overlay in Xsplit or Open Broad Caster (OBS). Usefull if we need to quick update a score or text eg. for Vs fighting games.


How to use :
============
	- Place the .exe where you want and launch it.
	- Chose first the methode :
		* File (For Xsplit only) : All data will be stored in a simple xml file. If you want you can chose a specified xml file. By default the xml file will be created in the same directory as the exe file. 
		* Folder (For OBS or Xplit) : All data will be stored in separated txt files in a folder.
	- Click Select/read File(s)
	- Since this kind of tool is usefull for Versus games, there a 6 informations stored in the file(s) :
		* Player 1 Nickname (<P1>)
		* Player 1 Score (<scrP1>)
		* Player 2 NickName (<P2>)
		* Player 2 score (<scrP2>)
		* Label (<label>)
		* Miscellaneous (<misc>)
	- Create a text area in obs or xsplit :
		* In OBS : 
			+ Click Add -> Text
			+ Enter the label for this text area (eg. "Player 1 nickname" or what you want)
			+ Select "Use Text From File"
			+ Browse for the txt file in the SBE folder (same location as the exe file). eg. "P1.txt" (if the file doesn't exit click on the update button in SBE. It will now be created)
			+ Configure the Font/Size/Solor/.... for the text.
			+ Click Ok
		* In Xsplit :
			+ Click Add -> "Add Title"
			+ Select "Remote Text Update"
			+ Set the refresh interval to 1 or 2 sec
			+ put the url of the xml or txt file in the "Remote Url" form. eg. "C:\Stream\SBE\scrP2.txt" or "C:\Stream\scoreboard.xml" if the SBE exe is in the "C:\Stream\" folder
			+ If you use file methode enter the xml tag to select the desired information. eg. if you want to display the Player 2 score, use the <scrP2> and </scrP2> tags. (Case sensitive!)
			+ If you use folder methode empty the 2 tags forms. 
			+ Configure the Font/Size/Solor/....
			+ Click Ok
	- Now if everything is configured correctly when you update the information in SBE it will automatically display changes on the stream.

Rem :
	- Minus Button cannot decrease the score under 0
	- "Auto Update" check box willautomatically push the update button when another button is pushed (+/-/switch/reset/...)


Contact :
=========
	sbe <at> soulsociety. be	