# Mac "Open in VSCode"

This is a tiny app that declares folders ending in `.git`, `.vscode`, and
`.code` as [macOS packages]. When the package is opened, it will open the folder
in Visual Studio Code.

[macos packages]: https://en.wikipedia.org/wiki/Package_(macOS)

## Why this is useful

Currently, double-clicking a project/repo folder opens it in Finder. When you
double-click the folder, you probably wanted to open it in VSCode.

If your code project is folder contains thousands of tiny files (hi,
`node_modules`!), they clutter up your Spotlight searches.

Instead, if you use this tool, you can now do a Spotlight search for your
project and press enter to immediately open it in VSCode!

## How to use

1. Download or clone this repo.
2. For each project you'd like to turn into a package, add one of these
   extensions to the end of the folder name: `.git`, `.vscode`, or `.code`.
   (Currently, the extensions are treated equally.)

## Future considerations

<details>

<summary>Some features that could be added in the future:</summary>

- [ ] Allow setting a preference to change the app the file opens in.
  - Workaround, edit the id near the bottom of this file:
    `Code Project Launcher.app/Contents/MacOS/Code Project Launcher`.
- [ ] Look into which supported extensions (`.git`, `.vscode`, `.code`) makes
      the most sense for most users, and perhaps change the app to only support
      that one.
- [ ] Allow a different app per extension.
- [ ] Allow showing a prompt for the user to choose which app to open the folder
      in.
- [ ] Add a Uniform Type Identifier to the type declaration such that the "Open
      With" menu shows more relevant results. (It probably should be
      `public.folder`.)

</details>
