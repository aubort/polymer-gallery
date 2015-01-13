Polymer Gallery
===============

This gallery uses pure Polymer to display images which are coming from a Google+ photo album. It uses the core-ajax to send a request to the Picasa web album API. 


Demo
====

You can check out a demo here:  http://polymer-gallery.appspot.com/


Getting Started
============

Get the code by cloning the code repository on your local machine

```
	$ git clone https://github.com/aubort/polymer-gallery.git
```

Go to the new repository and start a HTTP server using python

```
	$ python -m SimpleHTTPServer
```
You should see the following output on the console. If you are having trouble with the python simple http server, check out the doc here. 
https://docs.python.org/2/library/simplehttpserver.html#module-SimpleHTTPServer

```
	Serving HTTP on 0.0.0.0 port 8000 ...
```

Point your browser to http://localhost:8000 

That’s it, you should be seeing the polymer-gallery!

Configure
============

The gallery can be configured using the `app-globals.html` file. 
In order to display the album of your choice, you will need to replace the 
`userid` and `albumid` variables with the album id and user id of the album 
you want to display. 
Typically, a valid url will look like this:

```
https://picasaweb.google.com/data/feed/api/user/<userid>/albumid/<albumid>?alt=json
```

How to find the correct `userid` and `albumid`:

Go to Google Plus and then to the album you want to use. The URL should look like this: 

<pre>
https://plus.google.com/photos/<u>111664409766092880224</u>/albums/<b>5702010536228604337</b>
</pre>
The underlined part is the `userid` and the bold part is the `albumid`.




From there, the `<core-ajax>` component in the `image-service.html`will make a call to the rest service and return a json object to the image service - which then will process the response.

 