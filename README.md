#Aurelia Mvc5 Skeleton

This project is setup to integrate the Aurelia Typescript navigation skeleton with an Asp.Net Mvc5 project which uses .Net 4. 

Currently the .Net project skeletons provided by the Aurelia team support .Net Core only with nothing supplied to support .Net 4.*.

The steps used to create the skeleton were

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
9. Build and run in Visual Studio 2015

 
