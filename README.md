# Mac "Open in VSCode" Shortcut

This tool helps you make tiny helper apps that, when clicked, open the containing folder in Visual Studio Code.

## Why

macOS gives files great treatment -- you can open them from Spotlight or the Dock. Opening folders in VSCode isn't nearly as nice.

Currently, the fastest ways to do this are:

- Dragging the folder into the app icon or window.
- Opening VSCode, then finding the folder via "Open Recent".
- Using a third-party launcher.

In short, there's currently no quick, built-in way to open a folder in VSCode.

## How to use

1. Download or clone this repo.
2. In Finder, go to the folder you want to make a shortcut to.
3. Use Spotlight to search for the "Make VSCode Shortcut" app. (Or add it to the Dock and open it.) Note that the frontmost Finder window must showing the desired folder.
4. The app will make a new shortcut in the folder with the same name!

If you want to ignore these shortcuts in Git, add the following line to your global `.gitignore` file:

```gitignore
Open in Visual Studio Code.app
```
