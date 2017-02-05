# filesv
http server for sharing files in a local network for download

filesv - a tiny personal download http-Server for local networks

About
"filesv" is a simple webserver with a special function for file downloads. It generates a download website for making filesharing easy in a local network.

How to use
Simply copy your files in the download folder (/html/download) and share them for download in your local network. This can be more comfortable than handling with USB Memory or SD-Cards. The files are accessible to all devices within their web browser.
The file list is generated new every time you call or refresh the download homepage. It's not necessary to restart the server when you add new files. Just copy the new files in the download folder and then they are ready for download.
Windows will ask you on the first run for permission for the internel firewall.

On start you will be asked for two informations:
1) Port (default=80): Port 80 is standard for http. However, you can run multiple instances on different ports on the same machine.
2) Home (default=/html) You can try "/demo" instead. This is the home directory for the html-files of the server.
path			function
/html			html files for filesv
/html/download	download folder, place your files here
/demo			more complex demo files for filesv
/demo/download	download folder for the demo

The server print it's local network address on top of the screen. Type in this address in your web browsers address-field and you see the filesv homepage.
Below you can see some informations of the server (uptime, number of files or html-views)
Then there are ten lines for the status of parallel connections. There are usually not more than three connections used at the same time for a client.

[S]imple [N]etwork [C]onnection Library
The network stuff uses a modified "[S]imple [N]etwork [C]onnection" Lib from D. J. Peters (Link). The setup of IP address an port has been taken out of the constructor to make changes of that values possible at runtime. (Added some comments to the changes in the snc-sh.bi file).

Advanced features of filesv
"filesv" uses some self defined function-codes to insert informations in the web pages at runtime.
For example, every time, when you call the download page, it reads the current files in the "/download" folder and presents them in a table with links.
{DOWNLOADZIP} offers a table with ZIP files.
{DOWNLOADALL} offers a table with all files.
The number of files is limited to 50. It's easy to change that, if needed.
Have a look at the demo.

License
This program is open source, License: GPL V3
Have fun.
oog / proog.de
