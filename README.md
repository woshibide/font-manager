# font-manager
Command line utility to activate and de-activate fonts on macOS.

## Installation

1. Clone or download this repository.
2. Make the script executable:  
   ```bash
   chmod +x font-manager.swift
   ```
3. (Optional) Move the script to a directory in your PATH for easier access:  
   ```bash
   sudo mv font-manager.swift /usr/local/bin/font-manager
   ```
4. Alternatively, compile it into a binary:  
   ```bash
   swiftc font-manager.swift -o font-manager
   sudo mv font-manager /usr/local/bin/
   ```

## Enhancements

The CLI now supports multiple font files in a single command. For example, `font-manager register *.ttf *.otf` will register all matching fonts. This behavior extends to the `unregister` command as well.

    font-manager register /path/to/font.otf
    font-manager register *.ttf *.otf

    font-manager unregister /path/to/font.otf
    font-manager unregister *.otf

    font-manager list

    font-manager list-ext

Registering a font will make it appear in the font selection panel or menu of all apps. 

The fonts do NOT need to be within the standard OS font folders. 

You can also list all installed (registered) fonts. 

You can also list all activated fonts in 'external' locations (i.e. non-standard OS font folders), with their filepaths.

This code was created by Code Copilot, under my tutelage! 

## Usage

### Commands

- `font-manager register <path(s)>`: Register font file(s). Supports wildcards (e.g., `*.ttf`).
- `font-manager unregister <path(s)>`: Unregister font file(s). Supports wildcards.
- `font-manager list`: List all installed fonts.
- `font-manager list-ext`: List fonts in non-standard locations with paths.
