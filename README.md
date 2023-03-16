## nodejs api 101
This is a quick start guide to creating a node js api

## Needed Software
* install [GIT Download](https://git-scm.com/downloads)
* install [Node JS Download](https://nodejs.org/en/download/)

Create a Directory

### confirm install
run the following form you command line:
<pre>
npm -v
node -v
</pre>

create a directory to start a project
<pre>mkdir first-api
cd first-api
</pre>
create the project
<pre>npm init
</pre>
just hit enter for each prompt
<pre>
This utility will walk you through creating a package.json file.
It only covers the most common items, and tries to guess sensible defaults.

See `npm help init` for definitive documentation on these fields
and exactly what they do.

Use `npm install <pkg>` afterwards to install a package and
save it as a dependency in the package.json file.

Press ^C at any time to quit.
package name: (first-api)
version: (1.0.0)
description:
entry point: (index.js)
test command:
git repository:
keywords:
author:
license: (ISC)
</pre>

you should now have a file "package.json"

install express which wil be your server
<pre>
npm i express
</pre>

create a file called "index.js"

<pre>
var express = require("express");
var app = express();
app.listen(3000, () => {
 console.log("Server running on port 3000");
});

app.get("/hello", (req, res, next) => {
 res.json({"message":"hi world", "version": 1});
});
</pre>

save the file and return to the command line
<pre>
node index.js
</pre>

open this link in browser: [http://3000/hello](http://3000/hello)

others:
* [Firebase function init](./firebase-quick.md)

