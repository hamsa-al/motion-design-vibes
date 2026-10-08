# Contributing

Thanks for helping the catalogue grow. There are two ways to add an animation.

## 1. Suggest one (no code)

Paste a website link into **Find animations on other websites** on the home page, or [open an issue](../../issues/new) with:

- the link to the website
- what caught your eye (optional, but it helps)

The site gets scouted and anything new is added to the catalogue.

## 2. Add one yourself with Claude Code

1. Fork this repo and clone your fork.
2. Open it in Claude Code and ask:
   > Use the motion-scout skill: scout https://example.com for animations that aren't in the Motion Vibe Playground yet and add them to the catalogue in index.html.

   Or describe the animation in your own words:
   > Add a "confetti burst" animation to the catalogue in the feedback section.
3. Open `index.html` in your browser and check that it plays well with every vibe, with reduced motion on, and with a pasted design.
4. Open a pull request with a short description and, if you can, a link to where you saw it.

## What makes a good addition

- It's something a product designer would actually reach for, not a duplicate of an existing card with a different name.
- It follows the motion rules in `.claude/skills/motion-vibes/SKILL.md` (UI motion stays under 300 ms, nothing scales from 0, exits are quicker than entrances, and reduced motion is respected).
- Its card says in one short line when to pick it.
- Everything stays in the single `index.html` file, with no libraries or build step.

## For the maintainer: handling suggestions

Each suggestion issue ends with a request. Paste it into Claude Code in this repo, review the result, then commit and push. The live site updates on its own within a minute or two.
