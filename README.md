# MapVisualizer.odin

A map generator and visualizer written in Odin to learn and test things with this language. This first was intended as a world generation for a city building game.

It uses multiple Perlin noise layers to generate a rather detailed world map that can be navigated and zoomed through using either the mouse or the keyboard. We can increase the generated size and change the seed too.

## Checking it

Binaries are available in the release tags.

## Developing

```bash
.\vendor\builder.bat run debug
```

Update submodules to fetch `ols`, then install it
```bash
git submodule update --init --remote --recursive
cd ols
.\build.bat # Or .sh for linux
```

Add ols config for the OS:
```json
{
  "collections": [
		{ "name": "raygame", "path": "/path/to/collection" },
	],
	"enable_semantic_tokens": true,
	"enable_document_symbols": true,
	"enable_hover": true,
	"enable_snippets": true,
  "enable_auto_import": true,
  "verbose": true,
	"profile": "default",
  "checker_args": "-strict-style -vet -vet-cast -vet-semicolon -debug",
	"profiles": [
		{ "name": "default", "checker_path": ["src"] }
	],
}
```

Add Coc config:
```json
"languageserver": {
    "odin": {
        "command": "ols\\ols.exe",
            "filetypes": ["odin"],
            "rootPatterns": ["ols.json"]
    }
}
```

# Kanban

https://github.com/users/Asmoddym/projects/4


# Optis:

-o:speed in release mode
-no-bounds-check for maybe better timings
