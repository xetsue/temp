# Screenshots
Status Bar Icon
><img width="1080" height="127" alt="1000467547" src="https://github.com/user-attachments/assets/ea3936aa-e842-4c23-8c85-94759a6beb48" />

Notification
><img width="1080" height="684" alt="1000467549" src="https://github.com/user-attachments/assets/98e63103-1000-432a-8f10-a345460836ea" />

QS Tile
><img width="1080" height="239" alt="1000467551" src="https://github.com/user-attachments/assets/83f8c665-e24a-4280-a348-31d3c1fc0643" />

Logs
><img width="1080" height="1018" alt="1000467557" src="https://github.com/user-attachments/assets/1a9e3245-82c9-4965-86f6-29281b8b4053" />

# Details
A QS Tile Shortcut 
---
To monitor 🌡️ Temperature and ⚡ Volt.
Additional: Timestamp and Current usage in mA.

🐥 The battery temperature values are used as Notification icon. This allows showing values in real time on your status bar without the need to expand them.

Screenshots: https://imgur.com/a/0gsDrYx
Alternative Link: https://github.com/xetsue/temp/blob/main/README.md

💬 Details are recorded into flow logs incase you need to check recently recorded data. To avoid logs size overflow, the logs will automatically be cleared and QS tile will be restored once the notification is dismissed / cleared away. To prevent the log being cleared, avoid dismissing the notification and instead manually stop this flow.

🔋 This flow is only active when the notification is active, when cleared away / not present, the QS tile and this flow itself simply goes to sleep saving resources and battery. No activity will be monitored or memory being used in this state.

> This flow was made with the intention to monitor app usage as battery temperature is an important consideration when executing heavy tasks. Commonly used for emulators or general testing.

### 🚩 Stop Auto Logging
To permanently stop the auto logging, check "Only when logging enabled" in the Log Append Block @ Block 53.

### 🚩 Stop Auto Log Clears Permanently
Disconnect Block 55 @ Write To File Block.

### 🚩 Fullscreen Apps / Hidden Statusbar
You may use the same approach using floating buttons by inserting the variable into icon value for floating button block instead if you need an active floating temperature monitor in full-screen apps that hides status bar.  This would require you to replace the notification block with a floating notification block instead.
