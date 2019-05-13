# Url shortener

Simple url-shortener based on **flask** and **sqlite3**.  
Each time a user placed a link to the form and click on Submit button new link with variable part length of 4-7 chars is generated. Both values (link address and generated link id) are stored in DB.  
Links belonged to the address in which the server runs does not accepted by the programm as link address. It is realised to avoid server redirection to itself.  

### How to install

``` bash 
$ git clone
$ pip install -r requirements.txt
```

### Run

``` bash
python3 app.py
```

### Todo

(What was not done. However, have ideas how it should be done):

* Deploy to Heroku. I did not succeed it yet.  

* Add authorization:
    * Add a 'User' table with two columns (user, password)
    * Add a column to 'Link' table with foreigh key to user
    * Add functionality of authorization (@register, @login) to the app

* To add a statistic view
    * add a db-request to all links created by the user. Then group non-unique links and count occurences for each one.
    * Show the table at page.  