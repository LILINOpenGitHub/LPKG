# What is LPKG
LPKG (LILIN Software Packaging Script) is the descriptive script for third-party developer's applications including libraries and binaries run on LILIN camera.  The LPKG script is used to retrieve information about developer's libraries and binaries by the IP camera.  It is a user interface for accessing developer plug-in via LILIN IP camera.

# LPKG description
LPKG script is in JSON (JavaScript Object Notation) format that is a lightweight data-interchange format. It is easy for humans to read and write. It is easy for machines to parse and generate.

# What is inside LPKG
A LPKG example is descrbed below:
```
{
  "name" : "LILIN LPR",
  "description" : "LILIN LPR functional programming.",
  "homepage" : "http://www.meritlilin.com.tw",
  "keywords" : ["LPR", "functional", "server", "client", "browser"],
  "author" : "chirun <chirun@meritlilin.com.tw >",
  "root" : "/lpr"
  "shell" : "/lpr/lilinshell.sh",
  "port" : "8592",
  "md5" : "WQEWRFFDFWEIUHEDEDREF",
  "url_index" : "/lpr/index.htm",
  "url_icon" : "/lpr/lilin.png",
  "version" : "1.1.6"
}
```

| Parameter	 	| Description			 |
| --- 			|  --- 				|
| name | LPKG name |
| description | LPKG description |
| homepage | LPKG home page |
|Author | Contact person |
|root	| LPKG root path |
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
  
For example:

updateamba_cv22.sh (CV22)
updateamba_cv25.sh (CV25)
updateamba_s2.sh (CV2)

	LPKG.json is the script of your plug-in.
![image](https://github.com/LILINOpenGitHub/LPKG/blob/main/image/image.jpg)
<BR>
Image is a directory of your software.

updateamba_cv22.sh is using to control installtion process and the file name must be “updateamba_xx.sh”. The xx the is SOC platform name.
  
For example:

updateamba_cv22.sh (CV22)
updateamba_cv25.sh (CV25)
updateamba_s2.sh (CV2)

LPKG.json is the script of your plug-in.

