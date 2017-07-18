# Study - StackInTheFlow Development Tool
## General Guidlines :
There have been a few modifications to the codebase that is specific for this study. 
- We have created a bypass for user/server authentication. As long as you fill each field on the settings page, you should be logged in.
- All server communication and persitance has been disabled. To better simulate server latency, there is a slight delay added to every server call.

Although these changes may be related to the given problems, they don't directly affect solving the problems and should not be altered during the study.

## Problem 1 - Swipe Delete Enhancement
 - https://github.com/stefan-niedermann/nextcloud-notes/pull/185/files

### Problem Statement :
 - Users are able to delete notes by swiping left or right when viewing the note-list screen. However, some users are reporting that it is not clear what the swipe motion does until after the note is deleted. Also, some have said that the swipe motion requires too little horizontal distance and therefore makes it easy to accidently delete notes.
 - Help improve the app by adding an icon/animation that appears when the user attempts to swipe a note. It should inform the user that if the swipe is completed, the note will be deleted. Also, make the it harder for a user to accidently delete a note through swiping by making the swipe motion longer. 

## Problem 2 - Splash Screen Enhancement
 - https://github.com/stefan-niedermann/nextcloud-notes/commit/472d549677ea0ed8a14400667a27a802fa925fed
 
### Probelm Statement :
 - When users starts the app, they are taken to the note-list screen directly, unless they haven't configured the settings yet. If the user has entered the persistance-server information and credentials previously, the app will automatically attempt to make a connection to the server. Depending on the latency, this could take a few seconds which blocks the users interaction with the app. 
 - Help improve the user experience by creating a splash screen that displays when the user starts the app. It should help obfuscate the latency between the app and the server.

## Problem 3 - Saved Password Bugfix
 - https://github.com/stefan-niedermann/nextcloud-notes/pull/208/files

### Problem Statement :
 - Users are able to configure their server authentication credentials on the settings screen. If they are entering their password, they have the option to toggle the password obfuscation. If the users go to the settings screen after the credentials have already been configured, the credentials stay in the form, to let the user know what credentials are being used. However, if the user has previously entered their credentials and then returns to the settings screen, the old password can still be deobfuscated. This is a security issue.
 - Help improve the app by not letting the user deobfuscate the password if it is the saved password. The user should still be able to deobfuscate the password if it has just been entered.

## Problem 4 - Back Button Bugfix
 - https://github.com/stefan-niedermann/nextcloud-notes/pull/209/files
 
### Problem Statement :
 - Users can create and save notes on the create-note screen. If the user has started creating a new note, when the Android back button is pressed, all of their work is lost. Users have complained that they want the app to save their progress, even if they don't expilcitly press the 'save' button. 
 - Help improve the app by making the Android back button save the note as if the user had pressed the 'save' button. However, don't save the note if the user has not entered any text yet (they probably didn't intend to save an empty note). 
