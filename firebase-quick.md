## firebase quick start

### init firebase
Create a directory for the firebase project
<pre>
md my-app
cd my-app
</pre>
run the init process
<pre>
firebase init functions
</pre>

<pre>
Enter a project name and select default settings
</pre>

* in the function folder edit the package.json and add line:
<pre>
  "type": "module",
</pre>
* in the index.js file create helloWorld function
<pre>
export const helloWorld = functions.https.onRequest((request, response) => {
   functions.logger.info("Hello logs!", {structuredData: true});
   response.send("Hello from Firebase!");
});
</pre>
* Manually create firestore database after you create function
* Set up the project for pay as you go
* Create storage
* Deploy function
<pre>
cd function
npm run deploy
</pre>

<hr />
For the app configurations, use file ".runtimeconfig.json"

To get the settings into PROD, edit the file online

1) Go the Google Cloud Account https://cloud.google.com/
2) Choose the same project as the project you're hosting in2 firebease.
3) Go to the service cloud function
4) Find your service and click on edit and your can add env variable, build variable.
5) See the build files, add or edit .runtimeconfig.json
