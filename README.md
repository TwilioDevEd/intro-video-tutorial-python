<a href="https://www.twilio.com">
  <img src="https://static0.twilio.com/marketing/bundles/marketing/img/logos/wordmark-red.svg" alt="Twilio" width="250" />
</a>

# Twilio Video JavaScript SDK Tutorial for Python

## About

This application uses the lightweight [Flask Framework](http://flask.pocoo.org/).
Once you set up the application, you will be able to create and join free two-person Video chat rooms.

You can read the [Video Tutorial](https://www.twilio.com/docs/video/tutorials/get-started-with-twilio-video-python-flask-server)
that walks through the process of building this application from the ground up, or follow the instructions below to
set up this application locally and start using it right away.

## Set Up

### Requirements

- [Python 3](https://wiki.python.org/moin/BeginnersGuide/Download) (version 3.6 or above)
- [pip](https://pip.pypa.io/en/stable/installation/) for installing dependencies
- A free Twilio account. Sign up for a [free account](https://www.twilio.com/try-twilio) or log into an [existing account](https://www.twilio.com/console).

### Twilio Account Settings

Before we begin, we need to collect all the config values we need to run the application.

| Config Value                                   | Description                                                                                                                                                                                                                                 |
| :--------------------------------------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `TWILIO_ACCOUNT_SID`                           | Your primary Twilio account identifier - find this [in the console here](https://www.twilio.com/console).                                                                                                                                   |
| `TWILIO_API_KEY_SID` / `TWILIO_API_KEY_SECRET` | Your REST API Key information needed to create an [Access Token](https://www.twilio.com/docs/iam/access-tokens) - create [an API key here](https://www.twilio.com/console/project/api-keys). The `API_KEY` value should be the key's `SID`. |

### Local development

1. First, clone this repository and `cd` into it.

   ```bash
   git clone https://github.com/TwilioDevEd/intro-video-tutorial-python.git
   cd intro-video-tutorial-python
   ```

2. Run `make install`. This command will create a Python virtual environment, load it, and install the Python dependencies.

   ```bash
   make install
   ```

3. Create a configuration file for your application by copying the `.env.example` file to a new file called `.env`. Then, edit the `.env` file to include your account and application details.

   ```bash
   cp .env.example .env
   ```

   See [Twilio Account Settings](#twilio-account-settings) to locate the necessary environment variables.

4. Run the application. It will run locally on port 5000.

   ```bash
   make serve
   ```

5. Navigate to [http://localhost:5000](http://localhost:5000).
   Enter the name of a video room you'd like to join and click "Join Room". You might be prompted to grant access to your camera and microphone.

   You can open a new browser tab, navigate to [http://localhost:5000](http://localhost:5000) again, and join the same
   room from the new tab. Now, you should see two videos in each window, one for each browser tab.

6. **Optional**: Install ngrok

   Expose your application to the wider internet using [ngrok](https://ngrok.com/download). This step will allow others to join
   the application that's running on your local computer.

   First, [download and install ngrok](https://ngrok.com/download). Then, run it with the following command:

   ```bash
   ngrok http 5000
   ```

   When ngrok starts up, it will assign a unique URL to your tunnel and label it as the "Forwarding" URL. You can send this URL to others so
   that they can test your application too.
