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
* Create Web App to get firebaseConfig
