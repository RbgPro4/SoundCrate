<p align="center">
  <img src="img/SoundCrate_Logo.png" width="120" alt="SoundCrate logo">
</p>

<h1 align="center">SoundCrate</h1>
<p align="center">A local music player for the music you own, with optional support for your own server.</p>

<p align="center">
  <a href="https://github.com/RbgPro4/SoundCrate/releases/latest"><b>⬇ Download for Windows</b></a>
</p>

<p align="center">
  <img src="https://img.shields.io/github/v/release/RbgPro4/SoundCrate" alt="Latest version">
</p>

## Highlights

- 🎵 **Local or streamed:** open a music folder (each subfolder becomes a library, and an `.m3u8` inside sets the track order) or connect to your own SoundCrate server.
- 📶 **Offline login:** songs cached on disk keep playing when the server is off.
- 🎚️ **Sound:** 8 or 15-band equalizer with saved presets, crossfade, fade in/out, volume normalization and output device selection.
- 🏷️ **Hi-res aware:** reads ID3, FLAC, MP4 and WAV tags and cover art, with colour-coded quality badges by sample rate and bit depth.
- ⚡ **Built for huge libraries:** preloads neighbouring songs, caches in RAM or on disk, and plays multi-GB files from a disk cache with seeking.
- 🗂️ **Built-in organizer:** reorder, number files (`01 - Name`), sort, shuffle, undo/redo and write `.m3u8` playlists, on local folders and on the server.
- 🏠 **Home page and Favorites:** recently played, most played, and hearted songs kept separately for local and each server.
- 🪟 **Desktop integration:** floating mini player, system tray menu, taskbar media buttons and auto-update from GitHub Releases.
- 🎨 **Customizable:** 5 themes, frosted-glass UI, ambient cover glow, Away Mode and a Sleep Mode timer.

## Full feature list

<details>
<summary><b>Sources and connections</b></summary>

- **Open a folder:** each subfolder becomes a library, and an `.m3u8` inside sets its track order. Nested folders such as `Album/Disc 1/song.flac` work.
- **Connect to a server:** name, IP, port and password. The app checks the server version first, and if the server is still indexing it waits and continues on its own.
- **Live library updates:** the server pushes events, so a "new library" card with a progress bar appears as soon as a folder starts arriving. Auto-refresh can load changes without interrupting playback.
- **Saved servers and folders:** the start screen shows "pick up where you left off" cards. Server passwords are encrypted with the OS keychain.
- **Offline login:** with the server off, open the last saved library list. Songs cached on disk stay playable and everything else is greyed out. There is also a manual offline mode.
- **Connection watchdog:** detects server restarts and shows "Connection lost / Reconnecting…".
- **Held libraries:** if a library leaves the server while playing, its already buffered songs keep playing until you refresh.
- **Remember Startup:** reconnects to the last server or reopens the last folder at launch.
- **Formats:** mp3, flac, wav, m4a, aac, ogg, wma, opus. Tags and cover art are read from ID3, FLAC, MP4 and WAV, in worker threads so the UI stays smooth.

</details>

<details>
<summary><b>Playback and sound</b></summary>

- Play/pause, previous/next, shuffle (with history), repeat (off / all / one), seek and volume.
- Autoplay next track and an "Up Next" queue.
- Full-screen player with a spinning-disk cover that eases up and down like a turntable.
- Fade in/out and crossfade, each with adjustable length.
- Volume normalization: Disabled, Lower, Normal, Loud.
- Audio output device selection.
- **Equalizer:** 8 or 15 bands, each keeping its own curve, with saved presets (Save as, Update, Delete, Reset).
- Muffled "underwater" fade-out when the app closes.
- Quick-settings panel for output, normalization, EQ and autoplay.

</details>

<details>
<summary><b>Library, browsing and organizing</b></summary>

- **Home page:** time-of-day greeting, now playing, library overview stats, "Jump back in", Recently played and Most played.
- **Favorites:** a heart on every song. Local and per-server favorites are kept separate, and a favorite survives a renumbered file.
- **Track list:** windowed rendering for huge libraries, with Title, Quality, Format, Cached, Size and Time columns that can be reordered and hidden.
- **Quality badges:** colour-coded tiers for FLAC, WAV and lossless M4A by sample rate and bit depth.
- **Search:** libraries and tracks, with scroll to the first match and a "follow now playing" auto-scroll.
- **Rename:** libraries and songs, as display names only. Files on disk are not changed.
- **Organizer** (right-click a library, then *Organize This Library*):
  - drag, ▲▼ or type-a-position reordering
  - Sort A–Z, Shuffle, Undo and Redo
  - Apply sequence (`01 - Name`), Apply changed only, Clear numbering
  - Create or update an `.m3u8` playlist
  - nothing touches the disk until you press Apply
  - works on local folders and on servers

</details>

<details>
<summary><b>Caching and streaming</b></summary>

- Preloads 0 to 8 songs on each side of the playing one, with a speed limit.
- Song cache in **RAM or on disk**, with a RAM limit (500 MB to 10 GB) and a disk limit (2 to 100 GB). The least recently used songs are removed first.
- **Keep songs on disk**, set globally or per library.
- Pre-buffer an entire playlist, or cache a single song.
- **Big-file cache:** huge songs (100 MB to 2 GB+) play from a cache file on disk with seeking anywhere, and can be fully cached in the background.
- Server library cache for tags and covers, with covers shrunk once into small thumbnails.
- Move the cache folder with progress and cancel.
- Storage page showing what uses space, with quick clean-up.

</details>

<details>
<summary><b>Desktop integration</b></summary>

- **Floating mini player:** frameless, resizable, with a keep-on-top pin. The audio stays in the main window.
- **System tray:** now playing, play/pause, previous/next, shuffle, repeat, mini player, hide/show, check for updates and quit. On Windows it uses a custom styled menu.
- **Taskbar thumbnail buttons** (Windows): previous, play/pause, next.
- **Auto-update** through GitHub Releases. Nothing downloads without asking, then choose *Restart now* or *Later*.
- Graceful shutdown: saves settings and disconnects from the server before closing.
- Single-instance lock, so a second copy can't fight over the same data folder.
- First-run welcome guide and a searchable Settings page.

</details>

<details>
<summary><b>Appearance and performance</b></summary>

- **Themes:** Rose (default), Ember, Violet, Abyss, Crimson.
- **UI look:** Plain or Frosted Glass, with frost intensity and per-area toggles (sidebar, Home cards, Settings, mini player).
- **Ambient glow:** the playing track's blurred artwork behind the UI, with brightness, dim-when-paused and brighter-while-playing controls.
- Fixed or scrolling header, square or spinning-disk mini player artwork, and Reduce Motion.
- **Quality / Performance mode**, **Resource Saver** (unloads parts you are not looking at) and a **hardware acceleration** toggle.
- **Away Mode:** the app sleeps when idle to save memory and CPU, with an adjustable delay and an option to keep the player running.
- **Sleep Mode:** a timer that dims the screen and fades out the music.
- Activity Log and an expandable console.

</details>
