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


<img width="798" alt="Screen Shot 2023-07-02 at 18 24 47" src="https://github.com/Shizoqua/darey.io-pbl/assets/136805224/2f98844f-c775-443d-8340-d425b81bbebc">


###### * A new database was created by running the command below from my MySQL console.
<img width="698" alt="Screen Shot 2023-07-02 at 15 01 12" src="https://github.com/Shizoqua/darey.io-pbl/assets/136805224/3f7821df-b1f4-4181-985d-5ce6be2e2953">


###### * A new user was named example_user using mysql_native_password as default authentication method and the password as "password". The password could be replaced with a choice of yours. 
<img width="700" alt="Screen Shot 2023-07-02 at 17 41 29" src="https://github.com/Shizoqua/darey.io-pbl/assets/136805224/450eeed6-5534-4b16-a439-e9737b4a5e8a">

###### * The new user was granted full privileges over the database using the command below. 
<img width="699" alt="Screen Shot 2023-07-02 at 17 41 53" src="https://github.com/Shizoqua/darey.io-pbl/assets/136805224/55522d4b-a6e9-4cf0-a30a-300ac5eb4cff">

<img width="803" alt="Screen Shot 2023-07-02 at 18 34 42" src="https://github.com/Shizoqua/darey.io-pbl/assets/136805224/31eb1e23-e8c4-424a-abc1-2a2df5032508">


###### * The MySQL shell was then exited using the command line below.
<img width="700" alt="Screen Shot 2023-07-02 at 17 54 42" src="https://github.com/Shizoqua/darey.io-pbl/assets/136805224/4f2b947d-9f2b-4169-a1c6-db75319b08e4">

###### * The command linebelow was run to test if the new user has the proper permissions by logging in to the MySQL console again, this time using the custom user credentials.
<img width="701" alt="Screen Shot 2023-07-02 at 17 54 58" src="https://github.com/Shizoqua/darey.io-pbl/assets/136805224/0de0e1ba-d28f-416b-971f-64e474c3e2f1">

###### * After logging in to the MySQL console, confirm that you have access to the example_database database runing the command below.
<img width="699" alt="Screen Shot 2023-07-02 at 18 05 12" src="https://github.com/Shizoqua/darey.io-pbl/assets/136805224/d18fe1a0-b56e-4def-adee-7cfaaf5aa495">

<img width="796" alt="Screen Shot 2023-07-02 at 18 41 26" src="https://github.com/Shizoqua/darey.io-pbl/assets/136805224/a8c73132-2771-452c-abea-3d56f6bfab2f">

###### * Test table named todo_list was created with the command below.
<img width="700" alt="Screen Shot 2023-07-02 at 18 55 39" src="https://github.com/Shizoqua/darey.io-pbl/assets/136805224/bea63e93-3f97-403f-801d-54f42eb513fa">

###### * 4 rows were instered using diferent values with the comand line below. The first row is "My first important item", second row is "My second important item", third row is "My very third important item" and the fourth row is "and this one more thing".
<img width="699" alt="Screen Shot 2023-07-02 at 18 56 01" src="https://github.com/Shizoqua/darey.io-pbl/assets/136805224/a988b169-5f01-414c-bdb3-2c20f78c0ce6">

<img width="797" alt="Screen Shot 2023-07-03 at 06 10 07" src="https://github.com/Shizoqua/darey.io-pbl/assets/136805224/2f2ed081-3680-4aa8-ae74-fb1392a4ea84">


###### * The command was to confirm that the data was successfully saved to the table and to present to us all the data we inserted in tabular form.After this, we can exit the MySQL environment with (mysql> exit).
<img width="703" alt="Screen Shot 2023-07-02 at 18 56 21" src="https://github.com/Shizoqua/darey.io-pbl/assets/136805224/051b9f54-9ab3-40af-a17b-d12ba15b1ebd">

<img width="798" alt="Screen Shot 2023-07-03 at 06 12 31" src="https://github.com/Shizoqua/darey.io-pbl/assets/136805224/104f1e51-d217-4dac-b330-05f2778458a6">

###### * PHP script was created next with the command below to conect to the MySQL database and to query for the content of the todo_list table. 
<img width="700" alt="Screen Shot 2023-07-03 at 06 24 22" src="https://github.com/Shizoqua/darey.io-pbl/assets/136805224/79de425a-884b-4301-87fc-27252f6baa25">


###### * The content below was copied into the todo_list.php script.
<img width="701" alt="Screen Shot 2023-07-03 at 06 24 53" src="https://github.com/Shizoqua/darey.io-pbl/assets/136805224/25cc4bd9-97d7-43b7-9ec5-236343e395f1">

<img width="800" alt="Screen Shot 2023-07-03 at 06 32 45" src="https://github.com/Shizoqua/darey.io-pbl/assets/136805224/40e3ee9d-8dbd-4894-80ea-3d6abd979db7">

###### * After the file was saved and closed after editing it, the page is now viewed on web browser using "http://<Public_domain_or_IP>/todo_list.php". 
######  The outcome is shown below.

![Screen Shot 2023-07-03 at 14 47 26](https://github.com/Shizoqua/darey.io-pbl/assets/136805224/082f2e25-be1e-4572-acc2-382b599de599)











