# Set up Speech Synthesis Voice

see
https://developer.mozilla.org/en-US/docs/Web/API/SpeechSynthesisUtterance/lang

1. Type the following code and play with changing/hearing the text:

   ```js
   // set up speech synthesis voice
   const host = new SpeechSynthesisUtterance();
   host.lang = "en-US";
   host.text = "hello world";
   speechSynthesis.speak(host);
   ```

1. Create a webpage with an h1 of 'hello world'
1. Make browser speak h1's text content.
1. Type `host` to see what the console outputs.
1. Type `speechSynthesis` to see what the console outputs.
   * How would you view all the voices available?
1. Set a different voice using `host.voice = speechSynthesis.getVoices()[4]`
1. Type `host.rate = 1.5` to hear what it sounds like. How about 0.5?
