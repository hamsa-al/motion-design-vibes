# Motion Vibe Playground

Motion catalogue for product design.

Browse almost 100 animations (loading states, transitions, page changes, text effects and more), tune each one by feel (snappy, calm, playful, premium…), try it on your own designs, then export a motion spec that Claude Code turns into real code.

**Open it:** https://hamsa-al.github.io/motion-vibe-playground

No sign-up, no install. It runs entirely in your browser.

## How to use it

1. **Pick an animation** from the catalogue. Each card says when it's the right choice.
2. **Tune the feel.** Choose a vibe, then adjust speed and amount until it feels right.
3. **Try it on your design.** Paste or drop a screenshot of your component or screens (in Figma: right-click a frame, then Copy/Paste as → Copy as PNG). To load straight from a Figma link, see [Load designs from Figma](#load-designs-from-figma).
4. **Export for Claude Code.** Copy the spec or download it, then paste it into Claude Code in your project:
   > Apply this motion spec to the save button.

Your tuned animations are remembered in your browser. Tune several and you can export them all as one `MOTION.md` for your project.

## Load designs from Figma

Loading a design from a Figma link works through **Claude Code with the Figma MCP**, so you need your own copy of the repo running on your computer. The hosted site can't reach Figma by itself.

1. **Fork** this repo (top right on GitHub), then clone your fork.
2. Open the folder in Claude Code.
3. Connect Figma once. Run this in your terminal, then type `/mcp` in Claude Code to sign in:
   ```
   claude mcp add --transport http figma https://mcp.figma.com/mcp
   ```
4. Paste your Figma link into Claude Code (in Figma, right-click a frame → **Copy link to selection**) and say which animation to try it on, for example:
   > Load this Figma frame into the playground on the button press animation: https://www.figma.com/design/…
5. Claude Code saves the frame, opens the playground and plays the animation on your design.

On the hosted site, the Figma field stays turned off, since it can't reach Figma from there.

Your designs are saved in the `designs/` folder, which is never uploaded to GitHub.

## Using it with Claude Code

This repo includes three skills in `.claude/skills/`:

- **motion-vibes** turns feelings ("make it snappier") into motion, and knows how to apply specs from the playground.
- **motion-figma** loads a Figma frame into the playground through the Figma MCP.
- **motion-scout** looks at a website, finds animations the catalogue doesn't have yet, and adds them.

To use **motion-vibes** in your own project, copy the `.claude/skills/motion-vibes` folder into your project's `.claude/skills/` folder.

## Suggest an animation

Seen a great animation on a website? Paste the link into **Find animations on other websites** on the home page. It opens a GitHub issue for you to submit. Each one gets scouted and the new animations are added to the catalogue.

You can also [open an issue](../../issues/new) directly, or add an animation yourself. See [CONTRIBUTING.md](CONTRIBUTING.md).

## Run it locally

Download `index.html` and open it in your browser. That's it.

## Credits

Created by Hamsa 🖤

Motion principles inspired by [Emil Kowalski](https://emilkowal.ski/).
