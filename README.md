# Microsoft-auto-sign-in
Automatically signs you in to a Microsoft account using your email address, password and 2 factor authentication if needed 

Requires a credential called "Microsoft Account" w/ your UiPath email/password
Requires a credential called "2FA Secret" with your 2FA secret key (see bellow)

# Obtaining a secret key (for 2 factor auth):

Download google's authenticator app on your phone

In your browser:
* https://mysignins.microsoft.com/security-info
* Sign in
* Click  "+ Add sign-in method"
* Choose "Authenticator app"
* Click  "I want to use a different authenticator app"
* On the "Scan the QR code" page - click "Can't scan image"
* Copy the "secret key" to clipboard
* Go back to displaying the QR Code

On your phone:
* Open the Google Authenticator App on your phone
* Add a new authentication method by scanning the QR code

In your browser:
* Click next
* Enter the auth code displayed in the Google Auth App (on your mobile)

In your browser:
* Go in Orchestrator in your Personal Workspace and create a new asset
* Name: 2FA Secret
* Type: Credential
* Username: secret
* Password: paste the secret key from your clipboard
* Save and close
* Create another asset asset:
* Name: Microsoft Account
* Type: Credential
* Username: Your UiPath email address
* Password: Your UiPath password
* Save and close
