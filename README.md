# StratPad

> V1 was built as a Capstone project and has since been taken down. V2 is in active development and will represent a significant re-architecting of the core systems.

StratPad is a game-agnostic dashboard builder for tabletop games. Rather than targeting a single game system, it provides 11 fully-featured core modules that players can mix and match to build the tracking tool their specific game requires — then share it with the community.

For popular games like Dungeons & Dragons, rich ecosystems of digital tools already exist. StratPad is for everything else.

<Embed the compressed Video here>

---

## Modules

StratPad ships with 11 core modules:

**Stopwatch** - Useable as either a Stopwatch (count up) or Timer (count down)
**Score Table** - Editable table for tracking score or other metrics. Toggleable `Totals` row, and highlightable winner via `Show Highlight` and `High or Low Score`.
**Notes** - A simple rich text editor
**Nested Dictionary** - A folder-like structure for rich text & images. Useful for storing rules, references, and more. Upload & download available via JSON.
**List** - Text list featuring drag-to-reorder, and toggleable `QTY` and `Checkbox` columns
**Counter** - Simple integer counter. Configurable `Min` and `Max`, `Increment`, `Default Value`, as well as `Prefix` and `Suffix` for the rendered count.
**Resource Bar** - Configurable list of sliders. Can add or remove, change `colour`, `title`, `max`, `step`, and `default value`.
**Image** - Single image container - able to fullscreen on click.
**Dice** - 3d Rendered Dice of all shapes from `d4` to `d20`. Able to quickly add/remove dice, and add a ` +/- modifier` to the total.
**Coin Toss** - Simple animated coin toss.
**Spin Wheel** - Animated randomizer for a collection of strings.

---

## Screenshots


---

## Architecture

StratPad is a [Next.js](https://nextjs.org/) application backed by a [PostgreSQL](https://www.postgresql.org/) database, and image storage via [CloudFlare R2](https://www.cloudflare.com/en-ca/developer-platform/products/r2/).

<Add some pictures>


**Key design decisions:**

<Talk about Saving & DB shape>

<Talk about the Pinch-pan-zoom wrapper>

<Talk about serving images via the server to avoid complexity for public vs private data>


---

## Getting Started

### Prerequisites

- Node.js `v24`
- PostgreSQL `v14+`
- A `.env` file based on `.env.example`

### Installation

```bash
# Clone the repo
git clone https://github.com/<your-username>/stratpad.git
cd stratpad

# Install dependencies
npm install

# Set up environment variables
cp .env.example .env
# Fill in your values in .env

# Set up the database
npx prisma migrate deploy

# Start the development server
npm run dev
```

The app will be running at `http://localhost:3000`.

---

## License

MIT License

Copyright (c) [2026] [JR-Basmati]

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