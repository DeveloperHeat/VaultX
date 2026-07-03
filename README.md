# VaultX

**Your Advanced Personal Cyber Security Vault**

VaultX is a fully client-side, privacy-focused security vault designed for secure credential management and enhanced digital protection[cite: 1]. It empowers users to protect, manage, and understand their data without surrendering control to cloud-based services[cite: 1].

Here is the live link: https://developerheat.github.io/VaultX/

## Table of Contents
* [Features](#features)
* [Security Philosophy](#security-philosophy)
* [Technical Architecture](#technical-architecture)
* [Usage](#usage)

---

## Features

VaultX bridges the gap between high-level security and user accessibility:

* **Zero-Knowledge Client-Side Storage:** All cryptographic operations happen locally in your browser. No credentials, plaintext, or metadata are ever transmitted to or stored on external servers.
* **Themed Passphrase Generator:** Move beyond unmemorable random strings. Generate secure, high-entropy passphrases based on custom themes (e.g., animals, colors, or user-defined word lists).
* **Educational Security Analytics:** 
    * **Password Strength Meter:** Provides visual feedback and estimates time-to-crack using brute-force simulation to educate users on why specific passwords are weak or strong.
    * **AI-Powered Phishing Detection:** An integrated, client-side Deep Feed-Forward Neural Network (TensorFlow.js) that analyzes URLs for suspicious patterns and provides immediate risk assessments.
* **Intuitive Single-Page Interface:** Designed for ease of use by non-technical users, featuring a clean, responsive layout.

---

## Security Philosophy

VaultX is built on the **"privacy-by-design"** model, adhering to the principle of least privilege. 

* **No Cloud Dependency:** By eliminating server-side storage, VaultX mitigates the risks of large-scale data breaches common in centralized password managers[cite: 1].
* **Transparency:** The application is transparent about how data is handled, ensuring users retain full autonomy over their digital credentials[cite: 1].

---

## Technical Architecture

VaultX utilizes industry-standard cryptographic practices to ensure data integrity and confidentiality:

* **Key Derivation:** Employs **PBKDF2** (Password-Based Key Derivation Function 2) with a randomly generated 16-byte salt and 100,000 iterations to derive a strong encryption key from the user's master password.
* **Encryption:** Uses **AES-GCM** (Advanced Encryption Standard in Galois/Counter Mode) to provide authenticated encryption.
* **Data Handling:** All encrypted payloads, along with their unique initialization vectors (IVs) and salts, are stored in browser `localStorage` as serialized JSON. All decrypted data is discarded when the vault is locked or the browser tab is closed.

---

## Usage

1. **Initialize:** On your first visit, set up your Master Password.
2. **Manage:** Add, edit, or delete credentials via the dashboard. Changes trigger immediate re-encryption of the dataset.
3. **Generate:** Use the "Passphrase Generator" tab to create memorable, high-entropy passwords.
4. **Protect:** Use the "Tools" section to analyze URLs for phishing risks before visiting them.
5. **Backup/Restore:** Use the Export/Import feature to safely back up your vault as an encrypted file.

> **Important:** Your Master Password is the only way to access your encrypted vault. It is not stored anywhere. **If you forget it, your vault data will be permanently lost.**
