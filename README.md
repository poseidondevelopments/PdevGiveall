# PdevGiveall - Give All Items Script

A FiveM resource for GTA5 that allows server administrators to give items, weapons, or money to all online players simultaneously using a single command.

## 📋 Description

This script provides a convenient admin command (`/giveall`) that distributes items, weapons, or money to every player currently online on your server. It's built for the QBCore framework and requires admin permissions to use.

## ✨ Features

- **Give items to all players** - Distribute any item from your server's item database
- **Give weapons to all players** - Distribute weapons to all online players
- **Give money to all players** - Distribute cash to all online players
- **Admin-only command** - Restricted to administrators only
- **Real-time notifications** - Players receive inventory notifications when items are added
- **Error handling** - Validates input and provides helpful error messages

## 🚀 Installation

1. Download or clone this repository
2. Place the `PdevGiveall` folder in your FiveM server's `resources` directory
3. Add `ensure PdevGiveall` to your `server.cfg` file
4. Restart your server or start the resource manually

## 📖 Usage

### Command Syntax

```
/giveall <type> <name> <amount>
```

### Parameters

- **`type`** - The type of item to give. Options:
  - `item` - Regular items (e.g., bread, water, lockpick)
  - `weapon` - Weapons (e.g., WEAPON_PISTOL, WEAPON_KNIFE)
  - `money` - Cash money

- **`name`** - The name of the item, weapon, or "money" (for money type)
  - For items: Use the item name as defined in your QBCore items database
  - For weapons: Use the weapon hash (e.g., `WEAPON_PISTOL`)
  - For money: Use `money` or `cash`

- **`amount`** - The quantity to give to each player
  - For items: Number of items (e.g., `1`, `10`, `100`)
  - For weapons: Usually `1` (weapons are given one at a time)
  - For money: Amount of cash (e.g., `1000`, `5000`)

### Examples

**Give bread to all players:**
```
/giveall item bread 5
```

**Give a pistol to all players:**
```
/giveall weapon WEAPON_PISTOL 1
```

**Give $10,000 to all players:**
```
/giveall money money 10000
```

## ⚙️ Requirements

- **FiveM Server** - Running GTA5
- **QBCore Framework** - This script is built for QBCore
- **Admin Permissions** - Only administrators can use this command

## 🔒 Permissions

This command is restricted to administrators only. The permission check is handled by QBCore's command system using the `"admin"` permission level.

## 📝 Technical Details

- **Framework:** QBCore
- **Script Type:** Server-side only
- **Lua Version:** Lua 5.4
- **Game:** GTA5

### How It Works

1. The command validates the input arguments (type, name, amount)
2. Retrieves a list of all online players using `QBCore.Functions.GetPlayers()`
3. Iterates through each player and gives them the specified item/weapon/money
4. Sends inventory notifications to players when items are added
5. Notifies the admin when the command completes successfully

## 🐛 Troubleshooting

**Command not working?**
- Ensure you have admin permissions
- Check that QBCore is properly loaded
- Verify the item/weapon name exists in your server's database

**Items not appearing?**
- Check server console for error messages
- Verify the item name matches exactly with your QBCore items database
- Ensure players have inventory space

**Permission denied?**
- Make sure your QBCore admin permissions are properly configured
- Check that your admin group has the required permissions

## 📄 License

This script is created by **poseidondev**. Please respect the original author's work.

## 👤 Author

**poseidondev**

## 📞 Support

For issues, questions, or contributions, please contact the author or create an issue in the repository.

or create a ticket in our discord server https://discord.gg/3w8bdfZusD

---

**Version:** 1.0.0


