# PhoneGap plugin for Couchbase Lite

Couchbase Lite is an embedded JSON database for occasionally connected devices. It syncs data in the background, so users can collaborate across devices. There is an event based `_changes` JSON feed API so you can drive data-binding UI frameworks like Sencha and Backbone to reflect remote updates interactively.

It works with native code as well as Cordova / PhoneGap on iOS and Android (you can even sync with Mac desktops), so it doesn't matter where your users are, they can work with the data, and as soon as they get back online, everyone will see their changes.

For instructions on using the plugin, see the [PhoneGap Getting Started](https://developer.couchbase.com/documentation/mobile/current/installation/phonegap/index.html) page.

## Zebra 1024 Updates

* This plugin includes a CouchBase Lite Java build from the following repositories
* https://github.com/zebra1024/couchbase-lite-java-core - branch tls12fix
* https://github.com/zebra1024/couchbase-lite-android - branch tls12fix 
* The tls12fix was branched from the 1.4.1 branch.
* The CBL java code was updated to support TLS v1.2 for Android API level 16-21

The TLS v1.2 fix uses code from https://github.com/square/okhttp/issues/2372. 

###Library Updates:
* OKHttp - version 3.10.0.
* Jackson - 2.9.4
   
#Add Plugin to project
To add the plugin to Cordova run the following command.

cordova plugin add https://github.com/zebra1024/Couchbase-Lite-PhoneGap-Plugin.git#1.4.1A

## Architecture

This is where the plugin fits in the picture:

![architecture.png](http://cl.ly/image/3b15030Y3f0q/couchbase-lite-phonegap-plugin-android.png)

_Note:_ your JavaScript code can also directly communicate with Couchbase Lite over a Javascript<->Native bridge, to [ask it what URL it has launched on for subsequent XHR access](https://github.com/couchbaselabs/LiteGap/blob/master/www/litegap-example.html)

# Where to go from here

There's an [example chat app with PhoneGap](https://github.com/couchbaselabs/CouchChat-PhoneGap) that illustrates the channel sync API. You can [read more about the app here](https://github.com/couchbaselabs/CouchChat-PhoneGap).

If you made it this far, you are now ready to build your custom PhoneGap App by editing the HTML, CSS, and Javascript files under the www directory.  Your same application code will work on both the iOS and Android platforms!
