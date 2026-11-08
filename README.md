# UncleDev — Free FiveM Scripts

Free, open-source FiveM resources by **UncleDev**. Download one, drop it in, `ensure` it. No escrow and no license keys, so you can read every line of the code.

![License: GPL-3.0](https://img.shields.io/badge/license-GPL--3.0-blue)
![FiveM](https://img.shields.io/badge/FiveM-cerulean-orange)

## Scripts

| Script | What it does | Frameworks | Download |
|---|---|---|---|
| **UncleDev Radio** (UD-9000 TOUCH) | Touchscreen police radio as an ox_inventory item: callsigns, channel roster, officer GPS blips, in-game channel editor, admin moderation. Needs pma-voice + ox_inventory. | ESX · Qbox · ACE · Public | [uncledev_radio.rar](uncledev_radio.rar) |

<!--
Add one row per script, for example:
| [uncledev_example](resources/uncledev_example) | One-line description | ESX · Qbox · Standalone | [Latest](../../releases?q=uncledev_example&expanded=true) |
-->

## Installing a script

1. Download the script (from **[Releases](../../releases)**, or the file linked in the table above).
2. Extract the folder into your server's `resources` folder. **Keep the folder name** as it is.
3. Add it to `server.cfg` after the resources it depends on:

   ```cfg
   ensure uncledev_radio
   ```

4. Read that script's own `README.md` for config and permissions.

## Help & bug reports

- Found a bug? [Open an issue](../../issues/new/choose) using the bug report form, and include your server artifact version and framework.
- Want a feature? Use the feature request form.
- Want to contribute? Read [CONTRIBUTING.md](CONTRIBUTING.md).

## License

Everything in this repository is released under the [GNU GPL v3.0](LICENSE).

You can use, edit and share these scripts on your server, including servers that make money.
If you **redistribute** a script, or a modified version of it, you must share the full source under
the same license and keep UncleDev's copyright notices. **Re-releasing these scripts closed-source,
for example escrowed on Tebex, breaks the license.**
