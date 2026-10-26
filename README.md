Hyperwave Command Center
Version 0.4.0-beta · by TaiiRepublic · free for every streamer
Hyperwave Command Center is a complete streamer suite in one small Windows app. It's built to replace StreamElements-style tools, but it's simpler, it runs on your own PC, and it works across Twitch, Kick, YouTube and TikTok at the same time.
	What you get
⚡ Alerts	Follows, subs, gifts, bits and Kicks, raids and hosts, tips, Super Chats, channel points, and TikTok gifts, shares and likes, all designed on one page
▣ Overlays	A drag-and-drop Overlay Studio with 15 widgets: chat, goals, event lists, countdowns, credits, emote wall and more
✦ Chatbot	Custom commands, timers, thank-you messages, built-in commands
🎲 Chat modules	Hyperspace Gamble, Salvage Run, Ion Duel, Supply Drop and the Launch Alert, all renamable
◆ Loyalty points	Name them whatever you like (e.g. -RUs-) and viewers earn them on every platform
⛨ Moderation	Link, caps, symbol, word and length filters
◎ Sensors	Everything from Hyperwave Sensors: channel analytics, bot and spam flags with an options menu, lurkers and viewbot clusters, Deep scan, History, best times to stream, earnings on your own channels, and your phone as a remote
▦ OBS & Stream Deck	The Hyperwave Deck on your PC, phone or Elgato Stream Deck: scenes, clips, sounds, mute, category changes and chat
♫ Music	Now Playing from Spotify, YouTube Music, Last.fm or any player, song requests and Remote DJ
💬 Chat overlay	Hyperwave Chat: every platform's chat in one overlay, with 20 animations
Everything is set up in Command Center's own window, in the Hyperwave look (plates, crimson, amber and cyan, Chakra Petch). It keeps running in the tray while you stream. Nothing is sent to a cloud. There's no account to make.
> **Beta build.** Command Center now carries Hyperwave Station and Hyperwave Sensors inside it. Expect the odd rough edge, and please send feedback from **Settings → About → Send feedback**.
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
Sensors: analytics and bot & spam review
OBS & Stream Deck, Music and Chat overlay (the Hyperwave Station tools)
Coming from Hyperwave Station or Hyperwave Sensors
Firing alerts from other apps
Where your settings live, and backups
Ports and safety
Troubleshooting
Version numbers and updates
Roadmap
Credits and licences
---
1. What's in the download
```
HyperwaveCommand/
├── HyperwaveCommand.exe      ← the app (double-click to start)
├── HyperwaveCommandUpdater.exe ← installs, updates or removes the app
├── README.md                 ← this guide
├── CHANGELOG.md              ← what changed in every version
├── LICENSE.txt               ← free to use; the TaiiRepublic credit stays
├── docs/
│   └── Music-Deck-DJ-Guide.md   ← full guide to the music, deck and DJ tools
├── web/
│   └── about.json            ← edit to change the About box (your links, tip page)
├── streamerbot/
│   └── Hyperwave-Spotify.cs  ← optional Streamer.bot song-request action
├── branding/                 ← app icon (SVG, PNG, ICO)
└── licenses/                 ← font and library licences
```
The web folder is optional. Any page you put in it overrides the built-in copy, the same way it worked in Station.
---
2. Install and first launch
You need: Windows 10 or 11, and OBS Studio 28 or newer.
For YouTube you also need Streamer.bot (free).
For TikTok you also need TikFinity (free).
Easiest: download HyperwaveCommandUpdater.exe from https://github.com/TaiiRepublic/Hyperwave-Command/releases/latest and double-click it. Its window walks you through it:
Install suggests `C:\HyperwaveCommand\`. Keep it, or pick another folder. Tick Start Command Center when Windows starts if you like.
It downloads the newest version, checks the download, installs it, and adds Hyperwave Command Center to your Start menu and desktop.
Command Center opens in its own window.
If Windows says "Windows protected your PC", click More info → Run anyway.
The same updater finds and updates any older version (it keeps your settings), and Command Center shows up in Windows Settings → Apps, where Uninstall removes it cleanly.
By hand:
Make a folder: `C:\HyperwaveCommand\`
Copy everything from the zip into it.
Double-click HyperwaveCommand.exe.
Windows may say "Windows protected your PC". Click More info → Run anyway.
Command Center opens in its own window. Its address is http://127.0.0.1:7580 if you ever want it in a browser.
The window and the tray icon
Closing the window doesn't quit. Command Center keeps running in the tray (the icons by the clock), so alerts, overlays, the chatbot, Sensors, the deck and song requests stay live. The first time, a small note tells you where it went.
Click the tray icon to open the window again. Right-click it for Check for updates, Open the Command Center folder and Quit Command Center.
Start with Windows: Settings → Window and tray → Start with Windows. It starts quietly in the tray.
Starting Command Center when it's already running brings its window to the front.
Sign-ins and links to other sites (Twitch, Kick, Google, the Deck, the overlay designers) open in your normal browser.
Console (bottom of the menu) shows what Command Center is doing. It's also saved to `hyperwave-command.log` next to your settings (the last run's log is `hyperwave-command.old.log`).
No window, only a browser tab? The window needs the Microsoft Edge WebView2 runtime, which comes with Windows 11 and up-to-date Windows 10. Without it, the dashboard opens in your browser and everything else works the same. To get the window, install the free Evergreen Bootstrapper from https://developer.microsoft.com/microsoft-edge/webview2/ and start Command Center again.
---
3. Quick start: your first alert in OBS in 5 minutes
Dashboard → Connections → Twitch → step 1: type your Twitch channel name (e.g. `taiirepublic`) and click Save. Chat now flows into Command.
Dashboard → Overlays & widgets → Your OBS links: click Copy next to Main HUD.
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
Dashboard → Overlays & widgets → Test an alert: click ★ Follow. The alert plays in OBS.
To get real alerts, finish the Twitch sign-in on Connections (section 5).
---
4. The Command Center (home page)
This is the page to keep open while you stream. On a wide screen it shows three columns: OBS on the left, chat in the middle, and activity and channel points on the right. On a smaller window the columns stack.
Along the top
Status tiles show Twitch, Kick, YouTube, TikTok, OBS and Streamer.bot. Green means connected, amber means partly working, red means a problem, and grey means not set up. Click a tile to go to its setup.
Session counters count followers, subs, gifted subs, bits and Kicks, tips (including Super Chats), raids, TikTok diamonds and likes. A new session starts:
when you go live on Twitch,
when Command starts after 8 quiet hours,
or when you press New session.
Pause alerts holds alerts in a queue, and Resume plays them in order. Skip alert ends the alert on screen now.
Stream preview (needs the OBS connection, section 5)
Shows what OBS is sending, with a LIVE badge while you're streaming.
Pick Light (1 fps), Normal (3 fps) or Smooth (6 fps). Untick Show to turn the preview off and save CPU and GPU. Command remembers your choice.
Under the picture: stream time, bitrate (kbps), dropped frames, OBS's frame rate and CPU use, and the recording timer. Dropped frames over 1% turn red.
● Go live / ■ End stream (both ask first), ● Record / ■ Stop recording, Save replay (when the OBS Replay Buffer is on) and Clip.
Scenes shows every scene in your OBS, in the same order as the OBS Scenes dock. Click one to switch to it. The live scene has a red outline. Tick Thumbnails to see a small picture of each scene (refreshed every 15 seconds).
Audio shows your OBS audio sources. Click one to mute or unmute it. 🔇 with a red edge means muted.
Chat puts Twitch, Kick, YouTube and TikTok chat in one list, with each platform's tag.
Twitch and Kick emotes show as pictures, and so do 7TV, BTTV and FFZ emotes for your Twitch channel.
Type in the box and press Enter or Send. All sends to every chat Command can post in; pick Twitch, Kick or YouTube to send to one. TikTok doesn't let apps post in LIVE chat, so it's read only.
☺ opens the emote picker: your Twitch channel emotes, Twitch global, Kick, 7TV, BTTV and FFZ, with a search box. Click an emote to add it to your message.
Hover a Twitch or Kick message for Delete, 10m (time out for 10 minutes) and Ban (asks first). This needs the Twitch or Kick sign-in.
Activity lists every event from every platform, newest first. ↻ replays that alert. Replays aren't counted twice.
Channel points (the tab next to Activity) works with Twitch and Kick:
Waiting redemptions for rewards made in Command: ✓ marks one done and ↩ refunds the points.
Rewards: Pause/Resume and Turn off/Turn on. Twitch and Kick only let the app that made a reward change it, so rewards you made on Twitch or Kick themselves show without buttons. Use Make a new reward (platform, name, cost, description, and whether the viewer types a message) to make ones you can control here.
Redeemed this session lists every redemption from any platform.
After updating from 0.3.0-beta, Twitch and Kick each need one fresh sign-in to allow channel points (the tab shows a Sign in again link).
Test an alert, Your OBS links, Restart countdowns and Roll the credits are on Overlays & widgets (section 7).
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
`clips:edit` `user:write:chat` `channel:manage:broadcast` `moderator:read:followers` `channel:read:subscriptions` `bits:read` `channel:manage:redemptions` `moderator:manage:banned_users` `moderator:manage:chat_messages`
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
Scopes	`user:read`, `channel:read`, `channel:write`, `chat:write`, `moderation:ban`, `moderation:chat_message:manage`, `channel:rewards:read`, `channel:rewards:write`
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
StreamElements (straight to Command, no Streamer.bot)
Open streamelements.com/dashboard/account/channels and log in.
Click Show secrets and copy the JWT Token.
In Command (Connections → Tips → StreamElements): tick StreamElements tip alerts, paste the token into JWT Token, and click Save. The status turns Connected.
Streamlabs (straight to Command, no Streamer.bot)
Open streamlabs.com/dashboard → Settings → API Settings → API Tokens.
Copy Your Socket API Token.
In Command (Connections → Tips → Streamlabs): tick Streamlabs donation alerts, paste the token into Socket API Token, and click Save.
Both tokens work like passwords, so never show them on stream. Command keeps them on your PC and the page never shows them again (leave the box empty to keep the saved one).
Ko-fi, TipeeeStream, Fourthwall (through Streamer.bot)
In Streamer.bot, open Integrations and connect your tip site.
In Command, tick Tip alerts through Streamer.bot and click Save. This needs the Streamer.bot connection above.
If StreamElements or Streamlabs is connected straight to Command and through Streamer.bot, Command skips Streamer.bot's copy, so each tip plays once.
For anything else (PayPal, your own website), see section 16.
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
✕ on a picture or sound removes it from the alert. The file stays in your library. Remove the last picture to go back to the profile picture (or no picture).
Sound → None makes the alert silent.
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
Your own panel: upload a PNG, GIF, WebP or WebM frame or background (or pick one From my library). It's shown behind the whole alert. Choose Stretch to the alert, Fit inside or Fill and crop the edges, and set the Space inside the panel. Match the panel's shape makes the alert the same shape as your art.
Place the words myself: tick it, then drag the dashed box on the preview to move the words and drag its corner to resize them. The words shrink to fit the box. Set the alert's width and height, and line the words up left, centre or right. Reset the words box puts it back.
Text over picture keeps the words inside the picture: they wrap and shrink to fit.
Copy this look to every alert gives all the other alerts the same layout, font, sizes, colours and motion. Their accent colours, words, pictures and sounds stay as they are.
➤ Motion
Comes in: Fade, Drop down, Rise up, Slide from right or left, Zoom, Bounce, Hyperspace warp, Flip, Spin, Glitch or Heavy drop.
Goes out: Fade, Fly up, Drop away, Slide left or right, Zoom out, Hyperspace jump, Spin away or Glitch out.
Name animation: Wave, Pulse, Glow, Shake or Rainbow.
Animation speed and On screen for (seconds).
⚙ When it shows: only when the amount is at least a number, and only from certain platforms.
Apply a look to every alert (top of the page) gives every alert a theme in one click: Fleet console, Hyperspace jump, Big picture, Slim banner or Arcade. Words, pictures and sounds stay as they are.
Variations: a different alert for big moments
Click + Variation in the Editing bar under the preview. It starts as a full copy of the alert. Delete removes it straight away (a small card asks first).
Set Plays when: Amount is at least, Months are at least, Platform is, or Tier is, and a Value (e.g. `1000` bits, `6` months, `kick`, `3`).
Change anything you like (picture, sound, words, look) with the same controls. The preview uses an amount that matches the rule.
Click Main design or a variation in the Editing bar to switch between them. When several variations match, the biggest "at least" wins.
Starter variations come included: Resub (2+ months), Big raid (25+ pilots, fleet alarm) and 1,000 bits (fanfare and rainbow).
For every alert: the pause between alerts, and words that hide a viewer's message (the alert still plays).
Alerts only in OBS: if you'd rather not use an overlay, add `http://127.0.0.1:7580/alerts` as a 1920 × 1080 Browser source.
---
7. Overlays and the Overlay Studio
Dashboard → Overlays & widgets. Each overlay is one Browser source in OBS. Copy its link and add it the same way as in the quick start.
Under the overlays and the widget library:
Test an alert sends a pretend event to every overlay. You can pick the platform and amount. Tests are never counted in stats or credits.
Your OBS links has the links for your first overlays and for Alerts only, ready to copy.
On-screen controls: Restart countdowns resets every Countdown widget, and Roll the credits restarts every End credits widget.
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
13. Sensors
Dashboard → Sensors lists the channels you're scanning and how many accounts are flagged. Open Sensors opens the full Sensors pages right in the window (← Command Center at the top takes you back).
Scan your channel, or any channel you name, on Twitch, Kick, YouTube and TikTok:
Overview: viewers now, peak and average, active chatters, messages per minute, chat engagement, followers, and the viewers-over-time chart. Export CSV saves the readings.
Bot and spam flags: every account gets a 0–100 score with plain-English reasons: selling viewers, promo-spam services, hidden links, look-alike letters, copy-paste waves, rapid-fire, brand-new accounts, follow bursts.
Nothing happens on its own. Each flagged account has an Options menu: Ban, Timeout (1m/10m/1h/24h), Warn, Delete their messages, Block, Keep watching, Not a bot, Always allow, Open profile, Copy name. Options a platform doesn't support are greyed out with the reason.
Protected accounts: the channel owner, mods, VIPs and subs/members are never flagged. Helper bots (StreamElements, Nightbot, Streamer.bot, Sery_Bot, Botrix…) are protected by default, and you can edit the list in Sensors → Settings.
Lurkers: silent viewers, known viewer-list bots, viewbot clusters (accounts all made on the same day) and join waves (Twitch and TikTok).
All viewers: everyone in chat, page by page, with NEW ACCOUNT and FIRST VISIT badges.
Deep scan: returning vs new chatters, top chatters, hype moments with VOD timestamps, trending words, the stream timeline, time per category and best times to stream.
History: import your Twitch, Kick, YouTube or TikTok analytics file, pull past broadcasts, rebuild a Twitch stream's deep scan from its VOD chat, or add streams by hand.
Earnings: tips, subs, bits, Super Chats, KICKs and TikTok gifts, only on your own channels (signed in as that account). Platform amounts are estimates; StreamElements tips sync with your JWT token.
Sensor alerts: viewer spikes with no raid, follow bursts, raids, and very low chat for the viewer count.
Setting up: Sensors → Settings has step-by-step setup for each platform, with the exact values to copy, plus a guided YouTube setup. The first time you open Sensors it can walk you through it.
Your phone: Sensors → Settings → Phone, turn it on, then scan the QR code (or type the PIN) on a phone on the same Wi-Fi.
Sensors keeps its own address, http://localhost:7490, so the redirect URLs in your Twitch, Kick and Google developer apps stay the same.
---
14. OBS & Stream Deck, Music and Chat overlay
Everything from Hyperwave Station 2.0 is built in, split into three tools under Hyperwave tools in the menu. Each one opens to a short page of steps; click a step to open its settings.
▦ OBS & Stream Deck: connect OBS, then run the Hyperwave Deck on your PC, phone or Elgato Stream Deck: scenes, clips, a soundboard, mute, category changes and chat.
♫ Music: pick your music (any player on your PC, the YouTube Music app, Spotify Premium, or Last.fm), the Now Playing overlay and designer, song requests with rules, chat replies, commands without a bot and Remote DJ (a mod runs your music from their phone).
💬 Chat overlay: the Hyperwave Chat designer, every platform's chat in one overlay.
The settings pages show only the tool you opened, with a switcher at the top of their menu. Setup (all tools) under it has Platforms (every Twitch, Kick, YouTube, TikTok and Streamer.bot setting for these tools) and Streamer.bot.
The full guide is in `docs/Music-Deck-DJ-Guide.md`.
> **Spotify users:** Command uses port 7580, so add `http://127.0.0.1:7580/callback` as an extra **Redirect URI** in your Spotify developer app (keep Station's 7575 one if you still use Station).
---
15. Coming from Hyperwave Station or Hyperwave Sensors
Settings → Bring over Hyperwave Station or Hyperwave Sensors moves your whole setup in one click.
Open Settings. Command Center lists every copy of Station and Sensors it finds on this PC, with what's in each (channels, deck buttons, pictures and sounds, layouts, history).
Click Bring it over next to the one you want.
Not listed? Click Pick a Station or Sensors folder… and choose the folder Station or Sensors runs from, or Pick a Station backup (.zip)… for a backup made in Station's Settings.
Command Center saves a copy of your current setup (in `command-data\backups`), brings everything over, and restarts for a few seconds.
The Command Center page also shows a bring your setup over link when it finds Station or Sensors you haven't brought over yet. Your own Command Center settings, alerts, overlays and chatbot stay as they are.
Hyperwave Station
What comes over:
channel names
OBS, Streamer.bot and TikFinity settings
your music choice and your Spotify sign-in
song request rules and chat replies
deck buttons, launchers and quick messages
Remote DJ settings
your deck pictures and sounds
saved chat and music layouts
Sign in to Twitch and Kick once on Connections. Command Center asks for a few more permissions than Station did (alerts and mod tools), so Station's Twitch and Kick sign-ins can't be reused.
Command Center looks for Station in its own folder, the folder next to it, `C:\Hyperwave\` (where Station's installer puts it), `%APPDATA%\HyperwaveStation`, and `Hyperwave` folders on your Desktop, Downloads and Documents.
Command uses ports 7580 / 7581 / 7582 and Station uses 7575 / 7576 / 7577, so you can run both while you test.
When Station isn't running, Command Center also answers on Station's overlay address (`127.0.0.1:7575`), so chat and Now Playing browser sources made for Station keep working without changes.
Streamer.bot actions that send requests to Station (port 7575, e.g. `/api/sr` for song requests) should be changed to `7580` when you switch over for good.
Hyperwave Sensors
Close the standalone Sensors app first. The first time Command Center starts, it brings over Sensors from `%APPDATA%\HyperwaveSensors` by itself (it copies it, so the old app still works if you go back).
Kept Sensors somewhere else? Use Settings → Pick a Station or Sensors folder… and choose the folder with Sensors' `config.json` and `data` folder in it.
What comes over: your channels, sign-ins, developer apps and YouTube setup, detection settings and protected names, paired phones, earnings settings, and all your history (readings, past streams, imports and earnings). Channels already in Command Center's Sensors are kept too.
Sensors keeps its address (`localhost:7490`), so your developer apps and paired phones work as before.
Sensors Lite (the phone-only web app) is separate and keeps working on its own.
---
16. Firing alerts from other apps
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
17. Where your settings live, and backups
Next to the app (or in `%APPDATA%\HyperwaveCommand` if that folder is read-only):
File / folder	Holds
`hyperwave-command.json`	connections, sign-ins, music and deck settings
`command-data\alerts.json`	your alert designs
`command-data\overlays.json`	your overlays and widgets
`command-data\bot.json`	commands, timers, thank-you messages, chat modules, points and filter settings
`command-data\points.json`	everyone's loyalty points
`command-data\events.json`	recent events and this session's counts
`hyperwave-media\`	your uploaded pictures, videos and sounds
`command-data\sensors\`	Sensors' settings and sign-ins (`config.json`) and its history, stream summaries and earnings (`data\`)
`overlays\`	the Station chat and Now Playing overlays that run without the app
`hyperwave-command.log`	what the Console page shows (the last run is `hyperwave-command.old.log`)
Backup: copy those files and folders somewhere safe. To move to a new PC, copy them next to the app there. `hyperwave-command.json` holds your sign-ins, so don't share it.

Backup and restore
Settings → Backup and restore.
⬇ Save a backup downloads one zip, `HyperwaveCommand-backup-DATE.zip`, with your settings and sign-ins, alerts, overlays, chatbot, chat modules, loyalty points, Sensors settings and history, deck buttons, your pictures, videos and sounds, scene layouts and the About file. It holds your sign-ins, so keep it private.
⬆ Restore a backup… puts it all back and restarts Command. A copy of what you had is saved first in `command-data\backups`.
Moving to a new PC:
Install with the updater.
Open Settings → Restore a backup….
Copy diagnostics
Settings → Need help? → 📋 Copy diagnostics copies a help report: your version, connection lights, settings and the last 300 log lines. Passwords, keys, passkeys and sign-ins are replaced with `(hidden)`. Paste it into the feedback form or a message. Show it lets you read it first.
---
18. Ports and safety
Port	Used for	Who can reach it
7580	dashboard, overlays, studio, live events	this PC only
7581	Remote DJ (only through the DJ tunnel, with the DJ passkey)	off until you open DJ access
7582	Wi-Fi deck for phones (with the deck passkey)	off until you turn it on
7490	Sensors (and paired phones on your Wi-Fi)	this PC; paired phones on your home network once you turn Phone on
7575	Station's old overlay address, only while Station isn't running	this PC only, overlays only
Command keeps Hyperwave Station's protections:
Only Command's own pages and OBS can use the dashboard and live events. Other websites are blocked, including through tricks like DNS rebinding and hidden frames.
Everything people type (chat, names, tip messages) is shown as plain text and can never run as code in your overlays.
Pictures and sounds load only from your own uploads or `https://` links.
Twitch and Kick sign-ins use the official sign-in pages. Command never sees your password.
---
19. Troubleshooting
Problem	Fix
Overlay is blank in OBS	Check Command Center is running (its icon is in the tray). Open the overlay link in your browser: a note in the corner says what's wrong (these notes never show inside OBS).
No sound from alerts on stream	In the OBS Browser source, tick Control audio via OBS, and check the source isn't muted in the Audio Mixer.
Twitch alerts don't arrive	Connections → Twitch should show ✓ Listening for: with your events. If it lists Not available, click Sign in again to give Command the missing permission.
"Twitch refused every event"	Your sign-in is from another app or has expired. Click Sign in again.
Kick chat works but no Kick alerts	Paste your Channel ID (see section 5). Kick's follow alerts depend on Kick sending them, which isn't guaranteed.
YouTube says "can't reach Streamer.bot"	Start Streamer.bot's WebSocket Server, then check the port and password match.
YouTube chat is empty	YouTube only sends chat while a broadcast is live and Streamer.bot is connected to it.
TikTok says "can't reach TikFinity"	Open TikFinity, connect it to your LIVE, and check the port matches (default `21213`).
Bot doesn't answer on Twitch	Chatbot → Try it & log: the log shows the reason. Usually you need to sign in to Twitch, or switch Chat replies to Streamer.bot.
Bot doesn't answer on Kick	Sign in to Kick (Connections → Kick step 2), or turn on Streamer.bot with Kick connected there.
"Port 7580 is busy" / nothing happens when I start it	Command Center is already running. Starting it again brings its window to the front; if not, click its icon in the tray (by the clock).
I closed the window and the overlays still work	That's on purpose: Command Center keeps running in the tray. Right-click the tray icon → Quit Command Center to stop it.
It opens in the browser instead of its own window	Install the Microsoft Edge WebView2 runtime (see The window and the tray icon in section 2), then start Command Center again.
Sensors says port 7490 is in use	The standalone Hyperwave Sensors app is still open. Close it, then quit Command Center from the tray and start it again.
A sign-in opened my browser and I'm back in Command Center	That's normal: finish the sign-in in the browser. The page in Command Center shows you're connected when you refresh it.
The stream preview is black or says OBS didn't send a picture	Check OBS is green on Connections. A scene with nothing visible (or only a game capture OBS can't see yet) shows black. Untick Show if you don't need it.
Channel points says "Sign in again"	Twitch and Kick need one fresh sign-in after 0.4.0-beta to allow channel points. Click Sign in again on Connections.
StreamElements or Streamlabs says it didn't accept the token	Copy the token again (StreamElements makes a new JWT when you reset it) and paste it, then Save.
Windows SmartScreen warning	More info → Run anyway.
Fonts look plain	Chakra Petch and Inter are built in. Other fonts load from Google Fonts and need internet.
---
20. Version numbers and updates
Command uses MAJOR.MINOR.PATCH:
PATCH (0.1.0 → 0.1.1): fixes and small polish only.
MINOR (0.1.x → 0.2.0): new features or pages. Your settings carry over.
MAJOR (0.x → 1.0.0): the first stable public release, and later any change that needs setting up again.
`-alpha` / `-beta` on the end means a test build.
Every update gets an entry in `CHANGELOG.md` and on the dashboard's What's new page.
Updating
Command Center checks github.com/TaiiRepublic/Hyperwave-Command for new versions when it starts and every six hours.
Version in the menu: under the app name. It's green when you're up to date. It's red when a new version is out, with a red "vX is out · Update" link under it. The tray icon gets a red dot and an Update to Command Center … item too.
Update card: at the top of the Command Center page, it shows what's new in that version before you do anything.
Update now downloads the release, checks the download, swaps in the new version and restarts by itself. The window reloads on the new version.
If you're live, it asks first, because overlays blank out for a few seconds while it restarts.
Never touched: settings, sign-ins, alerts, overlays, points, Sensors history, uploads and the `web` folder.
Settings → Updates: turn the checks off, Check now, open the releases on GitHub, or download the updater.
On an older version or a new PC? Download HyperwaveCommandUpdater.exe and double-click it. It finds your install (or asks where), closes a running copy, installs the newest version, keeps your settings and starts it again.
---
21. Roadmap
Ideas for the next beta builds, roughly in order. Each one gets its own version number when it ships.
First-run wizard that walks through Connections, adds the overlay to OBS for you (through the OBS connection), and fires a test.
Text-to-speech for tips and cheers, with a word filter and a minimum amount.
Giveaways: keyword entry from all four chats, points tickets, a fair draw with a winner alert.
Chat games: bring Homeworld Fleet Battles, trivia and Phasmo betting into the bot, with points.
Custom widgets: paste your own HTML/CSS/JS as a sandboxed widget, then share widget and overlay theme packs (one file with the overlay, alerts and pictures).
Hyperwave Cloud (optional): a hosted relay so the bot and overlays keep running when your PC is off. It would also handle official Kick webhooks, a public tip page through a payment provider (Stripe or PayPal handle the money), and Streamer.bot-free YouTube. This needs hosting costs and real security work, so it comes after the local app is solid.
Shared sign-ins: sign in to Twitch, Kick and YouTube once and let Sensors use the same connection as alerts and the chatbot.
---
22. Credits and licences
Made by TaiiRepublic: twitch.tv/taiirepublic · kick.com/taiirepublic. o7
Includes Hyperwave Station 2.0 and Hyperwave Sensors.
Fonts: Chakra Petch and Inter, SIL Open Font License 1.1 (see `licenses/`).
Open-source components and their licences are listed in `licenses/THIRD-PARTY-NOTICES.txt`.
Free to use; see `LICENSE.txt`.
Homeworld is a trademark of its owners. Hyperwave Command Center is a fan-made, unofficial tool and isn't affiliated with or endorsed by them.
