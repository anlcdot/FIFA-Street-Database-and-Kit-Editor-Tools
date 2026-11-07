# FIFA Street Mod Tools (Database, Kit & Logo Editor)

A modding toolkit designed for the decompiled/PC port of FIFA Street (ReStreet) that enables full control over the database, kits, and UI team crests.

---

## Credits & Acknowledgements

This project integrates and builds upon the following open-source work:

* **[dmitri-fm](https://github.com/dmitri-fm)** – Developer of **[Rx3Tools](https://github.com/FIFA-Mods/Rx3Tools)**. The `chunklzx` decompression algorithm for Xbox 360 `.rx3` containers was adapted from Rx3Tools and integrated directly into the Kit Swapper pipeline.

---

## Installation & Setup

1. Download and extract **`ModTools.zip`** to any directory.
2. Inside the folder, you will find all three standalone tools:
   * **Database Manager**
   * **Kit Swapper**
   * **Logo Swapper**
3. Ensure you know your game's directory path (e.g., `C:\FIFA Street\ReStreet\Game`).

---

## How To Use

### 1. Database Manager
1. Launch the Database Manager.
2. Click **"Oyundan çıkar"**.
3. Select your installation's **`Game`** directory (e.g., `C:\FIFA Street\ReStreet\Game`).
4. Make your desired edits (player names, attributes, teams, colors) and click **"Kaydet"**.
5. Click **"Oyuna yaz"** to apply your changes directly to the game files.

---

### 2. Kit Swapper
1. Run `fsmod.py` (or the Kit Swapper executable).
2. Click **"Big dosyasi sec"** and select `data3.big` located inside your `Game` folder (e.g., `C:\FIFA Street\ReStreet\Game\data3.big`).
3. Select the kit you want to edit. *(If the list is empty, make sure the top **Kategori** dropdown is set to **Formalar(Kit)**)*.
4. Click **"PNG Cikar (rx3c)"**. The tool will automatically open the output workspace folder.
5. Replace or edit the textures (`jersey_cm.png`, `shorts_cm.png`, `crest_cm.png`, etc.) with your custom graphics.
6. Once saved, return to the application and click **"PNG klasorunden aktar(rx3c)"**.
7. Click **"2)Designları big'e yaz"** and confirm with **Yes**.
8. Close the application and launch the game.

---

### 3. Logo Swapper (Menu & UI Crests)
The workflow is identical to the Kit Swapper, but handles UI badges and menu assets:

1. Launch the **Logo Swapper**.
2. Click **"Big dosyasi sec"** and select `data1.big` from your `Game` folder (e.g., `C:\FIFA Street\ReStreet\Game\data1.big`).
3. Locate and select the team crest you want to replace (supports small, medium, and big assets).
4. Click **"DDS Cikar"** (or the respective extraction button) to dump the target texture to your workspace.
5. Replace the crest asset with your custom graphic.  
   > **Note:** Because UI assets are stored in `.dds` format, it is highly recommended to use **[Paint.NET](https://getpaint.net/)** (or Photoshop with DDS plugins) to preserve alpha transparency and DXT compression headers without corrupting the file.
6. Return to the tool, click **"DDS klasorunden aktar"**, and then **"Designları big'e yaz"**.
7. Close the tool and start the game to see your updated badges in the menus.

---

## Known Notes & Future Roadmap

* This toolkit is an evolving project and is able to development.
* Minor UI bugs or edge cases may occur. Ongoing updates aim to merge all three utilities into a unified, compact single-executable suite. Maybe one day.
