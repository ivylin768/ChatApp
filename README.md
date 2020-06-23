# ChatApp
Chat App Created Records While Learning Android Studio


## The app in *1155131776_a1.zip* has the following features

• Two activities (Main Activity and Chat Activity)

• There is a button on Main Activity which will allow the user to enter the Chat Activity

• The Chat Activity has a back button on the Action Bar, allowing the user to go back to the Main Activity

• The Chat Activity consists of a ListView for listing past messages, an EditText for user input, and an ImageButton or ImageView for user to send the message.

• Each item in the ListView should contain two elements, one is the message itself, another is the time (HH:MM) when the message is sent

• When the user clicks on the send button, the app should perform the following actions:
o Check if the user has input any text (i.e. check whether the input area is empty)
o If the user has input some text, add a new item containing the message to the end of the ListView; and then clear the input area

## The app in *1155131776_a2.zip* have the following features
• Two activities (Main Activity and Chat Activity)

• When the Main Activity is created, you should fetch a list of chatrooms from the server using the /get_chatrooms API, and then populate the ListView in the activity with the names of the chatrooms.

• When the user clicks on one of the chatrooms, the Chat Activity will be shown, in which the following functions should be realized.

• There should be a refresh button on the Action Bar.

• The Chat Activity should fetch the first page of messages in the selected chatroom using the /get_messages API when the user enters the chat room, or when the user clicks on the refresh button, and the messages should be shown in the ListView.

• When the user inputs some text and clicks the Send button, the app should clear the input area, and submit the message to the server using the /send_message API, and then add the message to the bottom of the ListView

• When the user scrolls to the topmost message in the ListView, the app should automatically fetch the next page of the messages, unless the current page is the last page. (Pay attention to the “total_pages” field in the JSON returned by the /get_messages API).

• Each message should display the name of the user who wrote the message, the message, as well as the message_time of the message (you can decide how to present the time).

## The server application developed in *1155131776_a3.zip* have the following features:
• A server application written in Python using the Flask framework
• The server application should implement the three APIs to support the instant messaging app
o API 1: GET: /api/asgn3/get_chatrooms:
Returns a list of chatrooms available (you should at least create one chatroom in your database).
o API 2: GET: /api/asgn3/get_messages:
Returns the list of messages in a particular chatroom, sorted in reverse chronological order (the latest message comes first), and implements the paging mechanism as shown in the example.
o API 3: POST: /api/asgn3/send_message:
Allows the app to submit a new message to a chatroom, which should be inserted into the database.
