# Webex Teams Browser SDK Demo

## 1) Prerequisites
Ensure you have Node.js installed on your OS and that you have a valid Webex Teams access token from [developer.webex.com](https://developer.webex.com/), this can be either a bot or personal user access token.

## 2) Build and run the demo
Open a terminal, create a new directory and run the following commands:
```
git clone https://github.com/amankhoza/webex-teams-browser-sdk-demo-with-facial-expression-recognition.git
cd webex-teams-browser-sdk-demo-with-facial-expression-recognition
npm init -y
npm install --save webex express
npm install --global browserify watchify
```
Open `public/app.js` with your favourite editor and replace `<insert_your_access_token_here>` on line 3 with your own access token.

Then run:
```
watchify public/app.js -o public/bundle.js -v
```

This will package up all of the dependencies in app.js into a bundle and automatically repeat this whenever app.js changes.

Keep that running and in a separate terminal window run:

```
node server.js
```

This will run the Express.js server which will serve the demo web app.

## 3) Try the demo

Visit [localhost:3000](http://localhost:3000) in your web browser to try the demo.

The demo sets up a video call, then performs manipulation on the local video stream and provides a visualisation for the audio in the call. Local and remote video frames can be captured programmatically, however for the purposes of the demo we have provided buttons that allow you to easily download the current local or remote video frames respectively.

This is just a brief demonsration of what you can do with the raw video and audio streams. For more information and inspiration lookup the html5 `<video>` `<audio>` and `<canvas>` tags, as well as the [Media Streams API](https://developer.mozilla.org/en-US/docs/Web/API/Media_Streams_API).

For inspiration simple facial expression recognition has also been included in this demo. To enable it click "detect facial expressions" after the call has been set up.

# Resources

[Webex Teams Browser SDK Samples](https://developer.webex.com/docs/sdks/browser/samples) | Original Single Party Call sample code taken from here. More demos can be found here.

[Mozilla Developer Guide: Audio and Video manipulation](https://developer.mozilla.org/en-US/docs/Web/Guide/Audio_and_video_manipulation) | Greyscale video manipulation code taken from here.

[Mozilla Developer Guide: Web Audio API Analyser Node](https://developer.mozilla.org/en-US/docs/Web/API/AnalyserNode) | Audio visualisation code taken from here.

[face-api.js](https://github.com/justadudewhohacks/face-api.js/) | Facial expression recognition (and more) API used in demo.
