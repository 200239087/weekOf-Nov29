# 2 ways to add audio

## 1. via `<audio>` + querySelector

1. Add audio HTML element where src is the path to the soundfile.

   `<audio src="sounds/new.ogg"></audio>`

1. Optionally add some kind of id so you can hook into it later and/or add the
   "controls" keyword to display player

   `<audio src="sounds/new.ogg" data-play="addhero" controls></audio>`

1. Get audio element via some kind of querySelector

   `let soundAddHero = document.querySelector('audio[data-play="addhero"]');`

1. Play sound

   `soundAddHero.play();`

## 2. via new Audio()

1. Add audio in javascript by using new Audio() whose parameter is the path to
   the sound file.

   `const music = new Audio('music.mp3');`

1. Play sound

   `music.play();`

1. Pause sound

   `music.pause();`

1. View the duration of the music in seconds. See
   https://developer.mozilla.org/en-US/docs/Web/API/HTMLMediaElement/duration

   `music.duration`

1. Forward the music by 60 seconds, then play the music

   ```js
   music.currentTime = 60;
   music.play();
   ```

**See browser compatibility**
https://developer.mozilla.org/en-US/docs/Web/HTML/Supported_media_formats#Browser_compatibility

# Exercise using Audio

1. Download a soundfile from https://notificationsounds.com/tags/email
1. Create a blank webpage
1. Choosing either method above, add audio to your webpage and play it
1. Optional: make it play upon `<button>` click
1. Optional: try clicking the button many times quickly
   * Problem: audio doesn't play because it hasn't finished playing yet
   * Solution: set currentTime = 0 before play()

* Challenge: make a music player like: player.jpg that plays your existing mp3s
* Challenge: make it connect to an API like soundcloud.com

# Exercise using Video

1. Add a `<video>` tag and include the attribute:
   src="https://player.vimeo.com/external/194837908.sd.mp4?s=c350076905b78c67f74d7ee39fdb4fef01d12420&profile_id=164"

1. Add the following code:

   ```js
   const vid = document.querySelector("video");
   vid.play();
   ```
