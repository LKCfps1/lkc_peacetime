Absolutely! Here’s a **GitHub README.md** for your peacetime script.
It includes features, setup, usage, config, credits, and a strong note on credit requirements.

---

````markdown
# LKC Peacetime Script

A standalone FiveM peacetime script to **block all weapons, fighting, and most animation/emote menus** while active. Supports any framework—ESX, QBCore, or completely standalone.

---

## 🚦 Features

- **Peacetime Mode:** No combat, no weapons, no melee, no trolling—players can’t shoot, fight, or use most emote/animation menus while peacetime is active.
- **Admin Command:** Toggle peacetime with `/peacetime` (admin-only, uses ace perms by default).
- **Auto Mode:** Peacetime automatically enables for the first and last X minutes of each restart (fully configurable).
- **Clean UI:** “PEACETIME ENABLED” notification appears in the top right with a green banner during peacetime.
- **Universal:** Works on *any* server, framework-free.
- **Fully Configurable:** Change timings, control blocklist, auto mode, and more in `config.lua`.

---

## 📦 Installation

1. **Download or clone this repo**  
   Place the folder in your `resources` directory.

2. **Add to your `server.cfg`:**
    ```
    ensure lkc_peacetime
    ```

3. **(Optional) Configure `config.lua`**  
   Adjust peacetime windows and options to fit your server.

---

## ⚙️ Configuration

All config is in `config.lua`:

```lua
Config = {}

Config.UseAutoPeacetime = true  -- Enable/disable auto-peacetime at restart
Config.PeacetimeStartMinutes = 30  -- Minutes peacetime is ON after restart
Config.PeacetimeEndMinutes = 30    -- Minutes peacetime is ON before restart
Config.ServerRestartMinutes = 240  -- Total minutes between scheduled restarts (ex: 4 hours = 240)
````

---

## 🕹️ Usage

* **/peacetime** — Toggle peacetime manually (admin-only by ace permission)
* **Auto Mode** — Script auto-enables peacetime at start/end of restart cycle (configurable)
* **Players see a green banner in the top right when peacetime is enabled**

---

## 🔒 Permissions

* Only players with ace permission `"command"` (or server console) can use `/peacetime`.
* To give yourself permission, add this in your `server.cfg`:

  ```
  add_ace group.admin command allow
  add_principal identifier.steam:YOURHEXID group.admin
  ```

---

## 🎨 Credits (MUST READ!)

> **YOU MUST CREDIT `LKC Scriptz` IF YOU USE OR SHARE THIS SCRIPT.**
> Please leave credits in your server’s Discord, server list, or resource.

*Script by LKC Scriptz. Enjoy, and let the city chill!*

---

## 💬 Support / Contact

* Open a GitHub issue or DM LKC Scriptz for help, custom features, or bug reports.
