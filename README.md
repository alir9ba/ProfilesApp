# Profiles Directory App (React Native + Express)

**Student Name:** [Alireza Bagheri]
**Student ID:** [210408910]

This project is a React Native mobile application that fetches a list of profiles from a local Express.js server. It features pagination, stack navigation, and a detailed profile view.

---

## 📂 Project Structure

* **ProfilesApp/** - The React Native frontend application.
* **ProfilesServer/** - The Express.js backend API (provided).

---

## 🚀 Setup Instructions

### Part 1: Starting the Backend Server
The app requires the server to be running first.

1.  Open a terminal and navigate to the server folder:
    ```bash
    cd ProfilesServer
    ```
2.  Install dependencies:
    ```bash
    npm install
    ```
3.  Start the server:
    ```bash
    node server.js
    ```
    > You should see: `Server running on http://localhost:3000`

### Part 2: Starting the React Native App

1.  Open a new terminal and navigate to the app folder:
    ```bash
    cd ProfilesApp
    ```
2.  Install dependencies:
    ```bash
    npm install
    ```
3.  **Crucial Configuration (.env):**
    * Find the `.env` file in the root of `ProfilesApp`.
    * Ensure the IP address matches your computer's local network IP.
    * Example format: `EXPO_PUBLIC_API_BASE_URL=http://192.168.1.XX:3000`
4.  Start the Expo server:
    ```bash
    npx expo start
    ```
5.  Scan the QR code with your phone (using Expo Go) or run on an emulator.

---

## ⚙️ Configuration & IP Address

**Important:** Because the server runs locally on a computer, the phone needs the computer's **Local IP Address** to connect. `localhost` will not work on the phone.

* **My Configured IP:** `[INSERT THE IP YOU USED, e.g., 192.168.1.105]`
* **Port:** `3000`

**How to find your IP:**
* **Windows:** Run `ipconfig` in terminal (look for IPv4 Address).
* **Mac:** Run `ipconfig getifaddr en0` in terminal.

---

## 📱 Features Implemented

* **Stack Navigation:** Setup between `ProfilesList` and `ProfileDetail` screens.
* **Networking (Axios):** Configured with a central API client and base URL from `.env`.
* **Pagination:** Automatically loads more profiles when scrolling to the bottom.
* **Dynamic Data:** Clicking a user fetches their specific details dynamically using their ID.
* **Error Handling:** Handles network failures, timeouts, and 404 errors gracefully.
* **Pull-to-Refresh:** Users can pull down on the list to reload data.

---

## ⚠️ Troubleshooting

If the app says **"Network Error"** or sticks on **"Loading..."**:
1.  Ensure both Phone and Computer are on the **Same WiFi network**.
2.  Check that the IP in `.env` is correct.
3.  Restart the Expo server (`CTRL+C` then `npx expo start --clear`).
