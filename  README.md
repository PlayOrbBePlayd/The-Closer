# THE CLOSER

A browser based two dimensional learning game that teaches real, ethical sales technique. You walk a pixel world, gather intel, learn a named move, use it on a buyer against a rapport meter, then play a short arcade bonus round. This is the playable build of Chapters 1 through 4.

## Folder layout

Put these at the root of your repository.

```
index.html
images/
README.md
```

The game is the single file index.html. The images folder holds your full scene images. The folder can start empty, and the game will simply use its pixel art until you add images.

## Full scene images (the fun part)

The world stays pixel art until someone speaks. When a conversation opens, if you have given that person an image, the whole scene becomes that image with the conversation text on top. If there is no image, or it fails to load, the pixel scene shows instead, so nothing ever breaks.

To set images, open index.html and find the block that begins with `const SCENES`. Map a speaker id to an image. The recommended pattern is to drop a file into the images folder and point to it:

```
const SCENES = {
  maria:  "images/maria.jpg",
  marcus: "images/marcus.jpg",
  diane:  "images/diane.jpg",
  earl:   "images/earl.jpg",
};
```

A full web address or a data URI also works. The build ships with one labeled placeholder on maria so you can see the swap immediately. Replace that value with your own image, or delete the line to keep maria as pixel art.

Speaker ids you can set:

* Clients: maria, marcus, diane, earl
* Recon characters: cafe, hardware, laundry, theo, barista2, shopkeep2, resident2, sister3, contractor3, neighbor3, frontdesk4, fleet4, owner4

## Image and content rules

* Use only images you have the right to use. Your own AI generated scenes are perfect.
* Use invented people and places. Avoid real public figures and branded or copyrighted characters.
* Keep everything fine for a fifteen and up audience.

## Editing rule that must hold

No dashes in any text the player can see. That means no em dashes, no en dashes, and no hyphens used as connectors, in menus, dialogue, or any on screen words. Write compounds open, for example "high rise" rather than the hyphenated form. Real code, such as CSS property names, is the only exception.

## Put it on GitHub Pages

1. Add index.html and the images folder to your repository and commit.
2. Push to the main branch.
3. In the repository, open Settings, then Pages.
4. Under Build and deployment, choose Deploy from a branch, pick main, and the root folder.
5. Save. After a minute the page goes live at the URL shown there. Open it on your phone or share it.

## Test the look locally first

You do not need GitHub to see your images. From the folder that holds index.html, start a tiny local server and open the address it prints.

```
npx serve
```

or, if you have Python:

```
python3 -m http.server
```

Opening index.html straight from the file system can block images in some browsers, so the small local server above is the reliable way to preview.

## What comes next

Hosting also sets up the score leaderboard later, which a chat artifact cannot do. Chapter 5 and beyond will add new clients, each able to use full scene images the same way.
