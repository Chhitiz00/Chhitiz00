<!DOCTYPE html>
<!--Kindly copied from ChaptGPT-->
<html>
<head>
    <title>Chatbot AI</title>
    <script>
        function chat() {
            // Get user input
            var userInput = document.getElementById("userInput").value;
            
            // Clear input field
            document.getElementById("userInput").value = "";
            
            // Get chat history element
            var chatHistory = document.getElementById("chatHistory");
            
            // Display user input
            var userMessage = document.createElement("p");
            userMessage.innerHTML = "<strong>You:</strong> " + userInput;
            chatHistory.appendChild(userMessage);
            
            // AI responses
            var response;
            if (userInput.includes("hello")) {
                response = "Hello! How can I assist you today?";
            } else if (userInput.includes("bye")) {
                response = "Goodbye! Have a great day!";
            } else {
                response = "I'm sorry, I didn't understand that.";
            }
            
            // Display AI response
            var aiMessage = document.createElement("p");
            aiMessage.innerHTML = "<strong>Chatbot:</strong> " + response;
            chatHistory.appendChild(aiMessage);
        }
    </script>
</head>
<body>Note:Only hello and bye will be answered as we are newly developers.
    <h1>Chatbot AI</h1>
    <div id="chatHistory"></div>
    <input type="text" id="userInput" placeholder="Type your message...">
    <button onclick="chat()">Send</button>
</body>
</html>
