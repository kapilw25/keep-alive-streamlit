# Keep Streamlit App Alive

This GitHub Action pings my Streamlit app daily to prevent it from going idle.

Streamlit App: [text2image-bykapil](https://text2image-bykapil.streamlit.app/)

## Features

- **Daily Ping**: Automatically pings the app every day at 2 AM PST (9 AM UTC)
- **GitHub Notifications**: GitHub automatically sends email notifications when workflows fail
- **Status Logging**: Maintains a history of ping results in `logs/ping_history.log`
- **Manual Trigger**: Can be triggered manually via GitHub Actions interface

## Email Notifications

GitHub will automatically send you email notifications when the workflow fails. To ensure you receive these:

1. Go to your GitHub account → Settings → Notifications
2. Under "Actions", make sure "Email" is checked for "Failed workflows only"
3. Verify your email address is confirmed in your GitHub account

No additional setup or secrets required!

## Logs

The workflow maintains a ping history log that tracks:
- Timestamp of each ping attempt
- Success/failure status
- Automatic commits to preserve the log history

## Alternative Email Options

If you want custom email notifications, you can:
- Use services like SendGrid, Mailgun, or AWS SES (with API keys)
- Set up a webhook to services like Discord, Slack, or Microsoft Teams
- Use GitHub Issues to create automatic issue reports on failures
