# How to use webcam

1. Create a webpage and add an empty `<video>` tag in the body
1. Add the following script:

   ```js
   const video = document.querySelector("video");

   navigator.mediaDevices
     .getUserMedia({ video: true, audio: false })
     .then(localMediaStream => {
       console.log(localMediaStream);
       video.src = window.URL.createObjectURL(localMediaStream);
       video.play();
     })
     .catch(err => {
       console.error(`error`, err);
     });
   ```

1. View your webpage via a local server
