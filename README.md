*annyang!*
-----------------------------------------------

A tiny javascript SpeechRecognition library that lets your users control your site with voice commands.

annyang has no dependencies, weighs just 2kb, and is free to use and modify under the MIT license.

Demo
----
[Visit the demo and docs site](https://www.talater.com/annyang)

Usage
-----
It's as easy as adding [one javascript file](//cdnjs.cloudflare.com/ajax/libs/annyang/1.1.0/annyang.min.js) to your document, and defining the commands you want.
````html
<script src="//cdnjs.cloudflare.com/ajax/libs/annyang/1.1.0/annyang.min.js"></script>
<script>
if (annyang) {
  // Let's define a command.
  var commands = {
    'show tps report': function() { $('#tpsreport').show(); }
  };

  // Add our commands to annyang
  annyang.addCommands(commands);

  // Start listening.
  annyang.start();
}
</script>
````

**For more details, [visit the demo and docs site](https://www.talater.com/annyang).**

(annyang) would like to use your microphone
----------
![](http://i.imgur.com/96AcBjh.png)

SpeechRecognition API behaves differently based on the protocol used:

- `http://`: Asks for permission repeatedly on every page load.

- `https://`: Asks for permission once and remembers the choice.

- `file://`: SpeechRecognition doesn't work on file protocol. Use a web server with http or https.

Author
------
Tal Ater: [@TalAter](https://twitter.com/TalAter)

Developing
-------

Prerequisities: node.js

First, install dependencies:

    cd <project_folder>
    npm install -g grunt-cli
    npm install

Then run:

    grunt dev

Point your browser to `https://localhost:8443/demo/` to see the demo page. Since it's using self-signed certificate, you might need to *"Proceed Anyway"*.

License
-------
Licensed under [MIT](https://github.com/TalAter/annyang/blob/master/LICENSE).
