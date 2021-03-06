----------------------------------------
Thank you for installing dotnetreport.
----------------------------------------

The nuget package adds client side code to your project, which calls a remote service at https://www.dotnetreport.com. 

Installing this package adds app setting keys to your web.config, and you have to replace the dummy values with your Account Api tokens. 
You must create an online account get the Api tokens.  

You can run your project and navigate to:
	http://localhost/report for the Report Builder
	http://localhost/report/dashboard for the Reports Dashboard
	http://localhost/setup for the Admin Setup 

To start the Scheduler Job, add the following line to your Startup.cs:

	JobScheduler.Start();

For .net Core, dotnet Report uses npm packages for all the client side libraries, and uses gulp to place them in the wwwroot/js/lib folder. 

----------------------------------------------
-----------------IMPORTANT--------------------
----------------------------------------------
client side packages need to be added manually. The list is included package-addme.json and gulpfile-addme.js.
Please manually merge the contents in to your project's actual package.json and gulpfile.js.

You would also need to add Controller with Views and set NewtonSoft Json setting in your Startup.cs

		services.AddControllersWithViews()
                .AddNewtonsoftJson(options => options.UseMemberCasing());

For more details and documentation, you can visit https://www.dotnetreport.com. 

