# Hyperwave Command Center

**Version 0.9.7.3-beta** · by TaiiRepublic · free for every streamer

Hyperwave Command Center is a complete streamer suite in one small Windows app. It's built to replace StreamElements-style tools, but it's simpler, it runs on your own PC, and it works across **Twitch, Kick, YouTube and TikTok** at the same time.

| | What you get |
|---|---|
| ⚡ **Alerts** | Follows, subs, gifts, bits and Kicks, raids and hosts, tips, Super Chats, channel points, and TikTok gifts, shares and likes, all designed on one page |
| ▣ **Overlays** | A drag-and-drop **Overlay Studio** with 20 widgets: chat, goals, event lists, latest supporters with their profile pictures, countdowns, a giveaway wheel, credits, emote wall and more, each with its own styles |
| ✦ **Chatbot** | Custom commands, timers, thank-you messages, built-in commands |
| 🎁 **Giveaways** | Viewers join with a command or a channel point reward, a countdown on stream, then a prize wheel you spin. One or several entries each, add names yourself or load a saved list |
| 🎲 **Chat modules** | A `!timer` countdown, point games (gamble, slots, duels, drops, heists, treasure hunts, stream check-ins) and a going-live message, all renamable. Updating from before 0.9.5 keeps the space-themed versions (Hyperspace Gamble, Ion Duel, Fleet Battles…) |
| ◆ **Loyalty points** | Name them whatever you like (e.g. **-RUs-**) and viewers earn them on every platform |
| ⛨ **Moderation** | Link, caps, symbol, word and length filters |
| ◎ **Sensors** | Everything from Hyperwave Sensors: channel analytics, bot and spam flags with an options menu, lurkers and viewbot clusters, Deep scan, History, best times to stream, earnings on your own channels, and your phone as a remote |
| ▦ **OBS & Stream Deck** | The Hyperwave Deck on your PC, phone or Elgato Stream Deck: scenes, clips, sounds, mute, category changes and chat |
| ♫ **Music** | Now Playing from Spotify, YouTube Music, Last.fm or any player, song requests and Remote DJ |
| 💬 **Chat overlay** | Hyperwave Chat: every platform's chat in one overlay, with 20 animations |

Everything is set up in Command Center's own window, in the Hyperwave look (plates, crimson, amber and cyan, Chakra Petch). It keeps running in the tray while you stream. Nothing is sent to a cloud. There's no account to make.

> **Beta build.** Command Center now carries Hyperwave Station and Hyperwave Sensors inside it. Expect the odd rough edge, and please send feedback from **About → Send feedback**.

---

## Contents

1. [What's in the download](#1-whats-in-the-download)
2. [Install and first launch](#2-install-and-first-launch)
3. [Quick start: your first alert in OBS in 5 minutes](#3-quick-start-your-first-alert-in-obs-in-5-minutes)
4. [The Command Center (home page)](#4-the-command-center-home-page)
5. [Connections: Twitch, Kick, YouTube, TikTok, tips, OBS](#5-connections)
6. [Alerts](#6-alerts)
7. [Overlays and the Overlay Studio](#7-overlays-and-the-overlay-studio)
8. [Widget reference](#8-widget-reference)
9. [Chatbot](#9-chatbot)
10. [Giveaways and chat modules: chat timer, point games and the Launch Alert](#10-chat-modules)
11. [Loyalty points](#11-loyalty-points)
12. [Moderation](#12-moderation)
13. [Sensors: analytics and bot & spam review](#13-sensors)
14. [OBS & Stream Deck, Music and Chat overlay (the Hyperwave Station tools)](#14-obs--stream-deck-music-and-chat-overlay)
15. [Coming from Hyperwave Station or Hyperwave Sensors](#15-coming-from-hyperwave-station-or-hyperwave-sensors)
16. [Firing alerts from other apps](#16-firing-alerts-from-other-apps)
17. [Where your settings live, and backups](#17-where-your-settings-live-and-backups)
18. [Ports and safety](#18-ports-and-safety)
19. [Troubleshooting](#19-troubleshooting)
20. [Version numbers and updates](#20-version-numbers-and-updates)
21. [Roadmap](#21-roadmap)
22. [Credits and licences](#22-credits-and-licences)

---

## 1. What's in the download

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
│   └── about.json            ← edit to change the About page (your links, tip page)
├── streamerbot/
│   └── Hyperwave-Spotify.cs  ← optional Streamer.bot song-request action
├── branding/                 ← app icon (SVG, PNG, ICO)
└── licenses/                 ← font and library licences
```

The **web** folder is optional. Any page you put in it overrides the built-in copy, the same way it worked in Station.

---

## 2. Install and first launch

**You need:** Windows 10 or 11, and OBS Studio 28 or newer.
- For YouTube you also need **Streamer.bot** (free).
- For TikTok you also need **TikFinity** (free).

**Easiest:** download **HyperwaveCommandUpdater.exe** from https://github.com/TaiiRepublic/Hyperwave-Command/releases/latest and double-click it. Its window walks you through it:
1. **Install** suggests `C:\HyperwaveCommand\`. Keep it, or pick another folder. Tick **Start Command Center when Windows starts** if you like.
2. It downloads the newest version, checks the download, installs it, and adds **Hyperwave Command Center** to your Start menu and desktop.
3. Command Center opens in its own window.

If Windows says *"Windows protected your PC"*, click **More info → Run anyway**.

The same updater finds and updates any older version (it keeps your settings), and Command Center shows up in **Windows Settings → Apps**, where **Uninstall** removes it cleanly.

**By hand:**

1. Make a folder: `C:\HyperwaveCommand\`
2. Copy everything from the zip into it.
3. Double-click **HyperwaveCommand.exe**.
   - Windows may say *"Windows protected your PC"*. Click **More info → Run anyway**.
4. Command Center opens in its own window. Its address is **http://127.0.0.1:7580** if you ever want it in a browser.

### The window and the tray icon

- **Closing the window doesn't quit.** Command Center keeps running in the tray (the icons by the clock), so alerts, overlays, the chatbot, Sensors, the deck and song requests stay live. The first time, a small note tells you where it went.
- **Click the tray icon** to open the window again. **Right-click** it for **Check for updates**, **Open the Command Center folder** and **Quit Command Center**.
- **Start with Windows:** **Settings → Window and tray → Start with Windows**. It starts quietly in the tray.
- Starting Command Center when it's already running brings its window to the front.
- Sign-ins and links to other sites (Twitch, Kick, Google, the Deck, the overlay designers) open in your normal browser.
- **Console** (bottom of the menu) shows what Command Center is doing. It's also saved to `hyperwave-command.log` next to your settings (the last run's log is `hyperwave-command.old.log`).
- **No window, only a browser tab?** The window needs the Microsoft Edge WebView2 runtime, which comes with Windows 11 and up-to-date Windows 10. Without it, the dashboard opens in your browser and everything else works the same. To get the window, install the free **Evergreen Bootstrapper** from https://developer.microsoft.com/microsoft-edge/webview2/ and start Command Center again.

---

## 3. Quick start: your first alert in OBS in 5 minutes

On a new install, a **5-step setup** opens by itself on the Command Center page (closed it? click **Start the 5-step setup** in the welcome bar):

1. **Your channel:** type your Twitch channel name (and Kick, if you stream there).
2. **Twitch app:** make your own free Twitch app once (about 2 minutes). Every value to type has a **Copy** button. Paste its **Client ID**, then **Sign in to Twitch**.
3. **OBS:** in OBS, **Tools → WebSocket Server Settings**, tick **Enable WebSocket server**, click **Show Connect Info**, and paste the **Server Password**. Click **Connect to OBS**.
4. **Overlay:** click **Add it to OBS for me**. Your Main HUD (alerts and chat) goes into the scene OBS is showing.
5. **Test alert:** send a pretend follow and watch it in OBS, then tick the alerts you want on stream.

**New installs start quiet:** every alert and everything that posts in chat starts switched off. Turn on what you want on the **Alerts** and **Chatbot** pages. (Updating from an older version changes nothing of yours.)

Adding the overlay yourself instead: **Overlays & widgets → Your OBS links**, **Copy** next to **Main HUD**, then in OBS **Sources → + → Browser**: paste it into **URL**, **Width** `1920`, **Height** `1080`, tick **Control audio via OBS**, click **OK**.

---

## 4. The Command Center (home page)

This is the page to keep open while you stream. On a wide screen it shows three columns: OBS on the left, chat in the middle, and activity and channel points on the right. On a smaller window the columns stack.

**Along the top**
- **Status tiles** show Twitch, Kick, YouTube, TikTok, OBS and Streamer.bot. Green means connected, amber means partly working, red means a problem, and grey means not set up. Click a tile to go to its setup.
- **Session counters** count followers, subs, gifted subs, bits and Kicks, tips (including Super Chats), raids, TikTok diamonds and likes. A new session starts:
  - when you go live on Twitch,
  - when Command starts after 8 quiet hours,
  - or when you press **New session**.
- **Pause alerts** holds alerts in a queue, and **Resume** plays them in order. **Skip alert** ends the alert on screen now.

**Stream preview** (needs the OBS connection, section 5)
- Shows what OBS is sending, with a **LIVE** badge while you're streaming.
- Pick **10**, **20** or **30 fps**. Higher is smoother but uses more CPU and GPU. The corner of the preview shows the frame rate you're really getting (OBS can only make pictures so fast). Untick **Show** to turn the preview off. Command remembers your choice.
- Under the picture: stream time, bitrate (kbps), dropped frames, OBS's frame rate and CPU use, and the recording timer. Dropped frames over 1% turn red.
- **● Go live** / **■ End stream** (both ask first), **● Record** / **■ Stop recording**, **Save replay** (when the OBS Replay Buffer is on) and **Clip**.

**Scenes** shows every scene in your OBS, in the same order as the OBS Scenes dock. Click one to switch to it. The live scene has a red outline. Tick **Thumbnails** to see a small picture of each scene (refreshed every 15 seconds).

**Audio** shows your OBS audio sources. Click one to mute or unmute it. 🔇 with a red edge means muted.

**Chat** puts Twitch, Kick, YouTube and TikTok chat in one list, with each platform's tag.
- Twitch and Kick emotes show as pictures, and so do **7TV**, **BTTV** and **FFZ** emotes for your Twitch channel.
- Type in the box and press **Enter** or **Send**. **All** sends to every chat Command can post in; pick **Twitch**, **Kick** or **YouTube** to send to one. TikTok doesn't let apps post in LIVE chat, so it's read only.
- **☺** opens the emote picker: your Twitch channel emotes, Twitch global, Kick, 7TV, BTTV and FFZ, with a search box. Click an emote to add it to your message.
- Hover a Twitch or Kick message for **Delete**, **10m** (time out for 10 minutes) and **Ban** (asks first). This needs the Twitch or Kick sign-in.

**Activity** lists every event from every platform, newest first. **↻** replays that alert. Replays aren't counted twice.

**Watching** (the third tab) shows how many people are watching each of your channels right now, and who:
- **Twitch:** the viewer count and everyone signed in and in your chat, with how long they've been there and whether they're chatting or lurking. Twitch never names people watching while logged out, so it says "and N watching logged out".
- **Kick:** the viewer count, and everyone who has chatted this stream (Kick doesn't share a viewer list).
- **YouTube:** the viewer count (YouTube doesn't name viewers). **TikTok:** the viewer count and TikTok's top viewers.
- Mods (🛡), VIPs (💎) and subs (★) are marked, and so are **first visits** and accounts Sensors flagged as **likely bots**. Click a name to open it in Sensors.
- The names come from **Sensors**. If Sensors isn't watching one of your channels yet, click **Show who's watching** in that channel's row.

**Channel points** (the tab next to Activity) works with Twitch and Kick:
- **Waiting redemptions** for rewards made in Command: **✓** marks one done and **↩** refunds the points.
- **Rewards**: **Pause**/**Resume** and **Turn off**/**Turn on**. Twitch and Kick only let the app that made a reward change it, so rewards you made on Twitch or Kick themselves show without buttons. Use **Make a new reward** (platform, name, cost, description, and whether the viewer types a message) to make ones you can control here.
- **Redeemed this session** lists every redemption from any platform.
- After updating from 0.3.0-beta, Twitch and Kick each need **one fresh sign-in** to allow channel points (the tab shows a **Sign in again** link).

### Chat and activity as OBS docks

Click **⧉ Pop out** on the **Chat** box or next to the **Activity** tab. You get a link to put that box in OBS as a dock, or **Open in a browser window** to put it on another screen.

1. In OBS, open **Docks → Custom Browser Docks…**
2. **Dock Name:** `Hyperwave Chat` (or `Hyperwave Activity`)
3. **URL:** `http://127.0.0.1:7580/dock/chat` (or `http://127.0.0.1:7580/dock/activity`), then click **Apply**.
4. Drag the dock wherever you like. OBS keeps it there.

- The **chat dock** has everything the Chat box has: every platform's chat, sending, emotes, and **Delete**, **10m** and **Ban**.
- The **activity dock** shows events as they come in, with a **Points** tab for channel point redemptions and a **Watching** tab (who's watching), plus **Pause** and **Skip** for alerts.
- **A−** and **A+** change the text size in each dock. The light in the corner is green while Command Center is running.

**Your OBS links**, **Restart countdowns** and **Roll the credits** are on **Overlays & widgets** (section 7). Test alerts at the bottom of the **Alerts** page (**Test any alert**).

---

## 5. Connections

All of this is on **Dashboard → Connections**, with the same steps shown on the page. Everything saves by itself: change something and **Saved ✓** shows at the top. Ports, addresses, Kick IDs and Streamer.bot only show after you tick **Show advanced** (top of the page, or **Settings**).

Everything Command Center, Sensors and your music connect to is on this one page, in groups: **Streaming platforms**, **Tips**, **Stream tools** (OBS, Streamer.bot), **Music** and **Sensors**.

- **Each box opens and closes.** Click its title bar. A box that's connected closes by itself and shows a **green light**. **Red** means it isn't connected or isn't set up yet, and **amber** means it's partly working. Command remembers which boxes you opened or closed.
- **The row of lights at the top** shows every connection at a glance. Click one to jump to its box.
- **Expand all / Collapse all** is at the top. On a new install only Twitch and OBS are open.
- The lights update every few seconds, so a sign-in you finish in your browser turns green on its own.

### Twitch: chat, alerts, chatbot, mod tools

**Step 1. Channel.** Type your **Twitch channel name**. Chat is read with no sign-in.

**Step 2. Make your own free Twitch app (once).** Open **dev.twitch.tv/console/apps/create** and fill in:

| Field | Value |
|---|---|
| Name | `Hyperwave Command YOURNAME` (Twitch names must be unique) |
| OAuth Redirect URLs | `http://localhost` → click **Add** |
| Category | `Application Integration` |
| Client Type | `Public` |

Click **Create**. Then click **Manage**, copy the **Client ID**, paste it into **Client ID** on the Connections page. It saves by itself.
*Already made one for Hyperwave Station? Reuse the same Client ID.*

**Step 3. Sign in.** Click **Sign in to Twitch**. A short code appears.
1. Open the **twitch.tv/activate** link shown.
2. Type the code.
3. Click **Authorize**.

The page updates by itself. One sign-in covers alerts, chatbot replies, clips, category changes and mod tools. It asks for these Twitch permissions:
`clips:edit` `user:write:chat` `channel:manage:broadcast` `moderator:read:followers` `channel:read:subscriptions` `bits:read` `channel:manage:redemptions` `moderator:manage:banned_users` `moderator:manage:chat_messages` `moderator:read:chatters` `moderator:manage:warnings` `user:manage:blocked_users` `user:read:moderated_channels` `channel:read:redemptions`

The last five are for Sensors (viewer lists, warnings, blocks, the channels you mod, and channel point redeems). **Signed in before 0.6.1-beta?** Click **Sign in again** once to add them.

**Step 4. Announcer account (optional).** A second Twitch account, like `YourNameBot`, that posts the chatbot's messages, timed messages, replies and the deck's chat instead of your own account.
1. Make the account on Twitch, then type `/mod accountname` in your chat so slow mode and link rules never stop it.
2. Open a **private / incognito window** and log in to Twitch there as the announcer.
3. Click **Add an announcer account**. In the private window, open the **twitch.tv/activate** link shown, type the code, check the name at the top is the announcer, and click **Authorize**.
4. Click **Send a test message**.

You only do this once: Command Center keeps the announcer signed in through restarts and updates, the same as your own account. It only asks for `user:write:chat`. **Post as me for now** keeps it signed in but sends from your own account. If the announcer ever can't post, the message goes out from your own account instead. Its messages show on your chat overlay but never count as a viewer (no welcome, alerts or points, and Sensors never flags it).

**Step 5. Alerts from Twitch.** Leave **Follows, subs, resubs, gift subs, bits, raids and channel point redeems** ticked. Under the box you'll see **✓ Listening for:** with every event Twitch accepted.

### Kick: chat, subs, gifts, hosts, follows, Kicks

**Step 1. Channel.** Type your **Kick channel name** (e.g. `taiirepublic`). Command looks up your chatroom and channel IDs by itself.
- If Kick blocks the lookup, open `https://kick.com/api/v2/channels/YOURNAME` in your browser.
- Copy `"id"` into **Channel ID** and `"chatroom" → "id"` into **Chatroom ID**.

Leave **Alerts from Kick** ticked.

**Step 2 (optional). Post in Kick chat and time out spammers.** Without this step the bot can still post on Kick through Streamer.bot. Open **kick.com/settings/developer** → **Create new**:

| Field | Value |
|---|---|
| Application name | `Hyperwave Command Center` |
| Redirect URL | `http://localhost:7580/kick/callback` |
| Scopes | `user:read`, `channel:read`, `channel:write`, `chat:write`, `moderation:ban`, `moderation:chat_message:manage`, `channel:rewards:read`, `channel:rewards:write` |

Copy the **Client ID** and **Client Secret** into Command (they save by themselves), then click **Sign in to Kick** and approve.

### YouTube: chat, members, Super Chats

**Watch only with just your channel.** Command Center reads your live chat straight from YouTube, the way YouTube's own pop-out chat does. No sign-in, no API key and nothing to install.

1. **Connections → YouTube**: type your YouTube **@handle** (or paste your channel link) in **YouTube @handle or channel link**, e.g. `@TaiiRepublic`.
2. Leave **YouTube alerts** ticked.

Command Center checks every minute and connects by itself when you go live. You get chat (with YouTube's emojis) for your overlays, the deck and the chatbot, plus Super Chats, Super Stickers, new members, gifted memberships, deleted messages and your viewer count.

**Watch only means nothing goes back to YouTube.** Your replies and the chatbot can't post in YouTube chat, and Delete, 10m and Ban don't work there. To post in YouTube chat, also connect **Streamer.bot**:

1. In Streamer.bot, **Platforms → YouTube**: sign in with your YouTube account.
2. **Servers/Clients → WebSocket Server**:

   | Field | Value |
   |---|---|
   | Address | `127.0.0.1` |
   | Port | `8080` |
   | Auto Start | ticked |
   | Authentication | ticked (recommended) with a password you choose |

   Click **Start Server**.
3. Connect Streamer.bot in its own box on Connections, then tick **Use Streamer.bot for YouTube** in the YouTube box.

While Command Center reads YouTube itself, it skips Streamer.bot's copy of YouTube chat so nothing shows twice. New subscribers (follows) only come through Streamer.bot.

### TikTok: chat, gifts, follows, shares, likes

**Watch only.** Command Center reads your LIVE straight from TikTok. Nothing to install, no TikTok sign-in.

1. **Connections → TikTok**: type your TikTok **@name**, e.g. `@taiirepublic`.
2. Leave **TikTok alerts** ticked.

Command Center checks every minute and connects by itself when you go LIVE. You get chat for your overlays, the deck and the chatbot, plus gifts, follows, shares, subscribers, likes and your viewer count (with TikTok's top viewers).

- **Watch only means nothing goes back to TikTok.** TikTok doesn't let apps post in LIVE chat, delete messages or ban, so the chatbot only listens there.
- **How it connects:** TikTok only accepts the live connection when it's signed. Command Center uses the free **Euler Stream** signing service, the same one most TikTok LIVE tools use. It only gets your LIVE's room number: no sign-in and nothing about you. The free service allows a few connections a minute from one internet connection, which is plenty for one stream. If you ever need more, paste an Euler Stream key under **How it connects, and using TikFinity instead**.
- **Prefer TikFinity?** It still works: open **TikFinity** (tikfinity.zerody.one), connect it to your LIVE, and tick **Also read TikTok through TikFinity** in the same section (port `21213` unless you changed it). You can use both; nothing shows twice.

How TikTok events behave:
- A gift sent as a streak alerts **once** when the streak ends, showing the total (e.g. "5× Rose").
- Likes are added up per viewer and sent every 20 seconds. They're off in Alerts by default.

### Tips

Command shows tip alerts but **doesn't take payments**. Taking money needs a company to handle cards, refunds and chargebacks. Keep your tip page (StreamElements, Ko-fi and so on).

**StreamElements (straight to Command, no Streamer.bot)**
1. Open **streamelements.com/dashboard/account/channels** and log in.
2. Click **Show secrets** and copy the **JWT Token**.
3. In Command (**Connections → Tips → StreamElements**): tick **StreamElements tip alerts**, paste the token into **JWT Token**. It saves by itself. The status turns **Connected**.

**Streamlabs (straight to Command, no Streamer.bot)**
1. Open **streamlabs.com/dashboard → Settings → API Settings → API Tokens**.
2. Copy **Your Socket API Token**.
3. In Command (**Connections → Tips → Streamlabs**): tick **Streamlabs donation alerts**, paste the token into **Socket API Token**. It saves by itself.

Both tokens work like passwords, so never show them on stream. Command keeps them on your PC and the page never shows them again (leave the box empty to keep the saved one).

**Ko-fi, TipeeeStream, Fourthwall (through Streamer.bot)**
1. In Streamer.bot, open **Integrations** and connect your tip site.
2. In Command, tick **Tip alerts through Streamer.bot**. This saves by itself. This needs the Streamer.bot connection above.

If StreamElements or Streamlabs is connected straight to Command *and* through Streamer.bot, Command skips Streamer.bot's copy, so each tip plays once.

For anything else (PayPal, your own website), see [section 16](#16-firing-alerts-from-other-apps).

### Streamer.bot

Its own box under **Stream tools**. In Streamer.bot: **Servers/Clients → WebSocket Server**: Address `127.0.0.1`, Port `8080`, tick **Auto Start**, click **Start Server**. In Command: tick **Connect to Streamer.bot**, check the address and port, type the password if you turned one on. It saves by itself. YouTube chat and alerts, and Ko-fi, TipeeeStream and Fourthwall tips, come through it.

### OBS

1. In OBS: **Tools → WebSocket Server Settings** → tick **Enable WebSocket server**, set Server Port `4455`, then click **Show Connect Info** and copy the **Server Password**.
2. In Command: tick **Connect to OBS**, set Address `127.0.0.1`, Port `4455`, paste the password. It saves by itself.

### Music

The **Music** box picks where your music comes from, with the setup for each one:
- **Any player on this PC:** nothing to set up.
- **YouTube Music app:** install it, turn on **Plugins → API Server [Beta] → Enabled**, click **Connect YouTube Music**, then **Allow** in the app.
- **Spotify Premium:** make your Spotify developer app (the box shows the exact Redirect URI to paste), paste the **Client ID**, **Save**, then **Connect Spotify**.
- **Last.fm:** paste your username and API key and **Save**.

This is the only place you pick your music source. Song request rules, the player to follow and the DJ page are on the Music page.

### Sensors

**Sensors uses your Twitch and Kick sign-ins from the boxes above.** Sign in there once and the **Sensors · Twitch** and **Sensors · Kick** lights turn green too. Nothing else to set up.

- **Separate account for Sensors** (for example a mod account): open **Use a separate Twitch app for Sensors** (or Kick) in that box. It has the steps and exact values to make your own app, paste its **Client ID** and **Client Secret**, **Save**, and **Sign in to …**. While that sign-in is there, Sensors uses it instead.
- **Set Sensors up with its own app before 0.6.0-beta?** It keeps working. To use one sign-in for everything, open that section and click **Disconnect**.

**Sensors · YouTube** still needs its own Google sign-in (YouTube's chat and mod tools need a Google Cloud project). The box links to the step-by-step Google setup in Sensors. TikTok in Sensors uses the same TikFinity port as above, and Sensors earnings use the StreamElements token from **Tips**, so you only type them once.

### Chat replies

**Post Twitch messages through:**
- **Automatic:** your Twitch sign-in, or Streamer.bot if you're not signed in.
- **My Twitch sign-in**
- **Streamer.bot**

Kick replies use your Kick sign-in if you have one, otherwise Streamer.bot. YouTube replies always go through Streamer.bot.

---

## 6. Alerts

**Dashboard → Alerts.** Pick an alert on the left; its switch turns it on or off. The big box at the top is **your stream** (1920 × 1080): where an alert sits in it is exactly where it pops up in OBS.

- **▶ Preview** plays the alert in that box, with its sound and motion. Click the box to stop it.
- **Send a test to OBS** saves your changes and plays the alert on stream straight away. Under the button it says what happened: **Playing in OBS now**, in line behind an alert that's showing, or what to fix (no overlay open in OBS, or OBS didn't get it). Tests always play, even when the alert is switched off or alerts are paused, and pressing it again replaces the test that's showing. When you're editing the main design, the test uses an amount under your variations, so you see the design you're editing.
- **On screen for** is how long the whole alert stays up.
- **Save alerts** updates every OBS source at once, with no refresh needed.
- **Copy OBS link** (top of the page) copies the alerts link. In OBS: **Sources → + → Browser**, paste it, Width 1920, Height 1080. Overlays refresh themselves when Command Center updates.

| Kind | Comes from |
|---|---|
| Follow | Twitch, Kick, TikTok, YouTube (new subscriber) |
| Subscription | Twitch (incl. resubs), Kick, YouTube (new member), TikTok |
| Gift subs | Twitch, Kick, YouTube (gifted memberships) |
| Bits / Kicks | Twitch bits, Kick Kicks |
| Raid / host | Twitch raids, Kick hosts |
| Tip | StreamElements, Streamlabs, Ko-fi, Tipeee, Fourthwall, your own links |
| Super Chat | YouTube Super Chats and Super Stickers |
| Channel points | Twitch channel point redeems, Kick rewards |
| TikTok gift | TikTok gifts (once per streak) |
| Share | TikTok shares (off by default) |
| Likes | TikTok likes, added up every 20 s (off by default) |
| First chatter | The very first time someone ever chats on your channels, any platform (see below) |
| Special greeting | People you pick, the first time they chat each stream (see below) |

### First chatter and Special greetings

- **✧ First chatter** (and **Special greetings**) do nothing at all while that alert is switched off on the Alerts page: no alert, no sound and no chat message. People who chat while it's off still count as seen. It plays the very first time someone ever says something in your chat, on Twitch, Kick, YouTube or TikTok. Command Center remembers everyone who has chatted (in `command-data\chatters.json`) and never forgets them, so it happens once per person, ever: not again next stream, not after a restart or an update, not when their name shows a little differently (like YouTube through Streamer.bot), and not when the same name chats on another platform. Everyone who already had loyalty points counts as having chatted. You and chat bots like Nightbot never set it off. In the First chatter box, pick **how they're welcomed**:
  - **Alert + chat** or **Alert only**: your alert on stream, set up below like any alert. Use a ready-made panel, your own, or **No panel**, with or without a **Sound** (**None** for a silent alert).
  - **Chat only**: just a message in chat, plus an optional **Sound on stream** that plays with nothing shown (or **No sound**). The alert designer hides itself, since nothing shows.
  - With chat, type **what the chatbot says** (`{user}` is their name). **Test it** does the real thing and says whether each part worked.
- **♛ Special greeting**: pick **Special greeting** on the left and click **+ Add someone**. Add as many people as you like. For each one:
  - the **platform** (or Any platform) and their **username**
  - **how they're greeted**: **Alert + chat**, **Alert only** or **Chat only**
  - **On stream**: the words on the alert (use `{name}` for their name, like `All hail {name}!`)
  - **In chat**: what the chatbot says (leave it empty to say the same as the alert)
  - their **sound**: a built-in one, one of your sounds, or **⬆ Upload a sound…**. For **Chat only** people the sound still plays on stream, with nothing shown (pick **No sound** for silence).

  The first time they chat in each stream, they're greeted the way you picked. **Test** does the real thing: it plays their alert or sound in OBS and posts their line in your real chat, then says whether each part worked (and why not, if it didn't). **✓ Greeted this stream** shows who has been greeted, and **Greet again** lets them be greeted once more. **▶** plays their sound, and the tick turns one person off without deleting them. People on the list get their greeting instead of the First chatter alert. The chat message goes to the platform they chatted on (TikTok doesn't let apps post in chat, so TikTok viewers only get the alert).
- Both look like any other alert: set the panel, text, spot on your stream and sound below. A new stream starts when you go live on Twitch, when you click **New session** on the Command Center page, or after 8 quiet hours.

### Make an alert in four steps

1. **Pick a panel** in the **🖼 Panel** box: a ready-made one (**Fleet console**, **Neon frame**, **Hyperspace**, **Glass card**, **Slim banner**, **Fleet emblem**), the **viewer's profile picture**, **No panel**, or **+ Add your own** (PNG, JPG, GIF, WebP, WebM or MP4). You can also drag a file straight onto the page. The ready-made panels use the alert's own colour. The **🗑** on one of your own files deletes it for good (and takes it off any alert that used it).
2. **Type what it says** in the **✎ Text** box, like `{name} just enlisted`. Click a fill-in to add it where your cursor is. Press Enter for a second line.
3. **Drag them where you want them** on your stream:
   - Drag the **panel** (orange box) or the **words** (blue box) to move them. They snap to the middle when you get close.
   - Drag a **corner** to make it bigger or smaller. Your own panels keep their shape; the ready-made panels stretch to fit your words. Dragging a corner of the words makes the letters bigger or smaller too, and the side handles make the words wider or narrower.
   - **Hold Alt and drag an edge** of the panel to cut that side off, like cropping a source in OBS. **Undo crop** in the Panel box puts it back.
   - **Words move with the panel** (ticked) moves both together when you drag the panel. Untick it to move the panel on its own.
   - **Move it to** puts the whole alert in a corner, an edge or the middle in one click.
   - **Show my stream behind it** puts a picture of what OBS is showing behind the box, so you can see what the alert will cover (OBS must be connected).
   - Click a box and use the arrow keys to nudge it (Shift moves it further).
4. **Pick a sound** in **🔊 Sound**, then click **Save alerts**.

**Where the sounds play:** every alert sound (special greetings and chat-only greetings included) plays from your alerts **Browser source in OBS**, the one you add with **Copy OBS link**. Command Center itself plays nothing on stream. For your stream to hear it, that source needs **Control audio via OBS** ticked (in OBS: right-click the source → **Properties** → tick it → **OK**). With OBS connected, the **🔊 Sound** box checks this for you and **Turn it on for me** ticks it. The source then shows in the OBS Audio Mixer, where you set its volume. To hear it yourself too: **Edit → Advanced Audio Properties** → **Monitor and Output**.

| File | Works as |
|---|---|
| PNG, JPG, WebP | still picture (up to 8 MB) |
| GIF | animated picture (up to 8 MB) |
| **WebM** | animation or video **with see-through parts**, like the rotating Taii logo (up to 40 MB) |
| MP4 | video without see-through parts (up to 40 MB) |
| MP3, WAV, OGG, M4A, FLAC | sound (up to 15 MB) |

### The boxes under your stream

- **🖼 Panel**
  - the panels to pick from (Ctrl-click several to play one at random each time), and 🗑 to delete your own files
  - **Comes in**: Fade, Swipe in from the left or right, Pop in, Drop in from the top, Rise up, Zoom, Bounce, Wipe, Glitch, Hyperspace warp, Spin, Flip, or Just appear
  - **Goes out**: Fade, Swipe out left or right, Pop out, Fly up, Drop away, Zoom out, Glitch out, Hyperspace jump, Spin away, or Just disappear
  - **While it's showing**: Still, Float, Pulse, Bounce, Swing, Spin, Shake or Jelly wobble
- **✎ Text**
  - **What it says**, with fill-ins:
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

  - **Font** (16 to choose from), **Size**, **B** bold, *I* italic, U underline, line up left, centre or right, **Text** colour, **Name** colour (for the name and numbers), **Shadow** and **Outline**
  - **Comes in** and **Goes out**: the same choices as the panel, so the words can swipe in after the picture lands
  - **Make the name move**: Wave, Pulse, Glow, Shake or Rainbow
  - **Shows up after** (0–5 s) and **Stays for** (0 = the whole alert)
  - **Also show what the viewer wrote** and **Show which platform it came from**
- **🔊 Sound**: built-in sounds or your own, **Volume**, and **Start the sound after** (0–5 s) to line it up with your animation. Pick more than one and one plays at random.
- **⚙ When it shows:** only when the amount is at least a number, and only from certain platforms.

**Give every alert a look** (top of the page) gives every alert one of the ready-made styles in one click: panel, spot, text style and motion. Words and sounds stay as they are. **Copy to every alert** copies the alert you're on (panel, spot, text style and motion) to all the others.

Alerts you made before 0.7.1 carry over by themselves: your panel or picture, words, font, colours, motion and sounds come along, placed near the top in the middle. Drag them where you want them, then click **Save alerts**.

### Bigger alerts for bigger moments

Every alert with an amount (Bits / Kicks, Gift subs, Tips, Super Chats, Raids, TikTok gifts, Likes) and Subscriptions can have bigger alerts that play instead of the main design when the moment is bigger.

1. **+ Ready-made levels** (in the **Editing** bar under the preview) adds a whole set in one go, each a little bigger and longer than the one before: bits 100 / 500 / 1,000 / 5,000 / 10,000, gift subs 5 / 10 / 25 / 50 / 100, tips and Super Chats $10 / $25 / $50 / $100, raids 10 / 25 / 50 / 100, TikTok coins 100 / 500 / 1,000 / 5,000, and for subs 2 / 3 / 6 / 9 / 12 / 18 / 24 / 36 months, Tier 2 and Tier 3. Levels you already have are skipped.
2. **+ Bigger alert** adds one at a time. It starts as a full copy of the main design.
3. Click a level in the **Editing** bar and set **Plays when** (*Amount is at least*, *Months are at least*, *Tier is* or *Platform is*) and the amount. Then change anything you like for that level: picture, sound, words, size, time on screen.
4. When several fit, the biggest one that's **on** wins. The number beside an alert in the list (like **+5**) shows how many bigger alerts it has; when some are off it shows how many are on (like **7/10**). **Delete** removes one (a small card asks first).
5. **Words:** a level uses the main alert's words, and follows them when you change them, until you type its own in **What it says** while the level is open. **Use the main alert's words instead** puts it back.
6. **Turn any level on or off** without deleting it: click the **ON / OFF** switch on its chip in the **Editing** bar, or the **✓ Enabled / ⦸ Disabled** button when it's open. **All levels on** and **All levels off** flip them all. A level that's off is skipped: a 9-month resub with 9+ months off gets the 6+ months alert. Switching a level (or a whole alert) on or off takes effect straight away; no need to press Save.

**Time on screen and the other sliders** each have a small box beside them: drag the slider, or type an exact number (like `7.75` seconds) and press Enter.

**For every alert:** the pause between alerts, and words that hide a viewer's message (the alert still plays).

**Alerts only in OBS:** if you'd rather not use an overlay, add `http://127.0.0.1:7580/alerts` as a 1920 × 1080 Browser source.

---

## 7. Overlays and the Overlay Studio

**Dashboard → Overlays & widgets.** Each overlay is **one Browser source** in OBS. Copy its link and add it the same way as in the quick start.

Under the overlays and the widget library:
- **Test any alert** (bottom of the Alerts page) sends a pretend event to every overlay. You can pick the platform and amount. Tests are never counted in stats or credits, and the page says whether OBS showed it.
- **Your OBS links** has the links for your first overlays and for **Alerts only**, ready to copy.
- **On-screen controls:** **Restart countdowns** resets every Countdown widget, and **Roll the credits** restarts every End credits widget.

Two overlays come ready made: **Main HUD** and **Be Right Back**. **+ New overlay** offers these templates:
- **Blank**
- **Gameplay HUD**
- **Just Chatting**
- **Starting Soon**
- **Be Right Back**
- **Ending / credits**

**Overlay Studio** opens when you click **Edit in studio**.

| Do this | How |
|---|---|
| Add a widget | click it under **Add a widget** (left) |
| Move | drag it on the canvas |
| Make it bigger or smaller (everything inside grows too: text, pictures, the giveaway wheel and countdown, the chat timer) | drag a **corner**, or use **Size of what's inside** (− / + / type a % / **100%**) on the right |
| Give it more room without changing the text size | drag an **edge** (or hold **Shift** while dragging a corner) |
| Exact position / size | the four boxes under **Position and size** (left, top, width, height) |
| Place freely without snapping | hold **Alt** while dragging, or untick **Snap** |
| Nudge | arrow keys (hold **Shift** for 10 px) |
| Duplicate / delete | **Ctrl+D** / **Delete** |
| Undo | **Ctrl+Z** or **↶ Undo** (40 steps) |
| Show / hide, lock, reorder | the buttons on each layer (left) |
| Change settings | the panel on the right |
| One widget as its own OBS source | **Own link** (size the source to the widget) |
| Canvas size | 1920×1080, 1280×720, 2560×1440 or **1080×1920 vertical** for TikTok |
| See it with fake data | **Sample data** (untick to see real and test events) |
| Preview background | Checker, Game scene, Dark or Green |
| Save | saves by itself; **Ctrl+S** or **Save** to save now |

Saving updates OBS at once. Changes appear on stream while you work, so tweak positions while you're off-air.

---

### 🌀 Chaos wheel

**Dashboard → Chaos wheel** (under On screen). Your viewers set it off by reaching amounts you choose; the wheel pops up on stream, spins, and lands on one of your results.

1. **What sets it off:** tick any of Follows, Subs, Gifted subs, Bits / Kicks, Tips, Super Chats, Raids, TikTok gifts or a Channel point reward, and type the amount it takes. **In one go** means one cheer, tip or gift that big (e.g. 500 bits). **Added up over the stream** means every time the total reaches it (e.g. every 1,000 bits, or every 10 follows). Spins wait their turn.
2. **What's on the wheel:** your own results ("Potato cam for 5 minutes", "Play with no HUD"…). Make some **2×, 3× or 5× as likely**, and a result can **press a Hyperwave Deck button** when it lands (switch scene, play a sound, show a source…).
3. **When it lands:** say the result in chat (`{user}` `{why}` `{result}`), how long it spins and how long the result stays on screen.
4. **Show it on stream:** **Make the Chaos wheel overlay** → **Copy OBS link** → add it in OBS as a Browser source (1920 × 1080, tick **Control audio via OBS**). It stays hidden and pops up only to spin. Style it in the studio like the giveaway wheel (Game show lights, Neon, Glossy 3D…).

The **Console** has **Test spin** (spins on stream, no chat message, no deck button), **Spin for real** and **Clear waiting spins**. A Hyperwave Deck button can spin it too (step **Spin the Chaos wheel**). Test alerts from the Alerts page never set it off.

The **History** box under the Console lists every spin: the time, who set it off, why and where it landed, with **Up next** showing spins still waiting. A spin stopped with **Stop now** shows crossed out, test spins say **TEST**. The last 300 spins are kept after a restart; **Clear** empties it.

## 8. Widget reference

| Widget | What it does | Main settings |
|---|---|---|
| ⚡ Alert box | Plays your alerts, each exactly where you placed it on the Alerts page (the box itself can sit anywhere) | Which alerts |
| 💬 Chat | Twitch + Kick + YouTube + TikTok chat with emotes | Style (Fleet console, Bubbles, Text with shadow, Plain), platforms, font, size, colour, most messages, hide after, **platform** (round logo, short tag or hidden; the logos grow with the text size), badges, profile pictures, hide `!commands`, hide bot names, newest at the top |
| 🎯 Goal bar | Progress toward a goal | **Style** (Bar, Slim line, Blocks, Ring), title, what it counts, **Keep counting across streams** (with **Start this goal over**), start from, target, manual value, bar colours, height, percent, auto-raise the target when reached |
| 📜 Recent events | Latest follows, subs, tips… | Which events, how many, **style** (Fleet console, Cards, Pills, Neon, Plain), profile pictures, font |
| 🏷 Latest / top supporter | One supporter with their value: latest bits (`500 bits`), latest sub (`Tier 1 · 6 months`), latest raid (`42 raiders`), latest tip (`$10`), top gifter… | Event, latest or top, **layout** (One line, Card, Badge), label, profile picture (circle, rounded, hexagon), show the value, colours |
| 🏅 Latest supporters | Several at once: latest follower, sub, bits, raid, tip… side by side, stacked or in a grid | Which ones, latest or top, arrange, each as Card / One line / Badge, labels, profile pictures, values, hide empty ones |
| 🔢 Counter | A number (followers today, bits this stream, likes…) or a **chat counter** like `!deaths` (section 10) | **Style** (In a line, Big number, Stacked, Badge, Rolling numbers), what it counts, label, add to it |
| ⏱ Countdown | Counts down from N minutes | **Style** (see the timer styles below), minutes, label, text at zero, warning colour (restart from Overlays & widgets) |
| ⏳ Chat timer | The `!timer` countdown (section 10) | **Style**, title, text at zero, hide after, warning colour, sound at zero, font, colours |
| 🎁 Giveaway countdown | Time left to enter a giveaway, how to enter, how many entered | **Style**, title, how-to-enter line, newest names, text when it closes, font, colours |
| 🌀 Chaos wheel | Pops up and spins when a viewer reaches one of your amounts, lands on one of your results | Same styles as the giveaway wheel, title, result banner, sounds, confetti |
| 🎡 Giveaway wheel | Prize wheel of everyone who entered; spins and lands on the winner | **Style** (Classic, Game show lights, Neon, Flat, Glossy 3D, Fleet console), **pointer** (Triangle, Arrow, Needle, Gem), colours (Fleet, Neon, TaiiRepublic, Steel, Rainbow), when it shows, title, winner banner, tick and win sounds, confetti |
| 🔤 Text | Any words | Text, font, size, colour, glow, outline, weight, align, CAPITALS, animation |
| 🖼 Picture / video | Logo, frame, GIF or transparent WebM | File or link, fit, opacity, rounded corners, slow spin |
| 🎵 Now playing | The song playing, with art and progress | Font, colours, "requested by", hide when idle |
| 🎉 Emote wall | Emotes from chat float, rain or pop | Emote size, most at once, seconds, motion |
| 🎬 End credits | Rolls raiders, subs, gifters, cheers, tips, TikTok gifts, followers and top chatters | Title, font, speed, chatters, loop |
| 📰 Ticker | A line of your text, recent events, and the **latest values** (latest bits, sub, raid, tip… with their amounts) or the **top this stream** | What it shows (tick any mix), which ones, show values, **motion** (Scroll, Slide up one at a time, Fade, Typewriter), speed or seconds on each, colours |
| 🕑 Clock | Your local time | **Style** (Digital, LCD, Analog hands, Time with the date, Flip clock), 12/24 h, seconds |
| 🌐 Web page | Any page inside your overlay | Address (e.g. your Hyperwave Chat design link) |

**Timer styles** (Countdown, Chat timer, Giveaway countdown): Big numbers, Numbers + draining bar, Ring beside the numbers, Numbers inside a ring, Flip clock, Digital (LCD), Minutes and seconds boxes, Numbers + blocks, One small line.

**Looks (a frame around a widget):** most text widgets (supporters, counters, timers, clock, text, goal, recent events, now playing, ticker) have a **Look** at the bottom of their settings: None, Dark panel, Glass, Fleet console, Neon frame, Hologram, Pill, Outline, Solid banner, Terminal, Sticker or Underline, with your own **Frame colour** and **Space inside the frame**.

**Profile pictures** come from Twitch, YouTube and TikTok. When there isn't one (Kick, tips), a circle with their first letter shows instead.

**What goals and counters can count** (for this stream):
- followers
- subs including gifted, new subs only, or gifted subs
- bits and Kicks
- tips, Super Chats, or both
- TikTok diamonds or likes
- raid viewers
- **Manual**: you set the number

**Start from** adds your current total. For example, set Start from to `210` and Target to `250` for a follower goal that counts up from your real follower count.

---

## 9. Chatbot

**Dashboard → Chatbot.** The **Bot on** switch turns the whole bot on or off.

The bot answers on the platform the message came from:

| Platform | How replies are posted |
|---|---|
| Twitch | your Twitch sign-in or Streamer.bot |
| Kick | your Kick sign-in or Streamer.bot |
| YouTube | Streamer.bot |
| TikTok | can't reply (TikTok doesn't allow apps to post); the bot only listens |

**Commands.** Click **+ Add command** and fill in:
- **Command:** the name without `!`.
- **Other names:** aliases, comma separated.
- **Reply.**
- **Who can use it:** Everyone, Subs & up, VIPs & up, Mods, or Only me.
- **Cooldown** for everyone and a **per-viewer cooldown**. Mods and you skip cooldowns.
- **Costs points.**
- **Platforms.**

Reply fill-ins:

| Fill-in | Becomes |
|---|---|
| `{user}` | who typed it |
| `{touser}` | the first name after the command (without @), or the person |
| `{args}` / `{1}`…`{9}` | everything after the command / each word |
| `{count}` | how many times the command has been used |
| `{points}` / `{pointsname}` | their points / your points name |
| `{uptime}` | how long you've been live (from Twitch) |
| `{song}` | the song playing now |
| `{platform}` | Twitch, Kick, YouTube or TikTok |
| `{random:1-100}` | a random number |
| `{pick:yes\|no\|maybe}` | one of the choices at random |

**Starter commands:** `!lurk`, `!hype`, and `!discord` and `!socials` (switched off until you add your links).

**Timed messages** (Chatbot → **Timed messages** → **+ Add timed message**) post a message every N minutes, taking turns if you write more than one, but only after at least N chat lines, so the bot never talks to an empty room. Each one shows when it will post next. The chatbot has to be on (**Bot on**).

**Thank-you messages** are posted when something happens, on that platform. Tips from tip sites are thanked on every platform. Fill-ins: `{user}` `{amount}` `{money}` `{months}` `{tier}` `{item}` `{message}`.

**Built-in commands** (each can be switched off):

| Command | Who | Does |
|---|---|---|
| `!commands` | everyone | lists the commands they can use |
| `!points` (or `!<your points name>`) | everyone | shows points; `!points @name` for someone else |
| `!give @name 50` | everyone | gives some of their points away |
| `!top` | everyone | top 5 on that platform |
| `!addpoints @name 100` | mods | gives or (with a minus number) takes points |
| `!uptime` | everyone | live time from Twitch |
| `!so @name` | mods | shoutout with their Twitch or Kick link |
| `!permit @name` | mods | lets them post one link |

**Command symbol** (Built-in commands tab): `!` by default.

**Try it & log** tests a command without posting it, and shows everything the bot said, with any errors.

The song-request and DJ chat commands from Station (`!sr`, `!skip`, `!vol` …) still work as before. Set them up on the Music page.

---

### ♫ Song requests in chat

**Chatbot → ♫ Song requests.** Tick **Take these commands in Twitch chat** (and Kick, YouTube or TikTok if you like; YouTube answers need Streamer.bot connected to YouTube, and TikTok doesn't let apps answer in chat). Command Center then takes `!sr song name or link`, `!song` (what's playing) and the mod DJ commands (`!skip`, `!prev`, `!pause`, `!play`, `!vol 40`, `!shuffle`, `!repeat`, `!playlist`, `!playnow`, `!sron` / `!sroff`), and answers in chat with the chatbot.
- Each command can be switched **on or off**, **renamed** (only the new name works then), and set to **Everyone** or **Mods**. Mods and the **Extra DJs** you list can always use the mod ones.
- **Channel point reward:** type the reward's exact title; the viewer types the song when they redeem it. **Make this reward on Twitch** makes one for you, and then **Give the points back when the song can't be added** works (Twitch only lets an app give points back for rewards it made).
- If Streamer.bot also runs the Hyperwave music action, turn that action off, or every request runs twice.

### 🔔 Chat ping (only you hear it)

**Chatbot → 🔔 Chat ping**, or the 🔕/🔔 button on the Command Center chat card. A short sound plays **on this PC** when someone chats, so chat on a platform you don't usually watch isn't missed. It never goes on stream and works with Command Center closed to the tray. Off until you turn it on.
- **Platforms:** tick the ones that ping (none ticked = all).
- **Sound and volume:** Chime, Blip, Bell, Pop or Coin, or **Use one of my sounds…** (MP3 or WAV work best). **▶ Test** plays it.
- **At most once every** N seconds (default 10), and **only after that platform's chat was quiet for** N minutes (0 = always), so a busy chat doesn't ding nonstop.
- **Not for bots or me** skips Nightbot, StreamElements and the like, and you.

## 10. Chat modules

**Dashboard → Chat modules.** The **Chat timer** sits at the top (see below; **Giveaways** have their own page). Under it are Hyperwave's own takes on the classic chat games. **New installs (0.9.6 and later)** get them in everyday words: **Gamble** (`!gamble`), **Slots** (`!slots`), **Duel** (`!duel`, `!accept` / `!deny`), **Point Drop**, **Heist** (`!heist @name`), **Treasure Hunt** (`!hunt`) and **Stream check-in**, all switched off to start. Copies set up before that keep the space-themed versions in the table below. Each card shows a chat preview using your current wording, an on/off switch, and **⚙ Edit**. In Edit you can rename the module and **every command and reply**. **Back to the original words** undoes your changes.

The point games use **Loyalty points** (section 11) and need points and the chatbot switched on. Mods and you skip game cooldowns.

| Module | What it is | Commands | Settings |
|---|---|---|---|
| 🛰️ **Hyperspace Gamble** | roulette | `!jump 500` · `!jump 50%` · `!jump all` | chance to win (45%), smallest/biggest bet, cooldown (30 s), replies for winning, losing and going all in |
| 🎰 **Salvage Run** | slot machine | `!salvage` | cost (100), reel symbols (🛰️ ☄️ 🚀 💠 ⭐, or your own emoji or words), three-the-same pays 10×, two-the-same pays 1× (fuel back), cooldown |
| ⚔️ **Ion Duel** | duel between two viewers | `!duel @name 500`, then `!engage` or `!evade` | smallest/biggest duel, seconds to accept (60), cooldown, every reply |
| 📦 **Supply Drop** | raffle | mods: `!drop 3000` (or `!drop 3000 120` for 120 seconds); viewers: `!claim` | usual prize (1,000), seconds to claim (60), number of winners, every reply |
| 🚀 **Launch Alert** | go-live announcement | (automatic) | the message, which platforms, send when Twitch says you're live and/or when OBS starts streaming |

**⚔️ Fleet Battles** sit under the other modules. They start switched off; turn each on with the toggle on its card.

| Module | What it is | Commands | Settings |
|---|---|---|---|
| 💥 **Boarding Raid** | send a boarding party at another viewer's ship, decided by a D20 | `!board @name` | chance the raid succeeds (45%) and that both fleets break off (10%; the rest is repelled), amount seized on a success (50–500), amount the target captures if you're repelled (50–300), what a target always keeps (100), how much a target needs to be boarded (more than 100), cooldown (5 min), time in the brig after being repelled (15 min), how long a target's shields recharge after a raid (10 min), open season bonus (off), names that can never be boarded, every reply |
| 🛸 **Bentusi Trade** | a free trade run on a cooldown | `!trade` | cooldown (15 min); chance and smallest/biggest payout for small (35%, 10–50), good (22%, 50–150), great (10%, 150–400) and a Bentusi relic (3%, 2,000–5,000); what an empty run costs (free); every reply |
| 📡 **Fleet Check-in** | report for duty once per stream for bonus points | `!checkin` and/or a channel point reward you name | points for checking in (100), extra for every stream in a row (+10), where the streak bonus stops growing (10 streams), the reply and the "already checked in" reply |

How they work:
- **Supply Drop:** viewers on **every** platform can claim. Joining is quiet, so chat isn't flooded. Halfway through it posts a reminder with how many have claimed, and at the end it draws the winners and announces them everywhere. The card has **Launch drop** (with prize and seconds), **Draw now** and **Cancel**.
- **Boarding Raid:** the roll is a D20. 1 or 20: both fleets break off and nothing moves. An odd number (3–19): the raid succeeds and seizes a random amount between your smallest and biggest, but the target always keeps what you set. An even number (2–18): the raid is repelled, the target captures a random amount (never more than the raider has) and the raider goes to **the brig** for the minutes you set. You, your channel names and the usual bots (Nightbot, StreamElements, Streamlabs, Moobot, Fossabot…) can never be boarded; add more under **Never board these names too**. Viewers can only board someone on the same platform who has been in chat. The cooldown and the brig apply to mods too. **Open season** gives extra chance against someone in the brig.
- **Bentusi Trade:** each run rolls 1–100. The relic sits at the top, then great, good and small; whatever is left is an empty run. The Edit window shows the chances as you type (for example *35% small · 22% good · 10% great · 3% relic · 30% empty*). An empty run is free unless you set a cost.
- **Fleet Check-in:** each viewer can check in once per stream. Tick **Check in with the chat command**, type a channel point reward's exact title, or use both. Make the reward on Twitch yourself (Creator Dashboard → Viewer Rewards → Channel Points → Add New Custom Reward), for example **Report for duty**. A stream is your Twitch live session when you're signed in to Twitch; without it, 6 hours with no check-ins starts a new stream. Checking in on streams in a row adds the streak bonus. Streaks are kept between streams.
- **Launch Alert:** fill-ins are `{channel}` `{title}` `{game}` `{link}` (each platform's own link) `{twitch}` `{kick}`. The title and category come from Twitch when you're signed in. It posts once even if Twitch and OBS both notice you went live. **Send it now** posts it by hand.
- **Commands don't clash** with your Homeworld Fleet Battles commands in Streamer.bot (`!battle`, `!fleet`, `!join`, `!retreat`). If you rename a module command to one that's already taken, Command tells you which.

Fill-ins for the games are listed at the top of each Edit window. For example, Hyperspace Gamble uses `{user}` `{amount}` `{points}` `{pointsname}` `{cmd}`.

**Chat alerts** ("Thank you for following…") are the **Thank-you messages** on the Chatbot page (section 9).

### 🎁 Giveaways

**Dashboard → Giveaways** (its own page, under Chat). A countdown on screen while viewers join, then a prize wheel you spin. Free for viewers (no points needed) on Twitch, Kick and YouTube. The page has four numbered steps on the left and the **Console** on the right, where you run the giveaway. Changes save by themselves (there's a **Save** button too).

**Set it up once:**
1. **The prize and the time:** what you're giving away (e.g. `a Steam key for Homeworld 3`), how long viewers can join (e.g. `5` min `0` sec) and how long the wheel spins (30 seconds by default).
2. **How viewers join:** viewers put themselves on the wheel. Nobody has to be added by hand.
   - **Join command:** `enter` means viewers type `!enter` and they're on the wheel. Keep it different from your Fleet Battles commands (`!join`, `!battle`, `!fleet`, `!retreat`).
   - **Twitch channel point reward** (optional, or instead of the command): make the reward on Twitch first (Creator Dashboard → Viewer Rewards → Channel Points → Manage Rewards → **Add New Custom Reward**), then type its title here exactly, e.g. `Enter the giveaway`. Needs your Twitch sign-in on Connections.
   - **Allow multiple entries** (see below), **who can join** (Everyone, or Subs, VIPs and mods only) and **platforms** (none ticked = all).
3. **What the chatbot says:** the messages for the start, entries closing and the winner (see below).
4. **Show it on stream (one time):** press **Make the giveaway overlay**, then in the studio press **Copy OBS link**. In OBS: Sources → **+** → **Browser**, paste the link, width `1920`, height `1080`, and tick **Control audio via OBS**. Nothing shows until a giveaway is running.

**Run a giveaway:**
1. Press **▶ Start giveaway**. The countdown appears on stream and the chatbot announces it.
2. Viewers type `!enter` (or redeem the reward) and land on the wheel by themselves. You see every name in the **Console**.
3. At zero, entries close by themselves. (**⏹ Close entries now** ends early.)
4. Press **🎡 Spin the wheel**. The wheel spins and lands on the winner, who is announced on screen and in chat.
5. Winner didn't answer? **↺ Redraw** takes them off the wheel, then spin again. **✓ Done, clear the screen** hides it all.

While a giveaway is running, the same buttons sit at the top of the **Command Center** page, and a **Hyperwave Deck** button can do **Giveaway → Spin the wheel** (or start, close, redraw, clear).

**Chat messages** (step 3 on the Giveaways page): when it starts, when entries close, the winner, and an optional reply to each entry. Fill-ins: `{prize}` `{cmd}` `{redeem}` `{time}` `{count}` `{winner}` `{user}` `{tickets}` (their entries). Untick **Announce the giveaway in chat** to keep it on screen only.

**Allow multiple entries** (step 2 on the Giveaways page): typing the command again, or redeeming the reward again, adds another entry. Set **Most entries per person** (0 = no limit). Each person gets a slice of the wheel as big as their entries, so more entries means a better chance. The Console shows how many each person has (e.g. **NovaPilot ×3**).

**Add names yourself or load a saved list** (open it at the bottom of the Console):
- Type names, one per line or separated by commas, and click **+ Add names**. With multiple entries on, `NovaPilot, 3` gives NovaPilot 3 entries.
- **📂 Load a saved list…** reads a `.txt` file (one name per line) or a `.csv` file (names in the first column; a platform and a number of entries in other columns are used too).
- **⬇ Save this list** downloads everyone who entered as a `.csv` you can keep and load again later.
- With no giveaway running, adding names gets the wheel ready to spin straight away, with no countdown. Great for entries collected somewhere else, like Discord.
- **✕** next to a name takes that person off the list.

**+ 10 pretend entries** (while entries are open) fills the wheel with test names so you can try your overlay.

### ⏳ Chat timer

A countdown on stream that you or your mods start from chat, any time.

| Type in chat | What happens |
|---|---|
| `!timer 5` | 5 minutes |
| `!timer 90s` · `!timer 1:30` · `!timer 1h` | 90 seconds, 1 min 30 sec, 1 hour |
| `!timer 10 BRB` | 10 minutes with the title **BRB** |
| `!timer +2` · `!timer -1` | add 2 minutes, take 1 away |
| `!timer pause` · `!timer resume` | pause and carry on |
| `!timer stop` | cancel it |

Typing a new time replaces the running timer.

**Set it up once:** **Dashboard → Chat modules → Chat timer**, press **Make the timer overlay**, then **Copy OBS link** in the studio and add it to OBS as a Browser source. Change its look in the studio: big numbers, a draining bar or a ring, title, text at zero, a warning colour for the last seconds, a sound at zero, hide it a few seconds after zero, font, size and colours.

**Who can use it:** Mods (default), Mods and VIPs, or Everyone. You can always. Rename the command if you like. The **Console** has quick 1 / 5 / 10 / 15 / 30 min buttons, a box for any time, **+1 min**, **−1 min**, **Pause** and **Stop**. A **Hyperwave Deck** button can run any timer command too (e.g. `5` or `stop`).


### 🔢 Chat counters

Count anything on stream (deaths, wins, fails, hydration) and let you or your mods change it from chat.

| Type in chat | What happens |
|---|---|
| `!deaths` | shows the number (when **Say the number in chat** is on) |
| `!deaths +1` · `!deaths -1` · `!deaths +5` | add or take away |
| `!deaths set 10` · `!deaths reset` | set it, or back to 0 |

**Set it up:** **Dashboard → Chat modules → Chat counters**. A **Deaths** counter is ready to go; **+ Add a counter** makes more. For each one you choose:
- the **name** and the **chat command**,
- **who can change it** (Mods, Mods and VIPs, or Everyone; you always can; anyone can type just `!deaths` to see it),
- what **+** and **−** change it by, **Never go below 0**, and whether to **say the number in chat** (with your own message: `{name}` `{value}` `{user}`).

**On stream:** **Make a counter overlay** makes one OBS source with the counter in it. Or add the **Counter** widget to any overlay, set **Counts** to **A chat counter**, and type its command (e.g. `deaths`). Pick any counter style (big number, rolling numbers, badge…) and a Look. It pops a little each time it changes.

**Add to it by itself:** under each counter, **+ Add a rule** makes it count on its own, on top of chat and buttons. For example *Add 1 for every 5 gifted subs*, *Add 1 for every 400 bits*, *Add 1 for every $10 in tips*, or *Add 2 for every* redeem of a channel point reward. Amounts add up across the stream (3 gifted, then 2 more = 5 → +1), and a minus number takes away. Each new stream starts from 0, unless you tick **Keep counting toward the next one between streams**. Under each rule you can see how far along it is (*3 / 5 gifted subs toward the next +1*). Test alerts from the Alerts page never count; **Try it** sends a pretend amount through a rule so you can watch it work. **What changed it** lists the last changes and why (which rule and whose bits or subs, a chat command, a Stream Deck key, a deck button or the dashboard).

**Buttons:**
- The **− / +** buttons, the number box and **Reset** on the dashboard change it straight away.
- **Hyperwave Deck:** make a button with the step **Chat counter**, pick the counter and **+1**, **−1**, **+5** or **Reset**.
- **Elgato Stream Deck:** click **Copy Stream Deck +1 link** (or −1), then in the Stream Deck app drag **System → Website** onto a key, paste it into **URL** and tick **GET request in background**.
---

## 11. Loyalty points

**Dashboard → Loyalty points.**
- Choose a name, for example `-RUs-`. Viewers can then type `!-RUs-` or `!points`.
- Set how many points each thing gives:
  - a chat message, at most once every N seconds
  - following
  - subscribing
  - each gifted sub
  - every 100 bits or Kicks
  - raiding
  - every 1.00 tipped
  - each TikTok gift
- Set a starting amount for new viewers.
- Points are kept **per platform**: "Name" on Twitch and "Name" on Kick are separate.
- **Leaderboard:** search, filter by platform, change anyone's points by typing in the box, **Give** points (a minus number takes them away), or **Reset everyone**.

---

## 12. Moderation

**Dashboard → Moderation.**

**Filters** (switch them on first):
- **Block links.** Add **Allowed websites** (e.g. `twitch.tv, youtube.com, clips.twitch.tv`). Mods can type `!permit @name` to let someone post one link.
- **Too many CAPITALS:** a percent of capitals, in messages at least N letters long.
- **Too many symbols:** a percent of symbols.
- **Blocked words or phrases.**
- **Longest message.**

**What happens:**
- **Delete the message** or **Time them out** (for N seconds).
- On **Twitch** this uses your Twitch sign-in.
- On **Kick** Command can only time viewers out, and only with your Kick sign-in.
- On **every** platform the message disappears from your Command overlays at once.
- YouTube and TikTok don't let apps remove messages from the platform itself.

**Never filtered:** you and your mods. You can also tick **Don't filter subscribers / members** and **Don't filter VIPs**.

---

## 13. Sensors

**Dashboard → Sensors** lists the channels you're scanning and how many accounts are flagged. **Open Sensors** opens the full Sensors pages right in the window (← **Command Center** at the top takes you back).

Scan **your channel, or any channel you name**, on Twitch, Kick, YouTube and TikTok:
- **Overview:** viewers now, peak and average, active chatters, messages per minute, chat engagement, followers, and the viewers-over-time chart.
- **Bot and spam flags:** every account gets a 0–100 score with plain-English reasons: selling viewers, promo-spam services, hidden links, look-alike letters, copy-paste waves, rapid-fire, brand-new accounts, follow bursts.
- **Nothing happens on its own.** Each flagged account has an **Options** menu: Ban, Timeout (1m/10m/1h/24h), Warn, Delete their messages, Block, Keep watching, Not a bot, Always allow, Open profile, Copy name. Options a platform doesn't support are greyed out with the reason.
- **Protected accounts:** the channel owner, mods, VIPs and subs/members are never flagged. Helper bots (StreamElements, Nightbot, Streamer.bot, Sery_Bot, Botrix…) are protected by default, and you can edit the list in Sensors → Settings.
- **Lurkers:** silent viewers, known viewer-list bots, viewbot clusters (accounts all made on the same day) and join waves (Twitch and TikTok).
- **All viewers:** everyone in chat, page by page, with **NEW ACCOUNT** and **FIRST VISIT** badges.
- **Deep scan:** returning vs new chatters, top chatters, hype moments with VOD timestamps, trending words, the stream timeline, time per category and **best times to stream**.
- **🎁 Redeems** (Twitch and Kick):
  - **Your own Twitch channel:** every channel point redeem as it happens, straight from Twitch, plus your reward list with prices, cooldowns and limits.
  - **Any other Twitch channel:** redeems that show up in chat (rewards that ask for a message, plus Highlight, Gigantify, Message Effects and Sub-only).
  - **Kick:** reward redeems from Kick's chat.
  - Charts for redeems per day, most redeemed, top redeemers and time of day (last 7, 30 or 90 days, or all time).
  - **💡 Fair prices** (your own Twitch rewards): how long a viewer has to watch to afford each reward, how often it gets used, and a suggested price with the reason.
- **Past broadcasts pull themselves** for Twitch, Kick and YouTube channels: every 12 hours, and 15 minutes after each stream Sensors watches ends. They stay in History after the platform deletes the video. The past-broadcasts box says when it last pulled, or why it couldn't.
- **History:** import your Twitch, Kick, YouTube or TikTok analytics file, pull past broadcasts now, rebuild a Twitch stream's deep scan from its VOD chat, or add streams by hand.
- **TwitchTracker (Twitch channels):** Sensors pulls each Twitch channel's public stats from TwitchTracker the first time you open the channel, then every 6 hours: its rank, its last-30-days averages and its past streams with average and peak viewers, followers and watch time. They go into **History** next to everything else (the **Source** column says **TwitchTracker**). Sensors' own recordings and your analytics files win where both have a number; TwitchTracker fills in the streams they don't have. **History → TwitchTracker → Check again now** checks right away. While you're live, **Overview** shows your 30-day average and Twitch rank, and how this stream compares.
- **Stream reports:** **📄 Export report** (above the History list) lets you choose:
  - **Date range:** pick **From** and **To** dates (or **Last 7 days**, **Last 30 days**, **Last 90 days**, **Last year**, or **A whole month…**). The report has totals, highlights (biggest crowd, longest stream, best day of the week, best time to be live), the TwitchTracker summary, a chart of viewers per stream day, and every stream with its numbers. Each stream has a **Stream report →** link.
  - **One stream:** pick it from the list. Its report has the graphs: viewers, active chatters and lurkers over the whole stream, chat messages minute by minute with the hype moments marked, how it compares with your usual and with your TwitchTracker 30-day numbers, returning vs new chatters, top chatters, time in each category, what chat was saying, raids and what happened when. Streams Sensors didn't watch live (TwitchTracker or past broadcasts only) show their numbers without the graphs.
  - You can also open a single stream's report from **📄** next to it in the History list, or **📄 Report for this stream** on its page.
  - Reports open in your browser. **Print or save as PDF** and **Save this report** (one file you can send to anyone) are at the top. **Spreadsheet** saves the same streams for Excel or Google Sheets. **Export raw data** still saves every minute-by-minute reading.
- **Earnings:** tips, subs, bits, Super Chats, KICKs and TikTok gifts, **only on your own channels** (signed in as that account). Platform amounts are estimates; StreamElements tips sync with your JWT token.
- **Sensor alerts:** viewer spikes with no raid, follow bursts, raids, and very low chat for the viewer count.

**Setting up:** Sensors uses your Twitch and Kick sign-ins from **Connections**, so signing in there is all it needs. YouTube has its own guided Google setup (**Connections → Sensors · YouTube**, or **Sensors → Settings**), with the exact values to copy.

**Your phone:** **Sensors → Settings → Phone**, turn it on, then scan the QR code (or type the PIN) on a phone on the same Wi-Fi.

Sensors keeps its own address, **http://localhost:7490**, so the redirect URLs in your Twitch, Kick and Google developer apps stay the same.

---

## 14. OBS & Stream Deck, Music and Chat overlay

Everything from Hyperwave Station 2.0 is built in, as three tools under **Hyperwave tools** in the menu.

**▦ OBS & Stream Deck** is its own Command Center page:
1. **OBS:** the connection itself is on **Connections → OBS**. This page has the **Clip** settings: keep the replay buffer running, save the replay to your PC, also make a Twitch clip, and the Streamer.bot action used for Twitch clips.
2. **Chat on the deck:** the deck shows chat from every platform you've connected on Connections (the same chat as the Command Center page and the chat dock). Add your **quick replies** here (one per line, up to 12). Where replies are posted from is **Connections → Chat replies**.
3. **Phones and tablets:** tick **Let phones and tablets on my Wi-Fi open the deck**, then scan the QR code. With **Show advanced settings** on, you can also type or generate your own **deck passkey** (6–64 letters, numbers, dashes or underscores) and change the port (default `7582`).
4. **Sounds:** **Add the sound player to all my OBS scenes** adds the invisible **Hyperwave Sounds** browser source. **Play a test beep** checks it.
5. **Change your category:** shows whether Twitch and Kick are ready (signed in on Connections).
6. **Elgato Stream Deck:** pick what the button does, copy the link, then in the Stream Deck app use **System → Website** with **GET request in background** ticked.

**Open the Hyperwave Deck ↗** is at the top of the page.

**♫ Music** opens the Music pages: your music source (picked in the **Music** box on Connections), the **Now Playing** overlay and designer, **song requests** with rules, **song request replies**, **commands without a bot**, **Streamer.bot commands** and **Remote DJ** (a mod runs your music from their phone).

**Song requests in chat:** see **Chatbot → ♫ Song requests** (section 9).

**"Now playing" messages** (bottom of the Music page):
- **Hide "Now playing" in my chat overlay** stops every Hyperwave Chat overlay from showing each new song (song requests still show). Each chat design also has its own **Announce each new song** switch.
- **Say each new song in chat** posts your "Now playing" line (reworded under **Song request replies**) a few seconds after a song starts, so skipping through songs doesn't flood chat. **Post it in** every platform you're streaming on, or just Twitch, Kick or YouTube. It only posts while you're live unless you tick **Also when I'm not live**. Kick and YouTube posts go through Streamer.bot; TikTok doesn't let apps post.

**Platform logos in chat:** the Hyperwave Chat designer's **Platform marker** has **Round logo** (the default now), Name tag, Colored dot or Hidden. The logos are drawn at the size of the chat text, so they grow and shrink with it. If your OBS link was made before 0.9.0, pick **Round logo** and copy the link again.

**💬 Chat overlay** is its own page:
1. Click **Open the chat designer ↗**, pick a look, drag the chat where you want it, and click **Copy link**.
2. In OBS: **+** under Sources → **Browser** → OK. Paste the link into **URL**, Width `1920`, Height `1080`, OK.

Changed the design? **Copy link** again and paste it into the same source. If your **Main HUD** overlay (which has its own chat box) is in OBS too, click **Take the chat out of my Main HUD** so chat doesn't show twice. Rather have one source for everything? **Other way** puts your design inside the Main HUD instead.

In the designer, under **Chat sources**, set **YouTube** and **TikTok** to **Through Hyperwave Command Center** (the default for new designs) to show the YouTube and TikTok chat Command Center reads itself. That's **watch only**: those messages show on your overlay, but nothing is posted back to YouTube or TikTok (posting in YouTube chat needs Streamer.bot; TikTok doesn't allow it at all). Command Center has to be running for them to show.

The full guide is in `docs/Music-Deck-DJ-Guide.md`.

> **Spotify users:** Command uses port 7580, so add `http://127.0.0.1:7580/callback` as an extra **Redirect URI** in your Spotify developer app (keep Station's 7575 one if you still use Station).

---

## 15. Coming from Hyperwave Station or Hyperwave Sensors

**Settings → Bring over Hyperwave Station or Hyperwave Sensors** moves your whole setup in one click.

1. Open **Settings**. Command Center lists every copy of Station and Sensors it finds on this PC, with what's in each (channels, deck buttons, pictures and sounds, layouts, history).
2. Click **Bring it over** next to the one you want.
   - Not listed? Click **Pick a Station or Sensors folder…** and choose the folder Station or Sensors runs from, or **Pick a Station backup (.zip)…** for a backup made in Station's Settings.
3. Command Center saves a copy of your current setup (in `command-data\backups`), brings everything over, and restarts for a few seconds.

The Command Center page also shows a **bring your setup over** link when it finds Station or Sensors you haven't brought over yet. Your own Command Center settings, alerts, overlays and chatbot stay as they are.

### Hyperwave Station

- **What comes over:**
  - channel names
  - OBS, Streamer.bot and TikFinity settings
  - your music choice and your **Spotify sign-in**
  - song request rules and chat replies
  - deck buttons, launchers and quick messages
  - Remote DJ settings
  - your deck pictures and sounds
  - saved chat and music layouts
- **Sign in to Twitch and Kick once on Connections.** Command Center asks for a few more permissions than Station did (alerts and mod tools), so Station's Twitch and Kick sign-ins can't be reused.
- Command Center looks for Station in its own folder, the folder next to it, `C:\Hyperwave\` (where Station's installer puts it), `%APPDATA%\HyperwaveStation`, and `Hyperwave` folders on your Desktop, Downloads and Documents.
- **Hyperwave Station 3.0 and later** are music only, but they keep your old deck, OBS, Streamer.bot and chat settings in their settings file, so everything above still comes over.
- Command uses ports **7580 / 7581 / 7582** and Station uses **7575 / 7576 / 7577**, so you can run both while you test.
- **When Station isn't running,** Command Center also answers on Station's overlay address (`127.0.0.1:7575`), so chat and Now Playing browser sources made for Station keep working without changes.
- Streamer.bot actions that send requests to Station (port **7575**, e.g. `/api/sr` for song requests) should be changed to `7580` when you switch over for good.

### Hyperwave Sensors

- **Close the standalone Sensors app first.** The first time Command Center starts, it brings over Sensors from `%APPDATA%\HyperwaveSensors` by itself (it copies it, so the old app still works if you go back).
- Kept Sensors somewhere else? Use **Settings → Pick a Station or Sensors folder…** and choose the folder with Sensors' `config.json` and `data` folder in it.
- **What comes over:** your channels, sign-ins, developer apps and YouTube setup, detection settings and protected names, paired phones, earnings settings, and all your history (readings, past streams, imports and earnings). Channels already in Command Center's Sensors are kept too.
- Sensors keeps its address (`localhost:7490`), so your developer apps and paired phones work as before.
- Sensors Lite (the phone-only web app) is separate and keeps working on its own.

---

## 16. Firing alerts from other apps

Any app on your PC can fire a real alert by opening one address, for example Streamer.bot (**Sub-actions → Core → Network → Fetch URL**), a PayPal notification tool, or your own script:

```
http://127.0.0.1:7580/api/events/fire?kind=tip&user=Name&amount=5&currency=USD&message=Thanks!&platform=paypal
```

| Setting | Values |
|---|---|
| `kind` | `follow` `sub` `giftsub` `cheer` `raid` `tip` `superchat` `redeem` `tiktokgift` `share` `like` |
| `user` | the name to show |
| `amount` | bits, viewers, gift count, money… |
| `currency` | `USD`, `EUR`, `GBP`… (for tips) |
| `months`, `tier`, `item`, `message` | optional |
| `platform` | any word, shown as the source (e.g. `paypal`) |
| `avatar` | optional `https://` link to a profile picture |
| `id` | optional unique id. The same id twice only alerts once. |

These count in your stats, credits and points like any other event. Use the **Test** buttons for pretend ones.

---

## 17. Where your settings live, and backups

Next to the app (or in `%APPDATA%\HyperwaveCommand` if that folder is read-only):

| File / folder | Holds |
|---|---|
| `hyperwave-command.json` | connections, sign-ins, music and deck settings |
| `command-data\alerts.json` | your alert designs |
| `command-data\overlays.json` | your overlays and widgets |
| `command-data\bot.json` | commands, timers, thank-you messages, chat modules, points and filter settings |
| `command-data\points.json` | everyone's loyalty points |
| `command-data\events.json` | recent events and this session's counts |
| `hyperwave-media\` | your uploaded pictures, videos and sounds |
| `command-data\sensors\` | Sensors' settings and sign-ins (`config.json`) and its history, stream summaries and earnings (`data\`) |
| `overlays\` | the Station chat and Now Playing overlays that run without the app |
| `hyperwave-command.log` | what the Console page shows (the last run is `hyperwave-command.old.log`) |

**Backup:** copy those files and folders somewhere safe. To move to a new PC, copy them next to the app there. `hyperwave-command.json` holds your sign-ins, so **don't share it**.


### Backup and restore

**Settings → Backup and restore.**
- **⬇ Save a backup** downloads one zip, `HyperwaveCommand-backup-DATE.zip`, with your settings and sign-ins, alerts, overlays, chatbot, chat modules, loyalty points, Sensors settings and history, deck buttons, your pictures, videos and sounds, scene layouts and the About file. **It holds your sign-ins, so keep it private.**
- **⬆ Restore a backup…** puts it all back and restarts Command. A copy of what you had is saved first in `command-data\backups`.

Moving to a new PC:
1. Install with the updater.
2. Open **Settings → Restore a backup…**.

### Share your setup

**Settings → Share your setup.**
- **⬇ Save my setup to a file** saves how everything looks and works: alerts, overlays, chatbot, chat modules, giveaway, Chaos wheel, counters, deck buttons, song request rules and replies, and your pictures and sounds. **No sign-ins, passwords, channel names, viewers' points or history go in it**, so you can give it to another streamer.
- **⬆ Load a setup file…** puts those parts in place (your own connections and points stay), after saving a backup of what you had in `command-data\backups`, and restarts Command. Only load setups from people you trust.

### Copy diagnostics

**Settings → Need help? → 📋 Copy diagnostics** copies a help report: your version, connection lights, settings and the last 300 log lines. Passwords, keys, passkeys and sign-ins are replaced with `(hidden)`. Paste it into the feedback form or a message. **Show it** lets you read it first.

---

## 18. Ports and safety

| Port | Used for | Who can reach it |
|---|---|---|
| **7580** | dashboard, overlays, studio, live events | this PC only |
| **7581** | Remote DJ (only through the DJ tunnel, with the DJ passkey) | off until you open DJ access |
| **7582** | Wi-Fi deck for phones (with the deck passkey) | off until you turn it on |
| **7490** | Sensors (and paired phones on your Wi-Fi) | this PC; paired phones on your home network once you turn Phone on |
| **7575** | Station's old overlay address, only while Station isn't running | this PC only, overlays only |

Command keeps Hyperwave Station's protections:
- Only Command's own pages and OBS can use the dashboard and live events. Other websites are blocked, including through tricks like DNS rebinding and hidden frames.
- Everything people type (chat, names, tip messages) is shown as plain text and can never run as code in your overlays.
- Pictures and sounds load only from your own uploads or `https://` links.
- Twitch and Kick sign-ins use the official sign-in pages. Command never sees your password.

---

## 19. Troubleshooting

| Problem | Fix |
|---|---|
| Overlay is blank in OBS | Check Command Center is running (its icon is in the tray). Open the overlay link in your browser: a note in the corner says what's wrong (these notes never show inside OBS). |
| Overlays stopped working after an update | You don't need new links: they never change between versions. Right-click the source in OBS → **Properties** → **Refresh cache of current page**. To stop it happening, start Command Center before OBS (**Settings → Start with Windows**), and always update with the built-in updater or into the same folder (your settings live next to `HyperwaveCommand.exe`, so a new folder starts an empty setup). |
| Test alerts don't show in OBS | Read the line under **Send a test to OBS**: it says what's wrong. **Nothing showed it** means no overlay is open: add a Browser source with your overlay link (or `http://127.0.0.1:7580/alerts`, 1920 × 1080), and make sure OBS runs on the same PC. **No OBS source got it** means the Browser source is hidden, in another scene, or needs a right-click → **Refresh**. |
| No sound from alerts on stream | Sounds play from the alerts Browser source in OBS. Tick **Control audio via OBS** in its Properties (or click **Turn it on for me** in the Alerts page's 🔊 Sound box), and check it isn't muted in the Audio Mixer. |
| A greeting doesn't post in chat | Click **Test** on that person: it says whether the chat post worked and why not (usually the Twitch sign-in or **Connections → Chat replies**). Each person is greeted once per stream; **Greet again** resets it. |
| Twitch alerts don't arrive | **Connections → Twitch** should show **✓ Listening for:** with your events. If it lists **Not available**, click **Sign in again** to give Command the missing permission. |
| "Twitch refused every event" | Your sign-in is from another app or has expired. Click **Sign in again**. |
| Kick chat works but no Kick alerts | Paste your **Channel ID** (see section 5). Kick's follow alerts depend on Kick sending them, which isn't guaranteed. |
| YouTube says "can't reach Streamer.bot" | Start Streamer.bot's WebSocket Server, then check the port and password match. |
| YouTube chat is empty | YouTube only sends chat while a broadcast is live and Streamer.bot is connected to it. |
| TikTok says "can't reach TikFinity" | Open TikFinity, connect it to your LIVE, and check the port matches (default `21213`). |
| Bot doesn't answer on Twitch | **Chatbot → Try it & log**: the log shows the reason. Usually you need to sign in to Twitch, or switch **Chat replies** to Streamer.bot. |
| Bot doesn't answer on Kick | Sign in to Kick (Connections → Kick step 2), or turn on Streamer.bot with Kick connected there. |
| "Port 7580 is busy" / nothing happens when I start it | Command Center is already running. Starting it again brings its window to the front; if not, click its icon in the tray (by the clock). |
| I closed the window and the overlays still work | That's on purpose: Command Center keeps running in the tray. Right-click the tray icon → **Quit Command Center** to stop it. |
| It opens in the browser instead of its own window | Install the Microsoft Edge WebView2 runtime (see **The window and the tray icon** in section 2), then start Command Center again. |
| Sensors says port 7490 is in use | The standalone Hyperwave Sensors app is still open. Close it, then quit Command Center from the tray and start it again. |
| A sign-in opened my browser and I'm back in Command Center | That's normal: finish the sign-in in the browser. The page in Command Center shows you're connected when you refresh it. |
| The stream preview is black or says OBS didn't send a picture | Check **OBS** is green on Connections. A scene with nothing visible (or only a game capture OBS can't see yet) shows black. Untick **Show** if you don't need it. |
| Channel points says "Sign in again" | Twitch and Kick need one fresh sign-in after 0.4.0-beta to allow channel points. Click **Sign in again** on Connections. |
| StreamElements or Streamlabs says it didn't accept the token | Copy the token again (StreamElements makes a new JWT when you reset it) and paste it, then **Save**. |
| TwitchTracker says it's busy or blocked the request | TwitchTracker sometimes turns apps away for a while. Sensors tries again every 6 hours; everything else in History keeps working. |
| The TwitchTracker box says it couldn't read the page | TwitchTracker changed its page. Click **Save what TwitchTracker sent** and send the file to TaiiRepublic. |
| TwitchTracker doesn't know a channel | It only tracks channels after they've streamed. Check again after the next stream. |
| Redeeming the giveaway reward doesn't enter anyone | Sign in to Twitch on **Connections**, and type the reward's title on the **Giveaways** page (step 2) exactly as it is on Twitch. Entries only count while a giveaway is open. |
| `!timer` does nothing | Check the **Chat timer** switch is on and who can use it (Mods by default). Viewers who can't use it are ignored quietly. |
| The giveaway wheel or timer makes no sound | Sounds play from the overlay's own Browser source. In OBS, tick **Control audio via OBS** on it and check it isn't muted in the Audio Mixer. |
| Windows SmartScreen warning | **More info → Run anyway**. |
| Fonts look plain | Chakra Petch and Inter are built in. Other fonts load from Google Fonts and need internet. |

---

## 20. Version numbers and updates

Command uses **MAJOR.MINOR.PATCH**:

- **PATCH** (0.1.0 → **0.1.1**): fixes and small polish only.
- **MINOR** (0.1.x → **0.2.0**): new features or pages. Your settings carry over.
- **MAJOR** (0.x → **1.0.0**): the first stable public release, and later any change that needs setting up again.
- `-alpha` / `-beta` on the end means a test build.

Every update gets an entry in `CHANGELOG.md` and on the dashboard's **What's new** page.

### Updating

Command Center checks **github.com/TaiiRepublic/Hyperwave-Command** for new versions when it starts and every six hours.
- **Version in the menu:** under the app name. It's **green** when you're up to date. It's **red** when a new version is out, with a red **"vX is out · Update"** link under it. The **tray icon** gets a red dot and an **Update to Command Center …** item too.
- **Update box:** when a new version is out, a box pops up as Command Center starts, with what's new, **Update now** and **Later**. **Later** waits until the next time you start Command Center. The same notes stay on the **Command Center** page as a card.
- **Window closed?** Windows shows a notification from the tray icon. Click it to open Command Center.
- **Update now** downloads the release, checks the download, swaps in the new version and restarts by itself. The window reloads on the new version.
- **If you're live**, it asks first, because overlays blank out for a few seconds while it restarts.
- **Never touched:** settings, sign-ins, alerts, overlays, points, Sensors history, uploads and the `web` folder.
- **Settings → Updates:** turn the checks off, **Check now**, open the releases on GitHub, or download the updater.
- **On an older version or a new PC?** Download **HyperwaveCommandUpdater.exe** and double-click it. It finds your install (or asks where), closes a running copy, installs the newest version, keeps your settings and starts it again.

---

## 21. Roadmap

Ideas for the next beta builds, roughly in order. Each one gets its own version number when it ships.

- **First-run wizard** that walks through Connections, adds the overlay to OBS for you (through the OBS connection), and fires a test.
- **Text-to-speech** for tips and cheers, with a word filter and a minimum amount.
- **Giveaways:** keyword entry from all four chats, points tickets, a fair draw with a winner alert.
- **Chat games:** bring Homeworld Fleet Battles, trivia and Phasmo betting into the bot, with points.
- **Custom widgets:** paste your own HTML/CSS/JS as a sandboxed widget, then share widget and overlay **theme packs** (one file with the overlay, alerts and pictures).
- **Hyperwave Cloud (optional):** a hosted relay so the bot and overlays keep running when your PC is off. It would also handle official Kick webhooks, a public tip page through a payment provider (Stripe or PayPal handle the money), and Streamer.bot-free YouTube. This needs hosting costs and real security work, so it comes after the local app is solid.

---

## 22. Credits and licences

Made by **TaiiRepublic**: twitch.tv/taiirepublic · kick.com/taiirepublic. o7

**Special thanks** to the streamers who helped beta test Hyperwave Command Center before its full launch: **RyanOmightyTV**, **sloth_gaming216**, **rezomonn** and **BoxofRabbitz**. They're on the dashboard's **About** page too. o7

- Includes Hyperwave Station 2.0 and Hyperwave Sensors.
- Fonts: **Chakra Petch** and **Inter**, SIL Open Font License 1.1 (see `licenses/`).
- Open-source components and their licences are listed in `licenses/THIRD-PARTY-NOTICES.txt`.
- Free to use; see `LICENSE.txt`.
- Homeworld is a trademark of its owners. Hyperwave Command Center is a fan-made, unofficial tool and isn't affiliated with or endorsed by them.
