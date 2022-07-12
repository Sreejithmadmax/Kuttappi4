
## Whats new
- MegaDL added
- Overall download and upload progress.
- Pixeldrain DL support.
- Alert on when the bot boots up.


### ***Compulsory Vars***

- `API_HASH`
  - Values :- Valid API HASH obtained from Telegram.
  - Default Value :- `""`
  - Use :- To connect to Telegram.

- `API_ID`
  - Values :- Valid API ID obtained from Telegram.
  - Default Value :- `0`
  - Use :- To connect to Telegram.

- `BOT_TOKEN`
  - Values :- Valid BOT TOKEN Obtained from Botfather.
  - Default Value :- `""`
  - Use :- To connect to Telegram as BOT.

- `BASE_URL_OF_BOT`
  - Values :- Valid BASE URL of where the bot is deploy. Ip/domain of your bot like "http://myip" or if oy have chosen other port then 80 then "http://myip:port". No slash at the end.
  - Default Value :- `""`
  - Use :- This is used for file selection of the torrent.

- `ALD_USR`
  - Values :- It is a list of IDs of all the allowed groups and useres who can use this bot in private. 
    - To supply multiple IDs in ExecVarsSample.py seperate by comma ','. 
    - To supply multiple IDs from Environemnt variable seperate by spaces.
  - Default Value :- `[]` 
  - Use :- Users and groups with ids here can use the bot.

- `DATABASE_URL` = 
  - Values :- Postgres database URL. Just replace your credentials from below. OR directly Paste the URI you obtained from a database hosting or somewhere else.
  - Default Value :- `dbname=tortk user=postgres password=your-pass host=127.0.0.1 port=5432`
  - Use :- Used to connect to DB. DB is used for many stuff in this bot. 

- `OWNER_ID` = 
  - Values :- Owner's ID
  - Default Value :- `0`
  - Use :- Used to restrict use of certain stuff to owner only. 
### ***Optional Vars***
- `GD_INDEX_URL`
  - Values :- Base URL of the index that you are using. (Now that you should include the directory also in URL if you have set `RCLONE_BASE_DIR`). (Dosen't matter if a slash is at the end or not)
  - Default Value :- `False`
  - Use :- Provides an addition Index link for Google Drive Upload.

- `EDIT_SLEEP_SECS`
  - Values :- Seconds to Sleep before edits. Recommended is 40. (If you are using the bot for your own you can try 10 if you get FloodWait Error in LOGS then increase the value) [Can be set from settings menu]
  - Default Value :- `40`
  - Use :- The bot will update the progress regulary after these number of seconds.

- `TG_UP_LIMIT`
  - Values :- Telegram Upload limit in bytes. (you can set max `2147483648` which is ~2GB) [Can be set from settings menu]
  - Default Value :- `1700000000`
  - Use :- The bot will use this value to automatically slice the file bigger that this size into small parts to upload to Telegram.

- `FORCE_DOCUMENTS`
  - Values :- `True`/`False` [Can be set from settings menu]
  - Default Value :- `False`
  - Use :- Should all the upload to telegram be forced as documents or not.

- `COMPLETED_STR`
  - Values :- Any character [Only 1 character] [Can be set from settings menu]
  - Default Value :- `▰`
  - Use :- Character used to denote completed progress in the progress bar. 


- `REMAINING_STR`
  - Values :- Any character [Only 1 character] [Can be set from settings menu]
  - Default Value :- `▱`
  - Use :- Character used to denote remaining progress in the progress bar. 

- `RCLONE_BASE_DIR`
  - Values :- Rclone Base Directory to where stuff should be clonned inside your drive. [Cannot be configured from settings]
  - Default Value :- `"/"`
  - Use :- The bot will upload all the files to that folder in the drive.

- `LEECH_ENABLED`
  - Values :- `True`/`False` [Can be set from settings under control action]
  - Default Value :- `True`
  - Use :- Upload to telegram should be enabled or not.

- `RCLONE_ENABLED`
  - Values :- `True`/`False` [Can be set from settings under control action]
  - Default Value :- `False`
  - Use :- Upload to rclone should be enabled or not.


- `DEFAULT_TIMEOUT`
  - Values :- `"leech"`/`"rclone"`
  - Default Value :- `"leech"`
  - Use :- Default destination (rclone or leech) to choose if the user fails to choose upload destination in 60 seconds.

- `RCLONE_CONFIG`
  - Values :- Path to the RCLONE.conf file [IT IS RECOMMENDED TO SET THIS FROM SETTINGS MENU]
  - Default Value :- `False`
  - Use :- Rclone file path.

- `DEF_RCLONE_DRIVE`
  - Values :- Default Rclone drive from the config file. This is the heading of a config from the file. [IT IS RECOMMENDED TO SET THIS FROM SETTINGS MENU]
  - Default Value :- `""`
  - Use :- Name of the config in the conf file to refer to.

- `MAX_YTPLAYLIST_SIZE`
  - Values :- Max size of a playlist that is allowed (Number of videos) [Can be set from settings menu]
  - Default Value :- `20` 
  - Use :- Stops the user from downloading big playlists.

- `MAX_TORRENT_SIZE`
  - Values :- Max torrent size in GBs that is allowed. [Can be set from settings menu]
  - Default Value :- `10`
  - Use :- Stops the user from downloading big torrents.

- `USER_CAP_ENABLE` : Work in progress
- `USER_CAP_LIMIT` : Work in progress

- `QBitTorrent Configurations`
  - To modify QBT engine Preferences ... Please check `qBittorrent.conf` in root of the repo..
  - To modify Trackers for QBT ... Please check `start.sh` file in root of the repo.. or [click here](https://github.com/KangersHub/TorToolkitX/blob/master/start.sh#L2) to see.

- `Instagram Stuff`
  - `INSTA_UNAME` it is for instagram login put your instagram username.
  - `INSTA_PASS`  it is for instagram login put your instagram password.
  - without credentials instagram wont work whether post is public or private.
  - when passing passing instagram links to bot make sure it is like `https://www.instagram.com/p/CToApjNsHql/` or like `https://www.instagram.com/p/CToApjNsHql` dont pass any flags like `https://www.instagram.com/p/CToApjNsHql/?utm_medium=copy_link`....



## **Rest Variables are not to be changed**

## Commands

    leech - To Leech a torrent or download a direct link
    ytdl - Donwload YouTube Video
    pytdl - Download YouTube Playlist
    about - About the bot
    ustatus -  To See Your Active Tasks
    status - Status of all the downloads
    server - Get server status
    usettings - User Settings (private also)
    instadl - Instagram Post/Reel/IGTV download
    setthumb - Set the thumbnail
    clearthumb - Clear the thumbnail
    speedtest - Testing internet speed host
    settings - Settings of the bot ⚠️ Admin Only
    pauseall - Pause all torrents⚠️ Admin Only
    resumeall - Resume all torrents⚠️ Admin Only
    purge - Delete all torrents ⚠️ Admin Only
    getlogs - Get the robot logs ⚠️ Admin Only
     
