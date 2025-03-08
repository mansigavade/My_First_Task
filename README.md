# My_First_Task
This is my first code task in hithub
Task:1 Basic Chatbot
Create a text-based chatbot that can have conversations with users. You can use natural
language processing libraries like NLTK or spaCy to make your chatbot more
conversational.

pip install nltk 
import nltk
nltk.download('punkt')
nltk.download('stopwords')
nltk.download('wordnet')
import nltk
import random
from nltk.chat.util import Chat, reflections
patterns = [
(r'hi|hello|hey', ["Hello!", "Hi there!", "Hey! How can I help you today?"]),
(r'how are you?', ["I'm doing great, thank you for asking!", "I'm good, how about
(r'quit|bye|goodbye', ["Goodbye! It was nice chatting with you.", "See you later!"
(r'(.*) your name?', ["I am a friendly chatbot created using NLTK.", "You can call
(r'(.*) (location|from)', ["I exist in the digital world!", "I live in the cloud."
(r'(.*) (help|assistance)', ["Sure! How can I assist you today?", "I'm here to hel
(r'(.*)', ["Sorry, I didn't quite understand that.", "Could you clarify your quest
]
chatbot = Chat(patterns, reflections)
def chat():
print("Chatbot: Hi! Type 'quit' or 'bye' to exit the conversation.")
while True:
user_input = input("You: ")
if user_input.lower() in ['quit', 'bye']:
print("Chatbot: Goodbye! It was nice chatting with you.")
break
response = chatbot.respond(user_input)
print(f"Chatbot: {response}")
if __name__ == "__main__":
chat()
