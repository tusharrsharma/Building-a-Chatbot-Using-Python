# Building-a-Chatbot-Using-Python
import random
# Define a dictionary 
responses = {
    "hello": ["Hi!", "Hello!", "Hey!"],
    "hi": ["Hi!", "Hello!", "Hey!"],
    "how are you": ["I'm good, thanks!", "I'm doing well!", "I'm great!"],
    "what's your name": ["I'm Chatbot!", "My name is Chatbot!", "I'm called Chatbot!"],
    "default": ["I didn't understand that.", "Sorry, can you repeat that?", "I'm not sure what you mean."]
}

def get_response(message):
    # Convert the message to lowercase
    message = message.lower()
    # Check if the message is in the responses dictionary
    if message in responses:
        # Return a random response from the list
        return random.choice(responses[message])
    else:
        # Return a default response
        return random.choice(responses["default"])
def chatbot():
    print("Welcome to the chatbot!")
    while True:
        # Get the user's message
        message = input("You: ")

        # Get the response
        response = get_response(message)

        # Print the response
        print("Chatbot:", response)

# Start the chatbot
chatbot()
