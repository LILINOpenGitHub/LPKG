# What is LPKG
LPKG (LILIN Software Packaging Script) is the descriptive script for third-party developer's applications including libraries and binaries run on LILIN camera.  The LPKG script is used to retrieve information about developer's libraries and binaries by the IP camera.  It is a user interface for accessing developer plug-in via LILIN IP camera.

# LPKG description
LPKG script is in JSON (JavaScript Object Notation) format that is a lightweight data-interchange format. It is easy for humans to read and write. It is easy for machines to parse and generate.

# What is inside LPKG
A LPKG example is descrbed below:
```
{
  "name": "LILIN Aida Camera Plug-in",
  "description": "LILIN Aida Camera Plug-in",
  "homepage": "http://www.meritlilin.com",
  "keywords": [
    "gynet"
  ],
  "author": "LILIN <fae@meritlilin.com.tw>",
  "root": "/Aida",
  "root_data": "/Aida_data",
  "shell": "/Aida_data/aiengine",
  "port": "8592",
  "md5": "65142bd2198b3568803efdde6020b94e",
  "url_index": "/Aida/index.html",
  "url_icon": "/Aida/lilin.png",
  "version": "2.0.3.32-mod001"
}
```

| Parameter	 	| Description			 |
| --- 			|  --- 				|
| name | LPKG name |
| description | LPKG description |
| homepage | LPKG home page |
| keywords | the keywords to terminate your application | 
| Author | Contact person |
| root	| LPKG root path |
|shell	| LPKG start and stop shell script |
| | The shell script will add start or stop parameter for after your shell script automatically.  <BR> For example: <BR> /lpr/lilinshell.sh start  <BR> /lpr/lilinshell.sh stop |
| port	| LPKG plug-in server port | 
| md5	| md5 check sum of Image (for future use) | 
| url_index	| LPKG plug-in server index page path |
| url_icon	| LPKG plug-in icon path |
| The icon | file data format is PNG  |
| version	|LPKG plug-in version |

# LPKG installation package
Please follow the steps below for packaging your application with LPKG script below:

1.	Create the tar file in the directory.
```
tar -czf plugincv22s66.bin *  
```
2. Prepare a directory with the Image directory, update_cv22.sh, and LPKG.json. <BR>
<BR>

![image](https://github.com/LILINOpenGitHub/LPKG/blob/main/image/image.jpg)

<BR> 
For example:

updateamba_cv22.sh (CV22) <BR>
updateamba_cv25m.sh (CV25) <BR>
updateamba_s2.sh (CV2) <BR>

Image is a directory of your software.

updateamba_cv22.sh is using to control installtion process and the file name must be “updateamba_xx.sh”. The xx the is SOC platform name.
  
For example: <BR>

updateamba_cv22.sh (CV22) <BR>
updateamba_cv25m.sh (CV25) <BR>
updateamba_s2.sh (CV2) <BR>

LPKG.json is the script of your plug-in. <BR>

# Load your LPKG to the camera
After packaging your application including libraries and binaries, you are able to perform firmware upgrade.
  
# The result
The folowing is an example of third-party youtube streamer and LILIN AI plug-in.

![image](https://github.com/LILINOpenGitHub/LPKG/blob/main/image/firmwareupdate.jpg)

# The CGI command
Start plugin:<BR>
the CGI is: http://192.168.0.200:80/maintenance?lpkg_start=<PluginName> <BR><BR>
The curl syntax is:<BR>
curl -X GET http://admin:Pass1234@192.168.26.65/maintenance?lpkg_start=CameraPlug-in <BR>

where <PluginName> is the plugin name.

Stop plugin:<BR>
the CGI is http://192.168.0.200:80/maintenance?lpkg_stop=&#U+003CpluginName><BR><BR>
The curl syntax is: <BR>
curl -X GET http://admin:Pass1234@192.168.26.65/maintenance?lpkg_stop=CameraPlug-in <BR>

where <PluginName> is the plugin name.

