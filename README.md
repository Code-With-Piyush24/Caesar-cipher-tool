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

Decrypt the Text File
bash
Copy
Edit
python main.py decrypt output/encrypted.txt output/decrypted.txt --key 5
📄 Effect: Characters are shifted back by -5, restoring original text.

📌 Notes
Only .txt files are supported for encryption/decryption

Create two folders:

/input for source plaintext files

/output for encrypted/decrypted results

The key (shift value) must be an integer between 1 and 25

Non-alphabetic characters are preserved as-is or handled safely

Avoid spaces in file names for best results

Run with Python 3 and install any required packages using:

bash
Copy
Edit

