![Bkups mod by Blanq_Ky and TrasTick](https://cdn.modrinth.com/data/cached_images/8b3c744947d1aacec3b2728700cd95993f860315.png)
# Why Bkups?
- Comes with a GUI that will help you through out the mod
- Four different types of backups
- Many ways to protect your world or server
- Lots of option to have your own personal customization
- No cheats on needed
- Install and Play!
# Backup Manager (GUI)
![backup manager](https://cdn.modrinth.com/data/cached_images/9f8dd5b9c83516c3ba58e19548c92bc0abcd4f68.png)
![gifs](https://cdn.modrinth.com/data/cached_images/5a59314370101cf38800cff6797b3ae2f61e269c.gif)

## Types of Backups
![Types of backups](https://cdn.modrinth.com/data/cached_images/0073e581693fc11fdaa4f4f46bdacc0d33f16f07.png)
- **Manual:** this backup is made by the player manually
- **Auto:** this backup is made automatically according to the settings you've set
- **Exit:** this backup is made whenever you leave the world you're in
- **Legacy:** this type of backups are the ones that are created with the minecraft settings
## The Trash
To access the trash, click on the trash button in Backup Manager. All your deleted backups will appear here **if you have the trash enabled** (`/bkup trash on`).
![trash](https://cdn.modrinth.com/data/cached_images/4829b96d49e8f657b27d285faf1e724885864ae0_0.webp)
From the trash, you can **permanently delete** the backup and **recover** it.
## Favorites
You can add your backups to your favorites. The advantages are:
- Your backup will not be deleted by auto-cleanup
- Better visibility of your backups
## Tree Structure
The tree structure works to view backups easily (not working in 1.21.9-1.21.11)
# Commands
- `/bk [custom_name]` If you want to make a manual backup (`[custom_name]` it's used to name the backup)
- `/bkup <subcomand>` To do a lot of option to customization, **more about it bellow**
<details>
<summary>Subcommands</summary>


| Command | Description |
| :--- | :--- |
| `/bkup fav <file>` | Marks a backup as favorite (safe from auto-delete) |
| `/bkup unfav <file>` | Unmarks a backup (can be auto-deleted) |
| `/bkup delete <file>` | Deletes a backup (or moves to trash if enabled) |
| `/bkup auto <on/off>` | Toggles automatic backups |
| `/bkup exit <on/off>` | Toggles backup when stopping the server or leaving the world |
| `/bkup storage <lim> <type>` | Sets retention limit to gb and backups (e.g. `5 gb` or `10 backups`) |
| `/bkup trash <options>` | Manages trash system (`on`, `off`, `clear`, `recover`) |
| `/bkup compression <mode>` | Sets compression to `fast` (larger) or `heavy` (smaller) |
| `/bkup path <path>` | Changes the backup folder location |
| `/bkup config <options>` | Toggles chat notifications and progress bar |
| `/bkup admin <player>` | Grants backup permissions to non-OP players |
| `/bkup unadmin <player>` | Remove backup permissions to non-OP players |
| `/bkup status` | Shows current settings and disk usage |
| `/bkup help` | Displays the full command list in-game |


<details>
<summary>Detailed</summary>

| Command | Description |
| :--- | :--- |
| **Manual Backups** | |
| `/bk` | Creates an instant backup with a default name. |
| `/bk [custom_name]` | Creates a backup with a specific name (e.g., `/bk BossFight`). |
| **Restore & Manage** | |
| `/bkup restore <file>` | Restores a specific backup and restarts the server/world. |
| `/bkup delete <file>` | Deletes a backup. Moves it to Trash if enabled. |
| `/bkup fav <file>` | Marks as **[Fav]**. Protects file from auto-cleanup limits. |
| `/bkup unfav <file>` | Unmarks as favorite. File can now be auto-deleted. |
| **Automation** | |
| `/bkup auto on` | Enables auto-backups every 60 minutes. |
| `/bkup auto on <min>` | Enables auto-backups with a custom interval (e.g., `30`). |
| `/bkup auto off` | Disables automatic backups completely. |
| `/bkup exit on` | Enables backup when stopping the server (always). |
| `/bkup exit on <min>` | Enables exit backup only if session > `<min>` minutes. |
| `/bkup exit off` | Disables backups on server stop. |
| **Storage Limits** | |
| `/bkup storage <num> gb` | Sets limit by size (e.g., `5 gb`). Deletes oldest files when full. |
| `/bkup storage <num> backups`| Sets limit by quantity (e.g., `20 backups`). |
| **Trash System** | |
| `/bkup trash on` | Enables Trash. Deleted files stay for 24 hours. |
| `/bkup trash on <num> hours` | Custom Trash: Files expire after `<num>` hours. |
| `/bkup trash on <num> backups`| Custom Trash: Keeps a batch of `<num>` deleted files. |
| `/bkup trash on <num> accumulated`| Custom Trash: Rolling buffer of `<num>` deleted files. |
| `/bkup trash off` | Disables Trash. Files are deleted permanently instantly. |
| `/bkup trash clear` | Instantly empties the trash folder. |
| `/bkup trash recover <file>` | Restores a deleted file from Trash to the active folder. |
| **Technical Settings** | |
| `/bkup compression fast` | **Level 1**: Fastest backup speed, larger file size. |
| `/bkup compression heavy` | **Level 9**: Best compression, smaller file size (slower). |
| `/bkup path <path>` | Changes backup folder location (e.g., `D:/Backups`). |
| `/bkup path reset` | Resets storage folder to default (`/bkups`). |
| **Notifications & UI** | |
| `/bkup config noti on` | Reminds you to backup if you haven't in 3 hours. |
| `/bkup config noti on <hours>`| Sets custom reminder interval. |
| `/bkup config noti off` | Disables "long session" warnings. |
| `/bkup config progress show` | Shows the boss-bar progress on top of screen. |
| `/bkup config progress hide` | Hides the progress bar. |
| `/bkup config all hide mute` | Hides chat messages and mutes sounds for ALL backups. |
| **Admin & Info** | |
| `/bkup admin <player>` | Allows a player to use backup commands without OP. |
| `/bkup unadmin <player>` | Revokes backup privileges. |
| `/bkup status` | Prints current config, disk usage, and stats to chat. |
| `/bkup help` | Shows the main help menu. |

</details>



</details>



# How does Bkups work?
## How are folders created
Bkups creates a folder in `.minecraft\bkups` if any bkup is created (excluding legacy ones, they are stored in `.minecraft\backups`, wich is the vanilla minecraft folder)

Following this logic, if only one backup has been created in `.minecraft\bkups\manual` it will only be create in that specific folder
## Backups to World
When a backup is created, bkup compress the world in a .zip, this .zip is later decompress after restaured

The command `/bkup compression <mode>` changes the way in wich the folders .zip are stored
# Road Map
- Forge and NeoForge
- Fix [known bugs](https://github.com/BlanqKy/bkups/issues)
- Make all versions as similar as possible
# Credits
- Blanq_Ky: Mod and versions development, project lead
- TrasTick: Responsible for descriptions on CurseForge and Modrinth pages
