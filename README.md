#Aurelia Mvc5 Skeleton

This project is setup to integrate the Aurelia Typescript navigation skeleton (provided by the Aurelia team) with an Asp.Net Mvc5 project which uses .Net 4. 

Currently the .Net project skeletons provided by the Aurelia team support .Net Core only with nothing supplied to support .Net 4.*.

## Usage

### Install Prerequisites
Before you begin you will need to install the following if not already installed:

1. [Node.js](https://nodejs.org/en/)
2. [npm](https://github.com/felixrieseberg/npm-windows-upgrade)
3. [Git](https://git-scm.com/)

These steps are essential so please complete them before proceeding.

Next, open a console and run the following commands:

1. Gulp
	* `npm install -g gulp`
2. jspm
	* `npm install -g jspm`

Next, prep for TypeScript:

* Install [TypeScript 2.1.4](http://www.typescriptlang.org/index.html) if not already installed.
* Modify the PATH environment variable to point to this version, rather than an earlier one. You may need to restart Visual Studio for it to pick this up.
PATH=...;C:\Program Files (x86)\Microsoft SDKs\TypeScript\2.1\;...

Finally...

* Install [node-gyp](https://github.com/nodejs/node-gyp), following the instructions for your OS.

The following worked for me on Windows 10 64 bit:

* Install the latest [Python v2](https://www.python.org/downloads/) (**not v3!**)
* Make sure [Visual Studio 2015](https://www.visualstudio.com/en-us/products/visual-studio-community-vs.aspx) is installed with Visual C++ included
* Install the [Windows 7 64 bit SDK](https://www.microsoft.com/en-us/download/details.aspx?id=8279)


###  Download, Build and Run the project...

1. Clone or download the project and extract to a suitable location
2. Open a command prompt and change directory to the project's folder (the folder containing packages.json). `cd \project_root\AureliaMvc5\AureliaMvc5`
3. Run the following commands
	* `npm install`
	* `jspm install -y`
	* `node node_modules\protractor\bin\webdriver-manager update`
	* There should be no errors at this stage. Please fix any errors before proceeding.
4. Build and run the project using Gulp. 
	* Run the command `Gulp watch`
	* Open a browser and navigate to http://localhost:9000. The Aurelia app should run.
5. Build the project in Visual Studio; it should build with no errors after downloading nuget packages.
	* Note: I added a Task Runner task to copy the html files to the dist folder. If Task Runner explorer fails to open GulpFile.js you may need to apply the fix described [here in StackOverflow](http://stackoverflow.com/questions/31301582/task-runner-explorer-cant-load-tasks) 
	* Run the project and browse to http://localhost:63006 then navigate to http://localhost:63006/app. The Aurelia app should run at that url.
6. Run the unit tests with `gulp test`. They should all run and pass.
7. Run the e2e tests with `gulp serve e2e`. They should all run and pass.



## References
The Aurelia Typescript skeleton was obtained from [here](https://github.com/aurelia/skeleton-navigation) on GitHub

I got started with the useful information provided by [Rui Mourato's blog](http://ruimourato.com/2016/01/26/running-aurelia-on-mvc5.html)

Fix for Task Runner can't load tasks [here on StackOverflow](http://stackoverflow.com/questions/31301582/task-runner-explorer-cant-load-tasks)



## Project Creation Steps
The essential steps used to create the skeleton were:

1. Create a new MVC5 project
2. Copy the Aurelia Typescript skeleton into the root of the project
3. Run npm install 
4. Run jspm install -y
4. Accept the defaults for all the config files (config.js, package.json, tsconfig.e2e.json, karma.conf.js)
5. Prep for TypeScript:
	* Install TypeScript 2.1.4 if not already installed. The latest version can be found [here](http://disq.us/url?url=http%3A%2F%2Fwww.typescriptlang.org%2Findex.html%3A7sLV5XUHtkQV9R0VaVjUe-Q1H20&cuid=3586370)
	*   Modify the PATH environment variable to point to this version, rather than an earlier one. You may need to restart Visual Studio to pick this up.
PATH=...;C:\Program Files (x86)\Microsoft SDKs\TypeScript\2.1\;...
5. Install the TypeScript 2.1.4 nuget packages in Visual Studio
	* install-package microsoft.typescript.compiler
	* Install-Package Microsoft.TypeScript.MSBuild
	* Modify tsconfig.json to exclude the test folder
6. Test to make sure all is working using gulp watch
7. Create a controller and view for to run Aurelia
8. Copy index.html and paste into the index.cshtml for the Aurelia view (no layout used, no changes to the html needed)
9. Find a solution for e2e tests not running. This turned out to be running the command `node node_modules\protractor\bin\webdriver-manager update`
10. Build and run in Visual Studio 2015

 
