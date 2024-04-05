## CLOUDBOX # Image Manager Project 


## Overview
The Image Manager is a Flask-based web application designed to securely manage and share images. It utilizes Google Cloud Storage for image storage and Google OAuth 2.0 for authentication, ensuring that each user's images are private and securely accessible.

## Features
- User authentication via Google OAuth 2.0.
- Secure image upload to Google Cloud Storage.
- User-specific image management - upload, view, and delete functionalities.
- Secure sharing and download of images with time-limited URLs.
## Screen shots
SIGNUP PAGE:
![Signup page](https://github.com/prem465/ImageManager-Project/assets/63437492/383dd10f-d370-4590-935f-97f4643031ca)
APPLICATION PAGE:
![application page](https://github.com/prem465/ImageManager-Project/assets/63437492/d753aad6-c104-4899-8b4d-190fb3bd0ac4)
UPLOADED IMAGES PAGE:
![Uploaded images page](https://github.com/prem465/ImageManager-Project/assets/63437492/653cfe9a-8898-4ebc-b21f-5625e7b806a9)





## Prerequisites
Before you begin, ensure you have the following:
- Python 3.6 or later.
- A Google Cloud Platform account.
- A Google Cloud Storage bucket.
- OAuth 2.0 credentials for your application.

## Setup Instructions

### Google Cloud Setup
1. Create a new project in the [Google Cloud Console](https://console.cloud.google.com/).
2. Enable the Google Cloud Storage and Google+ API.
3. Create a storage bucket in Google Cloud Storage.
4. Navigate to `IAM & Admin > Service Accounts` in the Google Cloud Console and create a new service account with access to the storage bucket.
5. Generate and download a JSON key file for this service account.

### OAuth 2.0 Configuration
1. Go to the [Google Developer Console](https://console.developers.google.com/).
2. Create credentials for an OAuth 2.0 client ID. Configure the consent screen as required.
3. Add authorized redirect URIs that match the URLs you'll use in your application.

### Application Configuration
1. Clone the repository to your local machine.
2. Install the required dependencies by running `pip install -r requirements.txt`.
3. Set environment variables for your application:
   - `GOOGLE_APPLICATION_CREDENTIALS`: Path to the service account JSON key file.
   - `OAUTH_CLIENT_ID`: Your Google OAuth client ID.
   - `OAUTH_CLIENT_SECRET`: Your Google OAuth client secret.
   - Ensure these variables are set securely and are not hard-coded in your application.
4. Update `app.py` with your Google Cloud Storage bucket name.

### Running the Application
Run the application using the following command:
```sh
flask run

