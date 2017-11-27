# 2 ways to add audio

## 1. via `<audio>` + querySelector

1. Add audio HTML element where src is the path to the soundfile.

   `<audio src="sounds/new.ogg"></audio>`

1. Optionally add some kind of id so you can hook into it later

   `<audio src="sounds/new.ogg" data-play="addhero"></audio>`

1. Get audio element via some kind of querySelector

   `let soundAddHero = document.querySelector('audio[data-play="addhero"]');`

1. Play sound

   `soundAddHero.play();`

## 2. via new Audio()

1. Add audio in javascript by using new Audio() whose parameter is the path to
   the sound file.

   `const soundAddHero = new Audio('sounds/new.ogg');`

1. Play sound

   `soundAddHero.play();`

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
