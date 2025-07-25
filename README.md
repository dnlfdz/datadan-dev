# datadan-dev

Personal Website built with Hugo and a custom "Retro Terminal" theme.

## Overview
This project is a static site generated with [Hugo](https://gohugo.io/) using a custom theme inspired by retro IBM mainframe terminals. It features:
- **Retro terminal-inspired design**: Green-on-black color scheme, CRT scanlines, glowing text, and terminal-style UI elements.
- **Animated boot sequence**: Typing animation with playful greetings, geolocation, browser/OS detection, and a fake `rm -r /` animation.
- **Dynamic hacker handle**: Generates a random hacker nickname for each visitor.
- **Responsive design**: Looks great on desktop and mobile.
- **Content organization**: Posts, tags, and categories with easy navigation.
- **Easy deployment**: Ready for Vercel, Cloudflare Pages, or any static host.

## Features
### Retro Terminal Theme
- Custom CSS for CRT/terminal look (`themes/retro-terminal/assets/css/main.css`)
- ASCII art section dividers
- Terminal-style buttons and glowing text

### Animated Boot Sequence
- Typing animation introduces the site and user
- Greets user based on geolocation, browser, OS, and local time
- Playful fake terminal wipe (`sudo rm -r /`) and "just kidding" reveal
- Random hacker handle generator
- All animations can be skipped with `Ctrl+X`

### Content Structure
- Posts are written in Markdown with TOML front matter (see `themes/retro-terminal/content/posts/`)
- Tags and categories for easy filtering
- Example post front matter:
  ```toml
  +++
  title = 'Post 1'
  date = 2023-01-15T09:00:00-07:00
  draft = false
  tags = ['red']
  +++
  ```

## Local Development
1. **Install Hugo** (if not already):
   ```sh
   brew install hugo
   ```
2. **Start the local server:**
   ```sh
   hugo server
   ```
   - Visit [http://localhost:1313/](http://localhost:1313/) to preview.
   - If port 1313 is busy, Hugo will use another port (check terminal output).

## Deployment
### Vercel
- Connect your GitHub repo to Vercel.
- Use the following settings:
  - **Build Command:** `hugo`
  - **Output Directory:** `public`
  - **Environment Variable (optional):** `HUGO_VERSION=0.148.1`
- See `vercel.json` for static build config.

### Cloudflare Pages
- Set build command to `hugo` and output directory to `public`.
- Add `HUGO_VERSION` environment variable if needed.

## Customization
- **Theme config:** See `themes/retro-terminal/hugo.toml` for menu and Hugo version settings.
- **Site config:** See root `hugo.toml` for site-wide settings.
- **Add posts:** Place new Markdown files in `content/posts/` with TOML front matter.
- **Assets:** Place custom CSS/JS in `themes/retro-terminal/assets/`.

## Credits
- Built with [Hugo](https://gohugo.io/)
- Custom theme by Dan (dnlfdz)

---
Feel free to fork, customize, and deploy your own retro terminal site!
