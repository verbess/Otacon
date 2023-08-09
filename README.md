# Otacon
## Initializing C# Dev Kit and Unity
### Unity Settings
1. Install the Unity package `Visual Studio Editor` version 2.0.20 or higher.
2. Set `Visual Studio Code` as the external C# editor for Unity.
### Visual Studio Code Settings
1. Add `"dotnet.dotnetPath": "$YOURPATH",` to the `settings.json` file.

## Configuration
``` Json
// Editor settings:
"editor.formatOnSave": true,
// Documentation comment powered by OmniSharp
"editor.formatOnType": true,
"editor.wordWrap": "bounded",
"editor.renderWhitespace": "boundary",
"editor.stickyScroll.enabled": true,
"editor.cursorSmoothCaretAnimation": true,
// Bracket pair colorization
"editor.bracketPairColorization.enabled": true,
```