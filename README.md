# Memorabilia

**Cryptographic fingerprint for your words.**

A powerful tool that generates unique crypto art from any text. Each piece of text creates a one-of-a-kind visual pattern that can never be duplicated unless you know the exact input.

🔗 **[Try it live](https://memorabilia.netlify.app)** (or your deployment URL)

![Memorabilia Example](./preview.png)

---

## What Makes It Special?

**Your text can never be converted back.** You can only match images if they're identical. No two images will ever be the same unless created from the same text.

**The number of possible patterns exceeds the atoms in the observable universe.** With 2^1024 possible combinations, each Memorabilia is truly one of a kind.

Think of it like a public key — only you know its true meaning.

---

## How It Works

1. **Your text** is converted into a **SHA-512 hash** (cryptographic one-way function)
2. The hash is **mapped to digits 0-9**
3. Each digit becomes a **colored dot** on a 32×32 grid (1,024 dots total)
4. **Adjacent dots with the same digit connect automatically** with flowing lines
5. The result is a unique, unrepeatable visual pattern

The same text always produces the same pattern. Different texts (even by one character) produce completely different patterns.

---

## Use Cases

### Just for Fun 🎨
Create beautiful, unique artwork from your favorite quotes, song lyrics, or personal mantras.

### Memorabilia 🎁
- **Personalized gifts** — Print crypto art for credit cards, wall art, or merchandise
- **Special dates** — Commemorate anniversaries, birthdays, or milestones
- **Client gifts** — Unique, meaningful presents with hidden messages

### Digital Identity 👤
- **Avatars** — A unique visual identity that's mathematically yours
- **Profile pictures** — Stand out with art that only you can recreate
- **Brand identity** — Create logos or brand marks from company values

### Security & Verification 🔒
- **Document verification** — Match confidential documents to preserve authenticity
- **Proof of knowledge** — Demonstrate you know a secret without revealing it
- **Digital signatures** — Visual representation of data integrity
- **Commit-reveal schemes** — Commit to a value publicly, reveal later

### Creative Applications 🚀
- **Password visualization** — See your passwords as art (without storing them)
- **NFT metadata** — Generate unique visuals for blockchain assets
- **Time capsules** — Lock memories in visual form
- **Secret sharing** — Share visual patterns, reveal meaning later

---

## Features

### Create Mode
- **Real-time generation** — See your pattern update as you type
- **Download as PNG** — Save your Memorabilia in high quality
- **Copy to clipboard** — Quick sharing with one click
- **10 vibrant colors** — Pink, purple, lavender, cyan, teal, orange, coral, salmon

### Verify Mode
- **Upload & check** — Drop any Memorabilia image to verify
- **Pixel-perfect matching** — 95%+ similarity threshold
- **Visual feedback** — Green checkmark for matches, red X for mismatches
- **Percentage display** — See exactly how close the match is

### Design Features
- **Dark theme toggle** — Switch between light and dark modes
- **Responsive design** — Works on desktop, tablet, and mobile
- **Clean interface** — Minimalist, distraction-free experience
- **Smooth animations** — Polished interactions throughout

---

## Technical Details

- **Algorithm**: SHA-512 cryptographic hash function
- **Grid size**: 32×32 (1,024 dots)
- **Color palette**: 10 unique colors (digits 0-9)
- **Output format**: PNG image (350×350px)
- **Connection logic**: 4-directional adjacency (horizontal, vertical, diagonal)
- **Security**: Client-side only — your text never leaves your device

### Why SHA-512?
- Industry-standard cryptographic hash function
- Collision-resistant (virtually impossible to find two texts with the same hash)
- Deterministic (same input always produces same output)
- Irreversible (cannot derive input from hash)

---

## Installation & Deployment

### Option 1: Deploy to Netlify (Recommended)
1. Fork this repository
2. Connect your GitHub to Netlify
3. Deploy from your forked repo
4. Your app will be live at `your-site.netlify.app`

### Option 2: Run Locally
```bash
# Clone the repository
git clone https://github.com/vtmade/HashPrint.git

# Navigate to directory
cd HashPrint

# Open in browser
open index.html
```

### Option 3: Deploy to Any Static Host
The app is a single HTML file with no dependencies. Upload `index.html` to:
- GitHub Pages
- Vercel
- Cloudflare Pages
- AWS S3
- Any web server

---

## Usage Examples

### Creating Your First Memorabilia
1. Go to the **Create** tab
2. Type any text (quote, date, name, secret message)
3. Watch the pattern generate in real-time
4. Click **Download** to save as PNG
5. Or click **Copy** to copy to clipboard

### Verifying a Memorabilia
1. Go to the **Verify** tab
2. Click to upload a Memorabilia PNG image
3. Type the text you think created it
4. Click **Verify** to check
5. See instant match/no match result with percentage

### Creative Ideas
```
"Anniversary: June 15, 2020"
"Secret code: Alpha-Delta-9"
"My favorite quote by Einstein"
"Password: MyS3cr3tP@ss!"
"Bitcoin block #750000"
```

---

## Privacy & Security

✅ **100% client-side** — Your text never leaves your browser
✅ **No server** — No data collection, tracking, or storage
✅ **No analytics** — Your privacy is protected
✅ **Open source** — Inspect the code yourself

⚠️ **Important**: While the hash is cryptographically secure, Memorabilia is NOT meant for storing actual passwords or highly sensitive data. It's designed for creative, memorable, and fun use cases.

---

## Development

Built with vanilla JavaScript — no frameworks or build tools required.

### Project Structure
```
HashPrint/
├── index.html          # Main application (HTML + CSS + JS)
├── netlify.toml       # Netlify configuration
└── README.md          # This file
```

### Key Technologies
- **Canvas API** — For drawing the visual pattern
- **Web Crypto API** — For SHA-512 hashing
- **Clipboard API** — For copy functionality
- **FileReader API** — For image upload/verification

### Customization
Want to modify the colors, grid size, or style? Everything is in `index.html`:
- **Colors**: Line 360-370 (10-color array)
- **Grid size**: Line 386 (`GRID = 32`)
- **Dot size**: Line 390 (`DOT_R = CELL * 0.22`)
- **Line width**: Line 391 (`LINE_W = CELL * 0.15`)

---

## FAQ

**Q: Can the text be recovered from the image?**
A: No. SHA-512 is a one-way cryptographic function. The image reveals nothing about the original text.

**Q: How unique are the patterns?**
A: With SHA-512's 2^512 possible outputs mapped to 1,024 dots, the number of possible patterns far exceeds the atoms in the observable universe.

**Q: Will the same text always create the same image?**
A: Yes. The algorithm is deterministic. Same text = same hash = same pattern.

**Q: Can I use this for commercial projects?**
A: Yes! It's open source under MIT License. Use it freely.

**Q: Is it secure enough for passwords?**
A: The hashing is cryptographically secure, but we don't recommend using it for actual password storage. Use it for creative and fun applications instead.

**Q: Can I change the colors?**
A: Yes! Edit the `colors` array in `index.html` (lines 360-370).

**Q: Does it work offline?**
A: Yes! Once loaded, the entire app works offline. No internet connection needed.

---

## Contributing

Contributions are welcome! Here are some ideas:
- [ ] Add more color palettes
- [ ] Export as SVG format
- [ ] Batch generation mode
- [ ] Animation effects
- [ ] QR code integration
- [ ] Print optimization
- [ ] Additional hash algorithms (SHA-256, Blake2b)
- [ ] Customizable grid sizes

Feel free to open issues or submit pull requests!

---

## Credits & License

**Created by [Vinay Thakur](https://github.com/vtmade)**

Built with the assistance of AI tools.

### Open Source
This project is licensed under the **MIT License** — feel free to use, modify, and distribute.

```
MIT License

Copyright (c) 2025 Vinay Thakur

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```

---

## Links

🌐 **Live Demo**: [memorabilia.netlify.app](https://memorabilia.netlify.app)
💻 **GitHub**: [github.com/vtmade/HashPrint](https://github.com/vtmade/HashPrint)
👤 **Author**: [github.com/vtmade](https://github.com/vtmade)

---

**Made with ❤️ and cryptography**

*Your words, visualized. Forever unique.*
