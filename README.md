# Caesar Cipher Tool  
**SkillCraft Cybersecurity Internship – Task 1**  
**Author**: Piyush Kumar  
**Domain**: Cybersecurity

---

## 🛠️ Project Overview  
This is a Python-based Caesar cipher encryption and decryption tool developed for Task 1 of my internship at SkillCraft Technology. It applies a classic substitution cipher to text, offering simple yet effective reversible text obfuscation.

---

## 🔑 Features
- 🔐 Encrypt and decrypt any `.txt` file using Caesar cipher  
- 🔁 Fully reversible transformation using a defined key (shift value)  
- 📄 Supports both upper and lowercase letters, digits, and basic punctuation  
- ⚙️ Command-line interface (CLI) for ease of use and automation  
- 📁 Organized folder structure for input/output automation  

---

## 📚 Learning Outcomes
- Understood classical encryption principles (Caesar cipher)  
- Developed CLI-based encryption/decryption tools using `argparse`  
- Practiced reversible encryption logic using ASCII and modular arithmetic  
- Improved Python scripting skills for security-related tasks  

---

## ▶️ Sample Run

### Encrypt a Text File
```bash
python main.py encrypt input/message.txt output/encrypted.txt --key 5


# This function does the Caesar Cipher encryption or decryption
def caesar_cipher(message, shift, mode):
    new_message = ""

    for letter in message:
        if letter.isalpha(): 
            if letter.isupper():
                start = ord('A')  # ASCII value of A = 65
            else:
                start = ord('a')  # ASCII value of a = 97

            if mode == "encrypt":
                # Shift the letter forward
                new_letter = chr((ord(letter) - start + shift) % 26 + start)
            elif mode == "decrypt":
                # Shift the letter backward
                new_letter = chr((ord(letter) - start - shift) % 26 + start)

            new_message += new_letter
        else:
            # If not a letter, just add it as it is
            new_message += letter

    return new_message


# This is the main part of the program
def main():
    print("Welcome to the Caesar Cipher Program!")

    # Ask the user what they want to do
    mode = input("Type 'encrypt' to encode or 'decrypt' to decode: ").lower()

    # Make sure the input is valid
    if mode != "encrypt" and mode != "decrypt":
        print("Please type only 'encrypt' or 'decrypt'.")
        return

    # Ask for the message
    text = input("Enter your message: ")

    # Ask for the shift number
    try:
        shift = int(input("Enter the shift number (0 to 25): "))
        if shift < 0 or shift > 25:
            print("Shift must be between 0 and 25.")
            return
    except:
        print("Please enter a number for the shift.")
        return

    # Call the cipher function
    final_result = caesar_cipher(text, shift, mode)

    print(f"\nHere is your {mode}ed message: {final_result}")


# Run the program
main()

