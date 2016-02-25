# TabLayoutTest
Simple test app to show issue with 23.2.0 version of TabLayout

Steps to reproduce crash:

* Set the device Settings -> Developer options -> Don't keep activities switch to ON
* Run the test app. It defaults to two tabs. 
* Select 'Remove tab' from overflow menu.
* Select 'Empty Activity' from overflow menu to launch new Activity.
* Press Back button to return to MainActivity.

App will crash as it tries to reuse Tab in `sTabPool` 
