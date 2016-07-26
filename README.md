# Cordova Alert Plugin

Simple plugin that shows alert dialog in Android and IOS.

A alert dialog with title, message and button label. You can pass title, message and button label as a parameters. This plugin provides a simple example demonstrating how Cordova plugins work.

## Using
Clone the plugin

    $ git clone https://github.com/amitbindal09/cordova-plugin-alert.git

Create a new Cordova or Ionic Project

    $ cordova create Alert com.example.alertapp Alert
    $ ionic start Alert blank
    

Install iOS or Android platform

    cordova platform add ios
    cordova platform add android
    
Install the plugin

    $ cd Alert
    $ cordova plugin add path_to_plugin/cordova-plugin-alert
    

And add the following code inside `onDeviceReady`

```js
    var success = function(message) {
        alert(message);
    }
    
    Alert.alert('Put Title Here', 'Put Message Here', 'Put Button Label', success);
```
You can also call this by directly `cordova.exec`

```js
    cordova.exec(function(result){console.log(result)},
                null, // No failure callback
                "Alert",
                "alert",
                ['title', 'message', 'buttonLabel']);
```
    
Run the code

    cordova run 

## More Info

For more information on setting up Cordova see [the documentation](http://cordova.apache.org/docs/en/4.0.0/guide_cli_index.md.html#The%20Command-Line%20Interface)

For more info on plugins see the [Plugin Development Guide](http://cordova.apache.org/docs/en/4.0.0/guide_hybrid_plugins_index.md.html#Plugin%20Development%20Guide)
