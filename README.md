#Using
1. clone pingxx plugin

        $git clone git@github.com:oumind/cordova-plugin-pingxx.git
    
2. clone the demo project

        $git clone git@github.com:oumind/cordova-pingxx-demo.git

3. Install the plugin

        $cd cordova-pingxx-demo
        $cordova plugin add ../cordova-plugin-pingxx/ --variable URL_SCHEME=YOUR-URL-SCHEME
        
    URL_SCHEME is your app URL_SCHEME,about URL_SCHEME,you can see this project
    [EddyVerbruggen/Custom-URL-scheme](https://github.com/EddyVerbruggen/Custom-URL-scheme)
   
         
4. add ios platform

        cordova platform add ios
        
5. change code www/js/index.js

              pingxx.createPayment(charge, 'YOUR-URL-SCHEME');//TODO YOUR-URL-SCHEME is what in this command you hava specified
                                                                        // $cordova plugin add ../cordova-plugin-pingxx/ --variable URL_SCHEME=YOUR-URL-SCHEME

6. run the code

        $cordova run
        
#URL Scheme hints
##Please choose a URL_SCHEME which which complies to these restrictions:
- Don't use an already registered scheme (like `fb`, `twitter`, `comgooglemaps`, etc).
- Use only lowercase characters.
- Don't use a dash `-` because on Android it will become underscore `_`.
- Use only 1 word (no spaces).

TIP: test your scheme by installing the app on a device or simulator and typing yourscheme:// in the browser URL bar, or create a test HTML page with a link to your app to impress your buddies.
        
    
