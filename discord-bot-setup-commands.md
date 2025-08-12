# Discord Bot API Key Setup Commands

## 1. Get Your Discord Bot Token
1. Go to Discord Developer Portal: https://discord.com/developers/applications/1404851076649320471
2. Navigate to "Bot" section
3. Click "Reset Token" (if needed) or copy existing token
4. **IMPORTANT**: Copy the token immediately - you won't see it again!

## 2. Add Token to 1Password Using Standardized Script

```bash
# Use our standardized API key creation script
~/.claude/scripts/add-api-key.sh DISCORD DISCORD_BOT_TOKEN "your-bot-token-here" \
    "API/Communication" "discord.com" "DiscoBot Discord API token" \
    "https://discord.com/developers/docs/intro" \
    "https://discord.com/developers/applications/1404851076649320471/bot" \
    "Communication"
```

## 3. Example with Placeholder Token
```bash
# DRY RUN TEST (safe to run):
~/.claude/scripts/add-api-key.sh --dry-run DISCORD DISCORD_BOT_TOKEN "MTA0NDg1MTA3NjY0OTMyMDQ3MQ.example.token" \
    "API/Communication" "discord.com" "DiscoBot Discord API token" \
    "https://discord.com/developers/docs/intro" \
    "https://discord.com/developers/applications/1404851076649320471/bot" \
    "Communication"
```

## 4. Verify Storage
```bash
# Check the token was stored correctly
op item get "DISCORD_API_KEY" --vault="Private"

# Get just the token for use
op read "op://Private/DISCORD_API_KEY/credential"

# Get environment variable name
op read "op://Private/DISCORD_API_KEY/username"
```

## 5. Using the Token in Code
```bash
# Export as environment variable
export DISCORD_BOT_TOKEN=$(op read "op://Private/DISCORD_API_KEY/credential")

# Or in Python/Node.js
import os
token = os.getenv('DISCORD_BOT_TOKEN')
```

## Bot Information for Reference:
- **Application ID**: 1404851076649320471
- **Client ID**: 1404851076649320471  
- **Bot Name**: DiscoBot
- **Purpose**: Testing API workflow / Learning

## Next Steps After Token Setup:
1. Host Terms of Service and Privacy Policy pages
2. Update Discord app with legal page URLs
3. Complete app verification
4. Test bot functionality

**SECURITY**: Never commit bot tokens to git repositories or share them publicly!