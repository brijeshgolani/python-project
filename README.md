import nltk
from nltk.chat.util import Chat, reflections

# Define some basic patterns and responses
patterns = [
    (r'hi|hello|hey', ['Hello!', 'Hi there!', 'Hey!']),
    (r'how are you?', ['I am doing well, thank you!', 'I\'m fine, thanks for asking.']),
    (r'what is your name?', ['I am a chatbot.', 'You can call me Chatbot.']),
    (r'quit', ['Bye!', 'Goodbye!', 'Take care!']),
]

# Create a chatbot
chatbot = Chat(patterns, reflections)

# Start chatting
print("Hello! I'm a simple chatbot. You can start chatting with me. Type 'quit' to end the conversation.")
while True:
    user_input = input("You: ")
    response = chatbot.respond(user_input)
    print("Chatbot:", response)
    if user_input.lower() == 'quit':
        break
