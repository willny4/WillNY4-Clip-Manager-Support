# WillNY4 Clip Manager — Official Support

**WillNY4 Clip Manager** is a Windows plugin for **Elgato Stream Deck** that helps video creators review, save, and discard their latest MP4 or MKV recordings.

**Status:** Preparing for release on the Elgato Marketplace at a planned price of **$1.99 USD**. This public repository provides customer support and documentation only. The plugin is **not yet available for purchase**, and this repository does not distribute the plugin or its source code.

## Five Stream Deck actions

| Action | What it does |
| --- | --- |
| **Play Latest** | Opens the newest completed recording in the default Windows video player and remembers the reviewed clip. |
| **Save Latest** | Moves the newest completed recording to your active Saved Clips folder. |
| **Delete Reviewed** | Sends the clip last opened using Play Latest to the Windows Recycle Bin. |
| **Discard Latest** | Sends the newest completed clip to the Recycle Bin without reviewing it. |
| **Settings** | Opens the configuration page to choose recording and saved destination folders. |

This is a **native Stream Deck plugin**. It requires no separate BAT files, PowerShell installation, custom OBS connection, or additional running app.

## Requirements

- Windows 10 or 11 (64-bit)
- Stream Deck software 7.1 or newer and a compatible Stream Deck device
- MP4 or MKV video files saved by your recording application

## Installation and configuration

*These instructions apply after the Marketplace release.*

1. Install **WillNY4 Clip Manager** through the **Elgato Marketplace**.
2. Open Stream Deck and locate the **WillNY4 Clip Manager** action category.
3. Drag your preferred actions onto Stream Deck keys.
4. Press **Settings** to open the configuration page.
5. Choose the folder where your recording software saves videos.
6. Add Saved Clips destination folders and choose the **Active Saved Folder**.
7. Save the settings. You can switch destinations later without reassigning your buttons.

## MP4/MKV and deletion behavior

- If matching MP4 and MKV recordings have the same filename except for extension, Clip Manager prefers the MP4.
- Optional companion-file cleanup recycles the matching MKV during save or deletion operations.
- MKV-only clips are supported.
- Stop recording and close any player holding a clip open before managing the file.
- **Save Latest** will not overwrite an existing destination file.
- **Delete Reviewed** targets the exact clip previously played; **Discard Latest** targets the newest eligible clip and repeated presses can affect multiple clips.
- Deletions use the **Windows Recycle Bin**. If recycling fails, the plugin reports the error rather than deliberately deleting the file permanently.

**Test with disposable recordings before using the plugin on important videos.**

## Troubleshooting

**No clip found:** Check the Recording Folder in Settings, confirm the file is MP4 or MKV, and ensure recording has stopped.

**Video won't open:** Set a Windows default application for the video's extension under **Settings → Apps → Default apps**.

**Clip saved to the wrong project:** Open the plugin's Settings, select the correct **Active Saved Folder**, and save.

**Deletion failed:** Close the video in your player, confirm no application is using it, and verify the file location supports the Windows Recycle Bin.

**Configuration and logs:** Stored locally in `%LOCALAPPDATA%\WillNY4_Clip_Manager_Plugin`.

## Uninstall

Uninstall **WillNY4 Clip Manager** through the Stream Deck app's plugin management interface. Your recording and destination folders and their video files are not deleted. If you also want to clear saved preferences and logs, delete `%LOCALAPPDATA%\WillNY4_Clip_Manager_Plugin` manually.

## Get support

For questions, problems, or feature suggestions, [open a support issue](https://github.com/willny4/WillNY4-Clip-Manager-Support/issues/new).

Please include your Windows version, Stream Deck software version, the action involved, and any error message. **Do not upload personal recordings, sensitive information, or private file paths to public issues.**

---

Developed by **WillNY4**. This support repository is public; the development repository remains private.
