PHP-cURL-SOAP-Proxy
===================

For a recent project, I was tasked with needing to make a cross-domain AJAX call to a SOAP service (which cannot be done in most circumstances). To complete this task, I needed to write a quick proxy in PHP using cURL to make the actual request to the SOAP service, to make it a non-cross-domain AJAX call.

This is a pretty simple proxy and is intended to be used those who are uninitiated to the world of cURL.

The 'soap-proxy.php' file just needs to be placed somewhere on the server you will be making the AJAX call from. The 'soap-proxy-demo.html' file contains a quick little demo (that I removed my Encrypted Auth Key from so your SOAP response will say you aren't authorized). To use this, just put your SOAP request in place of mine in the JS, set up your headers (the entire JS array gets passed, so if your request needs more/different headers, you can set them up however you need), and change the SOAP endpoint to point where you need to make your request. In addition, you'll need to set up where the AJAX POST action happens (I currently have it set up in the form tag, but you could set it up in JS as well).