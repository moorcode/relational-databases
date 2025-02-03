# Relationsal Databases

## Boilerplate

In this 170-lesson course, you will learn terminal commands by creating a website boilerplate using only the command line.

This course runs in a virtual Linux machine using Gitpod.

1. __The first thing you need to do is start the terminal.__ Do that in VS Code the short way by pressing `ctrl+shift+\`\` , or the long way by clicking the _hamburger_ menu at the top left of the screen, going to the _terminal_ section, and clicking _new terminal_. Once you open a new one, type `echo hello terminal` into the terminal and press enter.

```
camper: /project$ echo hello terminal
hello terminal
```

2. What you see in the terminal is a __folder (or directory)__ on your machine. Type `pwd` into the terminal and press enter to see the __path__ of the folder. `pwd` stands for __print working directory__.

```
camper: /project$ pwd
/workspace/project
```

3. The output tells you where the folder you are in is located. In Gitpod, you are in the project folder, which is in the workspace folder. Type `ls` into the terminal to see what's in this folder. `ls` stands for __list__. 

```
camper: /project$ ls
freeCodeCamp
```

4. The output is showing everything in this folder. There's one folder in here. You can use `cd <folder_name>` to go into a folder. `cd` stands for __change directory__. Change to the `freeCodeCamp` directory.
	
> [!TIP]
> `Tab`will complete the folder name.

```
camper: /project$ cd freeCodeCamp/
camper: /freeCodeCamp$ 
```

5. You are in the `freecodecamp` folder now. You may have noticed that the prompt changed to include it. Print the working directory of the `freeCodeCamp` folder to see the full path of where you are.

```
camper: /freeCodeCamp$ pwd
/workspace/project/freeCodeCamp
```

6. You can see the path of the `freeCodeCamp` folder. It's in the project folder you were just in. List the contents of the `freeCodeCamp` folder to see what's here.

```
camper: /freeCodeCamp$ ls
node_modules  package.json  package-lock.json  reset.sh  setup.sh  test
```

7. There're several folders and files here. The folders are blue or green and the files include their extension. Next, change to that `test` directory.

```
camper: /freeCodeCamp$ cd test
camper: /test$ 
```

8. You can see you are in the `test` folder now. It shows `test` in the prompt. Print the full path of this directory. Remember that __folder__ and __directory__ are the same thing.

```
camper: /test$ pwd
/workspace/project/freeCodeCamp/test
```

9. That's the path to the `test` folder, it's in the `freeCodeCamp` folder. List the contents of this folder.

```
camper: /test$ ls
1000.test.js  1170.test.js  1330.test.js  1490.test.js  250.test.js  430.test.js  60.test.js   790.test.js
100.test.js   1190.test.js  1340.test.js  1500.test.js  260.test.js  440.test.js  610.test.js  800.test.js
1010.test.js  1195.test.js  1350.test.js  150.test.js   270.test.js  450.test.js  620.test.js  80.test.js
1020.test.js  1200.test.js  1360.test.js  1510.test.js  280.test.js  460.test.js  630.test.js  850.test.js
1030.test.js  120.test.js   1370.test.js  1520.test.js  285.test.js  470.test.js  640.test.js  860.test.js
1040.test.js  1210.test.js  1380.test.js  1530.test.js  290.test.js  480.test.js  650.test.js  870.test.js
1050.test.js  1215.test.js  1390.test.js  160.test.js   300.test.js  490.test.js  660.test.js  880.test.js
1055.test.js  1220.test.js  1400.test.js  170.test.js   30.test.js   500.test.js  670.test.js  890.test.js
1060.test.js  1230.test.js  1405.test.js  180.test.js   310.test.js  50.test.js   680.test.js  900.test.js
1065.test.js  1240.test.js  140.test.js   181.test.js   320.test.js  510.test.js  690.test.js  90.test.js
1070.test.js  1250.test.js  1410.test.js  182.test.js   330.test.js  520.test.js  700.test.js  910.test.js
1080.test.js  1260.test.js  1415.test.js  183.test.js   340.test.js  530.test.js  70.test.js   920.test.js
1090.test.js  1270.test.js  1420.test.js  184.test.js   350.test.js  540.test.js  710.test.js  930.test.js
10.test.js    1275.test.js  1430.test.js  185.test.js   360.test.js  550.test.js  720.test.js  940.test.js
1100.test.js  1280.test.js  1440.test.js  190.test.js   370.test.js  560.test.js  730.test.js  950.test.js
110.test.js   1290.test.js  1445.test.js  200.test.js   380.test.js  570.test.js  740.test.js  960.test.js
1110.test.js  1300.test.js  1450.test.js  20.test.js    390.test.js  580.test.js  750.test.js  970.test.js
1120.test.js  130.test.js   1460.test.js  210.test.js   400.test.js  585.test.js  755.test.js  980.test.js
1130.test.js  1310.test.js  1470.test.js  220.test.js   40.test.js   590.test.js  760.test.js  990.test.js
1135.test.js  1315.test.js  1475.test.js  230.test.js   410.test.js  5.test.js    770.test.js  utils.js
1150.test.js  1320.test.js  1480.test.js  240.test.js   420.test.js  600.test.js  780.test.js
```

10. These are all files. There's no more folders to go into here. You can use `cd ..` to go back a folder level. The two dots will take you back one level. Go back to the `freeCodeCamp` folder.

```
camper: /test$ cd ..
camper: /freeCodeCamp$ 
```

11. `test` got removed from the prompt since you left that folder and you're back in the `freeCodeCamp` folder. List the contents of what's here to remind yourself

```
camper: /freeCodeCamp$ ls
node_modules  package.json  package-lock.json  reset.sh  setup.sh  test
```

12. There's the `test` folder you were just in. You can see what's in a file with `more <filename>`. Use it to view what's in the `package.json` file.

> [!TIP]
> `Enter` advances one line. _Down arrow_ advances to the end.

```
camper: /freeCodeCamp$ more package.json 
{
  "name": "freecodecamp",
  "version": "1.0.0",
  "description": "",
  "main": "index.js",
  "scripts": {
    "programmatic-test": "mocha --config .mocharc.json",
    "test": "mocha --config .mocharc.json"
  },
  "author": "",
  "license": "ISC",
  "dependencies": {
    "mocha": "^7.2.0",
    "mocha-tap-reporter": "^0.1.3",
    "shell-quote": "^1.7.2"
  }
--More--(99%)
```

13. It looks like a __JSON object__. You can empty the terminal with `clear`. The terminal looks a little cluttered, why don't you `clear` it.

14. Now you have a fresh screen 😄 List what's in here again.

```
camper: /freeCodeCamp$ ls
node_modules  package.json  package-lock.json  reset.sh  setup.sh  test
```

15. You checked out the `test` folder and the `package.json` file. What next? Why don't you go into that `node_modules` directory.

```
camper: /freeCodeCamp$ cd node_modules/
camper: /node_modules$ 
```

16. Now the prompt includes `node_modules` since that's where you are. List what's in the folder.

```
camper: /node_modules$ ls
ansi-colors           es-to-primitive          is-regex                          readdirp
ansi-regex            fill-range               is-symbol                         require-directory
ansi-styles           find-up                  js-yaml                           require-main-filename
anymatch              flat                     locate-path                       semver
argparse              fs.realpath              lodash                            set-blocking
balanced-match        function-bind            log-symbols                       shell-quote
binary-extensions     get-caller-file          minimatch                         sprintf-js
brace-expansion       glob                     minimist                          string.prototype.trimend
braces                glob-parent              mkdirp                            string.prototype.trimstart
browser-stdout        growl                    mocha                             string-width
camelcase             has                      mocha-tap-reporter                strip-ansi
chalk                 has-flag                 ms                                strip-json-comments
chokidar              has-symbols              node-environment-flags            supports-color
cliui                 he                       normalize-path                    to-regex-range
color-convert         inflight                 object.assign                     which
color-name            inherits                 object.getownpropertydescriptors  which-module
concat-map            is-binary-path           object-inspect                    wide-align
debug                 is-buffer                object-keys                       wrap-ansi
decamelize            is-callable              once                              wrappy
define-properties     is-date-object           path-exists                       y18n
diff                  isexe                    path-is-absolute                  yargs
emoji-regex           is-extglob               picomatch                         yargs-parser
es-abstract           is-fullwidth-code-point  p-limit                           yargs-unparser
escape-string-regexp  is-glob                  p-locate
esprima               is-number                p-try
```

17. That's a lot of folders. You can add a __flag__ to a command to use it different ways like this: `ls <flag>`. List the contents of the `node_modules` folder in _long list format_. Do that by adding the `-l` flag to the _list_ command.

```
camper: /node_modules$ ls -l
total 80
drwxr-xr-x  3 gitpod gitpod   105 Feb  3 08:43 ansi-colors
drwxr-xr-x  2 gitpod gitpod    74 Feb  3 08:43 ansi-regex
drwxr-xr-x  2 gitpod gitpod    74 Feb  3 08:43 ansi-styles
drwxr-xr-x  2 gitpod gitpod    92 Feb  3 08:43 anymatch
drwxr-xr-x  3 gitpod gitpod   105 Feb  3 08:43 argparse
drwxr-xr-x  2 gitpod gitpod    95 Feb  3 08:43 balanced-match
drwxr-xr-x  2 gitpod gitpod   157 Feb  3 08:43 binary-extensions
drwxr-xr-x  2 gitpod gitpod    74 Feb  3 08:43 brace-expansion
drwxr-xr-x  3 gitpod gitpod   105 Feb  3 08:43 braces
drwxr-xr-x  2 gitpod gitpod    74 Feb  3 08:43 browser-stdout
drwxr-xr-x  2 gitpod gitpod    92 Feb  3 08:43 camelcase
drwxr-xr-x  4 gitpod gitpod   148 Feb  3 08:43 chalk
drwxr-xr-x  4 gitpod gitpod    98 Feb  3 08:43 chokidar
drwxr-xr-x  3 gitpod gitpod   118 Feb  3 08:43 cliui
drwxr-xr-x  2 gitpod gitpod   132 Feb  3 08:43 color-convert
drwxr-xr-x  2 gitpod gitpod   129 Feb  3 08:43 color-name
drwxr-xr-x  4 gitpod gitpod   126 Feb  3 08:43 concat-map
drwxr-xr-x  4 gitpod gitpod   116 Feb  3 08:43 debug
drwxr-xr-x  2 gitpod gitpod    74 Feb  3 08:43 decamelize
drwxr-xr-x  3 gitpod gitpod   181 Feb  3 08:43 define-properties
drwxr-xr-x  4 gitpod gitpod   163 Feb  3 08:43 diff
drwxr-xr-x  3 gitpod gitpod   129 Feb  3 08:43 emoji-regex
drwxr-xr-x 12 gitpod gitpod  4096 Feb  3 08:43 es-abstract
drwxr-xr-x  2 gitpod gitpod    74 Feb  3 08:43 escape-string-regexp
drwxr-xr-x  4 gitpod gitpod   102 Feb  3 08:43 esprima
drwxr-xr-x  5 gitpod gitpod  4096 Feb  3 08:43 es-to-primitive
drwxr-xr-x  2 gitpod gitpod    74 Feb  3 08:43 fill-range
drwxr-xr-x  2 gitpod gitpod    74 Feb  3 08:43 find-up
drwxr-xr-x  3 gitpod gitpod   119 Feb  3 08:43 flat
drwxr-xr-x  2 gitpod gitpod    88 Feb  3 08:43 fs.realpath
drwxr-xr-x  3 gitpod gitpod  4096 Feb  3 08:43 function-bind
drwxr-xr-x  2 gitpod gitpod   115 Feb  3 08:43 get-caller-file
drwxr-xr-x  2 gitpod gitpod   125 Feb  3 08:43 glob
drwxr-xr-x  2 gitpod gitpod    74 Feb  3 08:43 glob-parent
drwxr-xr-x  3 gitpod gitpod   155 Feb  3 08:43 growl
drwxr-xr-x  4 gitpod gitpod    85 Feb  3 08:43 has
drwxr-xr-x  2 gitpod gitpod    74 Feb  3 08:43 has-flag
drwxr-xr-x  4 gitpod gitpod   173 Feb  3 08:43 has-symbols
drwxr-xr-x  4 gitpod gitpod   101 Feb  3 08:43 he
drwxr-xr-x  2 gitpod gitpod    77 Feb  3 08:43 inflight
drwxr-xr-x  2 gitpod gitpod   104 Feb  3 08:43 inherits
drwxr-xr-x  2 gitpod gitpod    92 Feb  3 08:43 is-binary-path
drwxr-xr-x  2 gitpod gitpod    92 Feb  3 08:43 is-buffer
drwxr-xr-x  4 gitpod gitpod  4096 Feb  3 08:43 is-callable
drwxr-xr-x  4 gitpod gitpod   175 Feb  3 08:43 is-date-object
drwxr-xr-x  3 gitpod gitpod   137 Feb  3 08:43 isexe
drwxr-xr-x  2 gitpod gitpod    74 Feb  3 08:43 is-extglob
drwxr-xr-x  2 gitpod gitpod    74 Feb  3 08:43 is-fullwidth-code-point
drwxr-xr-x  2 gitpod gitpod    74 Feb  3 08:43 is-glob
drwxr-xr-x  2 gitpod gitpod    74 Feb  3 08:43 is-number
drwxr-xr-x  4 gitpod gitpod   178 Feb  3 08:43 is-regex
drwxr-xr-x  4 gitpod gitpod  4096 Feb  3 08:43 is-symbol
drwxr-xr-x  5 gitpod gitpod   128 Feb  3 08:43 js-yaml
drwxr-xr-x  2 gitpod gitpod    74 Feb  3 08:43 locate-path
drwxr-xr-x  3 gitpod gitpod 20480 Feb  3 08:43 lodash
drwxr-xr-x  2 gitpod gitpod   110 Feb  3 08:43 log-symbols
drwxr-xr-x  2 gitpod gitpod    78 Feb  3 08:43 minimatch
drwxr-xr-x  4 gitpod gitpod   126 Feb  3 08:43 minimist
drwxr-xr-x  3 gitpod gitpod    91 Feb  3 08:43 mkdirp
drwxr-xr-x  5 gitpod gitpod   187 Feb  3 08:43 mocha
drwxr-xr-x  3 gitpod gitpod    70 Feb  3 08:43 mocha-tap-reporter
drwxr-xr-x  2 gitpod gitpod    77 Feb  3 08:43 ms
drwxr-xr-x  2 gitpod gitpod   151 Feb  3 08:43 node-environment-flags
drwxr-xr-x  2 gitpod gitpod    74 Feb  3 08:43 normalize-path
drwxr-xr-x  4 gitpod gitpod  4096 Feb  3 08:43 object.assign
drwxr-xr-x  4 gitpod gitpod  4096 Feb  3 08:43 object.getownpropertydescriptors
drwxr-xr-x  5 gitpod gitpod  4096 Feb  3 08:43 object-inspect
drwxr-xr-x  3 gitpod gitpod  4096 Feb  3 08:43 object-keys
drwxr-xr-x  2 gitpod gitpod    73 Feb  3 08:43 once
drwxr-xr-x  2 gitpod gitpod    74 Feb  3 08:43 path-exists
drwxr-xr-x  2 gitpod gitpod    74 Feb  3 08:43 path-is-absolute
drwxr-xr-x  3 gitpod gitpod   105 Feb  3 08:43 picomatch
drwxr-xr-x  2 gitpod gitpod    92 Feb  3 08:43 p-limit
drwxr-xr-x  2 gitpod gitpod    74 Feb  3 08:43 p-locate
drwxr-xr-x  2 gitpod gitpod    92 Feb  3 08:43 p-try
drwxr-xr-x  2 gitpod gitpod    92 Feb  3 08:43 readdirp
drwxr-xr-x  2 gitpod gitpod   134 Feb  3 08:43 require-directory
drwxr-xr-x  2 gitpod gitpod    98 Feb  3 08:43 require-main-filename
drwxr-xr-x  3 gitpod gitpod   123 Feb  3 08:43 semver
drwxr-xr-x  2 gitpod gitpod    98 Feb  3 08:43 set-blocking
drwxr-xr-x  4 gitpod gitpod   146 Feb  3 08:43 shell-quote
drwxr-xr-x  6 gitpod gitpod   161 Feb  3 08:43 sprintf-js
drwxr-xr-x  4 gitpod gitpod  4096 Feb  3 08:43 string.prototype.trimend
drwxr-xr-x  4 gitpod gitpod  4096 Feb  3 08:43 string.prototype.trimstart
drwxr-xr-x  2 gitpod gitpod    74 Feb  3 08:43 string-width
drwxr-xr-x  2 gitpod gitpod    74 Feb  3 08:43 strip-ansi
drwxr-xr-x  2 gitpod gitpod    74 Feb  3 08:43 strip-json-comments
drwxr-xr-x  2 gitpod gitpod    92 Feb  3 08:43 supports-color
drwxr-xr-x  2 gitpod gitpod    74 Feb  3 08:43 to-regex-range
drwxr-xr-x  3 gitpod gitpod   105 Feb  3 08:43 which
drwxr-xr-x  2 gitpod gitpod    94 Feb  3 08:43 which-module
drwxr-xr-x  2 gitpod gitpod    74 Feb  3 08:43 wide-align
drwxr-xr-x  3 gitpod gitpod    94 Feb  3 08:43 wrap-ansi
drwxr-xr-x  2 gitpod gitpod    75 Feb  3 08:43 wrappy
drwxr-xr-x  2 gitpod gitpod    94 Feb  3 08:43 y18n
drwxr-xr-x  5 gitpod gitpod   156 Feb  3 08:43 yargs
drwxr-xr-x  3 gitpod gitpod   109 Feb  3 08:43 yargs-parser
drwxr-xr-x  2 gitpod gitpod    94 Feb  3 08:43 yargs-unparser
```

18. It is showing more details about each item in here and it's a little easier to read. One of the folders is named `has`, why don't you change into it.

```
camper: /node_modules$ cd has
camper: /has$ 
```

19. You are now in the has folder. List its contents.

```
camper: /has$ ls
LICENSE-MIT  package.json  README.md  src  test
```

20. 
There's a few files and folders here. Can you tell the difference? Take a look at more of that README.md file.

```
camper: /has$ more README.md 
# has

> Object.prototype.hasOwnProperty.call shortcut

## Installation

/```sh
npm install --save has
/```

## Usage

/```js
var has = require('has');

has({}, 'hasOwnProperty'); // false
--More--(77%)
```

21. Nothing noteworthy in there. You can't see what's in the here anymore, list the contents again.

```
camper: /has$ ls
LICENSE-MIT  package.json  README.md  src  test
```

22. That one file doesn't appear to have an extension. Strange. Take a look at more of the that _license_ file that doesn't show an extension.

```
camper: /has$ more LICENSE-MIT 
Copyright (c) 2013 Thiago de Arruda

Permission is hereby granted, free of charge, to any person
obtaining a copy of this software and associated documentation
files (the "Software"), to deal in the Software without
restriction, including without limitation the rights to use,
copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the
Software is furnished to do so, subject to the following
conditions:

The above copyright notice and this permission notice shall be
included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND,
EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES
--More--(68%)
```

23. Pretend you read all that. It looks a little messy in here again so why don't you clear the terminal.

24. Better. Remind yourself what's in here with the list command.

25. Go into that `src` directory to see what you can find in there.

26. View the full path of this folder.

```
camper: /src$ pwd
/workspace/project/freeCodeCamp/node_modules/has/src
```

27. Getting deeper still. You can see that each new folder has a `/` in front of it. Take a look at what's in this folder.

```
camper: /src$ ls
index.js
```

28. Only one file here. Show me what's in it with `more`.

```
camper: /src$ more index.js 
'use strict';

var bind = require('function-bind');

module.exports = bind.call(Function.call, Object.prototype.hasOwnProperty);
```

29. It's some JavaScript 😄 I think you've fooled around enough. Why don't you navigate out of here. Change back to the has directory.

```
camper: /src$ cd ..
camper: /has$ 
```

30. You're getting pretty good. Change back to the `node_modules` directory.

31. You can go back two folders with `cd ../..`. Each set of dots represents another folder level. Go back to the `project` directory from the `node_modules` directory.

```
camper: /node_modules$ cd ../..
camper: /project$ 
```

32. You are back in the `project` folder where you started. List what's in here again.

```
camper: /project$ ls
freeCodeCamp
```

33. That's right. Why don't you get a fresh start by clearing the terminal.

34. You will be making a __website boilerplate__. You can make a new folder with `mkdir <folder_name>`. `mkdir` stands for _make directory_. Make a `website` directory in this `project` folder. Remember that directory and folder mean the same thing.

```
camper: /project$ mkdir website
camper: /project$ 
```

35. List what's here to make sure it got created.

```
camper: /project$ ls
freeCodeCamp  website
```

36. It worked. The website files will be in the new directory. Change to the `website` directory so you can start creating them.

37. List the contents of this website folder.

38. It's brand new, there's nothing in it yet. The `echo` command lets you print anything to the terminal. You used it in the first lesson. Just type what you want to print after it. Use it to print `hello website` to the terminal.

39. Websites usually have an `index.html` file. You can use `touch <filename>` to create a new file. Create `index.html` in the `website` folder.

```
camper: /website$ touch index.html
camper: /website$ 
```

40. They usually have a CSS file as well. Create styles.css in the website folder using the same method.


41. List the contents of the website folder to make sure they got created.

```
camper: /website$ ls
index.html  styles.css
```

42. 

```
```

43. 

```
```

44. 

```
```

45. 

```
```
