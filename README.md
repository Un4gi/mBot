# mBot (A Go-Based Synack Mission Bot)

This mission bot contains functionality for onboarding, claiming missions, Discord notifications, and auto-relogin.

## Discord Setup Instructions

To get your Discord bot token, you will need to follow the steps at <https://www.writebots.com/discord-bot-token/>.

Once you have your Discord bot token, add the `CHANNEL_ID` and `DISCORD_TOKEN` to `config.json`.

## Authy Configuration

To get your Authy Secret, you will need to follow the instructions at <https://github.com/alexzorin/authy>.

Once you have your secret, add the `AUTHY_SECRET` to `config.json` along with your `EMAIL_ADDRESS`, and `PASSWORD` for Synack.

## Build Instructions

You can build mBot straight from the source directory:

```bash
go build .
```

## Usage

Example:

```bash
mBot -t auth_token_here -d 30
```

For help, use the `-h` flag:

```bash
mBot -h
```

| Flag | Description | Example |
|------|-------------|---------|
| `-d` | Specifies a delay between polls (to please Synack) | `mBot -d 30` |
| `-t` | Passes your Authorization: Bearer token to the bot (this is necessary) | `mBot -t auth_token_here` |