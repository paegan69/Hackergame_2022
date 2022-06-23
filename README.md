# HackergameV2
Browsergame made with Node.js and MySQL  
Play an early demo version here: [hackergameV2](https://game.marcelkaemper.de)  (*server down)
Take a look at the [Wiki](https://github.com/MarcelKaemper/HackergameV2/wiki/tutorial) to get started.  

## Features
* Top players list
* Clans
* Terminal
* Servers
* Server software
* SSH Connections to your servers via terminal
* Realtime stockmarket
* Mail system
* Money transfers


## Running it locally

### Installing NodeJS

#### Debian based distributions:
Start by running apt updates and downloading and updated NodeJS installer (offial distro repositories usually outdated): 
```
apt update
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.38.0/install.sh | bash
```
This will install the nvm script to your user account. To use it, you must first source your .bashrc file:
```
source ~/.bash_profile
```
Now, check which versions of NodeJS are available:
```
nvm list-remote
```
I recommend using one of the LTS: Fermium releases since this is what this fork was tested on:
```
nvm install v14.17.4
OR
nvm install lts/fermium
```
Verify that you’ve installed the new version by running node with the -v version flag:
```
node -v
```

#### Arch based distributions:

```
pacman -S nodejs
```

### Downloading the repository

```
git clone https://github.com/MarcelKaemper/HackergameV2.git
```
### Get an API key from finnhub.io
Create an account at https://finnhub.io/ to get a free API key to get access to live stock information.  

### Create database file

Create the file ```public/javascripts/functions/secret.js``` and fill in the credentials to your database.  
You can create a basic structure of the database with the file in ./db/db_structure_##.sql

Example dbconn.js
```
module.exports = {
    _DB: {
        _HOST: "",
        _USER: "",
        _PASSWORD: "",
        _DATABASE: "",
    },
    _API: {
        _KEY: "" # https://finnhub.io/ API_KEY
    }
}

```

### Run the server:  

``` 
npm install  
node bin/www  
OR
pm2 start bin/www
```
### Run the server:  

Access the game at http://[server-ip]:3000
