# SMM-Cross-Poster
YouTube, Telegram, Discord, VK Cross poster


## Scheduled posting videos from YouTube account to WordPress.
Now including future/postponed videos that uploaded and not published.

* Create `.env`:

```
# Google Data Api
CLIENT_SECRETS_FILE=client_secrets.json

# Wordpress config
WP_REST_URI="https://example/wp-json/"
WP_USERNAME="wordpress"
WP_APP_PASSWORD="abcd abcd abcd abcd abcd abcd"

# Post params
POST_DELAY=1 # days
POST_CATEGORY=1 # From Wordpress
MODE=0 # 0 - Future, 1 - Now, 2 - at date
PUBLISH_HOUR=24
PUBLISH_MIN=0

#--- Discord ---
DISCORD_TOKEN="" # developers
DISCORD_ID=""
LOGO_URL=""
AUTHOR_NAME=""
AUTHOR_NAME_RU=""
ADS=""

#--- Telegram ---
TELEGRAM_BOT_TOKEN="" # Bot Father
TELEGRAM_CHAT_ID= # https://t.me/chatid_echo_bot or https://api.telegram.org/bot{TOKEN}/getUpdates

```

* Get client_secret from google console https://console.cloud.google.com/apis/credentials? OAUTH 2

```
dotnet ef migrations add IsPublishedBool

dotnet ef database update    
```

Scaffold PgSQL:
```bash
dotnet ef dbcontext scaffold "Host=my_host;Database=my_db;Username=my_user;Password=my_pw" Npgsql.EntityFrameworkCore.PostgreSQL
```
