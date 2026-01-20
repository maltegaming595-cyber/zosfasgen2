# Secure File Download Portal

A Streamlit web application that serves as a secure file download portal with Discord authentication and Google Drive integration.

## Features

- Discord OAuth2 authentication
- Role-based access control
- Google Drive integration for file storage
- Secure file download functionality

## Local Setup

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/your-repo-name.git
   cd your-repo-name
   ```

2. Create a virtual environment:
   ```bash
   python -m venv venv
   venv\Scripts\activate  # On Windows
   source venv/bin/activate  # On macOS/Linux
   ```

3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

4. Create a `.streamlit/secrets.toml` file with your credentials:
   ```toml
   DISCORD_CLIENT_ID = "your_client_id"
   DISCORD_CLIENT_SECRET = "your_client_secret"
   DISCORD_REDIRECT_URI = "your_redirect_uri"
   GOOGLE_SERVICE_ACCOUNT_JSON_PATH = "path_to_service_account.json"
   ALLOWED_GUILD_ID = "your_guild_id"
   ALLOWED_ROLE_IDS = '["role_id1", "role_id2"]'
   ```

5. Run the app:
   ```bash
   streamlit run app.py
   ```

## Deployment to Streamlit Cloud

1. Push your code to GitHub (without sensitive data)
2. Go to [streamlit.io/cloud](https://streamlit.io/cloud)
3. Click "New app" and select your repository
4. Configure secrets in the app settings
5. Deploy!

## Environment Variables

- `DISCORD_CLIENT_ID`: Your Discord application's client ID
- `DISCORD_CLIENT_SECRET`: Your Discord application's client secret
- `DISCORD_REDIRECT_URI`: OAuth2 redirect URI
- `GOOGLE_SERVICE_ACCOUNT_JSON_PATH`: Path to Google service account JSON
- `ALLOWED_GUILD_ID`: Your Discord guild ID
- `ALLOWED_ROLE_IDS`: JSON array of allowed Discord role IDs

## Security Notes

- Never commit `.env` or `.streamlit/secrets.toml` files
- Always use environment variables for sensitive data
- Use Streamlit Cloud's Secrets Management for production
