# Python quickstart for users.message.songify

## Objectives

* Learn how to use the `users.message.songify` method.
* Convert a Gmail message into song lyrics.

## Prerequisites

* Python 3.x
* Google API Client Library for Python
* A Google Cloud Project with the Gmail API enabled.
* OAuth 2.0 credentials (client ID and client secret)
* A Gmail account with some messages.

## Set up your environment

### Enable the Gmail API

To enable the Gmail API, use the Google Cloud Console:

1.  Go to the [Google Cloud Console](https://console.cloud.google.com/).
2.  Select your project or create a new one.
3.  In the navigation menu, go to **APIs & Services > Library**.
4.  Search for "Gmail API" and enable it.

### Configure the OAuth consent screen

To configure the OAuth consent screen:

1.  In the Google Cloud Console, go to **APIs & Services > OAuth consent screen**.
2.  Choose "External" for the User Type and click **CREATE**.
3.  Fill in the required fields (App name, User support email, Developer contact
    information).
4.  Add "https://www.googleapis.com/auth/gmail.modify" as an authorized scope.
5.  Add test users if your app is not yet published.
6.  Save your changes.

## Prepare the workspace

1.  Install the Google Client Library for Python:

    ```bash
    pip install --upgrade google-api-python-client google-auth-oauthlib
    ```

2.  Create a new Python file named `songify_message.py`.

## Set up the sample

Add the following code to `songify_message.py`. This code authenticates
with the Gmail API and calls the `users.message.songify` method.

```python
import os.path
import base64

from google.auth.transport.requests import Request
from google.oauth2.credentials import Credentials
from google_auth_oauthlib.flow import InstalledAppFlow
from googleapiclient.discovery import build
from googleapiclient.errors import HttpError

# If modifying these scopes, delete the file token.json.
SCOPES = ["https://www.googleapis.com/auth/gmail.modify"]

def main():
    """Shows basic usage of the Gmail API.
    Converts a message to song lyrics using the songify method.
    """
    creds = None
    # The file token.json stores the user's access and refresh tokens, and is
    # created automatically when the authorization flow completes for the first
    # time.
    if os.path.exists("token.json"):
        creds = Credentials.from_authorized_user_file("token.json", SCOPES)
    # If there are no (valid) credentials available, let the user log in.
    if not creds or not creds.valid:
        if creds and creds.expired and creds.refresh_token:
            creds.refresh(Request())
        else:
            flow = InstalledAppFlow.from_client_secrets_file(
                "credentials.json", SCOPES
            )
            creds = flow.run_local_server(port=0)
        # Save the credentials for the next run
        with open("token.json", "w") as token:
            token.write(creds.to_json())

    try:
        service = build("gmail", "v1", credentials=creds)

        # Replace 'me' with the user's email address or 'me' for the authenticated
        # user. Replace 'YOUR_MESSAGE_ID' with the actual message ID.
        # You can get a message ID by listing messages first.
        message_id = "YOUR_MESSAGE_ID" # TODO(Replace with a real message ID)

        # Call the new songify method
        songified_message = service.users().messages().songify(
            userId="me", id=message_id
        ).execute()

        print(f"Message songified. New snippet: {songified_message['snippet']}")

    except HttpError as error:
        print(f"An error occurred: {error}")

if __name__ == "__main__":
    main()
```
TODO(Test code sample)

## Run the sample

1.  Save the code as `songify_message.py`.
2.  Download your OAuth 2.0 client configuration as `credentials.json`
    and place it in the same directory as `songify_message.py`.
3.  Run the script from your terminal:

    ```bash
    python songify_message.py
    ```

4.  Follow the browser prompts to authorize your account.
5.  The script will print the snippet of the songified message.

