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























   
