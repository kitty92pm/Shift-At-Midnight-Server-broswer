# Shift-At-Midnight-Server-broswer
A Steam-based public lobby browser for Shift - At - Midnight, built with MelonLoader. Adds a full in-game OnGUI server browser — create, host, and join public lobbies directly from within the game.


# Shift - At - Midnight | Server Browser

A **MelonLoader** mod that adds a fully functional **Steam server browser** to *Shift - At - Midnight*.  
Host public lobbies, browse available servers, and join them seamlessly — all through an in-game GUI.

---

##  Features

-  **Public Lobby Browser**
  - Displays all public lobbies hosted through Steam.
  - Auto-refreshes every few seconds for live updates.

-  **Host Public Servers**
  - Create a lobby that others can instantly discover.
  - Default lobby name uses your Steam display name (e.g. `Aledex's Room`).

-  **Player List**
  - View all players currently connected to your lobby.

-  **Simple & Stable**
  - No external servers or APIs — 100% Steam Matchmaking.
  - Host can stop hosting manually.
  - Clients cannot leave manually (must exit through the game).

-  **Integrated GUI**
  - Built using Unity’s `OnGUI` system.
  - Press **F2** in-game to open or close the browser.

---

##  How It Works

This mod uses the **Steamworks.NET** API via MelonLoader to interact with the game’s existing Steam P2P system.  
It simply exposes that system with a clean UI:

1. **Hosting:**  
   - Creates a Steam public lobby using `SteamMatchmaking.CreateLobby()`.  
   - Sets basic metadata (`name`, `host`).

2. **Browsing:**  
   - Calls `SteamMatchmaking.RequestLobbyList()` to show all available public rooms.  
   - Lets players click **Join** to instantly connect.

3. **Player Management:**  
   - Lists everyone inside the lobby using `SteamMatchmaking.GetNumLobbyMembers()`.

---

##  Controls

| Key | Action |
|-----|---------|
| **F2** | Toggle Server Browser |
| **Tab: Browse** | See public lobbies and join them |
| **Tab: Host** | Create and manage your public lobby |
| **Tab: Players** | View connected players |
| **Host Only** | Can stop hosting |
| **Clients** | Cannot leave manually; must exit game |

---

## ⚙️ Installation

### Requirements
- [MelonLoader 0.7.1+](https://melonwiki.xyz/)
- A copy of **Shift - At - Midnight** (Steam version)
- Steam running in the background

### Steps
1. Install MelonLoader into the game directory.  
2. Build or download the compiled DLL  
3. Place the DLL into the mods folder of your steam games path

4. Launch the game.  
5. Press **F2** in-game to open the browser.
