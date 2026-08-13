```
██╗      █████╗               ██╗    ██╗ ██████╗ ██████╗ ██╗  ██╗███████╗██╗  ██╗ ██████╗ ██████╗ 
██║     ██╔══██╗              ██║    ██║██╔═══██╗██╔══██╗██║ ██╔╝██╔════╝██║  ██║██╔═══██╗██╔══██╗
██║     ███████║    █████╗    ██║ █╗ ██║██║   ██║██████╔╝█████╔╝ ███████╗███████║██║   ██║██████╔╝
██║     ██╔══██║    ╚════╝    ██║███╗██║██║   ██║██╔══██╗██╔═██╗ ╚════██║██╔══██║██║   ██║██╔═══╝ 
███████╗██║  ██║              ╚███╔███╔╝╚██████╔╝██║  ██║██║  ██╗███████║██║  ██║╚██████╔╝██║     
╚══════╝╚═╝  ╚═╝               ╚══╝╚══╝  ╚═════╝ ╚═╝  ╚═╝╚═╝  ╚═╝╚══════╝╚═╝  ╚═╝ ╚═════╝ ╚═╝     
                                                                                                  
```

A place to dump and grab automations for [Lancer Automations](https://github.com/Agraael/lancer-automations).

I'm not curating this. Everyone gets a folder named after their GitHub account. A bot merges your pull request as long as you only touched your own folder.

> [!WARNING]
> An automation is JavaScript that runs in your world. Nobody reviews what lands here. Read what you import.

---

## Getting something out of here

Browse the folders, each one has a `List.md` saying what's inside.

**A single automation:** copy the whole `.json` text, then in the Activation Manager open an activation and hit **Paste** at the top right of the editor.

**A pack or a startup script:** download the file, then **Import Pack** in the Activation Manager. You get a summary dialog to pick what gets applied.

---

## Putting something in

> [!IMPORTANT]
> If you share an automation that hooks into paid LCP content, keep the content itself out of it: no item descriptions, no copied text. It's a fine line and I doubt it'll ever be a problem, but if it goes overboard I reserve the right to wipe what crosses it.
>
> For item-linked activations the bot enforces one piece of this: `triggerDescription` and `effectDescription` must stay empty. The reaction popup shows the item's own text anyway, those fields only override it, thy must not carry the rules of these items. General activations can use them freely.

### Export it

| What | How |
|------|-----|
| One activation | **Copy** at the top right of the activation editor, then paste it in a `.json` file |
| A pack | **Export Pack** in the Activation Manager, tick what you want, you get `la-pack-<name>.json` |
| A startup script | **Export Pack**, tick only the script under Startup Scripts |

### Drop it in your folder

Fork, then make `contributors/<your-github-name>/` if it's not there. Copy [`contributors/_template/`](contributors/_template):

```
contributors/your-name/
├── List.md
├── Automations/
├── Packs/
└── Startups/
```

Files go in the matching folder, then add a line in your `List.md` saying what the thing does, what it needs (an LCP, a module, a house rule), and the LA version you tested it with.

> [!IMPORTANT]
> The List.md has an **AI** column to flag creations made with AI help. Worth knowing if you're troubleshooting, since AI-generated logic can be messy, non-obvious or broken.

### Open the pull request

Only your folder, only `.json` and `.md` files, and it merges on its own. Anything else is just a normal PR.

---

## If you're here to learn how to write one

Wrong repo, this one is just storage. The real docs:

- [Automation Engine](https://github.com/Agraael/lancer-automations/blob/main/doc/feature/AUTOMATION_ENGINE.md), the Activation Manager and how an activation is built
- [Automation System](https://github.com/Agraael/lancer-automations/blob/main/doc/AUTOMATION_SYSTEM.md), triggers, filters, lifecycle
- [API Reference](https://github.com/Agraael/lancer-automations/blob/main/doc/API_REFERENCE.md), everything on `api.`

Workshop talk goes to the [workshop channel](https://discord.com/channels/426286410496999425/1537081666483527690) on the Lancer Discord. For the module itself, [my channel](https://discord.com/channels/426286410496999425/1436087781666455642).
