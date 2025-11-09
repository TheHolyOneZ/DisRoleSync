# DisRoleSync
DisRoleSync is a powerful Discord bot extension that enables seamless role synchronization between multiple Discord servers. With this feature, when a user receives a role in one server, they can automatically receive corresponding roles in linked servers, streamlining cross-server role management.
> 💡 **Built for the Zygnal Ecosystem — to download and use this extension, you must be part of the Zygnal Ecosystem.**  
> This extension (cog) is part of the **Zygnal Ecosystem** and is only available through its supported platforms.  
> You can use it with:  
> - The **[Discord Bot Framework](https://github.com/TheHolyOneZ/discord-bot-framework)** — ideal for developers who want full control and flexibility *(includes an integrated extension marketplace)*, or  
> - The **[ZygnalBot](https://zygnalbot.de)** — a prebuilt, plug-and-play Discord bot *(also includes an integrated extension marketplace)*.  
>
> Browse and install extensions at [zygnalbot.com/extension](https://zygnalbot.com/extension).  
> For help or community discussions, join us on Discord: [discord.gg/sgZnXca5ts](https://discord.gg/sgZnXca5ts)
# DisRoleSync Documentation

## Overview

DisRoleSync is a powerful Discord bot extension that enables seamless role synchronization between multiple Discord servers. With this feature, when a user receives a role in one server, they can automatically receive corresponding roles in linked servers, streamlining cross-server role management.

## Key Features

- **Server Linking**: Connect multiple Discord servers for role synchronization
- **Role Mapping**: Create one-way or two-way mappings between roles across servers
- **Approval System**: Optionally require admin approval for role sync requests
- **Auto-Sync**: Automatically sync roles when users join linked servers
- **Manual Sync**: Manually trigger role synchronization for specific users
- **Customizable Settings**: Configure sync behavior to suit your community's needs

## Commands

| Command | Description | Permission |
|---------|-------------|------------|
| `!disrolesync` | Display help information | Manage Roles |
| `!disrolesync servers` | Manage server links | Administrator |
| `!disrolesync roles [server_id]` | Manage role mappings | Administrator |
| `!disrolesync approvals` | Manage pending role sync approvals | Administrator |
| `!disrolesync serverrequests` | Manage pending server link requests | Administrator |
| `!disrolesync settings` | Configure sync settings | Administrator |
| `!disrolesync sync [user]` | Manually sync roles for a user | Manage Roles |

## Setup Guide

### 1. Link Servers

1. Use `!disrolesync servers` in your server
2. Click the "Link Server" button
3. Enter the ID of the server you want to link with
4. The bot must be present in both servers

### 2. Create Role Mappings

1. Use `!disrolesync roles` to select a linked server
2. Click "Add Mapping" to create new role mappings
3. Select source and target roles
4. Choose between one-way or two-way mapping

### 3. Configure Settings

Use `!disrolesync settings` to customize:
- Whether role syncs require approval
- Auto-sync behavior when users join
- Whether role removals should be synced
- Notification channel for sync events

## Role Sync Behavior

- **User Joins**: When a user joins a server, their roles from linked servers can be automatically synced (if enabled)
- **Role Added**: When a user receives a role in one server, they receive mapped roles in linked servers
- **Role Removed**: When a role is removed from a user, mapped roles can be automatically removed in linked servers (if enabled)

## Approval System

When approval is required:
1. Role sync requests are sent to the configured notification channel
2. Admins can review and approve/deny requests using `!disrolesync approvals`
3. Users receive their roles only after approval

## Security Considerations

- Only server administrators can link servers and create role mappings
- The approval system prevents unwanted role synchronization
- Server links can be removed at any time
- Role mappings can be one-way if you don't want bidirectional synchronization

## Use Cases

- **Community Networks**: Maintain consistent roles across multiple community servers
- **Event Servers**: Automatically grant access in temporary event servers based on roles in main server
- **Development/Testing**: Sync roles between production and testing environments
- **Partner Programs**: Easily manage roles across partner server networks

## Troubleshooting

- Ensure the bot has the "Manage Roles" permission in all linked servers
- The bot's role must be higher in the hierarchy than roles it needs to assign
- Check that servers are properly linked using `!disrolesync servers`
- Verify role mappings are set up correctly with `!disrolesync roles`

---

DisRoleSync simplifies cross-server role management, saving time and ensuring consistency across your Discord community network.
