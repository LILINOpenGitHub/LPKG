# What is LPKG
LPKG (LILIN Software Packaging Script) is the descriptive script for third-party developer's applications including libraries and binaries run on LILIN camera.  The LPKG script is used to retrieve information about developer's libraries and binaries by the IP camera.  It is a user interface for accessing developer plug-in via LILIN IP camera.

# LPKG Description
LPKG script is in JSON (JavaScript Object Notation) format that is a lightweight data-interchange format. It is easy for humans to read and write. It is easy for machines to parse and generate.

# What is inside LPKG
A LPKG example is descrbed below:

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
