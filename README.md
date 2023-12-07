# Chat-Application2
This is a Chat Application 2
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Simple Chat Application</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        #chat-container {
            max-width: 600px;
            margin: 20px auto;
            border: 1px solid #ccc;
            padding: 20px;
            height: 400px;
            overflow-y: scroll;
        }

        #message-input {
            width: calc(100% - 40px);
            padding: 10px;
            margin: 0;
        }

        #send-button {
            width: 40px;
            padding: 10px;
            margin: 0;
            cursor: pointer;
        }
    </style>
</head>
<body>
    <div id="chat-container"></div>
    <input type="text" id="message-input" placeholder="Type your message...">
    <button id="send-button" onclick="sendMessage()">Send</button>

    <script>
        function sendMessage() {
            var messageInput = document.getElementById('message-input');
            var message = messageInput.value;

            if (message.trim() !== '') {
                var chatContainer = document.getElementById('chat-container');
                var newMessage = document.createElement('p');
                newMessage.textContent = 'You: ' + message;
                chatContainer.appendChild(newMessage);

                // Clear the input field after sending the message
                messageInput.value = '';

                // Scroll to the bottom of the chat container
                chatContainer.scrollTop = chatContainer.scrollHeight;
            }
        }
    </script>
</body>
</html>
