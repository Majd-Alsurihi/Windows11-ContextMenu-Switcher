# 🖱️ Windows 11 Classic Context Menu Toggle

This repository contains two `.reg` files that allow you to switch between:

- The **default modern Windows 11 context menu**, and
- The **classic Windows 10-style context menu**

---

## 📂 Files Included

- `Enable_Classic_Context_Menu.reg`  
  ➤ Enables the old-style (classic) right-click menu in Windows 11.

- `Restore_Windows11_Context_Menu.reg`  
  ➤ Restores the default modern right-click menu in Windows 11.

---

## ⚙️ How to Use

1. Download or clone this repository.
2. Double-click the `.reg` file you want to apply.
3. Click **Yes** when prompted by the Registry Editor.
4. Restart your computer, or restart **Windows Explorer** via Task Manager.

---

## 🧠 How It Works

These `.reg` files modify a specific registry path:

```
HKEY_CURRENT_USER\Software\Classes\CLSID\{86ca1aa0-34aa-4e8b-a509-50c905bae2a2}
```

Creating this key with an empty `InprocServer32` value forces Windows to use the legacy context menu. Deleting the key reverts back to the default Windows 11 behavior.

---

## 🛡️ Backup Your Registry (Recommended)

Before making any registry changes, it's highly recommended to back up your registry in case something goes wrong.

### 📥 To back up the registry manually:

1. Press `Win + R`, type `regedit`, and press Enter.
2. In the Registry Editor, click on **File > Export**.
3. Choose **All** under *Export range*.
4. Name your backup (e.g., `FullRegistryBackup.reg`) and save it in a safe location.

To restore the registry later, simply double-click the `.reg` backup file you created.

---

## 🔁 How to Revert Changes

To undo the classic menu tweak and restore the default Windows 11 right-click menu:

1. Run the `Restore_Windows11_Context_Menu.reg` file.
2. Restart your PC or Windows Explorer.

---

## ⚠️ Disclaimer

- Use these files at your own risk.
- Editing the Windows Registry can impact system behavior. Always back up your data and registry before making changes.
- These scripts are provided for educational and productivity purposes only.

---

## 📌 License

This project is open-source and free to use under the [MIT License](LICENSE).
