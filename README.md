# cobra_crypt
# COBRA Crypt

COBRA Crypt is a Python-based file encryption tool paying homage to COBRA, the ruthless cartoon antagonists from *G.I. Joe*. It uses Fernet symmetric encryption and codename-style filename obfuscation to secure files—with a nostalgic 80s flair. Originally created as part of a systems programming course project, this utility combines serious cryptography with light-hearted theming.

---

## Features

- Symmetric encryption using the `cryptography` library (Fernet)
- Password-derived encryption key via SHA-256
- Cloaking via `.cobra_` prefix and randomized COBRA codename suffixes
- Decryption support to restore original content and filenames
- ASCII-art banner and themed command-line output
- Hidden "hail" easter egg for dramatic effect

---

## Requirements

- Python 3.6 or higher
- `cryptography` module

Install dependencies with:

```bash
pip install cryptography
```


## Usage

### Encrypt a directory
```bash
python cobra_crypt.py encrypt <directory_path>
```
### Decrypt a directory
```bash
python cobra_crypt.py decrypt <directory_path>
```
### Easter Egg
```bash
python cobra_crypt.py hail
```
## Password

You will be prompted for a password. Use the same password for encryption and decryption. If the password is incorrect during decryption, the process will fail gracefully.

### Example
```bash
$ python cobra_crypt.py encrypt ./intel
Enter COBRA clearance password: 
Files encrypted. Surveillance evaded. HAIL COBRA!

$ python cobra_crypt.py decrypt ./intel
Enter COBRA clearance password: 
Decryption complete. Operative safe. COBRA prevails.
```
## How It Works

   - Key Derivation: The password is hashed with SHA-256 and converted to a Fernet-compatible key.

   - Encryption: Files are encrypted with Fernet and overwritten in-place.

   - Filename Obfuscation: Original file names are replaced with .cobra_ plus a random codename.

   - Decryption: The tool scans for stealth files, decrypts them, and restores their original names.

## Acknowledgments

    This project was created as a course assignment in Operating Systems and Fundamentals.

    AI tools, including ChatGPT, were used for code structure planning, troubleshooting, and documentation support.

## Disclaimer

This project is a parody, made solely for educational and entertainment purposes.

All characters, codenames, and trademarks associated with G.I. Joe and COBRA are property of Hasbro and their respective rights holders. No affiliation or endorsement is implied.