# node-package-manager

NPM is now aquired by github ,microsoft runs github and npm as well.
It is a standard package manager for node.

### What is a package manager! exactyly?
1. while designing and developing our web app some time you have to design it from a prety low level.like creating a server,interacting with the sockets.
2. Eamples of some popular packages like

   1. lodash
   2. react
   3. chalk
   4. express
   5. vite@app
   
3. You can not just build everthing from scratch you have to build with other peoples work.
4. People solve the things and maintain their packages and put them to open source.
5. NPM acts as repository to host those packages.
6. Github is the place to host those code but npm act as repository to host the package only.
7. You not to visit the NPM website to use their packages you just use their packages by using their CLI tools.
8. NPM act as a command line tool to fetch and install and manage and remove update upgrade all the packages in your node application.
9. NPM is specifically for node it can not work with other languages like python and php also deno does not support it.
10. NPM acts as package manager allows you to download manage update upgrade remove packages easily.

### What is the difference between yarn and npm?

1. Yarn is a another package manager which is 100% just like npm.
2. It is an alternative of npm.
3. It is created by facebook.
4. Yarn is created because npm was very slow.

### Install node js to use NPM 
### Node Version Manager(nvm)
We use this to manage th different versions of node

### What is a node module?

1. Lodash  module -- it fetch a lot of  code from npm to a single package name lodash(your package is on both section on github or at npm)

```javascript
>>>>npm install lodash
```
2. Node module is a folder where all the external packages would be placed  by npm.(dont touch this folder)
3. Microsoft put the packages at github to beautify them and out the compressed version of it to npm to use it.
4. The file code of lodash is different at github and at npm.


### How actually npm install these modules?
1. To check the working of lodash use
   ```javascript

   >>>>npm view lodash
   
   ```
2. You can see a tar file (tarball:https//...tgz).
3. NPM only recieve this file from you as a pacakage developer.
4. npm does not care about what is in the package and github sourse code whether you hosted it on gihub or not.
5. NPM just care about getting this targ file.
6. Once npm get this file it store in their registery or cdn.
7. When you do "npm install lodash" it takes the url of lodash or tar url.
8. It goes to that url and downloads the lodash file from this link.
9. It installed file from that link and extracted that file to the folder called node-module.



### Solve the first warning when we install lodash.
 no such file and directory is open at package.json.

ANS :- whenever we install module of lodash with npm npm warn to put this file name in .json file to track the record.

Package.json is a file that contain a lots of information about your project.It has all the information of your dependencied used in your project.

### Explore package.json 

1. To install package.json you need to run.
```javascript
>>>>npm init
>>>>npm init -y 
```
it is used to initialize you package.

2. When you run this command it will ask of a lots of question.
3. The word written in the bracket like (npm_basics) is a default value.
4. No any filed is mendatory.
5. Initialize your package to avoud the first warning of lodash.
6. After doing this you can see the lodash in your json file.
7. The npm is able to edit this file by itself.


### How to install packages?

Shortcut to install lodash
```javascript

>>>>npm i <name-of-package>

```
i is here for install.
If you install it second time npm just upadate your previous module.


### How to remove packages with npm?

Use this command 
```javascript

>>>>npm remove <name-of-package>
>>>>npm remove lodash

>>>>npm uninstall lodash

```

remove and uninstall both work

### Local vs Global packages?
Local means you install all the packages into your folder and Global means you install package in your system.

```javascript

>>>>npm install create-react-app --global
>>>>npm install create-react-app -g

```

it install your react app globally.Dont install global packages.
To check the installed global modules in your system use this command
```javascript

>>>>npm root -g
>>>>npm root --global
>>>>GO TO THAT FOLDER AND
>>>>folderopend/dir

```
### NPM dependencies Intro..

#### Sementic versioning in npm
whenever you install packes from npm.
Every package has some version number. Three numbers with two dots

```javascript

>>>>version 16.13.1

```


This because npm follow sementic versioning of package.
Sementic versioning is a standard or guidlines to version your package.

It follows 

```javascript

>>>>major.minor.patch
>>>>16 is the major number 
>>>>13 is the minor number 
>>>>1 is the patch number

```

1. MAJOR version when you make incompatible API,changes.
2. MINOR version when you add functionality in a backwords compatible manner.
3. PATCH version when you make backwards compatible bug fixes.(useless for you)


### package-lock.json
There is such file before npm 5.
When you delete nodemodule folder and its dependencies are included in package.json then npm knows that these included dependencies are required for your project.
SO when to get back these packages run
```javascript

>>>npm install

```

to install any version of lodash first delete nodemodule folder and change the version of lodash in package.json.and run this command

```javascript

>>>npm install

```
It install the maximum version of MAJOR version.like version 4.22.3 is installed if full make requiest to install version 4.0.0
Package-lock.json hold each and every dependency.If we install lodash dependency it also install all the dependencies that are dependent on lodash.It locks all the dependencies because it contain all the liks of dependencies from where they are installed so that you can use the same as it is code in other system as well.We see so many errors in this cases because if the dependecy is updated that is not working with our current version of lodash then it will show you an error and ulter the funcitonality of your project.

### More on sementic versioning
NPM install highest version of lodash insted of installing version 4.0.0 --- 4.17.1
NPM install the latest or highest version because of carat sign in the version.

```javascript

>>>>"lodash":"^4.0.0",

```


This charat sign shows that if the major number is same just upgrade the MINOR and PATCH number as possible as you can.

##### To make same MINOR and MAJOR number use 

```javascript

>>>> "lodash":"~4.0.X"

```
here npm will update only the patch version as possible as you can.
By default npm uses ^.



##### To install exact that package remove all the signs in front of version number.

```javascript

>>>> "lodash":"12.12.3",
>>>>npm install

```

### What are dependencies?
we also have dev-deoendencies and pear-dependencies.

Whenever you install any package it goes to the package.json dependencies object

```javascript

>>>>npm i express

```
npm update the things which is present in the "dependencies" just do "npm install".directly depends on our project.

### dev-dependencies

these dependencies are used during development process like bundle file(webpack,babble).These files are not really required to run your application.Lodash ir required to run your application because your javascript wouldcrash without it.


```javascript

>>>>npm install webpack --save-dev

```

NPM install it in devdependencies object in json file.


##### To make your computer a server

```javascript

>>>>echo $node_env
>>>>node_env="production" npm install

```
webpack is not installed because you are now in production mode and in production mode only dependencies are installed.And in development phase you only need dev-dependencied.THis is the difference between dev-dependencies and dependencies that all the stuff goes to dev-dependencies which is not required for production.The things goes to dependencies which are used by your application or required to run your application.

### Pear-dependencies.
It is used to create npm package.Pear-dependecy is not really a dependency which is strictly required.

```javascript

>>>>npm install react-dom

```

Its a renderor for react for the web.It is installed as pear-dependencies because it tells us that we donot have react but we want to use its component.NPM gives you a warning to install reacr first but it does not force you that its a compulsary.

## NPM scripts
You can see a section called script in your package.json file.This is an object in json that hold key value pair.You have a certain key as a script name and a value or bash script as a value.You can write here your actual terminal script here (https://docs.npmjs.com/cli/v6/using-npm/scripts) 

```javascript

"script":{
"start":"echo 'This script was called'",
}

>>>>npm start
>>>>npm run start

```
##### Create a custom script

```javascript

"script":{
"custom_script":"echo 'This is a custom script'",
}

>>>>npm custom_script (does not work)
>>>>npm run custom_script 

```
Run says that heyy i am trying to run a script which might not be available in our predefined script. 
Predefined scripts like 'start' runs without using 'run' script.You can define  your lonag script in jsons script section and give it a name("key") and whenever you hit the key the corresponding script will run.


## NPX (introdued in npm 5.2 and above)
Its a npm extended.
It runs global binaries from npm withour installing them like "create-react-app" 

1. running local binaries:-
```javascript

>>>>npm install cowsay

```
It is installed in json file.
but How do you use it directly 

```javascript

>>>>node ./node_modules/cowsay/cli.js hello

```
By using NPX 

```javascript
"script":{
"saysomething":"cowsay hello"
}


>>>>npm run saysomething

```


```javascript

>>>>npx cowsay hello

```


##### Another use of npx is to run global binaries.
npx install the package runs it and uninsall the package (thats why we use it in 'create-react-app' because we no need to create the app so many times) so installing it globally is not a good idea for you.













   
