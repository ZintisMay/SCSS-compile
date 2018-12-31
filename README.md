Hi all,

This is going to be a small repo that demonstrates one way to compile SCSS. It should be pretty easy to get it up and running on your own machines.


##To get this repo working:

###Step 1:

Command line to the root directory.

###Step 2:

npm run watch-scss

###Step 3:

Open the index.html in browser, edit main.scss and more.scss to see how it works!

##To get it up and running from an empty repo:

###Step 1:

npm init

###Step 2:

npm install nodemon node-sass

###Step 3: in package.json, "scripts", add these lines:


     "build-scss": "node-sass --include-path scss scss/main.scss css/main.css",
     "watch-scss": "nodemon -e scss -x \"npm run build-scss\""

//The build-scss command accesses the files from /scss/main.scss and compiles it to /css/main.css

//You might need to change the file pathing to match your project. This one assumes you have two folders (/css and /scss), and a file (/scss/main.scss). 

###Step 4: To compile:

npm run build-scss

OR

npm run watch-scss

//watch-scss will automatically compile whenever you save main.scss. so just reference main.css in your html files and your good!