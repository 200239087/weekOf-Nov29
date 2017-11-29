# To listen for key detection

## Use window.addEventListener('keyup')

1. Open up the console
1. Type: `window.addEventListener('keyup', (e) => console.log(e))`
1. Click outside the console (click the webpage above)
1. Try typing and observe what outputs in the console
   * Which event properties tell you what key was pressed?

## Challenges

1. Make a web page where if 'a' is pressed, then console.log('You found the
   secret key')
   * Add https://github.com/VincentGarreau/particles.js/ so that upon 'a' being
     pressed, particles runs. (need to run local server for particles.js)
1. Modify the code so that instead of 'a', it detects the word 'open'
1. Modify the password so that instead of 'open' it's up, up, down, down, left,
   right, left, right, b, a (see buzzfeed.com)
