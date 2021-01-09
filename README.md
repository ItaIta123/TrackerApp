## Demo Video
https://youtu.be/JbvDDr5NcFE

## TrackerApp ##

As an off-road driver and a person who loves traveling in nature, I have always looked for an app that can record my trip. Tracker is an app that supplies exactly that!
It was important for me to develop an app in which I could come back anytime and see exactly where I traveled and some interesting information about my trips such as the highest altitude, speeds and etc...

## Devolpoing process ##
I created a RESTful API using Node Express and connected it to the MongoDB server. 
The app uses an authentication process, saving and reading Json Web Token on and from the device. The passwords in MongoDB are Hashed using a hash generator. For more info visit the Track-server repository.
Server development and testing were done using Postman and ngrok.

## Running Process ##
1. cd to track-server/ folder in the Terminal and run: "npm run dev" (this will connect us to the MongoDB server)
2. cd to tracks/ folder and run: "./ngrok http 3000"
3. After running the ngrok command copy the first Forwarding HTTP address to the tracker.js file (exp: http://176373b363ac.ngrok.io). A successful connection will post {"error":"You must be logged in."}
4. In order to cancel the artificial location movement (for the lazy people), go to TrackCreateScreen.js and comment out the first-row import "../_mockLocation";
5. The Lottie animation in the TrackCreateScreen.js might cause Android phones to crash.
