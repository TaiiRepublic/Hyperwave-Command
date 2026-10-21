Hyperwave Command Center
Version 0.2.0-alpha · by TaiiRepublic · free for every streamer
Hyperwave Command Center is a complete streamer suite in one small Windows app. It's built to replace StreamElements-style tools, but it's simpler, it runs on your own PC, and it works across Twitch, Kick, YouTube and TikTok at the same time.
	What you get
⚡ Alerts	Follows, subs, gifts, bits and Kicks, raids and hosts, tips, Super Chats, channel points, and TikTok gifts, shares and likes, all designed on one page
▣ Overlays	A drag-and-drop Overlay Studio with 15 widgets: chat, goals, event lists, countdowns, credits, emote wall and more
✦ Chatbot	Custom commands, timers, thank-you messages, built-in commands
🎲 Chat modules	Hyperspace Gamble, Salvage Run, Ion Duel, Supply Drop and the Launch Alert, all renamable
◆ Loyalty points	Name them whatever you like (e.g. -RUs-) and viewers earn them on every platform
⛨ Moderation	Link, caps, symbol, word and length filters
♫ Music, deck & DJ	Everything from Hyperwave Station: song requests, Remote DJ, Hyperwave Deck, Elgato Stream Deck, the chat and Now Playing designers
Everything is set up from a dashboard in your browser, in the Hyperwave look (plates, crimson, amber and cyan, Chakra Petch). Nothing is sent to a cloud. There's no account to make.
> **Alpha build.** This is the first build. It's for testing: expect rough edges, and please send feedback from **Settings → About → Send feedback**.
---
Contents
What's in the download
Install and first launch
Quick start: your first alert in OBS in 5 minutes
The Command Center (home page)
Connections: Twitch, Kick, YouTube, TikTok, tips, OBS
Alerts
Overlays and the Overlay Studio
Widget reference
Chatbot
Chat modules: point games and the Launch Alert
Loyalty points
Moderation
Music, deck and DJ (the Hyperwave Station tools)
Coming from Hyperwave Station
Firing alerts from other apps
Where your settings live, and backups
Ports and safety
Troubleshooting
Version numbers and updates
Building from source
Roadmap
Credits and licences
---
1. What's in the download
```
HyperwaveCommand/
├── HyperwaveCommand.exe      ← the app (double-click to start)
├── HyperwaveCommandUpdater.exe ← installs or updates the app from GitHub
├── README.md                 ← this guide
├── CHANGELOG.md              ← what changed in every version
├── docs/
│   └── Music-Deck-DJ-Guide.md   ← full guide to the music, deck and DJ tools
├── web/
│   └── about.json            ← edit to change the About box (your links, tip page)
├── streamerbot/
│   └── Hyperwave-Spotify.cs  ← optional Streamer.bot song-request action
├── branding/                 ← app icon (SVG, PNG, ICO)
├── licenses/                 ← font and library licences
└── source/                   ← the full source code, with build.bat
```
The web folder is optional. Any page you put in it overrides the built-in copy, the same way it worked in Station.
---
2. Install and first launch
You need: Windows 10 or 11, and OBS Studio 28 or newer.
For YouTube you also need Streamer.bot (free).
For TikTok you also need TikFinity (free).
Easiest: download HyperwaveCommandUpdater.exe from https://github.com/TaiiRepublic/Hyperwave-Command/releases/latest and double-click it.
It suggests `C:\HyperwaveCommand\`. Press Enter, or type another folder.
It downloads the newest version and checks its SHA-256 fingerprint.
It installs it, adds a Hyperwave Command Center shortcut to your desktop, and starts it.
If Windows says "Windows protected your PC", click More info → Run anyway.
The same updater updates any older version and keeps your settings.
By hand:
Make a folder: `C:\HyperwaveCommand\`
Copy `HyperwaveCommand.exe` (and the `web` folder, if you want your own About links) into it.
Double-click HyperwaveCommand.exe.
Windows may say "Windows protected your PC". The app isn't code-signed yet, so click More info → Run anyway. The full source code is in the `source` folder if you want to check it.
A console window opens with the Hyperwave Command Center banner, and your browser opens the dashboard at http://127.0.0.1:7580.
Keep the console window open while you stream. Closing it quits the app.
> **Start with Windows:** press `Win + R`, type `shell:startup`, press Enter, and drop a shortcut to `HyperwaveCommand.exe` into that folder.
---
3. Quick start: your first alert in OBS in 5 minutes
Dashboard → Connections → Twitch → step 1: type your Twitch channel name (e.g. `taiirepublic`) and click Save. Chat now flows into Command.
Dashboard → Command Center → Your OBS links: click Copy next to Main HUD.
In OBS: Sources → + → Browser, and set:
Field	Value
Name	`Hyperwave Main HUD`
Local file	unticked
URL	the link you copied, e.g. `http://127.0.0.1:7580/o/main1a2b`
Width	`1920`
Height	`1080`
Control audio via OBS	ticked (so alert sounds go to stream)
Refresh browser when scene becomes active	unticked
Click OK.
Dashboard → Command Center → Test an alert: click ★ Follow. The alert plays in OBS.
To get real alerts, finish the Twitch sign-in on Connections (section 5).
---
4. The Command Center (home page)
Status tiles show Twitch, Kick, YouTube, TikTok, OBS and Streamer.bot. Green means connected, amber means partly working, red means a problem, and grey means not set up. Click a tile to go to its setup.
Session counters count followers, subs, gifted subs, bits and Kicks, tips (including Super Chats), raids, TikTok diamonds and likes. A new session starts:
when you go live on Twitch,
when Command starts after 8 quiet hours,
or when you press New session.
Live activity lists every event from every platform, newest first, with the platform tag. ↻ replays that alert. Replays aren't counted twice.
Pause alerts holds alerts in a queue, and Resume plays them in order. Skip alert ends the alert on screen now.
Test an alert sends a pretend event to every overlay. You can pick the platform and amount. Tests are never counted in stats or credits.
Scene controls: Restart countdowns resets every Countdown widget, and Roll the credits restarts every End credits widget.
---
5. Connections
All of this is on Dashboard → Connections, with the same steps shown on the page. Click Save after changing anything.
Twitch: chat, alerts, chatbot, mod tools
Step 1. Channel. Type your Twitch channel name. Chat is read with no sign-in.
Step 2. Make your own free Twitch app (once). Open dev.twitch.tv/console/apps/create and fill in:
Field	Value
Name	`Hyperwave Command YOURNAME` (Twitch names must be unique)
OAuth Redirect URLs	`http://localhost` → click Add
Category	`Application Integration`
Client Type	`Public`
Click Create. Then click Manage, copy the Client ID, paste it into Client ID on the Connections page, and click Save.
Already made one for Hyperwave Station? Reuse the same Client ID.
Step 3. Sign in. Click Sign in to Twitch. A short code appears.
Open the twitch.tv/activate link shown.
Type the code.
Click Authorize.
The page updates by itself. One sign-in covers alerts, chatbot replies, clips, category changes and mod tools. It asks for these Twitch permissions:
`clips:edit` `user:write:chat` `channel:manage:broadcast` `moderator:read:followers` `channel:read:subscriptions` `bits:read` `channel:read:redemptions` `moderator:manage:banned_users` `moderator:manage:chat_messages`
Step 4. Alerts from Twitch. Leave Follows, subs, resubs, gift subs, bits, raids and channel point redeems ticked. Under the box you'll see ✓ Listening for: with every event Twitch accepted.
Kick: chat, subs, gifts, hosts, follows, Kicks
Step 1. Channel. Type your Kick channel name (e.g. `taiirepublic`). Command looks up your chatroom and channel IDs by itself.
If Kick blocks the lookup, open `https://kick.com/api/v2/channels/YOURNAME` in your browser.
Copy `"id"` into Channel ID and `"chatroom" → "id"` into Chatroom ID.
Leave Alerts from Kick ticked.
Step 2 (optional). Post in Kick chat and time out spammers. Without this step the bot can still post on Kick through Streamer.bot. Open kick.com/settings/developer → Create new:
Field	Value
Application name	`Hyperwave Command Center`
Redirect URL	`http://localhost:7580/kick/callback`
Scopes	`user:read`, `channel:read`, `channel:write`, `chat:write`, `moderation:ban`
Copy the Client ID and Client Secret into Command, click Save, then click Sign in to Kick and approve.
YouTube: chat, members, Super Chats, new subscribers
YouTube only lets approved apps read live chat, so Command uses Streamer.bot's YouTube connection.
In Streamer.bot:
Platforms → YouTube: sign in with your YouTube account.
Servers/Clients → WebSocket Server:
Field	Value
Address	`127.0.0.1`
Port	`8080`
Auto Start	ticked
Authentication	ticked (recommended) with a password you choose
Click Start Server.
In Command (Connections → YouTube):
Tick Connect to Streamer.bot.
Fill in Address `127.0.0.1`, Port `8080`, and the password if you set one.
Tick YouTube chat and YouTube alerts, then click Save.
YouTube chat events only arrive while you have a live broadcast running.
TikTok: chat, gifts, follows, shares, likes
Install TikFinity from tikfinity.zerody.one, sign in, and connect it to your LIVE. Leave it open while you stream.
Connections → TikTok: tick Connect to TikFinity and TikTok alerts. Leave the port at `21213` unless you changed it in TikFinity. Click Save.
How TikTok events behave:
A gift sent as a streak alerts once when the streak ends, showing the total (e.g. "5× Rose").
Likes are added up per viewer and sent every 20 seconds. They're off in Alerts by default.
TikTok doesn't allow apps to post in LIVE chat, so the chatbot only listens there.
Tips
Command shows tip alerts but doesn't take payments. Taking money needs a company to handle cards, refunds and chargebacks. Keep your tip page (StreamElements, Ko-fi and so on).
In Streamer.bot, open Integrations and connect your tip site: StreamElements, Streamlabs, Ko-fi, TipeeeStream or Fourthwall.
In Command, tick Tip alerts through Streamer.bot and click Save. This needs the Streamer.bot connection above.
For anything else (PayPal, your own website), see section 15.
OBS
In OBS: Tools → WebSocket Server Settings → tick Enable WebSocket server, set Server Port `4455`, then click Show Connect Info and copy the Server Password.
In Command: tick Connect to OBS, set Address `127.0.0.1`, Port `4455`, paste the password, and click Save.
Chat replies
Post Twitch messages through:
Automatic: your Twitch sign-in, or Streamer.bot if you're not signed in.
My Twitch sign-in
Streamer.bot
Kick replies use your Kick sign-in if you have one, otherwise Streamer.bot. YouTube replies always go through Streamer.bot.
---
6. Alerts
Dashboard → Alerts. Pick an alert on the left; its switch turns it on or off. Everything for that alert is on one page, under the preview:
▶ Preview plays the alert with its sound and animation.
Send a test to OBS saves your changes and plays the alert on stream.
Save alerts updates every OBS source at once, with no refresh needed.
Kind	Comes from
Follow	Twitch, Kick, TikTok, YouTube (new subscriber)
Subscription	Twitch (incl. resubs), Kick, YouTube (new member), TikTok
Gift subs	Twitch, Kick, YouTube (gifted memberships)
Bits / Kicks	Twitch bits, Kick Kicks
Raid / host	Twitch raids, Kick hosts
Tip	StreamElements, Streamlabs, Ko-fi, Tipeee, Fourthwall, your own links
Super Chat	YouTube Super Chats and Super Stickers
Channel points	Twitch channel point redeems, Kick rewards
TikTok gift	TikTok gifts (once per streak)
Share	TikTok shares (off by default)
Likes	TikTok likes, added up every 20 s (off by default)
Your own pictures, animations and sounds (the quick way)
Pick the alert on the left (for example Raid / host).
Drag your files onto the preview. Pictures, GIFs and videos become the alert's picture, and sound files become its sound. You can drop several at once.
Or click ⬆ Upload pictures or videos / ⬆ Upload sounds.
Or click From my library to reuse something you uploaded before. Click a file to add it, click again to remove it.
Click ▶ Preview, then Save alerts.
File	Works as
PNG, JPG, WebP	still picture (up to 8 MB)
GIF	animated picture (up to 8 MB)
WebM	animation or video with transparency, like the rotating Taii logo (up to 40 MB)
MP4	video without transparency (up to 40 MB)
MP3, WAV, OGG, M4A, FLAC	sound (up to 15 MB)
Several pictures or sounds on one alert play one at random each time. That's great for a set of raid GIFs or a pack of follow sounds.
Your own sound replaces the built-in one when you upload it. To mix them, click built-in sounds back on.
Built-in sounds (Chime, Hyperspace warp, Console blip, Fanfare, Fleet alarm, Coin) are made by the app, so there are no files to keep. Click one to hear it and pick it.
✕ on a picture or sound removes it from the alert. The file stays in your library.
The sections
🖼 Picture or animation
your pictures (a thumbnail each)
When I have no picture: show the viewer's profile picture, always show the profile picture, or show no picture at all
Picture motion: Still, Float, Pulse, Bounce, Swing, Spin, Shake or Jelly wobble
Picture height
🔊 Sound
built-in sounds and your sounds
Volume
Start the sound after (0–5 s), to line a sound up with your animation
✎ Words
main line, second line and small heading
Click a fill-in to put it where your cursor is
| Fill-in | Becomes |
|---|---|
| `{name}` | the viewer's name |
| `{amount}` | bits, viewers, gift count, likes, diamonds |
| `{money}` | the tip with its currency, e.g. `$5`, `€3`, `£2.50` |
| `{months}` | months subscribed |
| `{tier}` | Tier 1/2/3, Prime, or the YouTube membership level |
| `{item}` | reward or gift name |
| `{count}` | how many of a TikTok gift |
| `{platform}` | Twitch, Kick, YouTube, TikTok… |
| `{message}` | what the viewer wrote |
Fill-ins in the main line glow in the accent colour.
◐ Look
Layout: Fleet console panel, Picture beside text, Picture above text, Text over picture, or Slim banner.
Font: 16 to choose from.
Text size, whole-alert size, and text, accent and panel colours.
Copy this look to every alert gives all the other alerts the same layout, font, sizes, colours and motion. Their accent colours, words, pictures and sounds stay as they are.
➤ Motion
Comes in: Fade, Drop down, Rise up, Slide from right or left, Zoom, Bounce, Hyperspace warp, Flip, Spin, Glitch or Heavy drop.
Goes out: Fade, Fly up, Drop away, Slide left or right, Zoom out, Hyperspace jump, Spin away or Glitch out.
Name animation: Wave, Pulse, Glow, Shake or Rainbow.
Animation speed and On screen for (seconds).
⚙ When it shows: only when the amount is at least a number, and only from certain platforms.
Apply a look to every alert (top of the page) gives every alert a theme in one click: Fleet console, Hyperspace jump, Big picture, Slim banner or Arcade. Words, pictures and sounds stay as they are.
Variations: a different alert for big moments
Click + Variation in the Editing bar under the preview. It starts as a full copy of the alert.
Set Plays when: Amount is at least, Months are at least, Platform is, or Tier is, and a Value (e.g. `1000` bits, `6` months, `kick`, `3`).
Change anything you like (picture, sound, words, look) with the same controls. The preview uses an amount that matches the rule.
Click Main design or a variation in the Editing bar to switch between them. When several variations match, the biggest "at least" wins.
Starter variations come included: Resub (2+ months), Big raid (25+ pilots, fleet alarm) and 1,000 bits (fanfare and rainbow).
For every alert: the pause between alerts, and words that hide a viewer's message (the alert still plays).
Alerts only in OBS: if you'd rather not use an overlay, add `http://127.0.0.1:7580/alerts` as a 1920 × 1080 Browser source.
---
7. Overlays and the Overlay Studio
Dashboard → Overlays & widgets. Each overlay is one Browser source in OBS. Copy its link and add it the same way as in the quick start.
Two overlays come ready made: Main HUD and Be Right Back. + New overlay offers these templates:
Blank
Gameplay HUD
Just Chatting
Starting Soon
Be Right Back
Ending / credits
Overlay Studio opens when you click Edit in studio.
Do this	How
Add a widget	click it under Add a widget (left)
Move	drag it on the canvas
Resize	drag a handle on the edge or corner
Exact position / size	the four boxes under Position and size (left, top, width, height)
Place freely without snapping	hold Alt while dragging, or untick Snap
Nudge	arrow keys (hold Shift for 10 px)
Duplicate / delete	Ctrl+D / Delete
Undo	Ctrl+Z or ↶ Undo (40 steps)
Show / hide, lock, reorder	the buttons on each layer (left)
Change settings	the panel on the right
One widget as its own OBS source	Own link (size the source to the widget)
Canvas size	1920×1080, 1280×720, 2560×1440 or 1080×1920 vertical for TikTok
See it with fake data	Sample data (untick to see real and test events)
Preview background	Checker, Game scene, Dark or Green
Save	saves by itself; Ctrl+S or Save to save now
Saving updates OBS at once. Changes appear on stream while you work, so tweak positions while you're off-air.
---
8. Widget reference
Widget	What it does	Main settings
⚡ Alert box	Plays your alerts (designed on the Alerts page)	Which alerts, size
💬 Chat	Twitch + Kick + YouTube + TikTok chat with emotes	Style (Fleet console, Bubbles, Text with shadow, Plain), platforms, font, size, colour, most messages, hide after, platform tags, badges, profile pictures, hide `!commands`, hide bot names, newest at the top
🎯 Goal bar	Progress bar	Title, what it counts, start from, target, manual value, bar colours, height, percent, auto-raise the target when reached
📜 Recent events	Latest follows, subs, tips…	Which events, how many, style, font
🏷 Latest / top supporter	"Latest follower: Name" or "Top cheer: Name"	Event, latest or top, label, amount
🔢 Counter	A number (followers today, bits this stream, likes…)	What it counts, label, add to it
⏱ Countdown	Counts down from N minutes	Minutes, label, text at zero (restart from the Command Center)
🔤 Text	Any words	Text, font, size, colour, glow, outline, weight, align, CAPITALS, animation
🖼 Picture / video	Logo, frame, GIF or transparent WebM	File or link, fit, opacity, rounded corners, slow spin
🎵 Now playing	The song playing, with art and progress	Font, colours, "requested by", hide when idle
🎉 Emote wall	Emotes from chat float, rain or pop	Emote size, most at once, seconds, motion
🎬 End credits	Rolls raiders, subs, gifters, cheers, tips, TikTok gifts, followers and top chatters	Title, font, speed, chatters, loop
📰 Ticker	Scrolling line of latest supporters or your text	What it shows, speed, colours
🕑 Clock	Your local time	12/24 h, seconds
🌐 Web page	Any page inside your overlay	Address (e.g. your Hyperwave Chat design link)
What goals and counters can count (for this stream):
followers
subs including gifted, new subs only, or gifted subs
bits and Kicks
tips, Super Chats, or both
TikTok diamonds or likes
raid viewers
Manual: you set the number
Start from adds your current total. For example, set Start from to `210` and Target to `250` for a follower goal that counts up from your real follower count.
---
9. Chatbot
Dashboard → Chatbot. The Bot on switch turns the whole bot on or off.
The bot answers on the platform the message came from:
Platform	How replies are posted
Twitch	your Twitch sign-in or Streamer.bot
Kick	your Kick sign-in or Streamer.bot
YouTube	Streamer.bot
TikTok	can't reply (TikTok doesn't allow apps to post); the bot only listens
Commands. Click + Add command and fill in:
Command: the name without `!`.
Other names: aliases, comma separated.
Reply.
Who can use it: Everyone, Subs & up, VIPs & up, Mods, or Only me.
Cooldown for everyone and a per-viewer cooldown. Mods and you skip cooldowns.
Costs points.
Platforms.
Reply fill-ins:
Fill-in	Becomes
`{user}`	who typed it
`{touser}`	the first name after the command (without @), or the person
`{args}` / `{1}`…`{9}`	everything after the command / each word
`{count}`	how many times the command has been used
`{points}` / `{pointsname}`	their points / your points name
`{uptime}`	how long you've been live (from Twitch)
`{song}`	the song playing now
`{platform}`	Twitch, Kick, YouTube or TikTok
`{random:1-100}`	a random number
`{pick:yes|no|maybe}`	one of the choices at random
Starter commands: `!lurk`, `!hype`, and `!discord` and `!socials` (switched off until you add your links).
Timers post the next line of a list every N minutes, but only after at least N chat lines, so the bot never talks to an empty room.
Thank-you messages are posted when something happens, on that platform. Tips from tip sites are thanked on every platform. Fill-ins: `{user}` `{amount}` `{money}` `{months}` `{tier}` `{item}` `{message}`.
Built-in commands (each can be switched off):
Command	Who	Does
`!commands`	everyone	lists the commands they can use
`!points` (or `!<your points name>`)	everyone	shows points; `!points @name` for someone else
`!give @name 50`	everyone	gives some of their points away
`!top`	everyone	top 5 on that platform
`!addpoints @name 100`	mods	gives or (with a minus number) takes points
`!uptime`	everyone	live time from Twitch
`!so @name`	mods	shoutout with their Twitch or Kick link
`!permit @name`	mods	lets them post one link
Command symbol (Built-in commands tab): `!` by default.
Try it & log tests a command without posting it, and shows everything the bot said, with any errors.
The song-request and DJ chat commands from Station (`!sr`, `!skip`, `!vol` …) still work as before. Set them up on the Music page.
---
10. Chat modules
Dashboard → Chat modules. These are Hyperwave's own takes on the classic chat games, in the fleet's voice. Each card shows a chat preview using your current wording, an on/off switch, and ⚙ Edit. In Edit you can rename the module and every command and reply. Back to the original words undoes your changes.
The point games use Loyalty points (section 11) and need points and the chatbot switched on. Mods and you skip game cooldowns.
Module	What it is	Commands	Settings
🛰️ Hyperspace Gamble	roulette	`!jump 500` · `!jump 50%` · `!jump all`	chance to win (45%), smallest/biggest bet, cooldown (30 s), replies for winning, losing and going all in
🎰 Salvage Run	slot machine	`!salvage`	cost (100), reel symbols (🛰️ ☄️ 🚀 💠 ⭐, or your own emoji or words), three-the-same pays 10×, two-the-same pays 1× (fuel back), cooldown
⚔️ Ion Duel	duel between two viewers	`!duel @name 500`, then `!engage` or `!evade`	smallest/biggest duel, seconds to accept (60), cooldown, every reply
📦 Supply Drop	raffle	mods: `!drop 3000` (or `!drop 3000 120` for 120 seconds); viewers: `!claim`	usual prize (1,000), seconds to claim (60), number of winners, every reply
🚀 Launch Alert	go-live announcement	(automatic)	the message, which platforms, send when Twitch says you're live and/or when OBS starts streaming
How they work:
Supply Drop: viewers on every platform can claim. Joining is quiet, so chat isn't flooded. Halfway through it posts a reminder with how many have claimed, and at the end it draws the winners and announces them everywhere. The card has Launch drop (with prize and seconds), Draw now and Cancel.
Launch Alert: fill-ins are `{channel}` `{title}` `{game}` `{link}` (each platform's own link) `{twitch}` `{kick}`. The title and category come from Twitch when you're signed in. It posts once even if Twitch and OBS both notice you went live. Send it now posts it by hand.
Commands don't clash with your Homeworld Fleet Battles commands in Streamer.bot (`!battle`, `!fleet`, `!join`, `!retreat`). If you rename a module command to one that's already taken, Command tells you which.
Fill-ins for the games are listed at the top of each Edit window. For example, Hyperspace Gamble uses `{user}` `{amount}` `{points}` `{pointsname}` `{cmd}`.
Chat alerts ("Thank you for following…") are the Thank-you messages on the Chatbot page (section 9).
---
11. Loyalty points
Dashboard → Loyalty points.
Choose a name, for example `-RUs-`. Viewers can then type `!-RUs-` or `!points`.
Set how many points each thing gives:
a chat message, at most once every N seconds
following
subscribing
each gifted sub
every 100 bits or Kicks
raiding
every 1.00 tipped
each TikTok gift
Set a starting amount for new viewers.
Points are kept per platform: "Name" on Twitch and "Name" on Kick are separate.
Leaderboard: search, filter by platform, change anyone's points by typing in the box, Give points (a minus number takes them away), or Reset everyone.
---
12. Moderation
Dashboard → Moderation.
Filters (switch them on first):
Block links. Add Allowed websites (e.g. `twitch.tv, youtube.com, clips.twitch.tv`). Mods can type `!permit @name` to let someone post one link.
Too many CAPITALS: a percent of capitals, in messages at least N letters long.
Too many symbols: a percent of symbols.
Blocked words or phrases.
Longest message.
What happens:
Delete the message or Time them out (for N seconds).
On Twitch this uses your Twitch sign-in.
On Kick Command can only time viewers out, and only with your Kick sign-in.
On every platform the message disappears from your Command overlays at once.
YouTube and TikTok don't let apps remove messages from the platform itself.
Never filtered: you and your mods. You can also tick Don't filter subscribers / members and Don't filter VIPs.
---
13. Music, deck and DJ
Everything from Hyperwave Station 1.0.2 is built in. Open it from Dashboard → Music, deck & DJ or go to `http://127.0.0.1:7580/station`.
Music: any player on your PC, the YouTube Music app, Spotify Premium, or Last.fm.
Song requests with rules, plus a request list.
Remote DJ: a mod runs your music from their phone.
Hyperwave Deck on your PC, phone or Elgato Stream Deck.
The Hyperwave Chat and Now Playing designers, scene layouts, a soundboard, and category changes.
The full guide is in `docs/Music-Deck-DJ-Guide.md`.
> **Spotify users:** Command uses port 7580, so add `http://127.0.0.1:7580/callback` as an extra **Redirect URI** in your Spotify developer app (keep Station's 7575 one if you still use Station).
---
14. Coming from Hyperwave Station
Settings → Import from Hyperwave Station copies:
your channels
OBS, Streamer.bot and TikFinity settings
your music choice and song request rules
chat reply wording
quick messages and deck buttons
Sign-ins are not copied on purpose. Twitch and Kick hand out single-use renewal tokens, so sharing one would sign Station out. Sign in once on Connections.
Command finds Station's settings by itself when Station is in the same folder, in `C:\Hyperwave\` (the folder Station's guide used), or in `%APPDATA%\HyperwaveStation`.
Command uses ports 7580 / 7581 / 7582 and Station uses 7575 / 7576 / 7577, so you can run both while you test.
Streamer.bot actions that call Station's addresses (port 7575, e.g. `/api/sr` for song requests) keep talking to Station. When you switch over for good, change `7575` to `7580` in those actions.
---
15. Firing alerts from other apps
Any app on your PC can fire a real alert by opening one address, for example Streamer.bot (Sub-actions → Core → Network → Fetch URL), a PayPal notification tool, or your own script:
```
http://127.0.0.1:7580/api/events/fire?kind=tip&user=Name&amount=5&currency=USD&message=Thanks!&platform=paypal
```
Setting	Values
`kind`	`follow` `sub` `giftsub` `cheer` `raid` `tip` `superchat` `redeem` `tiktokgift` `share` `like`
`user`	the name to show
`amount`	bits, viewers, gift count, money…
`currency`	`USD`, `EUR`, `GBP`… (for tips)
`months`, `tier`, `item`, `message`	optional
`platform`	any word, shown as the source (e.g. `paypal`)
`avatar`	optional `https://` link to a profile picture
`id`	optional unique id. The same id twice only alerts once.
These count in your stats, credits and points like any other event. Use the Test buttons for pretend ones.
---
16. Where your settings live, and backups
Next to the app (or in `%APPDATA%\HyperwaveCommand` if that folder is read-only):
File / folder	Holds
`hyperwave-command.json`	connections, sign-ins, music and deck settings
`command-data\alerts.json`	your alert designs
`command-data\overlays.json`	your overlays and widgets
`command-data\bot.json`	commands, timers, thank-you messages, chat modules, points and filter settings
`command-data\points.json`	everyone's loyalty points
`command-data\events.json`	recent events and this session's counts
`hyperwave-media\`	your uploaded pictures, videos and sounds
`overlays\`	the Station chat and Now Playing overlays that run without the app
Backup: copy those files and folders somewhere safe. To move to a new PC, copy them next to the app there. `hyperwave-command.json` holds your sign-ins, so don't share it.

Backup and restore
Settings → Backup and restore.
⬇ Save a backup downloads one zip, `HyperwaveCommand-backup-DATE.zip`, with your settings and sign-ins, alerts, overlays, chatbot, chat modules, loyalty points, deck buttons, your pictures, videos and sounds, scene layouts and the About file. It holds your sign-ins, so keep it private.
⬆ Restore a backup… puts it all back and restarts Command. A copy of what you had is saved first in `command-data\backups`.
Moving to a new PC:
Install with the updater.
Open Settings → Restore a backup….
Copy diagnostics
Settings → Need help? → 📋 Copy diagnostics copies a help report: your version, connection lights, settings and the last 300 log lines. Passwords, keys, passkeys and sign-ins are replaced with `(hidden)`. Paste it into the feedback form or a message. Show it lets you read it first.
---
17. Ports and safety
Port	Used for	Who can reach it
7580	dashboard, overlays, studio, live events	this PC only
7581	Remote DJ (only through the DJ tunnel, with the DJ passkey)	off until you open DJ access
7582	Wi-Fi deck for phones (with the deck passkey)	off until you turn it on
Command keeps Hyperwave Station's protections:
Only Command's own pages and OBS can use the dashboard and live events. Other websites are blocked, including through tricks like DNS rebinding and hidden frames.
Everything people type (chat, names, tip messages) is shown as plain text and can never run as code in your overlays.
Pictures and sounds load only from your own uploads or `https://` links.
Twitch and Kick sign-ins use the official sign-in pages. Command never sees your password.
---
18. Troubleshooting
Problem	Fix
Overlay is blank in OBS	Check the console window is open. Open the overlay link in your browser: a note in the corner says what's wrong (these notes never show inside OBS).
No sound from alerts on stream	In the OBS Browser source, tick Control audio via OBS, and check the source isn't muted in the Audio Mixer.
Twitch alerts don't arrive	Connections → Twitch should show ✓ Listening for: with your events. If it lists Not available, click Sign in again to give Command the missing permission.
"Twitch refused every event"	Your sign-in is from another app or has expired. Click Sign in again.
Kick chat works but no Kick alerts	Paste your Channel ID (see section 5). Kick's follow alerts depend on Kick sending them, which isn't guaranteed.
YouTube says "can't reach Streamer.bot"	Start Streamer.bot's WebSocket Server, then check the port and password match.
YouTube chat is empty	YouTube only sends chat while a broadcast is live and Streamer.bot is connected to it.
TikTok says "can't reach TikFinity"	Open TikFinity, connect it to your LIVE, and check the port matches (default `21213`).
Bot doesn't answer on Twitch	Chatbot → Try it & log: the log shows the reason. Usually you need to sign in to Twitch, or switch Chat replies to Streamer.bot.
Bot doesn't answer on Kick	Sign in to Kick (Connections → Kick step 2), or turn on Streamer.bot with Kick connected there.
"Port 7580 is busy"	Command is already running. Look for its console window.
Windows SmartScreen warning	More info → Run anyway (the app isn't code-signed yet).
Fonts look plain	Chakra Petch and Inter are built in. Other fonts load from Google Fonts and need internet.
---
19. Version numbers and updates
Command uses MAJOR.MINOR.PATCH:
PATCH (0.1.0 → 0.1.1): fixes and small polish only.
MINOR (0.1.x → 0.2.0): new features or pages. Your settings carry over.
MAJOR (0.x → 1.0.0): the first stable public release, and later any change that needs setting up again.
`-alpha` / `-beta` on the end means a test build.
Every update gets an entry in `CHANGELOG.md` and on the dashboard's What's new page.
Updating
Command checks github.com/TaiiRepublic/Hyperwave-Command for new versions when it starts and every six hours.
Version in the menu: under the app name. It's green when you're up to date. It's red when a new version is out, with a red "vX is out · Update" link under it.
Update card: at the top of the Command Center page, it shows what's new in that version before you do anything.
Update now does the rest:
Downloads `HyperwaveCommand.zip` from GitHub.
Checks its SHA-256 fingerprint against `HyperwaveCommand.zip.sha256`, so a damaged or changed download is never installed.
Swaps in the new `HyperwaveCommand.exe` (and the README, changelog and docs) and restarts by itself. The dashboard reloads on the new version.
If you're live, it asks first, because overlays blank out for a few seconds while it restarts.
Never touched: settings, sign-ins, alerts, overlays, points, uploads and the `web` folder.
Settings → Updates: turn the checks off, Check now, open the releases on GitHub, or download the updater.
On an older version or a new PC? Download HyperwaveCommandUpdater.exe and double-click it. It finds your install (or asks where), closes a running copy, installs the newest version, keeps your settings and starts it again.
By hand: close the app, replace `HyperwaveCommand.exe` with the one from the zip, and start it again.
For releases on GitHub (so Update now and the updater find them), each release needs these files:
File	Why
`HyperwaveCommand.zip`	the app (with a `HyperwaveCommand/` folder inside)
`HyperwaveCommand.zip.sha256`	its fingerprint, checked before installing
`HyperwaveCommandUpdater.exe`	the one-click installer/updater
The tag must be the version, e.g. `v0.2.0-alpha`. Don't mark it as a pre-release: the always-newest download links (`/releases/latest/download/...`) skip pre-releases.
---
20. Building from source
Install Go 1.22 or newer from go.dev/dl.
Open the `source` folder and double-click build.bat. It builds `HyperwaveCommand.exe` one folder up, with the icon and version details built in (from `resource_windows_amd64.syso`).
To change the icon or version details:
Edit `versioninfo.json` and replace `hyperwave-command.ico`.
Run `goversioninfo -64 -o resource_windows_amd64.syso versioninfo.json` (from github.com/josephspurrier/goversioninfo).
Build again.
Run the automated tests with `go test ./...`.
How it fits together:
File	Does
`events.go`	the event engine (history, session counts, WebSocket and SSE live stream, test and fire endpoints)
`eventsub.go`	Twitch EventSub, Twitch moderation
`command_chat.go`	Kick live events, Kick chat and moderation API, chat hooks
`platform_events.go`	YouTube (via Streamer.bot), tips, TikTok (via TikFinity)
`bot.go`	chatbot, timers, points, filters
`games.go`	chat modules: Hyperspace Gamble, Salvage Run, Ion Duel, Supply Drop, Launch Alert
`update.go`	GitHub update checks, Update now, restarts
`backup.go`	backup and restore, Copy diagnostics
`updater/`	HyperwaveCommandUpdater.exe (`go build ./updater`)
`studio.go`	alert and overlay storage, overlay pages, Station import
`web/widgets.js`	every widget and the alert engine, shared by the dashboard, studio and OBS
`web/command.html`	the dashboard
`web/studio.html`	the Overlay Studio
`web/overlay.html`	the page OBS loads
everything else	Hyperwave Station 1.0.2 (music, deck, DJ, chat, OBS, Streamer.bot)
---
21. Roadmap
Ideas for the next alpha builds, roughly in order. Each one gets its own version number when it ships.
First-run wizard that walks through Connections, adds the overlay to OBS for you (through the OBS connection), and fires a test.
Text-to-speech for tips and cheers, with a word filter and a minimum amount.
Giveaways: keyword entry from all four chats, points tickets, a fair draw with a winner alert.
Chat games: bring Homeworld Fleet Battles, trivia and Phasmo betting into the bot, with points.
Custom widgets: paste your own HTML/CSS/JS as a sandboxed widget, then share widget and overlay theme packs (one file with the overlay, alerts and pictures).
Hyperwave Cloud (optional): a hosted relay so the bot and overlays keep running when your PC is off. It would also handle official Kick webhooks, a public tip page through a payment provider (Stripe or PayPal handle the money), and Streamer.bot-free YouTube. This needs hosting costs and real security work, so it comes after the local app is solid.
A code-signing certificate, so Windows stops showing the "protected your PC" warning.
---
22. Credits and licences
Made by TaiiRepublic: twitch.tv/taiirepublic · kick.com/taiirepublic. o7
Built on Hyperwave Station 1.0.2.
Fonts: Chakra Petch and Inter, SIL Open Font License 1.1 (see `licenses/`).
QR codes: go-qrcode by Tom Harwood, MIT licence.
Homeworld is a trademark of its owners. Hyperwave Command Center is a fan-made, unofficial tool and isn't affiliated with or endorsed by them.
