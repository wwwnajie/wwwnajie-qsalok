wwwnajie – Qsalok / قسەلۆک

1. Firebase Console > Firestore Database > Rules: paste firestore.rules and Publish after testing in Rules Playground/Emulator. This replaces the previous users-only rules.
2. Firebase Authentication > Settings > Authorized domains: add the exact HTTPS domain where you host index.html. Firebase phone auth on web requires an authorized domain and reCAPTCHA.
3. Host index.html over HTTPS (e.g. Firebase Hosting). Opening file:// is not supported for phone authentication.
4. To test without billed SMS, configure fictional test phone numbers and codes in Firebase Authentication > Sign-in method > Phone.
5. Open the hosted app in two browsers with two distinct test accounts. Both must log in before they appear in the user list.
6. This is a prototype. Before production: test Firestore rules, restrict public user-directory exposure, add blocking/reporting, abuse controls, message pagination, notification support, and end-to-end encryption if private messaging is promised.
7. Android/iOS native packages are NOT included. The web version can be opened on both platforms.

Note: The public Firebase web API key is embedded in the client by design. Never embed service account private keys.
