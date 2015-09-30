# Change Log #
  * Jan 07, 2015: Version 1.0.3 Compatible with gwt-2.7.x, multiple selection support is very stable and it's supported by all server implementations (java servlet, GAE memcache & blobstore, cgi perl and php. Added Experimental drag & drop. And a set  of [fixes](http://code.google.com/p/gwtupload/issues/list?can=1&q=label%3AMilestone-1.0.2)
  * Apr 27, 2014: Version 1.0.1. Compatible with gwt-2.6.x,  IE10 support and some [fixes](http://code.google.com/p/gwtupload/issues/list?can=1&q=label%3AMilestone-1.0.1)
  * Dec 31, 2013: Version 1.0.0. multiple selection, new approach for decorated buttons, fix for large files when using certain commons-fileupload versions, CSS distributed in a css-bundle, support for Cross-origin resource sharing (CORS),  and a many [fixes](http://code.google.com/p/gwtupload/issues/list?can=1&q=label%3AMilestone-1.0.0).
  * Dec 03, 2012: Version 0.6.6. The examples .war file can be run stand-alone: (`java -jar gwtupload-samples-x.x.x.war`), and a bunch of [fixes](http://code.google.com/p/gwtupload/issues/list?can=1&q=label%3AMilestone-0.6.6%20status%3AFixed).
  * Nov 30, 2012: Version 0.6.5. Release including  [these fixes](http://code.google.com/p/gwtupload/issues/list?can=1&q=label%3AMilestone-0.6.5%20status%3AFixed).
  * Nov 22, 2011: Version 0.6.4. PHP backend script. Better GAE support. Some changes in the API so as Uploader methods are overridables. Many fixes: safari in jsupload, events called twice, decorated buttons in IE, etc.
  * Dec 31, 2010: Version 0.6.3-compat. Backward compatibility version it works with gwt 1.6.x, 1.7.x, 2.0.x, gwt-2.1.x ([issue85](https://code.google.com/p/gwtupload/issues/detail?id=85))
  * Dec 30, 2010: Version 0.6.3. Server response is available in a client struct, so it is easier to get messages from the server. Take a look to this [document](http://code.google.com/p/gwtupload/wiki/Servlets#Getting_additional_server_information).
  * Dec 29, 2010: Version 0.6.2, Fixed [issue65](https://code.google.com/p/gwtupload/issues/detail?id=65) [issue66](https://code.google.com/p/gwtupload/issues/detail?id=66) [issue68](https://code.google.com/p/gwtupload/issues/detail?id=68) [issue73](https://code.google.com/p/gwtupload/issues/detail?id=73) [issue74](https://code.google.com/p/gwtupload/issues/detail?id=74) [issue75](https://code.google.com/p/gwtupload/issues/detail?id=75) [issue78](https://code.google.com/p/gwtupload/issues/detail?id=78) [issue82](https://code.google.com/p/gwtupload/issues/detail?id=82) [issue83](https://code.google.com/p/gwtupload/issues/detail?id=83) [issue84](https://code.google.com/p/gwtupload/issues/detail?id=84). Improvements in decorated file upload. Server side returns info about file uploaded by default. Blobstore should work but no progress bar.
  * Jul 26, 2010: Version 0.6.1, Internationalized server messages. Fixed [issue60](https://code.google.com/p/gwtupload/issues/detail?id=60) [issue61](https://code.google.com/p/gwtupload/issues/detail?id=61) [issue62](https://code.google.com/p/gwtupload/issues/detail?id=62) [issue63](https://code.google.com/p/gwtupload/issues/detail?id=63). Some changes to the decorated file upload. Added a new example using a customized image-button to open the browse dialog. Fixed an issue with sessions which made not work the progress bars the first upload.
  * Jul 09, 2010: Version 0.6, The project has been mavenized, the library is published in Maven Central repositories and the pom includes all external dependencies, see GwtUpload\_UsingMaven2. Experimental blobstore support. Enable/Disable and many other fixes. Improved security in the perl script used in non java applications (jsupload.cgi.pl) to avoid the server be used as an unauthorized storage area.
  * Apr 20, 2010: Version 0.5.8, it includes the new feature of hiding the file input rendered by the browser in favour of a customizable button. The server code for GAE has been split in a new library. It also includes many fixes.
  * Mar 16, 2010: 0.5.8-M5 (Beta) includes the ability to hide the default file input and to use a customizable a Choose button.
  * Feb 18, 2010: Created mailing list [gwtupload@googlegroups.com](http://groups.google.com/group/gwtupload/), http://groups.google.com/group/gwtupload
  * Jan 30, 2010: Version 0.5.6.
  * Nov 19, 2009: Version 0.5.5. Nothing important in gwtupload but some fixes in jsupload and cgi perl script.
  * Oct 23, 2009: Version 0.5.4 released. `FileUpload` widget can be customized.
  * Oct 11, 2009: Version 0.5.3 released. Server side can be deployed in Google App-engine, and upload listeners and file item factories can be customized. In the client side methods for handling status and cancel events have been added.
  * Sep 19, 2009: Version 0.5.2 released. It fixes some defects and improves the API, log messages and examples.
  * Sep 13, 2009: Version 0.5.1 has been released. It fixes several bugs and adds numerous improvements like cancel uploads.
# GWTUpload & JSUpload #

GWTUpload is a library for uploading files to web servers, showing a progress bar with real information about the process (file size, bytes transferred, etc). It uses ajax requests to ask the web server for the upload progress.
It has two components written in java, the server side with servlet and utility classes, and the client side that is compiled into javascript using gwt.

JSUpload is the same client library but compiled and exported into javascript, so non java developers can use it directly in web pages. I've  written an [article](http://code.google.com/p/gwtchismes/wiki/Tutorial_ExportingGwtLibrariesToJavascript_en) describing the technique used to do this.
JSUpload provides a server program coded in perl that can be installed in any web server as a cgi-bin script.

GWTUpload-GAE is a library including a special servlet to handle uploads in Google Application Engine servers (GAE).

## Goals ##
  * Both the client and server sides, are easy to use just writing a few lines of code.
  * The server side could be implemented in any language.
  * The client side can be used from gwt applications, or from javascript without knowing gwt.
  * There are available widgets for multiple and single uploads
  * You can customize the choose button looking similar in all browsers, instead of using the default file input rendered by the browser.
  * It works in any browser with js enabled, and it doesn't need any plugin installed like flash or gears.
  * The provided widgets are ready to use, in the sense that they come with a set of configured styles.
  * The user can customize the provided progress bars, or implement his own.
  * The user can configure customized functions for onChange, onStart and onFinish events
  * All the components are documented.
  * It works cross-domain out-of-the-box with browsers supporting CORS and servlet-containers supporting the url session (';jsessionid=' parameter).
  * It allows selecting multiple files in browsers supporting the multiple attribute.
  * Server side is prepared for receiving data sent using the new HTML5 FormData.

## Ajax Upload vs. Swf Upload ##
  * swfupload not only needs flash, but also specific versions of it.
  * swfupload's behavior is different for different combination of OS, browser and flash.
  * swfupload is very unstable, some times hungs the browser, some times is unable to update the progress bar.
  * swfupload doesn't work fine in linux
  * With swfupload you need to produce javascript to detect OS, browser and flash versions in order degradate the application and use the traditional way.
  * swfupload doesn't send user cookies.
  * swfupload doesn't use the browser proxy configuration
  * swfupload doesn't work with secure servers (https)

  * gwtupload needs server side code to update progress bar.

## How does it work. ##
  1. The browser renders a form with a file input and a hidden iframe.
  1. Once the user selects a file (automatically or pushing a submit button) the browser asks the server for a session cookie using an ajax request, and submits the form.
  1. The server starts the reception and continuously updates a session object with the process information.
  1. While the file is being uploaded, the browser asks periodically the server for the progress status using ajax. It is possible since most browsers can open two simultaneous connections to the same server.
  1. The server responds with a simple xml document with the real information about the size of the file and the amount of data transferred, or with an error message.
  1. The client parses the response, calculates percentage, speed, remaining time, and updates a progress bar widget with this information.
  1. Finally when the form has been completely sent, the server response is written in the iframe, instead of the main document.
  1. In the case of any error, the client shows a message to the user.
  1. The client code executes customisable methods when the file input changes, the upload process starts and finishes.
  1. It is possible to cancel the file while it is being transfered. Because of the impossibility to cancel an active upload in the client side, the browser sends an ajax request to the server, and the server closes the socket.

## Usage ##
  * For developing using gwt, read the [Getting Started](http://code.google.com/p/gwtupload/wiki/GwtUpload_GettingStarted) guide and the [library API](http://gwtupload.googlecode.com/svn/site/apidocs/core/index.html) documentation
  * API documentation for gwtupload server classes for Google appengine is  [here](http://gwtupload.googlecode.com/svn/site/apidocs/gae/index.html)
  * To use the library from javascript read the [JSUpload documentation](http://code.google.com/p/gwtupload/wiki/JsUpload_Documentation)
  * Download and deploy in a servlet container the [.war file](https://oss.sonatype.org/content/repositories/snapshots/com/googlecode/gwtupload/gwtupload-samples/0.6.4-SNAPSHOT/gwtupload-samples-0.6.4-SNAPSHOT.war) containing the project demos.

## To-dos ##
  * It should be nice if someone wanted to contribute adding swfupload, so as it were available in the appropriate browser-environment pairs and fallback to gwtupload in other cases (linux, https, slow IE, proxies etc).
  * Support HTML5 multiselect and drag&drop
  * Contributors writing code or plugins in other languages or frameworks are welcome.

# Screenshots #
  * Customizable choose button
> > ![http://gwtupload.googlecode.com/svn/trunk/website/screenshots/GWTUpload-button.jpg](http://gwtupload.googlecode.com/svn/trunk/website/screenshots/GWTUpload-button.jpg)
  * Muptiple Uploader using provided progress-bar
> > ![http://gwtupload.googlecode.com/svn/trunk/website/screenshots/GWTUpload-default.jpg](http://gwtupload.googlecode.com/svn/trunk/website/screenshots/GWTUpload-default.jpg)
  * Muptiple Uploader using GWTChismes progress-bar
> > ![http://gwtupload.googlecode.com/svn/trunk/website/screenshots/GWTUpload-chismes.jpg](http://gwtupload.googlecode.com/svn/trunk/website/screenshots/GWTUpload-chismes.jpg)
  * Muptiple Uploader using Incubator progress-bar
> > ![http://gwtupload.googlecode.com/svn/trunk/website/screenshots/GWTUpload-incubator.jpg](http://gwtupload.googlecode.com/svn/trunk/website/screenshots/GWTUpload-incubator.jpg)
  * Single uploader with a modal progress-bar
> > ![http://gwtupload.googlecode.com/svn/trunk/website/screenshots/GWTUpload-modal.jpg](http://gwtupload.googlecode.com/svn/trunk/website/screenshots/GWTUpload-modal.jpg)


---

_©2009-2012 [Manolo Carrasco Moñino](http://manolocarrasco.blogspot.com/)_
