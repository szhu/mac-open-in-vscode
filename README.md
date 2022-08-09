# Mac "Open in VSCode"

This is a tiny app that declares folders ending in `.git`, `.vscode`, and
`.code` as [macOS packages]. You can double-click these folders and it'll open
them in VSCode!

[macos packages]: https://en.wikipedia.org/wiki/Package_(macOS)

## Why this is useful

Currently, double-clicking a project/repo folder opens it in Finder, but more
often than not, what you really want to do with these folders is open it in
VSCode.

Also, if your code project is folder contains thousands of tiny files (hi,
`node_modules`!), all these files clutter up your Spotlight searches.

Instead, if you use this tool, you can now do a Spotlight search for your
project and press enter to immediately open it in VSCode!

## How to use

Download or clone this repo, then, for for each project you'd like to turn into
a package, add one of these extensions to the end of the folder name: `.git`,
`.vscode`, or `.code`.

That's it! You can now double-click the folder and it'll open in VSCode. To open
the folder in Finder, just right-click and select "Show Package Contents".

## What extension should I use?

Currently, the app declares all the extensions equally, but for some reason,
macOS treats `*.git` folders differently:

- Name your folder `*.git` to hide it and its contents from all Spotlight
  results.
- Name your folder `*.code` or `*.vscode` to have the folder and its contents
  still be indexed normally in Spotlight.

I'm still trying to figure out why this is happening, and to figure out if I can
create a declaration such that the only the folder (and not its contents) are
Spotlight-searchable.

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
