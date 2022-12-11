# extension-hub

This is the official repository for Universal Minecraft Tool extensions. All extensions are provided as-is with no guarantees. To report bugs or inquire about a specific extension, visit the repository for that extension directly.

Extensions are written in [Lua 5.3](https://www.lua.org/manual/5.3/). The manifest is written in JSON. The recommended editor for development is [Visual Studio Code](https://code.visualstudio.com/) with the [vscode-lua](https://marketplace.visualstudio.com/items?itemName=trixnz.vscode-lua) extension for syntax highlighting.

## Creating an extension

1. Create a repository for your extension from [this template](https://github.com/UniversalMinecraftTool/extension-template/generate).
2. Name your repository and set it to public. **The naming convention is PascalCase, however this is not a technical requirement.**
3. Open the newly created repository in your editor of choice. In Visual Studio Code, you can clone the repository directly from GitHub using the **Clone Git Repository...** command.
4. Edit the `manifest.json` file and supply the info for your extension.

```
{
  "link" : "",
  "name" : "ExtensionName",
  "version" : "1.0.0",
  "author" : "",
  "description" : "",
  "editions" : ["JAVA", "BEDROCK", "CONSOLE"],
  "extension_types" : ["NBT_EDITOR_STYLE"],
  "tags" : []
}
```

`link` should be the github repository link of your extension (NOT ending in .git).

`name` is a purely visual display name. It does not need to match the repository name or anything in your code.

`version` is the version of your extension. It is used to check for updates.

`author` is your preferred name to display in the extension browser.

`description` is a brief explanation of your extension. It should be kept succinct.

`editions` is a purely visual list of editions your extension supports.

`extension_types` is a purely visual list of extension types contained within your extension. Each extension can be composed of multiple types, but only `NBT_EDITOR_STYLE` is supported currently.

`tags` is a purely visual list of tags to help users identify key info and features about your extension.

5. Create your extension code in the `main.lua` file. Refer to the documentation on the Universal Minecraft Tool website for development guides and code examples. (Full documentation is not available yet, but will be created soon).

## Licensing

**If your extension does not have this license it will NOT be accepted!**

1. In your extension repository on GitHub, click **Add file** and then **Create new file**.
2. Name the file `LICENSE` and click the **Choose a license template** button.
3. Select `BSD 2-Clause "Simplified" License` from the list. Enter your information and click **Review and submit**.
4. Commit your change.

## Submitting an extension

1. Fork this [extension-hub repository](https://github.com/UniversalMinecraftTool/extension-hub).
2. In your forked repository, create a new file in the `extensions` directory with the name of your extension with these contents:

```
link=your repository link
commit=40 char commit hash
```

`link` should be the github repository link of your extension (NOT ending in .git).

`commit` should be the 40 character hash of the commit you want to publish.

4. Commit this added file to your fork.
5. Open a new pull request and enter a brief description of your extension.
6. Your extension will be reviewed and merged by one of our administrators. Your extension will only be accepted if it can be ensured it isn't malicious or poorly written. We reserve the right to deny any extensions from being added to the hub.

## Updating an extension

1. Increment the `version` field in the `manifest.json` file.
2. Update the `commit` field in your forked repository with the new commit hash.
3. Open a new pull request and enter a brief description of the changes made since the previously published version.

## Thumbnail

Thumbnail images are optional. They should be no larger than 64x64 pixels in .png format. Add the thumbnail image to the root directory of the extension repository with the name `thumbnail.png`.

If no thumbnail is supplied, a default image will be used.
