Android HTML5 WebSocket 
=======================

A Java library that make the WebSocket object available for project that uses a WebView (like PhoneGap project's)

The iOS version of the plugin was already existant (http://github.com/remy/PhoneGap-Plugin-WebSocket) and works well 
for me, and now here is the Android version.

/!\ it has never been really tested, even on real devide !

Usage
=====

* copy the Java source into the source folder of your project.
* copy websocket.js in your assets/www folder
* copy / paste these two line inside the onCreate of your activity
WebSocketFactory wsFactory = new WebSocketFactory(appView);
appView.addJavascriptInterface(wsFactory, "WebSocketFactory");

* in your javascript, create a new WebSocket, and overload its method 'onmessage', 'onopen', 'onerror', 'onclide';
