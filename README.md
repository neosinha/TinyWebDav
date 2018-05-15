WebDavServerlet
==========
Python class which implements a WebDav Serverlet. The server sits behind a webserver like Apache or Nginx with reverse proxy settings.
The intent of this servelet is to allow client applications have very easy access to a larger storage volume(s) on a server.

Usage: 
====

``` 
optional arguments:
  -h, --help            show this help message and exit
  -p PORT, --port PORT  Port number for WebDav Server
  -i IPADDRESS, --ipaddress IPADDRESS
                        Bind to the given ipaddress else, would run on a local
                        ip address. Loopback interface 127.0.0.1 would be used
                        if no option is provided This useful if running behing
                        a rev-proxy
  -d DIR, --dir DIR     Directory on a mounted volume to serve as the root of
                        the webdav-server
 
 ```
 
 Linux/MAC OS: 
 ====
 	In our example we use port 8085 and webdav volume location to be /Volumes/Disk03/datasets
	Go to a command line window 
	```
		python davserver.py --port 8805 --dir /Volumes/Disk03/datasets/ 
 	```
 	
 	On OSX, this should show a prompt asking if python app should be allowed to accept incoming connections on port 8085. This is just making a temporary exception to the firewall/security rules. 
 	On linux, please ensure that port 8085 is configured for HTTP traffic and is not blocked. 
 	![Server Firewall](https://github.com/neosinha/WebdavServlet/blob/gh-pages/docs/images/security-prompt.png)
 	
 	
 Servelet Deployment: 
 ====
 
![Servelet Architecture](https://github.com/neosinha/WebdavServlet/blob/gh-pages/docs/images/WebdavServelet.001.jpeg)


The project is forked of the awesome work that has been done on [TinyWebdavSever](https://github.com/wolf71/TinyWebDav). 




