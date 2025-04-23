# Secure-one-on-one-chat-app
A secure one-to-one chat app with Firebase login, two-way code verification, and Kyber-based encryption. Ensures only verified users can chat. Messages are end-to-end encrypted, stored, and retrieved securely, mimicking post-quantum encryption for high-level security.
🔐 Secure One-to-One Chat App with Firebase & Kyber-Based Encryption
A secure real-time one-to-one chat web app built using HTML, JavaScript, and Firebase. This app includes Firebase Authentication, a custom two-way user verification system, and client-side post-quantum encryption using a simplified Kyber-based algorithm.

🚀 Features
🔑 User Registration & Login using Firebase Authentication (email/password)

🔄 Two-Way Verification using shared email and phone number with random code confirmation

💬 One-to-One Chat between authenticated users

🕰️ Message History Retrieval from Firebase Realtime Database

🔐 Kyber-Inspired Encryption & Decryption on the client side

🧹 Clear Chat (Local Only) for user privacy

📌 Project Flow
Registration/Login:

Users register or log in using Firebase email-password auth.

User’s phone number is stored on registration for later verification.

Two-Way Verification:

Sender enters receiver’s email and phone number.

A 3-digit random code is generated.

Both users must select the same number from the random set to confirm session identity.

Key Exchange:

Simplified key exchange mimics Kyber algorithm.

Each user generates a public-private key pair.

Public keys are exchanged and used to derive a shared secret key.

Encryption & Decryption:

Messages are encrypted using the derived shared key.

Encrypted messages are sent to Firebase.

Receiver decrypts using the same shared key.

Chat Storage & Retrieval:

Messages are stored in Firebase Realtime Database under a unique chat room ID.

On page load, all past messages are fetched and decrypted locally.

🔒 Encryption Algorithm (Simplified Kyber Style)
Each user generates a random private key (a large number).

Public key = private key × base value mod prime number.

Shared key is derived from combining sender's private key and receiver's public key.

AES-style XOR encryption is applied using the shared key for messages.

🛠️ Tech Stack
Frontend: HTML, CSS, JavaScript

Backend: Firebase Authentication, Firebase Realtime Database

Encryption: Custom lightweight Kyber-style algorithm (client-side)
