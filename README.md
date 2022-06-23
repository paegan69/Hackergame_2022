# HackergameV2
Browsergame made with Node.js and MySQL  
Play an early demo version here: [hackergameV2](https://game.marcelkaemper.de)  
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

```
apt update
apt install nodejs
```
#### Arch based distributions:

```
pacman -S nodejs
```

### Downloading the repository

```
git clone https://github.com/MarcelKaemper/HackergameV2.git
```
# Get an API key from finnhub.io
Create an account at https://finnhub.io/ to get a free API key to get access to live stock information.  

### Create database file

Create the file ```public/javascripts/functions/secret.js``` and fill in the credentials to your database.  
You can download the structure of our database [here](https://marcelkaemper.dev/db_structure_09_20.sql) (If outdated -> Open an issue)  

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
