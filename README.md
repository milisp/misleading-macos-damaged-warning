# Misleading macOS “App is Damaged” Warning ❌

macOS users frequently see this misleading error:

![MCPLinker](./assets/MCPLinker-damage.png)

> "App is damaged and should be moved to the Trash."

In most cases, **the app works perfectly fine** — the error appears simply because it is **not notarized or signed by Apple**.

This repo collects:
- 💥 Real-world cases where users or developers were affected
- 🔧 Workarounds to run these apps safely
- ✊ A call to Apple to change this misleading wording

## 🔥 Why This Warning Is Misleading

Apple's warning says the app is "damaged", but this is almost never true.  
In most cases, the app is simply unsigned or not notarized.  
There is no corruption, malware, or malfunction — just a lack of Apple's approval stamp.  
Yet the message implies the app is broken or unsafe, causing unnecessary fear.

## 📦 Real-World Cases

### 🧑‍💻 CASE 1: XYZ Is Damaged and Can’t Be Opened. You Should Move It To The Trash

[url](https://discussions.apple.com/thread/253714860)

> I just started getting this error message for all of my files tonight "XYZ Is Damaged and Can’t Be Opened. You Should Move It To The Trash". I just updated to the latest version of Monterey this morning. My files (Word docs, Excels, Preview PDFs) were working just fine about 1 hour ago and then this just spontaneously happened. Any suggestions on how to fix this?

### CASE 2: "App Is Damaged And Can’t Be Opened" error on Ventura

[app_is_damaged_and_cant_be_opened_error_on_ventura](https://www.reddit.com/r/macsysadmin/comments/13vu7f3/app_is_damaged_and_cant_be_opened_error_on_ventura/)

> After updating to Ventura, some third party apps show "App Is Damaged And Can’t Be Opened This file was downloaded from an unknown date." error. Even disabling Gatekeeper won't get rid of the message.

## 💥 Harm to Developers and Users

This single line of misleading text has caused real damage:
- 💔 Users delete safe apps, fearing malware
- 🧑‍💻 Developers lose testers, users, and credibility
- 🕐 Countless hours are wasted explaining, debugging, and reassuring

## 🧪 Real-World Cases

See [CASES.md](./CASES.md) for detailed examples submitted by real developers and users.

## 🧰 How to Bypass the Warning

If you trust the app source, you can bypass the warning with:

```sh
xattr -rd com.apple.quarantine /path/to/your.app
```

You can also right-click → Open in Finder, which sometimes works.

🎥 [Watch: How to Fix “App is damaged and can’t be opened” on macOS (YouTube)](https://www.youtube.com/watch?v=MEHFd0PCQh4)

## 🤝 Join Us

If you've been confused or harmed by this warning:
- 📩 Submit your story in [CASES.md](./CASES.md)
- 🐛 Open an [Issue](https://github.com/milisp/misleading-macos-damaged-warning/issueshttps://github.com/milisp/misleading-macos-damaged-warning/issues) describing what happened
- ⭐ [Star](https://github.com/milisp/misleading-macos-damaged-warning) this repo to raise awareness
- 🔁 Share it on social media
- 🧾 Sign on to support better messaging from Apple