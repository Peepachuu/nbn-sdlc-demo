A few "secrets" were used for setting up the deployment and CI pipeline for this repository. They are:

1. FIREBASE_SERVICE_ACCOUNT_KEY_BASE64
2. NEXT_PUBLIC_FIREBASE_PROJECT_ID
3. NEXT_PUBLIC_FIREBASE_API_KEY
4. NEXT_PUBLIC_FIREBASE_AUTH_DOMAIN
5. NEXT_PUBLIC_FIREBASE_MESSAGING_SENDER_ID
6. NEXT_PUBLIC_FIREBASE_APP_ID
7. VERCEL_AUTOMATION_BYPASS_SECRET

Secrets 1-6 were generated from the firebase project, with one being done manually through the service accounts section. Secret 1 was originally downloaded as a json file which was then encoded in base64. Secret 7 was generated in the Vercel website in the "Deployment Protection" tab.