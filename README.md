# What is LPKG
LPKG (LILIN Software Packaging Script) is the descriptive script for third-party developer's applications including libraries and binaries run on LILIN camera.  The LPKG script is used to retrieve information about developer's libraries and binaries by the IP camera.  It is a user interface for accessing developer plug-in via LILIN IP camera.

# LPKG Description
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
| | The shell script will add start or stop parameter for after your shell script automatically.  
  For example: 
  /lpr/lilinshell.sh start 
  /lpr/lilinshell.sh stop |
| port	| LPKG plug-in server port | 
| md5	| md5 check sum of Image | 
| url_index	| LPKG plug-in server index page path |
| url_icon	| LPKG plug-in icon path |

| The icon | file data format is PNG  |
| version	|LPKG plug-in version |

