# Design and Implementation

## Frontend

### **General Implementation framework:**


The app will be developed in Kotlin, optimized for Android, and will use the Model-View-ViewModel (MVVM) architecture. This approach will ensure a structured and efficient management of the app’s UI and business logic. 


### **Navigation framework:** 


The navigation for the app will be coded using both the standard Android Library android.navigation:navigation-ui and the Compose standard library android.navigation:navigation-compose. The Compose framework defines the top level destination and the navigation within composable context. The Android Standard Library can be used outside of the scope of Composable in particular when using standard Alert Dialog outside the scope of composable.


### **UI framework:**


The app UI will be coded using the Jetpack Compose library. This allows for many interconnected components to work together. In addition this helps ensuring the longevity of the app because of the continuous support of Jetpack Compose and easy update to later version by only changing the bom.


### **Functionality specific framework:**


Standard libraries are used to perform specific tasks: 
The Google maps library is used to provide GPS navigation. The zxing library is used for scanning QR codes. The accompanist library is used to request permissions and privileges to the Android OS.


### **Dynamic UI Rendering Strategy:**


The data layer provides method for fetching both remotely and locally data. The ViewModel is tasked with synthesizing the data and exposing fragments to be displayed to the View. The viewModel gets informed by the view any times events susceptible of changing the fragments happen.


### **Top Level Destinations:**


The top level destinations are the destination accessible either accessible through the bottom bar of the app or that are part of mandatory user flows when opening the app. 


**Login and SignUp:**
 

These screens are part of mandatory user flows. When opening the app for the first time, the user isn’t signed in and cannot access any other screen without completing one of the flows associated with these destinations.


**Chats:**


Lists all the chats we can access.


**Events:**


Lists Events that we can interact with. This screen contains 5 tabs to show different subsets of events: 'Mine' for events organized by the user, 'Feed' for events matching the settings of the profile, 'Planned' for future events the user registered to, 'Followed' for events organized by people followed by the user, and 'Attended' for passed events that were attended.

**Map:**


Browse a map on which the events are shown.

**Profile:**


Display one’s own profile and its editing options.


## Backend


**Application Logic:**


The backend server will host all necessary application logic, enabling the client application to access and consume data from the Gatherspot Firebase server. It will handle communications between different personas.


**Framework:**


The backend is comprised of tools provided by Google Firebase. This includes Firestore Database for storing data into files and collections but also authentification to provide functions to add users, authenticate as a user and verify a user with email, as well as storage used to reference and store big files such as images.


## Data Model

We will use a remote Firebase server and a local Room LiteSQL database as our Data Layer.

**Profile:**

Purpose: Manages data specific to a user that is meant to be visible by other users.
Each profile is stored as its own document with primary key "uid" in a collection "profiles". 

Fields: uid (Primary key): uid of the authentication user corresponding to the profile. ; userName (unique); Bio; Image; Interests


**Event:**


Purpose: Organize gatherings that users can take part in
Each event is stored as its own document with primary key "id" in a collection called "events".


Fields: Id (Primary key) ; Title; Description; eventStartDate; eventEndDate; timeBeginning; timeEnding; attendanceMaxCapacity; attendanceMinCapacity; inscriptionLimitDate; inscriptionLimitTime; categories; organizerID; registeredUsers; finalAttendees; image


**Rating:**


Purpose: Collect user data about how well a passed event went, provide feedback on how well an event was rated as well as how well an organizer was rated in the past.
Individual rating by a user with id "uid" for the event with id eventID. It is stored in the collection: "event_ratings/\$eventID/attendee_ratings" as a document with id: $uid and field: rating. 


The individual ratings in attendees_ratings are aggregated into a document stored in the collection: "event_ratings" in document with id: "eventID" with fields: average (representing the average of ratings for the event), count (representing the number of ratings for the event), and eventID. This constitutes the event rating.


The event ratings get aggregated into an organizer rating in a document stored in the collection "organizer_ratings" where the id of the document is the field "organizerID" of the event with id "eventID" and the fields are: nEvents (the number of events organized by the organizer), nRatings (the number of ratings received on all events organized by the organizer), overallAverage (average of all ratings received on all events organized by the organizer)
This constitutes an organizer rating.


**Following:**


Purpose: List all the profiles followed by a user
In the case of the user with id "uid" following the profiles with uids $uid_1$, $uid_2$ , …, $uid_k$.
Each of the profiles followed are stored in their own document with id $uid_i$ in the collection "ID_LIST/FOLLOWING/uid".


**Followers:**


Purpose: List all the users that follow a particular profile.
In the case of the user with id "uid" being followed by the profiles with uids $uid_1$, $uid_2$ , …, $uid_k$.
Each of the profile uid are stored in the document located at "ID_LIST/FOLLOWERS/uid"


**Chat message:**


Purpose: Allow for participants and organizers to communicate through a dedicated chat channel.
In the case of a message sent by user with id "uid" in the chat of the event with id "eventID",
it will be stored in its own document in a collection "chatMessages/eventID/messages/id".

Fields: message, senderID(takes value uid), timestamp
 

**How is it shared/copied/cached?**


## Security Considerations


To maintain the integrity of the data we need to worry about writing privileges. At the moment our Firebase database does not discriminate between users and provides them all with the same writing privileges. The following are ideas on how to improve our Cloud Firestorm’s rules framework.


Many documents have no collision as far as writing is concerned, meaning that only one user should write into a document.


**Unique write access**


Chat messages should never be modified and are each stored in a separate document. Therefore the chat messages collection is purely additive in nature and only needs protection against overwriting existing files but no particular authentication check.


**Single exclusive write access**


Documents: profiles/uid, ID_LIST/FOLLOWING/uid and event_ratings/***/attendees_ratings/uid only allow the user corresponding to uid to write into that file.


**Share write access**


Documents: Events in /events/ should be in theory only be modified by the users with uid matching the field organizerID in the documents with the exception of the fields: finalAttendee and registeredUsers which allow any user to append themselves to the list. Hence one user may have all writing privileges over that document when the rest may only have specific append privileges on existing file.


**Automated writes**


Folders: /ID_LIST/, /organizer_ratings/ and /event_ratings/ are all made to maintain coherence with other writes that are initiated by an end point persona-user. A system automated sudo user could have an exclusive privilege to write the fields of these files to maintain coherence of the database.


## Infrastructure and Deployment


The app doesn’t require any additional infrastructure at the moment as all changes in the backend data are triggered by some frontend user activity. Therefore when necessary transactions cascade into another, it causes the user to be unknowingly complicit in maintaining the coherence of our database. 
The accessibility of the database is ensured by Firebase.


## Test Plan


**Firebase Connection Test**


We have compiled functions meant to communicate with Firebase in classes call FirebaseConnection and written tests for them. This is crucial to monitor correct behavior of the app when rolling out new changes but also as a proactive measure to monitoring changes to these services in order to quickly correct failures.


**ViewModel Tests**


These tests are possibly also dependent on the success of FirebaseConnectionTest since they monitor the correct behavior of the viewModels. They should be tested thoroughly in order to ensure the minimum privilege principle is respected.



