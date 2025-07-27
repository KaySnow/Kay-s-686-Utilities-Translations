# 686 Utilities: `/guides`

Guides are designed to help users with installations, common problems, and more — powered by interactive Discord embeds.

📌 These are **not** one-off answers. Guides should walk a user through a process step-by-step, in a way that a simple custom command cannot.

You can contribute new guides here. Each accepted contribution will be credited in the guide. 

⚠️If you need assistance, ask in our [Discord Server](https://discord.com/invite/gyw5rDHCfr).

---

## 🚀 How to Contribute

1. Fork this repository.
2. Add a new `.xml` file using lowercase (e.g., `install_sirens.xml`).
3. Follow the formatting style shown below.
4. Your guide must include:
   - A `Page` block with the `id="home"`.
   - Clear, logical, step-by-step instructions.
5. Test your XML using `/checkguide` in the `#commands` channel of **LSPDFR-TS**.
6. Submit a Pull Request with a short summary of what your guide covers.

---

## 🗂️ File Format

Each guide is a single `.xml` file.

It starts with a `<Guide>` block containing:
- `id`: Unique ID of the guide (should match the filename, without `.xml`)
- `name`: Display name used in the `/guides` command.

### ✅ Inside `<Guide>`:

- `<Author>`: Your Discord username (used for credit).
- One or more `<Page>` blocks, each with:
  - `id`: Unique per-guide page ID.
  - `<Title>`: Embed title.
  - `<Description>`: Embed description.
  - Optional:
    - `<ImageUrl>`: Embed image.
    - `<Fields>`: List of embed fields. You can set `inline="false"` to force a new line.
    - `<Buttons>`: One or more `<Button>` elements.

---

## 🔘 Buttons

Buttons are defined in the `<Buttons>` block. Their node value is used as the button label.

### Button Types:

- `interactive`: Navigates to another `<Page>` within the same guide (via the `id`).
- `ephemeral`: Sends a private embed to the user.  
   - **Note**: Target pages of `ephemeral` buttons must only use `link` buttons.
- `link`: Directs to a URL.

---

Need a starting point? Check out [`install_vehicles.xml`](https://github.com/686-Utilities/686-Utilities-Translations/blob/main/en-GB/Guides/install_vehicles.xml)
