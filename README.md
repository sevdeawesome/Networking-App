# Networking-App
## Introduction
In this project, we created a social networking application connected to an SQL database in Java. We used PostgreSQL to run the server and store the data files in csvs once the server stops. The csv files are loaded back into the database when the server is started. 

## Functionality
•  New User Registration: When users select “Create User” on the main menu, they can enter a username, password and email address that gets added to the Users table. We used an SQL insert statement to add the tuple to the table.

• User Login/Logout: When a user selects “Log in”, if their username and password exists in the user database, they will have access to view, send and delete connection requests and messages with other users. If an SQL selection finds a user with their unique login and password they are logged into the application.

• Change Password: When users are logged in, they have the option to change their password. This is done by updating their tuple in the users table with an SQL UPDATE statement.

• Search People: A user can search the users database for a username matching their input string. A SELECT statement is run, selecting for names or usernames matching what they’ve inputted, a list of matching profiles is returned to them and they can select who they’d like to interact with. 

• Sends Connection Request: After searching for someone in the database, the user can send a friend request or a message to that user with an options menu. Sending a request will use an SQL INSERT statement to create a tuple in the connections table with the two unique usernames as attributes. Sending a message will insert a tuple into the messages table with an SQL INSERT statement, both users will be attributes as well as a message status. The message will remain in the inbox of the receiver until deleted and the status attribute keeps track of who has viewed the message.

• Accepting or rejecting requests: A user can select “View Friend Requests” to see their current friends and the incoming requests they’ve received. The list of friend requests is found with an SQL SELECT statement where the receiver is the user and the status is “Request”.

• View Friends and then go to a friend's profile: The user can view their friends list and then go to a friend’s profile. From their friend’s profile they can also choose to view their friends list as well.

• Send a message to anyone on the network: 
We chose to implement our messaging through our search function. After searching for another user, the user is given an option to send them a message. The program reads a message from the user and uses an SQL INSERT statement to add the message to the Messages table.

• View Messages and then option to delete messages: 
When the user selects “View Messages” on the main menu, they are shown a list of messages that they have received along with the sender IDs. We selected the messages with an SQL SELECT statement and printed them as a list of strings. The user is then given an option to either delete the message or return to the main menu.


