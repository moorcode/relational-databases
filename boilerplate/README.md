# Relational Databases

## Boilerplate

> [!NOTE] 
> In this 170-lesson course, you will learn terminal commands by creating a website boilerplate using only the command line. This course runs in a virtual Linux machine using Gitpod. Start the course at [freeCodeCamp](https://www.freecodecamp.org/learn/relational-database/learn-bash-by-building-a-boilerplate/build-a-boilerplate).
>
> __Checkpoints:__ 
> echo, pwd, ls, cd, more, clear, mkdir, touch, cp, rm, mv, find, rmdir, flags (--help, --all, -r, etc.)



1. __The first thing you need to do is start the terminal.__ Do that the short way by pressing `ctrl+shift+\`\` , or the long way by clicking the _hamburger_ menu at the top left of the screen, going to the _terminal_ section, and clicking _new terminal_. Once you open a new one, type `echo hello terminal` into the terminal and press enter.

```bash
camper: /project$ echo hello terminal
hello terminal
```

2. What you see in the terminal is a __folder (or directory)__ on your machine. Type `pwd` into the terminal and press enter to see the __path__ of the folder. `pwd` stands for __print working directory__.

```bash
camper: /project$ pwd
/workspace/project
```

3. The output tells you where the folder you are in is located. In Gitpod, you are in the project folder, which is in the workspace folder. Type `ls` into the terminal to see what's in this folder. `ls` stands for __list__. 

```bash
camper: /project$ ls
freeCodeCamp
```

4. The output is showing everything in this folder. There's one folder in here. You can use `cd <folder_name>` to go into a folder. `cd` stands for __change directory__. Change to the `freeCodeCamp` directory.
	
> [!TIP]
> `Tab`will complete the folder name.

```bash
camper: /project$ cd freeCodeCamp/
camper: /freeCodeCamp$ 
```

5. You are in the `freecodecamp` folder now. You may have noticed that the prompt changed to include it. Print the working directory of the `freeCodeCamp` folder to see the full path of where you are.

```bash
camper: /freeCodeCamp$ pwd
/workspace/project/freeCodeCamp
```

6. You can see the path of the `freeCodeCamp` folder. It's in the project folder you were just in. List the contents of the `freeCodeCamp` folder to see what's here.

```bash
camper: /freeCodeCamp$ ls
node_modules  package.json  package-lock.json  reset.sh  setup.sh  test
```

7. There're several folders and files here. The folders are blue or green and the files include their extension. Next, change to that `test` directory.

```bash
camper: /freeCodeCamp$ cd test
camper: /test$ 
```

8. You can see you are in the `test` folder now. It shows `test` in the prompt. Print the full path of this directory. Remember that __folder__ and __directory__ are the same thing.

```bash
camper: /test$ pwd
/workspace/project/freeCodeCamp/test
```

9. That's the path to the `test` folder, it's in the `freeCodeCamp` folder. List the contents of this folder.

```bash
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

```bash
camper: /test$ cd ..
camper: /freeCodeCamp$ 
```

11. `test` got removed from the prompt since you left that folder and you're back in the `freeCodeCamp` folder. List the contents of what's here to remind yourself

```bash
camper: /freeCodeCamp$ ls
node_modules  package.json  package-lock.json  reset.sh  setup.sh  test
```

12. There's the `test` folder you were just in. You can see what's in a file with `more <filename>`. Use it to view what's in the `package.json` file.

> [!TIP]
> `Enter` advances one line. _Down arrow_ advances to the end.

```bash
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

```bash
camper: /freeCodeCamp$ ls
node_modules  package.json  package-lock.json  reset.sh  setup.sh  test
```

15. You checked out the `test` folder and the `package.json` file. What next? Why don't you go into that `node_modules` directory.

```bash
camper: /freeCodeCamp$ cd node_modules/
camper: /node_modules$ 
```

16. Now the prompt includes `node_modules` since that's where you are. List what's in the folder.

```bash
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

```bash
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

```bash
camper: /node_modules$ cd has
camper: /has$ 
```

19. You are now in the has folder. List its contents.

```bash
camper: /has$ ls
LICENSE-MIT  package.json  README.md  src  test
```

20. 
There's a few files and folders here. Can you tell the difference? Take a look at more of that README.md file.

```bash
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

```bash
camper: /has$ ls
LICENSE-MIT  package.json  README.md  src  test
```

22. That one file doesn't appear to have an extension. Strange. Take a look at more of the that _license_ file that doesn't show an extension.

```bash
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

```bash
camper: /src$ pwd
/workspace/project/freeCodeCamp/node_modules/has/src
```

27. Getting deeper still. You can see that each new folder has a `/` in front of it. Take a look at what's in this folder.

```bash
camper: /src$ ls
index.js
```

28. Only one file here. Show me what's in it with `more`.

```bash
camper: /src$ more index.js 
'use strict';

var bind = require('function-bind');

module.exports = bind.call(Function.call, Object.prototype.hasOwnProperty);
```

29. It's some JavaScript 😄 I think you've fooled around enough. Why don't you navigate out of here. Change back to the `has` directory.

```bash
camper: /src$ cd ..
camper: /has$ 
```

30. You're getting pretty good. Change back to the `node_modules` directory.

31. You can go back two folders with `cd ../..`. Each set of dots represents another folder level. Go back to the `project` directory from the `node_modules` directory.

```bash
camper: /node_modules$ cd ../..
camper: /project$ 
```

32. You are back in the `project` folder where you started. List what's in here again.

```bash
camper: /project$ ls
freeCodeCamp
```

33. That's right. Why don't you get a fresh start by clearing the terminal.

```bash
camper: /website$ clear
camper: /website$ 
```

34. You will be making a __website boilerplate__. You can make a new folder with `mkdir <folder_name>`. `mkdir` stands for _make directory_. Make a `website` directory in this `project` folder. Remember that directory and folder mean the same thing.

```bash
camper: /project$ mkdir website
camper: /project$ 
```

35. List what's here to make sure it got created.

```bash
camper: /project$ ls
freeCodeCamp  website
```

36. It worked. The website files will be in the new directory. Change to the `website` directory so you can start creating them.

37. List the contents of this website folder.

38. It's brand new, there's nothing in it yet. The `echo` command lets you __print__ anything to the terminal. You used it in the first lesson. Just type what you want to print after it. Use it to print `hello website` to the terminal.

```bash
camper: /website$ echo hello website
hello website
```

39. Websites usually have an `index.html` file. You can use `touch <filename>` to create a new file. Create `index.html` in the `website` folder.

```bash
camper: /website$ touch index.html
camper: /website$ 
```

40. They usually have a CSS file as well. Create `styles.css` in the `website` folder using the same method.


41. List the contents of the `website` folder to make sure they got created.

```bash
camper: /website$ ls
index.html  styles.css
```

42. There they are. Next is a JavaScript file. Create `index.js` in the `website` folder with the method you have been using.

43. You might turn this into a __git repository__. Create `.gitignore` in the `website` folder with the same method.

44. List the contents of the `website` folder to see your new files.

```bash
camper: /website$ ls
index.html  index.js  styles.css
```

45. There's three files, but where's the `.gitignore` file? I think it's hidden. Most commands have a `--help` flag to show what the command can do. Display the _help_ menu for the `ls` command. Here's an example: `command <flag>`

```bash
camper: /website$ ls --help
Usage: ls [OPTION]... [FILE]...
List information about the FILEs (the current directory by default).
Sort entries alphabetically if none of -cftuvSUX nor --sort is specified.

Mandatory arguments to long options are mandatory for short options too.
  -a, --all                  do not ignore entries starting with .
  -A, --almost-all           do not list implied . and ..
      --author               with -l, print the author of each file
  -b, --escape               print C-style escapes for nongraphic characters
      --block-size=SIZE      with -l, scale sizes by SIZE when printing them;
                               e.g., '--block-size=M'; see SIZE format below
  -B, --ignore-backups       do not list implied entries ending with ~
  -c                         with -lt: sort by, and show, ctime (time of last
                               modification of file status information);
                               with -l: show ctime and sort by name;
                               otherwise: sort by ctime, newest first
  -C                         list entries by columns
      --color[=WHEN]         colorize the output; WHEN can be 'always' (default
                               if omitted), 'auto', or 'never'; more info below
  -d, --directory            list directories themselves, not their contents
  -D, --dired                generate output designed for Emacs' dired mode
  -f                         do not sort, enable -aU, disable -ls --color
  -F, --classify             append indicator (one of */=>@|) to entries
      --file-type            likewise, except do not append '*'
      --format=WORD          across -x, commas -m, horizontal -x, long -l,
                               single-column -1, verbose -l, vertical -C
      --full-time            like -l --time-style=full-iso
  -g                         like -l, but do not list owner
      --group-directories-first
                             group directories before files;
                               can be augmented with a --sort option, but any
                               use of --sort=none (-U) disables grouping
  -G, --no-group             in a long listing, don't print group names
  -h, --human-readable       with -l and -s, print sizes like 1K 234M 2G etc.
      --si                   likewise, but use powers of 1000 not 1024
  -H, --dereference-command-line
                             follow symbolic links listed on the command line
      --dereference-command-line-symlink-to-dir
                             follow each command line symbolic link
                               that points to a directory
      --hide=PATTERN         do not list implied entries matching shell PATTERN
                               (overridden by -a or -A)
      --hyperlink[=WHEN]     hyperlink file names; WHEN can be 'always'
                               (default if omitted), 'auto', or 'never'
      --indicator-style=WORD  append indicator with style WORD to entry names:
                               none (default), slash (-p),
                               file-type (--file-type), classify (-F)
  -i, --inode                print the index number of each file
  -I, --ignore=PATTERN       do not list implied entries matching shell PATTERN
  -k, --kibibytes            default to 1024-byte blocks for disk usage;
                               used only with -s and per directory totals
  -l                         use a long listing format
  -L, --dereference          when showing file information for a symbolic
                               link, show information for the file the link
                               references rather than for the link itself
  -m                         fill width with a comma separated list of entries
  -n, --numeric-uid-gid      like -l, but list numeric user and group IDs
  -N, --literal              print entry names without quoting
  -o                         like -l, but do not list group information
  -p, --indicator-style=slash
                             append / indicator to directories
  -q, --hide-control-chars   print ? instead of nongraphic characters
      --show-control-chars   show nongraphic characters as-is (the default,
                               unless program is 'ls' and output is a terminal)
  -Q, --quote-name           enclose entry names in double quotes
      --quoting-style=WORD   use quoting style WORD for entry names:
                               literal, locale, shell, shell-always,
                               shell-escape, shell-escape-always, c, escape
                               (overrides QUOTING_STYLE environment variable)
  -r, --reverse              reverse order while sorting
  -R, --recursive            list subdirectories recursively
  -s, --size                 print the allocated size of each file, in blocks
  -S                         sort by file size, largest first
      --sort=WORD            sort by WORD instead of name: none (-U), size (-S),
                               time (-t), version (-v), extension (-X)
      --time=WORD            change the default of using modification times;
                               access time (-u): atime, access, use;
                               change time (-c): ctime, status;
                               birth time: birth, creation;
                             with -l, WORD determines which time to show;
                             with --sort=time, sort by WORD (newest first)
      --time-style=TIME_STYLE  time/date format with -l; see TIME_STYLE below
  -t                         sort by time, newest first; see --time
  -T, --tabsize=COLS         assume tab stops at each COLS instead of 8
  -u                         with -lt: sort by, and show, access time;
                               with -l: show access time and sort by name;
                               otherwise: sort by access time, newest first
  -U                         do not sort; list entries in directory order
  -v                         natural sort of (version) numbers within text
  -w, --width=COLS           set output width to COLS.  0 means no limit
  -x                         list entries by lines instead of by columns
  -X                         sort alphabetically by entry extension
  -Z, --context              print any security context of each file
  -1                         list one file per line.  Avoid '\n' with -q or -b
      --help     display this help and exit
      --version  output version information and exit

The SIZE argument is an integer and optional unit (example: 10K is 10*1024).
Units are K,M,G,T,P,E,Z,Y (powers of 1024) or KB,MB,... (powers of 1000).
Binary prefixes can be used, too: KiB=K, MiB=M, and so on.

The TIME_STYLE argument can be full-iso, long-iso, iso, locale, or +FORMAT.
FORMAT is interpreted like in date(1).  If FORMAT is FORMAT1<newline>FORMAT2,
then FORMAT1 applies to non-recent files and FORMAT2 to recent files.
TIME_STYLE prefixed with 'posix-' takes effect only outside the POSIX locale.
Also the TIME_STYLE environment variable sets the default style to use.

Using color to distinguish file types is disabled both by default and
with --color=never.  With --color=auto, ls emits color codes only when
standard output is connected to a terminal.  The LS_COLORS environment
variable can change the settings.  Use the dircolors command to set it.

Exit status:
 0  if OK,
 1  if minor problems (e.g., cannot access subdirectory),
 2  if serious trouble (e.g., cannot access command-line argument).

GNU coreutils online help: <https://www.gnu.org/software/coreutils/>
Full documentation <https://www.gnu.org/software/coreutils/ls>
or available locally via: info '(coreutils) ls invocation'
```

46. Scroll through the menu to see the flags that go with `ls`. The flag you are looking for is `--all`, or `-a` for short. List __all__ the contents of the `website` folder using the correct flag.

```bash
camper: /website$ ls -all
total 0
drwxr-xr-x 2 gitpod gitpod  76 Feb  3 09:28 .
drwxrwxrwx 6 gitpod gitpod 105 Feb  3 09:23 ..
-rw-r--r-- 1 gitpod gitpod   0 Feb  3 09:28 .gitignore
-rw-r--r-- 1 gitpod gitpod   0 Feb  3 09:26 index.html
-rw-r--r-- 1 gitpod gitpod   0 Feb  3 09:28 index.js
-rw-r--r-- 1 gitpod gitpod   0 Feb  3 09:27 styles.css
camper: /website$ ls -a
.  ..  .gitignore  index.html  index.js  styles.css
```

47. There's the hidden file. Do you see it? It didn't display before. It also includes `.` and `...` You used `cd ..` to go back a folder earlier. Change to the `.` directory.

```bash
camper: /website$ cd .
camper: /website$ 
```

48. You didn't go anywhere. The `.` takes you to the folder you are in, and `..` takes you back, or up, a folder. Websites need some images. Create `background.jpg` in the `website` folder.

```bash
camper: /website$ touch background.jpg
camper: /website$ 
```

49. Next, add a header image. Create `header.png` in the `website` folder.

```bash
camper: /website$ touch header.png
camper: /website$ 
```

50. Finally, create `footer.jpeg` in the `website` folder.

```bash
camper: /website$ touch footer.jpeg
camper: /website$ 
```

51. Use the __list__ command to check out the images you just added.

```bash
camper: /website$ ls
background.jpg  footer.jpeg  header.png  index.html  index.js  styles.css
```

52. Looks like images show up in pink. There's also three fonts to use for the website. The first one is _roboto_. Create `roboto.font` in the `website` folder.

```bash
camper: /website$ touch roboto.font
camper: /website$ 
```

53. The next one is _lato_. Create `lato.font` in the `website` folder.

```bash
camper: /website$ touch lato.font
camper: /website$ 
```

54. Lastly, create `menlo.font` in the `website` folder.

```bash
camper: /website$ touch menlo.font
camper: /website$ 
```

55. List the contents of this folder to see your new font files.

```bash
camper: /website$ ls
background.jpg  footer.jpeg  header.png  index.html  index.js  lato.font  menlo.font  roboto.font  styles.css
```

56. Your three font files are there. There's three icons for the website as well. Create `CodeAlly.svg` in the `website` folder. 

```bash
camper: /website$ touch CodeAlly.svg
camper: /website$
```

57. Next, create `CodeRoad.svg` in the `website` folder.

```bash
camper: /website$ touch CodeRoad.svg
camper: /website$ 
```

68. Finally, create `freeCodeCamp.svg` in the `website` folder.

```bash
camper: /website$ touch freeCodeCamp.svg
camper: /website$ 
```

59. Check out the new icons you just added by listing the contents of the folder they are in.

```bash
camper: /website$ ls
background.jpg  CodeRoad.svg  freeCodeCamp.svg  index.html  lato.font   roboto.font
CodeAlly.svg    footer.jpeg   header.png        index.js    menlo.font  styles.css
```

60. The icons are pink as well. I think the images should go in a separate folder to clean it up a little. Make an `images` directory in the `website` folder to put them in.

```bash
camper: /website$ mkdir images
camper: /website$ 
```

61. List the contents of the `website` folder to make sure your new folder is there.

```bash
camper: /website$ ls
background.jpg  CodeRoad.svg  freeCodeCamp.svg  images      index.js   menlo.font   styles.css
CodeAlly.svg    footer.jpeg   header.png        index.html  lato.font  roboto.font
```

62. There's your new `images` folder. It's blue. You can __copy__ a file with `cp <file> <destination>`. `cp` stands for __copy__. Copy `background.jpg` to your `images` folder.

```bash
camper: /website$ cp background.jpg images/
camper: /website$ 
```

63. Better make sure it worked. Change to the `images` directory.

```bash
camper: /website$ cd images/
```

64. List the contents to see if `background.jpg` is here.

65. There it is. Looks like the copy worked. Change back to the `website` directory so you can copy the other ones.

66. Remind yourself of the files here by listing the contents.

```bash
camper: /website$ ls
background.jpg  CodeRoad.svg  freeCodeCamp.svg  images      index.js   menlo.font   styles.css
CodeAlly.svg    footer.jpeg   header.png        index.html  lato.font  roboto.font
```

67. You copied the background image to the `images` folder so you don't need the one here anymore. You can __remove__ a file with `rm <filename>`. Remove `background.jpg` from the `website` folder.

```bash
camper: /website$ rm background.jpg 
camper: /website$ 
```

68. List the contents to make sure it's gone.

```bash
camper: /website$ ls
CodeAlly.svg  footer.jpeg       header.png  index.html  lato.font   roboto.font
CodeRoad.svg  freeCodeCamp.svg  images      index.js    menlo.font  styles.css
```

69. Okay, it's gone. Next, copy `header.png` to the `images` folder.

```bash
camper: /website$ cp header.png images/
camper: /website$ 
```

70. Last, copy the _footer_ image to the `images` folder.

```bash
camper: /website$ cp footer.jpeg images/
camper: /website$ 
```

71. All the images should be copied over. Change to the `images` directory so you can make sure.

```bash
camper: /website$ cd images/
```

72. Check if the images are here by listing the contents.

```bash
camper: /images$ ls
background.jpg  footer.jpeg  header.png
```

73. They all made it here. Go back to the `website` folder so you can delete the original files.

```bash
camper: /images$ cd ..
camper: /website$ 
```

74. List the contents to remind yourself of the filenames to delete.

```bash
camper: /website$ ls
CodeAlly.svg  footer.jpeg       header.png  index.html  lato.font   roboto.font
CodeRoad.svg  freeCodeCamp.svg  images      index.js    menlo.font  styles.css
```

75. There's two that you don't need anymore. Remove the _header_ image file from the `website` folder since you copied to the `images` folder.

```bash
camper: /website$ rm header.png 
```

76. It should be gone. Remove the _footer_ image from the `website` folder as well.

```bash
camper: /website$ rm footer.jpeg 
```

77. List the contents of the `website` folder to check if they are gone.

```bash
camper: /website$ ls
CodeAlly.svg  CodeRoad.svg  freeCodeCamp.svg  images  index.html  index.js  lato.font  menlo.font  roboto.font  styles.css
```

78. Looks like they're all deleted. There was a mistake with the extensions for the font files. You can __rename__ them with `mv` like this: `mv <filename> <new_filename>`. mv stands for __move__, it can __rename__ or move something. Rename `roboto.font` to `roboto.woff`.

```bash
camper: /website$ mv roboto.font roboto.woff
```

79. Use list to check if it worked.

```bash
camper: /website$ ls
CodeAlly.svg  CodeRoad.svg  freeCodeCamp.svg  images  index.html  index.js  lato.font  menlo.font  roboto.woff  styles.css
```

80. Do you see the _roboto_ font? The rename worked. Next, rename the _lato_ font file to `lato.ttf`.

```bash
camper: /website$ mv lato.font lato.ttf
```

81. Lastly, rename the _menlo_ font to `menlo.otf`.

```bash
camper: /website$ mv menlo.font menlo.otf
```

82. Use the list command to make sure those last two got renamed.

```bash
camper: /website$ ls
CodeAlly.svg  CodeRoad.svg  freeCodeCamp.svg  images  index.html  index.js  lato.ttf  menlo.otf  roboto.woff  styles.css
```

83. Take a look at the files to make sure they got renamed. Those font files could be organized into a folder as well. Make a `fonts` directory in the `website` folder to put them in.

```bash
camper: /website$ mkdir fonts
```

84. List the contents of the `website` folder to make sure your new folder is there.

```bash
camper: /website$ ls
CodeAlly.svg  CodeRoad.svg  fonts  freeCodeCamp.svg  images  index.html  index.js  lato.ttf  menlo.otf  roboto.woff  styles.css
```

85. See it? You renamed the font files with `mv`, you can also move files with it. Move the _roboto_ font to the new `fonts` folder. Here's an example: `mv <file> <destination>`.

```bash
camper: /website$ mv roboto.woff fonts/
```

86. You can use `find` to __find__ things or __view__ a file tree. Enter `find` to view the file tree of the `website` folder to see all the files and folders within it.

```bash
camper: /website$ find
.
./.gitignore
./CodeAlly.svg
./CodeRoad.svg
./freeCodeCamp.svg
./index.html
./index.js
./styles.css
./images
./images/background.jpg
./images/header.png
./images/footer.jpeg
./lato.ttf
./menlo.otf
./fonts
./fonts/roboto.woff
```

87. You can see everything in this `website` folder and its descendant folders. Notice that they all start with `./` to represent this folder. You can see that your font moved to the `fonts` folder. Next, move the _lato_ font to the `fonts` folder.

```bash
camper: /website$ mv lato.ttf fonts/
```

88. There's one more font to move. Move the _menlo_ font to the `fonts` folder.

```bash
camper: /website$ mv menlo.otf fonts/
```

89. Use `find` again to list the whole file tree and make sure those two got moved.

```bash
camper: /website$ find
.
./.gitignore
./CodeAlly.svg
./CodeRoad.svg
./freeCodeCamp.svg
./index.html
./index.js
./styles.css
./images
./images/background.jpg
./images/header.png
./images/footer.jpeg
./fonts
./fonts/roboto.woff
./fonts/lato.ttf
./fonts/menlo.otf
```

90. Yes, you can see them all in the `fonts` folder. Let's organize some more. Make a `client` directory in the `website` folder for the client side files.

```bash
camper: /website$ mkdir client
```

91. You can make a folder in that `client` folder from here by adding it to the path like this: `mkdir client/<new_folder_name>`. Make a `src` directory in the `client` folder from here.

```bash
camper: /website$ mkdir client/src
```

92. You can move files all the way across the system from here with the right path. Move `index.html` to the `client/src` folder from here.

```bash
camper: /website$ mv index.html client/src/
```

93. Use `find` to view the file tree and make sure it moved.

```bash
camper: /website$ find
.
./.gitignore
./CodeAlly.svg
./CodeRoad.svg
./freeCodeCamp.svg
./index.js
./styles.css
./images
./images/background.jpg
./images/header.png
./images/footer.jpeg
./fonts
./fonts/roboto.woff
./fonts/lato.ttf
./fonts/menlo.otf
./client
./client/src
./client/src/index.html
```

94. Can you see the `index.html` file in your new `src` folder? Looks like it moved 😄 There's some more files that can go in the `src` folder. Move `index.js` to it from here.

```bash
camper: /website$ mv index.js client/src/
```

95. Last is the CSS file. Move `styles.css` to the `src` folder.

```bash
camper: /website$ mv styles.css client/src/
```

96. Seems like you can do anything right from here. Take another look at the tree with `find`.

```bash
camper: /website$ find
.
./.gitignore
./CodeAlly.svg
./CodeRoad.svg
./freeCodeCamp.svg
./images
./images/background.jpg
./images/header.png
./images/footer.jpeg
./fonts
./fonts/roboto.woff
./fonts/lato.ttf
./fonts/menlo.otf
./client
./client/src
./client/src/index.html
./client/src/index.js
./client/src/styles.css
```

97. Things are looking more organized 😄 You can use`find` to display the tree of a different folder. View the file tree of the client folder from the `website` folder.

```bash
camper: /website$ find client
client
client/src
client/src/index.html
client/src/index.js
client/src/styles.css
```

98. Now you just see what's in the `client` folder. What else can `find` do? View the __help__ menu of the `find` command to look around.

```bash
camper: /website$ find --help
Usage: find [-H] [-L] [-P] [-Olevel] [-D debugopts] [path...] [expression]

default path is the current directory; default expression is -print
expression may consist of: operators, options, tests, and actions:
operators (decreasing precedence; -and is implicit where no others are given):
      ( EXPR )   ! EXPR   -not EXPR   EXPR1 -a EXPR2   EXPR1 -and EXPR2
      EXPR1 -o EXPR2   EXPR1 -or EXPR2   EXPR1 , EXPR2
positional options (always true): -daystart -follow -regextype

normal options (always true, specified before other expressions):
      -depth --help -maxdepth LEVELS -mindepth LEVELS -mount -noleaf
      --version -xdev -ignore_readdir_race -noignore_readdir_race
tests (N can be +N or -N or N): -amin N -anewer FILE -atime N -cmin N
      -cnewer FILE -ctime N -empty -false -fstype TYPE -gid N -group NAME
      -ilname PATTERN -iname PATTERN -inum N -iwholename PATTERN -iregex PATTERN
      -links N -lname PATTERN -mmin N -mtime N -name PATTERN -newer FILE
      -nouser -nogroup -path PATTERN -perm [-/]MODE -regex PATTERN
      -readable -writable -executable
      -wholename PATTERN -size N[bcwkMG] -true -type [bcdpflsD] -uid N
      -used N -user NAME -xtype [bcdpfls]      -context CONTEXT

actions: -delete -print0 -printf FORMAT -fprintf FILE FORMAT -print 
      -fprint0 FILE -fprint FILE -ls -fls FILE -prune -quit
      -exec COMMAND ; -exec COMMAND {} + -ok COMMAND ;
      -execdir COMMAND ; -execdir COMMAND {} + -okdir COMMAND ;

Valid arguments for -D:
exec, opt, rates, search, stat, time, tree, all, help
Use '-D help' for a description of the options, or see find(1)

Please see also the documentation at https://www.gnu.org/software/findutils/.
You can report (and track progress on fixing) bugs in the "find"
program via the GNU findutils bug-reporting page at
https://savannah.gnu.org/bugs/?group=findutils or, if
you have no web access, by sending email to <bug-findutils@gnu.org>.
```

99. The menu isn't very pretty, but there's a `-name` flag in there. You can use it to search for something with `find -name <filename>`. Use find with the `-name` flag to search for `index.html`

```bash
camper: /website$ find -name index.html
./client/src/index.html
```

100. It shows you where that file is. Using the same command, find where the styles.css file is.

```bash
camper: /website$ find -name styles.css
./client/src/styles.css
```

101. You can search for folders with it, as well. Using the same command and flag, find the `src` folder.

```bash
camper: /website$ find -name src
./client/src
```

102. 😄 View the file tree of the `website` folder to see what else you need to do.

```bash
camper: /website$ find
.
./.gitignore
./CodeAlly.svg
./CodeRoad.svg
./freeCodeCamp.svg
./images
./images/background.jpg
./images/header.png
./images/footer.jpeg
./fonts
./fonts/roboto.woff
./fonts/lato.ttf
./fonts/menlo.otf
./client
./client/src
./client/src/index.html
./client/src/index.js
./client/src/styles.css
```

103. What's next? More organizing! You should put all the assets in one spot. Change into the `client` folder.

```bash
camper: /website$ cd client/
camper: /client$ 
```

104. Make a new directory named `assets` in the `client` folder.

```bash
camper: /client$ mkdir assets
```

105. Change into the new `assets` folder.

```bash
camper: /client$ cd assets/
camper: /assets$ 
```

106. All the images and other assets can go here. Make an `images` directory in the `assets` folder for all the images.

```bash
camper: /assets$ mkdir images
```

107. Go to your new images folder.

```bash
camper: /assets$ cd images/
camper: /images$ 
```

108. You want the images here. Create `background.jpg` in this folder.

```bash
camper: /images$ touch background.jpg
```

109. Wait. You don't need to recreate them. You can just move the other images here. Go back to the `website` folder from here. It's three folders back.

```bash
camper: /images$ cd ../../..
camper: /website$ 
```

110. Now go to where the original images are. Change into the `images` folder.

```bash
camper: /website$ cd images/
camper: /images$ 
```

111. List the contents of the `images` folder to see the files here.

```bash
camper: /images$ ls
background.jpg  footer.jpeg  header.png
```

112. Umm, first I think you should move them back to the `website` folder. Move `header.png` back to the `website` folder. The destination for the file is `..`.

```bash
camper: /images$ mv header.png ..
```

113. List the contents of the `images` folder to see if it's gone.

```bash
camper: /images$ ls
background.jpg  footer.jpeg
```

114. It's gone. Go back to the `website` folder.

```bash
camper: /images$ cd ..
camper: /website$ 
```

115. List what's here.

```bash
camper: /website$ ls
client  CodeAlly.svg  CodeRoad.svg  fonts  freeCodeCamp.svg  header.png  images
```

116. There's the file you just moved. Next, you will move it to the `client/assets/images` folder. First, use find with the correct flag to search for `images`.

```bash
camper: /website$ find -name images
./client/assets/images
./client/src/images
./images
```

117. There's your two image folders. Move `header.png` to the one with the longer path. Just use it as the destination to do so.

```bash
camper: /website$ mv header.png client/assets/images/
camper: /website$ 
```

118. Use `find` to search for your `header.png` file and make sure it moved.

```bash
camper: /website$ find -name header.png
./client/assets/images/header.png
```

119. There it is. Right where you put it. Next, search for your `footer.jpeg` file so you can move that over there.

```bash
camper: /website$ find -name footer.jpeg
./footer.jpeg
./images/footer.jpeg
```

120. It's in the original `images` folder. You can use that path with the move command to move it. Move `footer.jpeg` to the `client/assets/images` folder while in the `website` folder.

```bash
camper: /website$ mv ./images/footer.jpeg client/assets/images/
camper: /website$ 
```

121. View the file tree of this folder to make sure all your images are over in their new folder. Don't use any flags.

122. You don't need the old `images` folder anymore. You can use `rmdir <directory_name>` to remove a folder. `rmdir` stands for __remove directory__. Try to remove the `images` folder with `rmdir`. Make sure it's the one in the `website` folder.

```bash
camper: /website$ rmdir images/
rmdir: failed to remove 'images/': Directory not empty
camper: /website$ 
```

123. Directory not empty? Oh yeah, there's still the background image in there. Remove the background image file in the `images` folder from here. Make sure it's the one in the `website/images` folder.

```bash
camper: /website$ rm images/background.jpg 
camper: /website$ 
```

124. Try to remove the `images` folder again with `rmdir`. Make sure it's the one in the `website` folder.

```bash
camper: /website$ rmdir images/
camper: /website$ 
```

125. I think it worked this time. List the contents to find out.

```bash
camper: /website$ ls
client  CodeAlly.svg  CodeRoad.svg  fonts  freeCodeCamp.svg  index.html  index.js  lato.font  menlo.font  roboto.font  styles.css
```

126. It worked, the `images` folder is gone. Make a new `icons` folder in your `assets` folder while in the `website` folder.

```bash
camper: /website$ mkdir client/assets/icons 
```

127. Move the `CodeAlly.svg` file to your new `icons` folder.

```bash
camper: /website$ mv CodeAlly.svg client/assets/icons/
```

128. View the file tree of the `website` folder and make sure it moved.

```bash
camper: /website$ find
.
./.gitignore
./CodeRoad.svg
./freeCodeCamp.svg
./index.html
./index.js
./lato.font
./menlo.font
./roboto.font
./styles.css
./client
./client/assets
./client/assets/images
./client/assets/images/background.jpg
./client/assets/images/header.png
./client/assets/images/footer.jpeg
./client/assets/icons
./client/assets/icons/CodeAlly.svg
./client/src
./client/src/index.html
./client/src/index.js
./client/src/styles.css
./client/src/images
./fonts
./fonts/lato.ttf
./fonts/menlo.otf
./fonts/roboto.woff
```

129. Verify that the file moved to the `icons` folder. Next, move the _CodeRoad_ file to your `icons` folder.

```bash
camper: /website$ mv CodeRoad.svg client/assets/icons/
```

130. Lastly, move the _freeCodeCamp_ file to your `icons` folder.

```bash
camper: /website$ mv freeCodeCamp.svg client/assets/icons/
```

131. View the file tree and make sure the files moved.

```
camper: /website$ find
.
./.gitignore
./index.html
./index.js
./lato.font
./menlo.font
./roboto.font
./styles.css
./client
./client/assets
./client/assets/images
./client/assets/images/background.jpg
./client/assets/images/header.png
./client/assets/images/footer.jpeg
./client/assets/icons
./client/assets/icons/CodeAlly.svg
./client/assets/icons/CodeRoad.svg
./client/assets/icons/freeCodeCamp.svg
./client/src
./client/src/index.html
./client/src/index.js
./client/src/styles.css
./client/src/images
./fonts
./fonts/lato.ttf
./fonts/menlo.otf
./fonts/roboto.woff
```

132. This looks much better. The three icons are now in the `icons` folder. Make a `fonts` folder in your `assets` folder from here for all the font files.

```bash
camper: /website$ mkdir client/assets/fonts
```

133. Turns out you want some different fonts for the website. From here, create `roboto-bold.woff` in your new `fonts` folder. You can put the path in front of the filename of where you want it to go.

```bash
camper: /website$ touch client/assets/fonts/roboto-bold.woff
```

134. Next, create `roboto-light.woff` in your new `fonts` folder from here.

```bash
camper: /website$ touch client/assets/fonts/roboto-light.woff
```

135. View the file tree of the `client/assets/fonts` folder from here to see if your new files are there.

```bash
camper: /website$ find client/assets/fonts/
client/assets/fonts/
client/assets/fonts/roboto-bold.woff
client/assets/fonts/roboto-light.woff
```

136. Two more fonts to go. Create `lato-bold.ttf` in the new `fonts` folder from here.

```bash
camper: /website$ touch client/assets/fonts/lato-bold.ttf
```

137. Lastly, create `lato-light.ttf` in your new fonts folder from here.

```bash
camper: /website$ touch client/assets/fonts/lato-light.ttf
```

138. View your file tree and make sure the files are there.

```bash
camper: /website$ find
.
./.gitignore
./index.html
./index.js
./lato.font
./menlo.font
./roboto.font
./styles.css
./client
./client/assets
./client/assets/images
./client/assets/images/background.jpg
./client/assets/images/header.png
./client/assets/images/footer.jpeg
./client/assets/icons
./client/assets/icons/CodeAlly.svg
./client/assets/icons/CodeRoad.svg
./client/assets/icons/freeCodeCamp.svg
./client/assets/fonts
./client/assets/fonts/roboto-bold.woff
./client/assets/fonts/roboto-light.woff
./client/assets/fonts/lato-bold.ttf
./client/assets/fonts/lato-light.ttf
./client/src
./client/src/index.html
./client/src/index.js
./client/src/styles.css
./client/src/images
./fonts
./fonts/lato.ttf
./fonts/menlo.otf
./fonts/roboto.woff
```

139. Things are looking more organized 😄 The new fonts are there. Now you can remove the old `fonts` folder and everything in it. You can't do that with `rmdir` since it's not empty. View the _help_ menu of the `rm` command to see if you can find anything.

```bash
camper: /website$ rm --help
Usage: rm [OPTION]... [FILE]...
Remove (unlink) the FILE(s).

  -f, --force           ignore nonexistent files and arguments, never prompt
  -i                    prompt before every removal
  -I                    prompt once before removing more than three files, or
                          when removing recursively; less intrusive than -i,
                          while still giving protection against most mistakes
      --interactive[=WHEN]  prompt according to WHEN: never, once (-I), or
                          always (-i); without WHEN, prompt always
      --one-file-system  when removing a hierarchy recursively, skip any
                          directory that is on a file system different from
                          that of the corresponding command line argument
      --no-preserve-root  do not treat '/' specially
      --preserve-root[=all]  do not remove '/' (default);
                              with 'all', reject any command line argument
                              on a separate device from its parent
  -r, -R, --recursive   remove directories and their contents recursively
  -d, --dir             remove empty directories
  -v, --verbose         explain what is being done
      --help     display this help and exit
      --version  output version information and exit

By default, rm does not remove directories.  Use the --recursive (-r or -R)
option to remove each listed directory, too, along with all of its contents.

To remove a file whose name starts with a '-', for example '-foo',
use one of these commands:
  rm -- -foo

  rm ./-foo

Note that if you use rm to remove a file, it might be possible to recover
some of its contents, given sufficient expertise and/or time.  For greater
assurance that the contents are truly unrecoverable, consider using shred.

GNU coreutils online help: <https://www.gnu.org/software/coreutils/>
Full documentation <https://www.gnu.org/software/coreutils/rm>
or available locally via: info '(coreutils) rm invocation'
```

140. There's a `-r` flag that says, __remove directories and their contents recursively__. That will remove the folder and everything in it. Use the __remove__ command with that flag to remove the `fonts` folder. Make sure it's the one in the `website` folder. Be careful not to remove the wrong folder.

```bash
camper: /website$ find -name fonts
./client/assets/fonts
./fonts
camper: /website$ rm -r ./fonts
```

141. List what's here to see if it's gone.

```bash
camper: /website$ ls
client  index.html  index.js  lato.font  menlo.font  roboto.font  styles.css
```

142. Looks like it’s gone. Surely, it went to the trash can right? No, it’s just gone. You should be very careful when recursively removing files like that. It will delete everything, and can destroy your operating system. There's a few more files for the boilerplate. Create `package.json` in the `website` folder.

```bash
camper: /website$ touch package.json
```

143. Next, create `server.js` in the `website` folder.

```bash
camper: /website$ touch server.js
```

144. Lastly, create `README.md` in the `website` folder.

```bash
camper: /website$ touch README.md
```

145. List the content of this folder to make sure your new files are there.

```bash
camper: /website$ ls
client  index.html  index.js  lato.font  menlo.font  package.json  README.md  roboto.font  server.js  styles.css
```

146. The boilerplate is complete. Use `echo` to print `Yay!` to the terminal.

```bash
camper: /website$ echo Yay!
Yay!
```

147. Print `I finished the boilerplate!` to the terminal.

148. Print `one more thing...` to the terminal

149. You can print to a file instead of the terminal with `echo text >> filename`. Use it to print I made this boilerplate to your `README.md` file.

```bash
camper: /website$ echo I made this boilerplate >> README.md 
camper: /website$ 
```

150. Use `more` to view your `README.md` file.

```bash
camper: /website$ more README.md 
I made this boilerplate
```

151. Now that line is in the file. Add `from the command line` to your `README.md` file with the `echo` command and the same method.

152. Use `more` to view the "readme" file again.

```bash
camper: /website$ more README.md 
I made this boilerplate
from the command line
```

153. Now the file has two lines. Add `for the freeCodeCamp bash lessons` to your _readme_ file with the `echo` command like you did before.

154. View your _readme_ file again like you did before.

155. 😄 Change to the project folder.

156. You are back where you started. List what's here.

157. Still the same items. Rename the `website` folder to `website-boilerplate`.

```bash
camper: /project$ mv website/ website-boilerplate/
```

158. List the contents of this folder to see the new name.

159. Thanks for making this. You need to make a copy of it. Take a look at the _help_ menu of the _copy_ command.

160. Scroll up to find that _recursive_ flag. You need to use it again to copy the whole folder. Copy the whole boilerplate into a folder named `toms-website`.

```bash
camper: /project$ cp -r website-boilerplate/ toms-website/
```

161. List the contents of the project folder to see the new copy.

161. Thanks. Use `find` to view the tree of toms-website.

162. Use `find` to view the tree of the boilerplate folder to make sure it matches.

163. Awesome! You are finished for now. Clear the terminal one last time.

164. Print _goodbye terminal_ to the terminal.

165. Use the __exit__ command to exit the terminal.