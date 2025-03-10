# Otacon
**Switch to the Godot engine; if you are still using the Unity engine, please do not update.**  
**If you accidentally updated, please revert to version [1.4.0](https://github.com/verbess/Otacon/releases/tag/v1.4.0).**

## Initializing C# Dev Kit
### Visual Studio Code Settings
Add some configuration options to the [settings.json](https://code.visualstudio.com/docs/getstarted/settings#_settingsjson) file, as shown in the following code.

``` Json
    "dotnet.dotnetPath": "$YOUR_DOTNET_INSTALL_PATH",
    "dotnetAcquisitionExtension.existingDotnetPath": [
        {
            "extensionId": "ms-dotnettools.csharp",
            "path": "$YOUR_DOTNET_INSTALL_PATH"
        },
        {
            "extensionId": "ms-dotnettools.csdevkit",
            "path": "$YOUR_DOTNET_INSTALL_PATH"
        },
        // If you are still using the Unity engine, add this too.
        // {
        //     "extensionId": "visualstudiotoolsforunity.vstuc",
        //     "path": "$YOUR_DOTNET_INSTALL_PATH"
        // }
    ]
    // Example:
    // "dotnet.dotnetPath": "/usr/local/bin",
    // "dotnetAcquisitionExtension.existingDotnetPath": [
    //     {
    //         "extensionId": "ms-dotnettools.csharp",
    //         "path": "/usr/local/bin/dotnet"
    //     },
    //     {
    //         "extensionId": "ms-dotnettools.csdevkit",
    //         "path": "/usr/local/bin/dotnet"
    //     },
    //     {
    //         "extensionId": "visualstudiotoolsforunity.vstuc",
    //         "path": "/usr/local/bin/dotnet"
    //     }
    // ]
```

## Initializing Godot
[Godot Engine 4.1 documentation](https://docs.godotengine.org/en/stable/tutorials/scripting/c_sharp/c_sharp_basics.html)

1. Set Visual Studio Code as the external editor in Godot.

    > In Godot's `Editor → Editor Settings` menu:  
    > Set `Dotnet -> Editor -> External Editor` to `Visual Studio Code`.

2. To configure a project for debugging, you need a `tasks.json` and `launch.json` file in the `.vscode` folder with the necessary configuration. An example configuration can be found [here](https://github.com/godotengine/godot-csharp-vscode/issues/43#issuecomment-1258321229).

    Fortunately, there is a [C# Tools for Godot](https://marketplace.visualstudio.com/items?itemName=neikeq.godot-csharp-vscode) Visual Studio Code extension to make this setup easier and to provide further useful tools.

    Use `C# Godot: Generate Assets for Build and Debug` command to generate `tasks.json` and `launch.json` file.

    How to use command? [Follow this](https://code.visualstudio.com/docs/getstarted/tips-and-tricks#_command-palette).

3. **Remember to create a C# solution and build the .NET project.**

    > 1. In Godot's `Project -> Tools -> C#` menu:  
    >    Click `Create C# solution`.  
    > 2. In Godot's `MSBuild` menu:  
    >    Click `Build -> Build Project`.

## Configuration
``` Json
// Editor settings:
"editor.renderWhitespace": "boundary",
"editor.wordWrap": "bounded",
"editor.wordWrapColumn": 120,
"editor.formatOnSave": true,
"editor.formatOnType": true,
"files.insertFinalNewline": true,
// Csharpier settings:
"[csharp]": {
    "editor.defaultFormatter": "csharpier.csharpier-vscode"
},
"[xml]": {
    "editor.defaultFormatter": "csharpier.csharpier-vscode"
},
```
