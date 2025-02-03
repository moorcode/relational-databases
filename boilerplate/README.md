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

16. 

```
```

17. 

```
```

18. 

```
```

19. 

```
```
