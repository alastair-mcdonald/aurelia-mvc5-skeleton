#Aurelia Mvc5 Skeleton

This project is setup to integrate the Aurelia Typescript navigation skeleton with an Asp.Net Mvc5 project which uses .Net 4. 

Currently the .Net project skeletons provided by the Aurelia team support .Net Core only with nothing supplied to support .Net 4.*.

## Usage
1. Clone or download the project and extract to a suitable location
2. Open a command prompt and change directory to the project's folder (the folder containing packages.json). `cd \project_root\AureliaMvc5\AureliaMvc5`
3. Run the following commands
	* npm install
	* jspm install -y
	* node node_modules\protractor\bin\webdriver-manager update
4. Build and run the project using Gulp. 
	* run the command `Gulp watch`
	* open a browser and navigate to http://localhost:9000. The Aurelia app should run.
5. Build the project in Visual Studio; it should build with no errors after downloading nuget packages.
	* Note: I added a Task Runner task to copy the html files to the dist folder. If Task Runner explorer fails to open GulpFile.js you may need to apply the fix described [here in StackOverflow](http://stackoverflow.com/questions/31301582/task-runner-explorer-cant-load-tasks) 
	* Run the project and browse to http://localhost:63006 then navigate to http://localhost:63006/app
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
5. Install TypeScript at 2.1.4
	* install-package microsoft.typescript.compiler
	* Install-Package Microsoft.TypeScript.MSBuild
	* Modify tsconfig.json to exclude the test folder
6. Test to make sure all is working using gulp watch
7. Create a controller and view for to run Aurelia
8. Copy index.html and paste into the index.cshtml for the Aurelia view (no layout used, no changes to the html needed)
9. Find a solution for e2e tests not running. This turned out to be running the command `node node_modules\protractor\bin\webdriver-manager update`
10. Build and run in Visual Studio 2015

 
