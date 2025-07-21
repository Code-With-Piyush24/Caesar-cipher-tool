# Caesar-cipher-tool
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
