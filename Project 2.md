# WEB STACK IMPLEMENTATION (LEMP STACK) IN AWS

### --The first step was to set up nginx web server as shown below.
![Screen Shot 2023-07-02 at 08 39 50](https://github.com/Shizoqua/darey.io-pbl/assets/136805224/253ef9a9-c1fc-4f94-a0c9-83723af7fead)
### --The second step was to install and secure mySQL server as shown below.
![Screen Shot 2023-07-02 at 09 46 45](https://github.com/Shizoqua/darey.io-pbl/assets/136805224/5bcfb301-1f17-4b99-93c2-4fe2e2fbdc8c)
### --The next step was to test the php installed with Ngnx. 
###### * To get this done, a test php file called info.php was created and opened in a text editor (nano) as shown below.
<img width="698" alt="Screen Shot 2023-07-02 at 14 23 59" src="https://github.com/Shizoqua/darey.io-pbl/assets/136805224/b5687a60-a7f2-42f1-b9c0-0e8c7159e6fd">

###### * Then type or paste the following lines as shown below into the new file created. This is valid PHP code that will return information about the server.
<img width="697" alt="Screen Shot 2023-07-02 at 14 23 40" src="https://github.com/Shizoqua/darey.io-pbl/assets/136805224/71dcf297-3bac-40ab-9d4b-0e4ca530035f">

###### * The web page was accessed in the browser by visiting the domain name/public IP address that was set up in the Nginx configuration file followed by /info.php as shown below.
![Screen Shot 2023-07-02 at 14 42 42](https://github.com/Shizoqua/darey.io-pbl/assets/136805224/069ca5a6-af84-4437-ab55-5791c0ed06fc)

###### * The web page containing the detailed infomation about the server is then displayed as shown below.
![Screen Shot 2023-07-02 at 14 43 00](https://github.com/Shizoqua/darey.io-pbl/assets/136805224/8f8e5535-c157-4b4b-ba0d-bd9d5764936d)

### -- last step was was to retrieve data from MySQL database with PHP. 

###### In this step, a test database (DB) was created with simple “To do list” with an access configured to it so the Nginx website could be able to query data from the database (DB) and display it. The database was named example_database and a user named example_user, but these could be replaced with any names of your choice. The stages in achieving this are highlighted below.

###### * Connect to the MySQL console as shown below.
<img width="703" alt="Screen Shot 2023-07-02 at 15 00 50" src="https://github.com/Shizoqua/darey.io-pbl/assets/136805224/77a127c1-ce8e-4c68-ae6f-01cd408d7843">

###### * A new database was created by running the command below from my MySQL console.
<img width="698" alt="Screen Shot 2023-07-02 at 15 01 12" src="https://github.com/Shizoqua/darey.io-pbl/assets/136805224/3f7821df-b1f4-4181-985d-5ce6be2e2953">

###### * A new user was named example_user using mysql_native_password as default authentication method and the password as "password". The password could be replaced with a choice of yours. 
<img width="700" alt="Screen Shot 2023-07-02 at 17 41 29" src="https://github.com/Shizoqua/darey.io-pbl/assets/136805224/450eeed6-5534-4b16-a439-e9737b4a5e8a">

###### * The new user was granted full privileges over the database using the command below. 
<img width="699" alt="Screen Shot 2023-07-02 at 17 41 53" src="https://github.com/Shizoqua/darey.io-pbl/assets/136805224/55522d4b-a6e9-4cf0-a30a-300ac5eb4cff">

###### * The MySQL shell was then exited using the command line below.
<img width="700" alt="Screen Shot 2023-07-02 at 17 54 42" src="https://github.com/Shizoqua/darey.io-pbl/assets/136805224/4f2b947d-9f2b-4169-a1c6-db75319b08e4">

###### * The command linebelow was run to test if the new user has the proper permissions by logging in to the MySQL console again, this time using the custom user credentials.
<img width="701" alt="Screen Shot 2023-07-02 at 17 54 58" src="https://github.com/Shizoqua/darey.io-pbl/assets/136805224/0de0e1ba-d28f-416b-971f-64e474c3e2f1">




