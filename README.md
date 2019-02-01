# ArduinoVisualIDE
Creating this project on GitHub to facilitate Bug and Issue tracking as well as communication. 

Deployed system available here - https://arduinovisualcreator.azurewebsites.net

Will commit the source code at some later date.


## General
This is a work in progress, so some notes:
 - Things are not perfect but constantly improving!
 - Features will be added, changed or removed over time.
 - There is a cookie created to help load the last sketch you where working on.
 - No other activity of yours is tracked except for some Telemetry captured through Application Insights.
 - Not all the libraries and boards are installed. Please make contact to get one installed.


## Arduino Create Agent
In order to allow you to upload a sketch directly from the creator you will need to:
1. Download and install the 'Arduino Create Agent' from [here](https://github.com/RealRoTeD/ArduinoVisualIDE).
2. Update the configuration of the 'Arduino Create Agent' to allow the site to communicate with it:
   1. Navigate to the installation directory of the Arduino Create Agent.
   2. Open the 'config.ini' file in a text editor.
   3. Find the line containing: origins = http://local.arduino.cc:8000
   4. Alter it so that it looks like: origins = \`http://local.arduino.cc:8000, https://arduinovisualcreator.azurewebsites.net`
   5. Save the file and restart the Arduino Create Agent.

Sample ini file can be located [here](https://github.com/RealRoTeD/ArduinoVisualIDE/config.ini).


## Special Thanks
Special thanks to:
 - Arduino Create Agent - https://github.com/arduino/arduino-create-agent
 - Arduino CLI - https://github.com/arduino/arduino-cli

Without these projects the Verify and Upload functions would not be possible.


##  Current Version: 0.0.10
###### Release Notes:
0.0.10-2019/02/01
 - ENH - Added blank drop down for empty selector on object/type.
 - ENH - Created a shared dropdown control that is reused throughout the solution.
 - ENH - Added a way to specify unsigned and volatile from a drop down.
 - ENH - Added in conversion for unsigned from previous versions of sketches.
 - ENH - Altered the menu and base sketch to include the changes made to unsigned.

0.0.9-2019/01/18
 - BUG - Resolved an issue where the move no longer works.
 - BUG - Fix a problem where the move will just create a new wrapper each time it is dropped instead of reusing old one.
 - ENH - Small edit to the about page to fix a layout issue.

0.0.8-2019/01/16
 - ENH - Changed the way the drop down menu works rather than accessing the DOM.
 - ENH - Making the control menu collapse in order to accommodate smaller displays.
 - ENH - Added in a Ctrl+Click handler that will continue a delete and duplicate operation.
 - ENH - Improved memory utilization by clearing control parameters.
 - ENH - Added an Arduino CLI screen to display the installed Platforms and Libraries.

0.0.7-2019/01/11
 - BUG - Fixed the level at which certain boxes are displayed.
 - ENH - Added a cookie consent pop up.
 - ENH - Added a loading screen when importing the sketch or loading the auto save.

0.0.6-2019/01/06
 - BUG - Resolved a problem where there is not enough room to display Line Numbers bigger than 1 character.
 - ENH - Changed the way the messages are displayed in the console.

0.0.5-2019/01/02
 - BUG - Resolved a problem were clearing of names stopped working.
 - ENH - Added some content to the about page.

0.0.4-2018/12/07
 - BUG - Solved an issue where the value and name boxes are not displayed on FireFox.
 - BUG - When cloning a control you can now immediately place it.

0.0.3-2018/12/01
 - ENH - Added a Verify function to the creator.
 - ENH - Added an Upload function to the creator that uses the 'Arduino Create Agent'.
 - ENH - Re-factored large portions of the services in order to improve the code.
 - ENH - Added a loading component and made use of it.
 - ENH - Changed the Creator Tools menu in order to clear some clutter.

0.0.2-2018/11/17
 - BUG - Moved setting up the component map into the workspace in order to prevent a circular dependency.
 - BUG - Added missing short to the allowed type lists for functions and variable declarations.
 - ENH - Changed the file export and auto save mechanisms in order to encode the sketch json in base64 format in order to prevent conflicts.

0.0.1-2018/11/16
 - ENH - Added Line Numbers to the work space and a way to flick them On or Off.
 - ENH - Added a Save button that will save the sketch to a temporary location.

0.0.0-2018/11/13
 - Initial release
