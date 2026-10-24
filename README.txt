POLYNEST V6 — Firebase Hosting + owner-only admin links

INCLUDED
- 5 branches: CSE, Electrical, Mechanical, Civil, Electronics
- Semesters 1st to 6th for every branch
- Separate YouTube Lectures and Google Drive Notes sections
- Google sign-in and owner-only Admin Panel
- Firestore rules: public can read links; only configured owner Gmail can add/update/delete records
- Responsive layout for mobile/tablet

OWNER GMAIL ALREADY SET: harshverma251309@gmail.com. You do not need to edit the owner Gmail. IMPORTANT: The package is not yet connected to your Firebase project. You must create a Firebase project, fill in firebase-config.json, enable Google sign-in, create Firestore, publish the rules, and deploy before the website is live.

SETUP (tablet-friendly)
1. Extract this ZIP into a folder. Keep index.html, firestore.rules, README.txt and firebase-config.json together.
2. Open https://console.firebase.google.com/ and create a project.
3. In Project settings > General > Your apps, add a Web app (</>) and copy its config values.
4. Open firebase-config.json and fill in apiKey, authDomain, projectId and appId using the values from your Firebase web app config. Do not leave PASTE_ placeholders. Keep this file in the same folder as index.html.
5. Owner Gmail is already set in index.html as harshverma251309@gmail.com.
6. Owner Gmail is already set in firestore.rules as harshverma251309@gmail.com.
7. Firebase Console > Authentication > Get started > Sign-in method > enable Google.
8. Firebase Console > Firestore Database > Create database. Then open Rules, paste the contents of firestore.rules (with your Gmail substituted), and Publish.
9. Deploy the folder to Firebase Hosting. The easiest robust tablet route is Firebase Studio/Cloud Shell if available; otherwise use a computer with Firebase CLI. Hosting needs index.html AND firebase-config.json at the deployed site's root. Never upload only index.html.
10. In Authentication settings, ensure your final web.app domain is listed under Authorized domains.
11. Open your https://PROJECT_ID.web.app site, sign in with the owner Gmail, open the hamburger menu > Admin Panel. Only the matching Gmail should see the link-add form.

ADDING LINKS
- Pick branch, semester, resource type and a title in Admin Panel.
- YouTube type: paste a public YouTube video or playlist URL.
- Notes type: paste a Google Drive/Docs URL. If the notes should be available to everyone, set sharing to Anyone with the link — Viewer. Never make private documents public accidentally.
- Press Add resource link. The entry should appear in the selected semester and remain saved in Firestore.

SECURITY / TROUBLESHOOTING
- Never share Firebase console passwords, OTPs, service-account keys, or sign-in codes.
- The Firebase web config is designed to be present in frontend apps; security comes from Firestore Rules, not hiding config.
- If login fails, check Google provider is enabled and the domain is authorized.
- If links do not load/save, check Firestore exists and the published rules have your exact owner Gmail.
- Do not test by opening index.html directly as a file. Test from the deployed HTTPS site or a local web server.
- Public read is enabled so students can view links. Only owner Gmail may create/update/delete resource documents.

LEGAL / OTHER
Privacy Policy, Terms, About and Contact are starter text and must be personalized before public launch. Ad placeholder is not connected to AdSense; earnings are not guaranteed.
