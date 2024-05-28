## Events

- `onMessage` gets called with a parameter of type Message

## Types

### DiscordBot

Returned by `require "discord-bot"`.

**Properties:**
- `user`, User

### User

**Properties:**
- `id`, string
- `username`, string
- `bot`, bool
- `flags`, int
- `mfa_enabled`, ?bool, only present for own account (DiscordBot.user)
- `discriminator`, string, "0" for most accounts nowadays

### Channel

**Properties:**
- `id`, string
- `client`, DiscordBot

**Methods:**
- `sendTyping()`
- `sendMessage(content: string)`

### Message

**Properties:**
- `content`, string
- `author`, User
- `channel`, Channel
- `channel_id`, string
- `guild_id`, ?string, absent for DMs
- `id`, string
- `client`, DiscordBot
- `attachments`, table
- `components`, table
- `embeds`, table
- `flags`, int
- `mention_everyone`, bool
- `mention_roles`, table
- `mentions`, table
- `nonce`, string
- `pinned`, bool
- `timestamp`, string
- `tts`, bool
- `type`, int

**Methods:**
- `mentionsMe(): bool`
- `reply(content: string)`
- `delete()`