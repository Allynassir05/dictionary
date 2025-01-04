# Initialize an empty dictionary to store words and their meanings
dictionary = {}

def add_word(word, meaning):
    """Adds a word and its meaning to the dictionary."""
    dictionary[word] = meaning
    print(f"The word '{word}' has been added to the dictionary.")

def search_word(word):
    """Searches for the meaning of a word in the dictionary."""
    meaning = dictionary.get(word)
    if meaning:
        print(f"The meaning of '{word}' is: {meaning}")
    else:
        print(f"The word '{word}' is not in the dictionary.")

def display_menu():
    """Displays the menu options."""
    print("\nDictionary Program")
    print("1. Add a word and its meaning")
    print("2. Search for a word's meaning")
    print("3. Exit")

def main():
    while True:
        display_menu()
        choice = input("Enter your choice (1/2/3): ").strip()

        if choice == '1':
            word = input("Enter the word: ").strip().lower()
            meaning = input("Enter the meaning: ").strip()
            add_word(word, meaning)
        elif choice == '2':
            word = input("Enter the word to search: ").strip().lower()
            search_word(word)
        elif choice == '3':
            print("Exiting the program. Goodbye!")
            break
        else:
            print("Invalid choice. Please enter 1, 2, or 3.")

# Start the dictionary program
main()
