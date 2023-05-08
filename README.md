Download Link: https://assignmentchef.com/product/solved-web322-assignment2
<br>
Create and publish a web app that uses multiple routes which serve static files (HTML &amp; CSS) as well as create a “data service” module for accessing data.  This will serve as the “scaffolding” for future assignments.

<h1>Specification:</h1>

This assignment will involve creating multiple routes that serve specific HTML pages &amp; JSON.

<h1>Part 1: Dev Environment, Home &amp; About</h1>




<h3><strong><u>Step 1:</u></strong> Development Environment</h3>

<ul>

 <li>Create a folder called <strong>web322-app</strong>. This will serve as our main application that we will be updating and modifying throughout this course.</li>

 <li>Inside this folder, initialize a local <strong>Git repository (</strong>using<strong> git init </strong>from the integrated terminal<strong>)</strong></li>

 <li>Add the file <strong>js</strong></li>

 <li>Add the file <strong>data-service.js</strong></li>

 <li>Create a <strong>json</strong> file using <strong>npm init</strong>. Ensure that your “entry point” is <strong>server.js</strong> (this should be the default), and “author” is your full name, ie: “John Smith”</li>

 <li>Obtain the <strong>js</strong> module using <strong>npm install express –save</strong></li>

 <li><strong>Commit</strong> your changes your <strong>local git repository</strong> (using the source control icon showing the number of changes) with the message “initial commit”</li>

</ul>

<h3><strong><u>Step 2:</u></strong> Adding Files / Folders</h3>

<ul>

 <li>Add the folder <strong>views</strong> – this will be the location of the .html files that we will be using in our application</li>

 <li>Add the folder <strong>public</strong> – this will be the location of the .css, client side .js &amp; image files that we use in our application</li>

 <li>Add the folder <strong>data</strong> – this will be a temporary source of static data (JSON) for our application</li>

 <li>Inside the <strong>views</strong> folder, add the files <strong>html</strong> and <strong>about.html</strong></li>

 <li>Inside the <strong>public </strong>folder, add the folder <strong>css</strong></li>

 <li>Inside the <strong>public/css</strong> folder – add the file <strong>css</strong> (this will serve as the main.css file for our app)</li>

 <li>Your folder structure should now look like the image to the right:</li>

</ul>

<h3><strong><u>Step 3:</u></strong> Adding Static Content (home.html &amp; about.html)</h3>

<ul>

 <li>Before starting on your <strong>js</strong> file, add some html to <strong>home.html</strong> &amp; <strong>about.html</strong> using the following template for both files<strong>: </strong><a href="https://scs.senecac.on.ca/~patrick.crawford/shared/winter-2018/web322/A2/template.html.txt">https://scs.senecac.on.ca/~patrick.crawford/shared/winter-2018/web322/A2/template.html.txt</a> – this leverages the Bootstrap 3 &amp; jQuery libraries (discussed in detail during Week 11)</li>

 <li>At this point, both files should be exactly the same, however we must make some changes to each page (what’s currently there is only a starting point)

  <ul>

   <li><strong>html</strong>

    <ul>

     <li>Update “Link 1” to read “Home”</li>

     <li>Update “Link 2” to read “About” and change it’s “href” property from “#” to “/about”:</li>

     <li>Update the page “title” to read “Home”</li>

     <li>Ensure the heading (h2) for the left column reads “Coming Soon” – and provide a relevant message to the user</li>

     <li>Ensure the heading (h2) for the right column reads “Welcome”</li>

    </ul></li>

   <li><strong>html</strong>

    <ul>

     <li>Update “Link 1” to read “Home”, remove the class “active” from the parent &lt;li&gt; element and change the link’s “href” property from “#” to “/”</li>

     <li>Update “Link 2” to read “About” and add the class “active” to the parent &lt;li&gt; element</li>

     <li>Update the page “title” &amp; heading (h2) to read “About”</li>

     <li>Modify the grid layout from 2 columns to 1 (col-md-12) column. This was discussed in WEB222, but you can reference week 11 (“Responsive Grid System” – <a href="https://web322.ca/notes/week11">https://web322.ca/notes/week11</a></li>

    </ul></li>

  </ul></li>

</ul>

if you need further help

<ul>

 <li>(<strong><u>both</u></strong> <strong>htm</strong>l &amp; <strong>about.html</strong>)

  <ul>

   <li>modify the “navbar-brand” span element to read “WEB322 – Student Name” where “Student Name” is your name, ie “John Smith”, etc</li>

   <li>Update “Link 3” to read “Employees” and change it’s “href property from “#” to “/employees”</li>

   <li>Update “Link 4” to read “Managers” and change it’s “href property from “#” to “/managers”</li>

   <li>Update “Link 5” to read “Departments” and change it’s “href property from “#” to “/departments”</li>

  </ul></li>

</ul>

<h3><strong><u>Step 4:</u></strong> Update server.js &amp; testing the app</h3>

<ul>

 <li>Now that all the files are in place, update your <strong>js</strong> file according to the following specifications (<strong>HINT</strong>: Refer to the sample code from <strong>week 2</strong> for reference):

  <ul>

   <li>The server must make use of the “<strong>express</strong>” module</li>

   <li>The server must listen on <strong>env.PORT</strong> <strong>|| 8080</strong></li>

   <li>The server must output: “Express http server listening on <strong><em>port</em></strong>” – to the console, where <strong><em>port</em></strong> is the port the server is currently listening on (ie: 8080)</li>

   <li>The route “<strong>/</strong>” must return the <strong>html </strong>file from the <strong>views</strong> folder</li>

   <li>The route “<strong>/about</strong>” must return the <strong>html</strong> file from the <strong>views</strong> folder</li>

   <li><strong>NOTE</strong>: for your server to correctly return the “css/site.css” file, the “<strong>static</strong>” middleware must be used: in your <strong>js</strong> file, add the line: <strong>app.use(express.static(‘public’));</strong> before your “routes” – we will discuss this in greater detail in Week 4</li>

   <li>From the integrated terminal, enter the command <strong>node server.js</strong> and verify the following:

    <ul>

     <li>The integrated terminal shows “Express http server listening on 8080”</li>

     <li>The url: <a href="http://localhost:8080"><strong>http://localhost:8080</strong></a> shows the “Home” page:</li>

     <li>The url: <a href="http://localhost:8080/about"><strong>http://localhost:8080/about</strong></a> shows the “About” page</li>

    </ul></li>

  </ul></li>

</ul>

<h1>Part 2: Data Service, Employees, Managers &amp; Departments</h1>

<h3><strong><u>Step 1:</u></strong> Obtaining the Data</h3>

<ul>

 <li>Create 2 new files inside the “data” folder: <strong>json</strong> and <strong>employees.json</strong></li>

 <li>Open your web browser and navigate to: <a href="http://scs.senecacollege.ca/~patrick.crawford/shared/winter-2018/web322/A2/departments.json">this link (departments.json)</a> and copy the contents of the JSON file to your own departments.json file (within the “data” folder).</li>

 <li>Next, navigate to: <a href="http://scs.senecacollege.ca/~patrick.crawford/shared/winter-2018/web322/A2/employees.json">this link (employees.json)</a> and copy the entire contents of the JSON file to your own employees.json file (within the “data” folder) – this should be an array of 280 “employee” objects</li>

</ul>

<h3><strong><u>Step 2:</u></strong> Updating the custom data-service.js module</h3>

<ul>

 <li>The file that we added at the beginning of this assignment (“data-service.js”) is going to be a module that we will use within our server.js file.</li>

 <li>Your first step is to “<strong>require</strong>” this module at the top of your <strong>js</strong> file so that we can use it to interact with the data from server.js</li>

</ul>

<h3><strong><u>Step 3:</u></strong> Adding additional Routes:</h3>

We will be making use of this employee data from a different location from our “/” and “/about” routes.  These routes will serve as the public-facing pieces of our application, whereas we will be dealing with employee management in a private area (later protected by a login page / user authentication, etc).

<strong><u> </u></strong>

Inside your server.js add routes to respond to the following “get” requests for the application.  Once you have written the routes, test that they work properly by returning a confirmation string using <strong>res.send()</strong> and testing the server using localhost:8080.  For example, <strong>localhost:8080/managers</strong> could be set up to return something like <strong>“TODO: get all employees who have isManager==true”</strong>.  This will help to confirm that your routes are set up properly.




<strong>Important Note</strong>: Any response sending JSON from the server must include the correct content-typeheader – see <a href="https://expressjs.com/en/4x/api.html#res.json">res.json([body])</a>




<u>/employees</u>




<ul>

 <li>This route will return a JSON formatted string containing all of the employees within the employees.json file</li>

</ul>

<u>/managers</u>




<ul>

 <li>This route will return a JSON formatted string containing all the employees whose <strong>isManager</strong> propertyis set to <strong>true</strong>.</li>

</ul>

<u>/departments</u>




<ul>

 <li>This route will return a JSON formatted string containing all of the departments within the departments.json file</li>

</ul>

<u>[ no matching route ]</u>




<ul>

 <li>If the user enters a route that is not matched with anything in your app (ie: http://localhost:8080/app) then you must return the custom message “<strong>Page Not Found</strong>” with an HTTP status code of <strong>404</strong>.</li>

 <li><strong>Note:</strong> at this point, you may wish to send a custom 404 page back to the user (completely optional, but everyone loves a good 404 page: <a href="https://medium.com/@CollectUI/404-page-design-inspiration-march-2017-f6d9f7efd054">https://medium.com/@CollectUI/404-page-design-inspiration-march-2017-f6d9f7efd054</a></li>

</ul>




<h3><strong><u>Step 4:</u></strong> Writing the data-service.js module:</h3>

<u> </u>

The promise driven data-service.js module will be responsible for reading the employees.json and departments.json files from within the “data” directory on the server, parsing the data into arrays of objects and returning elements (ie: “employee” objects) from those arrays to match queries on the data.

Essentially the data-service.js module will encapsulate all the logic to work with the data and only expose accessor methods to fetch data/subsets of the data.

<h3><strong><u>Module Data</u></strong></h3>

The following two arrays should be declared “globally” within your module:

<ul>

 <li><strong>employees </strong>– type: <strong>array</strong></li>

 <li><strong>departments</strong> – type: <strong>array</strong></li>

</ul>

<h3><strong><u>Exported Functions</u></strong></h3>

Each of the below functions are designed to work with the employees and departments datasets.  Since we have no way of knowing how long each function will take (we cannot assume that they will be instantaneous, ie: what if we move from .json files to a remote database, or introduce hundreds of thousands of objects into our .json dataset? – this would increase lag time).




Because of this, <strong><u>every one of the below functions</u> must return a promise </strong>that <strong>passes the data</strong> via it’s “<strong>resolve</strong>” method (or – if <strong>no data was returned</strong>, passes an <strong>error message</strong> via it’s “<strong>reject</strong>” method).




When we access these methods from the server.js file, we will be assuming that they return a promise and we will respond appropriately with <strong>.then()</strong> and .<strong>catch()</strong> (see “Updating the new routes…” below).

<u> </u>

<u>initialize()</u>




<ul>

 <li>This function will read the contents of the “./data/employees.json” file (<strong>hint</strong>: see the <a href="https://nodejs.org/api/fs.html#fs_file_system">fs module</a> &amp; the <a href="https://nodejs.org/api/fs.html#fs_fs_readfile_path_options_callback">readFile</a> method), convert the file’s contents into an array of objects (<strong>hint</strong>: see <a href="https://developer.mozilla.org/en/docs/Web/JavaScript/Reference/Global_Objects/JSON/parse">JSON.parse</a>) , and assign that array to the <strong>employees array</strong> (from above).</li>

 <li>Only once the read operation for “./data/employees.json” has completed successfully (not before), repeat the process for the “./data/departments.json” and assign the parsed object array to the <strong>departments</strong> <strong>array</strong> from above.</li>

 <li>Once these two operations have finished successfully, invoke the <strong>resolve </strong>method for the promise to communicate back to server.js that the operation was a success.</li>

 <li>If there was an error at any time during this process, invoke the <strong>reject</strong> method for the promise and pass an appropriate message, ie: reject(“unable to read file”).</li>

</ul>

<u>getAllEmployees()</u>




<ul>

 <li>This function will provide the full array of “employee” objects using the <strong>resolve</strong> method of thereturned promise.</li>

 <li>If for some reason, the length of the array is 0 (no results returned), this function must invoke the <strong>reject</strong> method and pass a meaningful message, ie: “no results returned”.</li>

</ul>

<u>getManagers()</u>




<ul>

 <li>This function will provide an array of “employee” objects whose <strong>isManager</strong> property is <strong>true</strong> using the <strong>resolve</strong> method of the returned promise.</li>

 <li>If for some reason, the length of the array is 0 (no results returned), this function must invoke the <strong>reject</strong> method and pass a meaningful message, ie: “no results returned”.</li>

</ul>

<u>getDepartments()</u>

<u> </u>

<ul>

 <li>This function will provide the full array of “department” objects using the <strong>resolve</strong> method of thereturned promise.</li>

 <li>If for some reason, the length of the array is 0 (no results returned), this function must invoke the <strong>reject</strong> method and pass a meaningful message, ie: “no results returned”.</li>

</ul>




<h3><strong><u>Step 5:</u></strong> Updating the code surrounding app.listen()</h3>




Before we start updating the routes in server.js to use our new data-service module, we must make a small update to the code <strong><em>surrounding </em></strong>the app.listen() call at the bottom of the server.js file.  This is where the <strong>initialize()</strong> method from our data-service.js module comes into play.




Fundamentally, initialize() is responsible for reading the .json files from the “data” folder and parsing the results to create the “global” (to the module) arrays, “employees” and “departments” that are used by the other functions.  However, it also returns a <strong>promise</strong> that will only <strong>resolve</strong> successfully once the files were read correctly and the “employees” and “departments” arrays were correctly loaded with the data.




Similarly, the promise will <strong>reject</strong> if any error occurred during the process.  Therefore, we must <strong>only call app.listen()</strong> if our call to the <strong>initialize()</strong> method is successful, ie: .<strong>then(() =&gt; { //start the server })</strong>.

If the initialize() method invoked <strong>reject</strong>, then we should not start the server (since there will be no data to fetch) and instead a meaningful error message should be sent to the console, ie: <strong>.catch(()=&gt;{ /*output the error to the console */})</strong>




<h3><strong><u>Step 6:</u></strong> Updating the new routes to use data-service.js</h3>




Now that the data-service.js module is complete, we must update our new routes (ie: /employees, /managers &amp; /departments) to make calls to the service and fetch data to be returned to the client. Recall: Any response sending JSON from the server must include the correct content-type header – see <a href="https://expressjs.com/en/4x/api.html#res.json">res.json([body])</a>.




Since our data-service.js file exposes functions that are guaranteed to return a <strong>promise</strong> that (if resolved successfully), will contain the requested data, we must make use of the <strong>.then()</strong> method when accessing the data from within our routes.




For example, the <strong>/departments</strong> route must make a call to the <strong>getDepartments()</strong> method of the data-service.js module to fetch the correct data.  If <strong>getDepartments()</strong> was successful, we can use <strong>.then((data) =&gt; { /*return JSON data*/ })</strong> to access the data from the function and send the response back to the client.




If any of the methods were unsuccessful however, the <strong>.then()</strong> method will not be called – the <strong>catch()</strong> method will be called instead.  If this is the case, the server <strong>must</strong> return a simple JSON object with 1 property: “message” containing the message supplied in the <strong>.catch()</strong> method, ie: <strong>.catch((err) =&gt; { /* return err message in the JSON format:</strong> {message: <strong><em>err</em></strong>}<strong>*/</strong> <strong>})</strong>.




By <strong>only</strong> calling <strong>res.json() </strong>from within <strong>.then()</strong> or <strong>.catch()</strong> we can ensure that the data will be in place (no matter how long it took to retrieve) before the server sends anything back to the client.




<h3><strong><u>Step 7:</u></strong> Pusing to Heroku</h3>

<ul>

 <li>Once you are satisfied with your application, deploy it to Heroku:

  <ul>

   <li>Ensure that you have checked in your latest code using <strong>git </strong>(from within Visual Studio Code)</li>

   <li>Open the integrated terminal in Visual Studio Code</li>

   <li>Log in to your Heroku account using the command <strong>heroku login</strong></li>

   <li>Create a new app on Heroku using the command <strong>heroku create</strong></li>

   <li>Push your code to Heroku using the command <strong>git push heroku master</strong></li>

  </ul></li>

 <li><strong>IMPORTANT NOTE: </strong>Since we are using an “<strong>unverified” free </strong>account on Heroku, we are limited to only <strong>5 apps</strong>, so if you have been experimenting on Heroku and have created 5 apps already, you must delete one (or verify your account with a credit card). Once you have received a grade for Assignment 1, it is safe to delete this app (login to the Heroku website, click on your app and then click the <strong>Delete app…</strong> button under “<strong>Settings</strong>“).</li>

</ul>




<h3><strong><u>Testing</u></strong>: Sample Solution</h3>




To see a completed version of this app running, visit: <a href="https://sleepy-mesa-28798.herokuapp.com">https://sleepy-mesa-28798.herokuapp.com</a>