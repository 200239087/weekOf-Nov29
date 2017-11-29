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

1. Now modify your HTML so includes both the `<video>` tag and the `<canvas>`
   tag, then change the script to look like this:

```js
const video = document.querySelector("video");
const canvas = document.querySelector("canvas");
const ctx = canvas.getContext("2d");

navigator.mediaDevices
  .getUserMedia({ video: true, audio: false })
  .then(localMediaStream => {
    console.log(localMediaStream);
    video.src = window.URL.createObjectURL(localMediaStream);
    // video.play();
  })
  .catch(err => {
    console.error(`error`, err);
  });

function takePhoto() {
  // take the data out of the canvas
  const data = canvas.toDataURL("image/jpeg");
  const link = document.createElement("a");
  link.href = data;
  link.setAttribute("download", "handsome");
  link.innerHTML = `<img src="${data}" alt="Handsome Man" />`;
  document.body.insertAdjacentElement("beforeEnd", link);
}

video.addEventListener("canplay", function() {
  const width = video.videoWidth;
  const height = video.videoHeight;
  canvas.width = width;
  canvas.height = height;

  return setInterval(() => {
    ctx.drawImage(video, 0, 0, width, height);
  }, 16);
});
```

1. Test it by loading the page via local server, then in console run function by
   typing: `takePhoto()`

# Challenge:

1. Create a photobooth style app
