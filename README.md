
# Password Manager

A simple command-line-based **Password Manager** built in Python using **cryptography** for encryption. This app allows you to securely store and manage your passwords for different accounts.

## Features

- **Secure encryption**: Passwords are encrypted using the Fernet symmetric encryption method.
- **Password management**: Add new passwords and view existing ones.
- **Automatic file generation**: The app automatically generates a key file (`key.key`) and a password file (`passwords.txt`) on the first run.
- **Simple to use**: Command-line interface that allows easy management of passwords.

## Installation

1. **Clone the repository**:
   ```bash
   git clone https://github.com/aaronpaddy/password-manager.git
   cd password-manager
   ```

2. **Install dependencies**:
   You need to install the `cryptography` package if it’s not installed already. You can do this using `pip`:
   ```bash
   pip install cryptography
   ```

3. **Run the application**:
   Once inside the project directory, you can run the app with Python:
   ```bash
   python password_manager.py
   ```

## Usage

### Add a New Password
- When prompted, select the `add` option to add a new password.
- Enter the account name and the corresponding password when asked.
- The password is encrypted and stored securely in the `passwords.txt` file.

### View Existing Passwords
- Select the `view` option to view the stored account passwords.
- The stored passwords will be decrypted and displayed along with the account name.

### Quit the Application
- Type `q` to quit the password manager.

## Folder Structure

When the program is run for the first time, two files will be created inside a `Password_Manager` folder:
- `key.key`: Stores the encryption key used to encrypt and decrypt the passwords.
- `passwords.txt`: Stores the encrypted passwords.

## Example

### Adding a Password:
```
Would you like to add a new password or view existing ones (view, add), press q to quit? add
Account Name: Gmail
Password: mysecurepassword123
```

### Viewing Passwords:
```
Would you like to add a new password or view existing ones (view, add), press q to quit? view
User: Gmail | Password: mysecurepassword123
```

## Security Note

- The `key.key` file is used to encrypt and decrypt your passwords. **Do not share this file**, as anyone with access to it can decrypt your passwords.
- You should also avoid sharing the `passwords.txt` file, as it contains your encrypted passwords.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for more information.
