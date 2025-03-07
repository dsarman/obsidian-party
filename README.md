<h1 align="center">
    <img src="https://raw.githubusercontent.com/yiliansource/party-js/main/.github/banner.svg"/>
</h1>

<p align="center">
    <a href="#installation">Installation</a> &bull;
    <a href="#usage">Usage</a> &bull;
    <a href="https://party.js.org/docs">Documentation</a>
</p>

# Party🎉
An implementation of the [party.js](https://party.js.org/) library for the [Obsidian](https://obsidian.md).

# Features
+ Create confetti and sparkles effects

<img src="https://raw.githubusercontent.com/shap-po/obsidian-party/master/images/confetti.gif" width="40%"/> <img src="https://raw.githubusercontent.com/shap-po/obsidian-party/master/images/sparkles.gif" width="40%"/>
+ What else do you want?

# Installation
Search for the "Party🎉" in the Obsidian plugin list.
## Manual Installation
1. Go to [Releases](https://github.com/shap-po/obsidian-party/releases) and download the latest release
2. Enable plugins in the Obsidian settings
3. Extract the contents of the zip file to obsidian plugins folder
4. You should have a folder named "obsidian-party", containing "main.js" and "manifest.json" files
5. Restart Obsidian and enable the plugin in the plugin list
## Manual build
1. Clone the repository
2. Run `npm i` or `yarn` to install dependencies
3. `npm run dev` to build the plugin

# Usage
Either add a `confetti` or `sparkles` class for an element, or make use of all features of the [party module](https://party.js.org/docs)!
Also, you'd better to not spam particles, because it can cause performance issues.

# Examples
## Simple confetti button
```html
<button class="confetti">Click me!</button>
```
## DataView JS support 
````
```dataviewjs
const buttonMaker = (text) => {
    const btn = this.container.createEl('button', {"text": text});
    btn.addEventListener('click', async (evt) => {
      evt.preventDefault();
	    party.confetti(btn); // <---- creating confetti
	    party.sparkles(btn); // <---- creating sparkles
    });
    return btn;
}

dv.table(["File", "Button"],
	dv.pages('"Dataview"')
    .map(t => [
      t.file.link,
      buttonMaker("Let's start the party!")
    ]
  )
)
```
````
