# Contributing

Thanks for helping out. Bug fixes, framework support and translations are all welcome.

## Reporting bugs

Use the **Bug report** form under [Issues](../../issues/new/choose). Include:

- the script name and version (the `version` line in its `fxmanifest.lua`)
- your server artifact version and framework (ESX, Qbox, standalone…)
- the exact error from the F8 console or the server console
- steps that reproduce it

## Pull requests

1. Fork the repo and create a branch: `fix/radio-blips`, `feat/qbox-support`, etc.
2. Keep each PR to **one script and one change**.
3. Test it on a real server. The automatic check only catches syntax and manifest mistakes.
4. Bump `version` in that script's `fxmanifest.lua` and add a line to its `CHANGELOG.md`.
5. Open the PR and fill in the template.

By opening a PR you agree that your contribution is released under the repository's
[GPL-3.0 license](LICENSE).

## Code style

- Lua 5.4. Four-space indent, `local` everywhere, no new globals except `Config`.
- **Never trust the client.** Validate `source`, permissions and every value a client sends.
- Prefix events with the resource name: `uncledev_example:server:doThing`.
- Avoid `while true do Wait(0)` loops unless something must run every frame.
- Keep anything a server owner might change in `config.lua`.

## Adding a new script (maintainers)

1. Copy `templates/uncledev_template` to `resources/<new_name>`.
2. Rename every `uncledev_template` inside it to `<new_name>`. Event names are built from the folder name automatically.
3. Fill in `fxmanifest.lua` (description, version `1.0.0`), the README and the CHANGELOG.
4. Add a row to the scripts table in the root `README.md`.
5. Merge to `main`, then publish a release by pushing a tag:

   ```bash
   git tag <new_name>-v1.0.0
   git push origin <new_name>-v1.0.0
   ```

   The **Release** workflow checks that the tag version matches `fxmanifest.lua`, zips
   `resources/<new_name>` and attaches it to a GitHub Release. The notes come from that version's
   section of the CHANGELOG.
