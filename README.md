# Study - StackInTheFlow Development Tool

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
 - 

## Problem 4 - Back Button Bugfix
 - https://github.com/stefan-niedermann/nextcloud-notes/pull/209/files
 
### Problem Statement :
 - Users can create and save notes on the create-note screen. If the user has started creating a new note, when the Android back button is pressed, all of their work is lost. Users have complained that they want the app to save their progress, even if they don't expilcitly press the 'save' button. 
 - Help improve the app by making the Android back button save the note as if the user had pressed the 'save' button. However, don't save the note if the user has not entered any text yet (they probably didn't intend to save an empty note). 
