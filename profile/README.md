<div align="center">
  <img
    src="https://github.com/user-attachments/assets/f30f9348-c22c-4f35-ba8b-30d5a27d7928"
    alt="logo_diamond"
    width="186"
    height="186"
  />

<h2>PaperTrailBot</h2>
<h4>This logo is drawn using MS Paint because I have never tried using a logo maker before</h4>
</div>

# Table of Contents

* [Overview](#overview)
* [Repositories](#repositories)
* [Using The Bot](#using-the-bot)

* [Help](#help)

# Overview

A free and open-source Discord bot that logs the changes made to a server and it's members and logs them to a dedicated
channel.

The following is a non-exhaustive list of events that the bot can log:

AutoMod Events, Onboarding Events,
Invites, Members, Roles, Channels, Threads, Stages, Events, Polls, Messages, Boosts, Emojis, Stickers, Soundboard,
Integrations, Webhooks, Moderation Action, Unusual DMs, Raids and Unknown events.

# Using The Bot

### By Inviting It

A deployed instance is the easiest way to use this bot. Just invite it to your server and that's all.

Get it from here: https://discord.com/discovery/applications/1381658412550590475

Make sure to read the [Privacy Policy](https://github.com/PaperTrailBot/.github/blob/main/PRIVACY_POLICY.md) and the [TOS](https://github.com/PaperTrailBot/.github/blob/main/TOS.md) before using it.

Run the `/help` slash command to see instructions on how to configure the bot for your server.

### By Self Hosting It

Read the deployment guide [here](https://github.com/PaperTrailBot/PaperTrailBot/blob/main/README.md)

# Help

If you face any problems during self-hosting or have a question that needs to be answered, please feel free to
open an issue in the Issues tab. I will try my best to respond as soon as I can.

I've considered putting the project in maintenance mode since I believe it's mostly feature complete.
I don't plan on introducing or changing anything major.
However, I will be regularly updating it to fix reported/detected issues, updating dependencies and log new events or
event keys if found, for as long as I can.

# No Support For Horizontal Scaling

I've considered designing for horizontal scaling before, but the issue is, the easiest way to do this is to place a HTTP proxy that will centrally handle global rate limits across scaled instances. This would also require disabling JDA's internal rate limitation and rely on the proxy instead. All of this will make self-hosting a bit more cumbersome, and unless your hosted bot actually as a very large userbase,
you will almost never need to scale horizontally.

The current implementation uses JDA's Shard Manager, so your bot won't be limited to a single shard (or 2500 guilds) only. The only limitation is that horizontal scaling isn't supported. But, if it is really required, I might consider adding support for it.
