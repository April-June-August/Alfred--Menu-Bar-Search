# <img src='Workflow/icon.png' width='45' align='center' alt='icon'> Menu Bar Search - An Alfred Workflow

Search through menu options of the frontmost application. 

[⤓ Install on the Alfred Gallery](https://alfred.app/workflows/mayjunejuly/menu-bar-search/)

## Usage

Search menu bar items of the frontmost app via the `menu` keyword.

![Searching through Xcode menu items](Workflow/images/keyword-usage.png)

* <kbd>↩</kbd> Action the item.

Configure the Hotkey for faster triggering.

Prepend your query with `#` to search by keyboard shortcut.

![Searching through Xcode menu items with shortcut](Workflow/images/keyword-usage-search-with-shortcut.png)

Fuzzy searches supported. For instance, `menu cw` will match the menu item ‘Close Window’.

## Changelog

<details>
<summary>Click to expand</summary>

- 1.0 - Initial Release
- 1.1 - Added Fuzzy Text Matching for Menus
- 1.1.1 - Changed run behaviour to terminate previous script, this makes the experience slightly more faster
- 1.2 - Completely native menu clicking, removed reliance on AppleScript
  - 1.2.1 - Performance improvements when generating menus using direct JSON encoding
  - 1.2.2 - More performance improvements while filtering menu items
- 1.3 - Added `-async` flag to allow threaded scanning and populating of menus
- 1.4 - Added `-cache` setting to enable menu result caching and also set a timeout for cache invalidation
  - 1.4.1 - Invalidate cache (if present) after actioning a menu press
  - 1.4.2 - Slide the cache invalidation window forward in case we get invalidated by a near miss
  - 1.4.3 - Speed improvements to caching, text search and fuzzy matching
  - 1.4.4 - Added `-no-apple-menu` flag that will skip the apple menu items
  - 1.4.5 - Tuned fuzzy matcher, allows non-continuous anchor token search
- 1.5 - Faster caching using protocol buffers
  - 1.5.1 - Reduced file creation for cache storage
  - 1.5.2 - Better support for command line apps that create menu bar owning applications
  - 1.5.3 - Protocol buffer everything - microscopic speed improvements, but hey...
  - 1.5.4 - Added various environment variables to fine tune menu listings
  - 1.5.5 - Tweaked ranking of search results for better menu listings
- 1.6 - Added per app customization via Settings.txt configuration file
- 1.7 - Universal build for M1 and Intel
- 1.8 - Fixed the universal build
- 1.9 - changed to user configuration, and signed executable (exported using Alfred 5)
- 2.0 - Alfred workflow gallery support! With added shortcut search, brand new configuration settings, tweaks to caching behaviour, brand new icons

</details>

## Credits

- This repo is a fork of [Benzi Ahamed](https://github.com/BenziAhamed)’s [Menu Bar Search](https://github.com/BenziAhamed/Menu-Bar-Search) ([abandoned](https://github.com/BenziAhamed/Menu-Bar-Search/pull/33)), including a [fix](https://github.com/occludedpixel/Menu-Bar-Search) from [occludedpixel](https://github.com/occludedpixel).
- Based on the ctwise’s ObjC implementation of [Menu Bar Search](https://www.alfredforum.com/topic/1993-menu-search/), which Benzi Ahamed have ported over to Swift and added caching and per app configuration to speed things up.
- Bundled with Apple’s [swift-protobuf](https://github.com/apple/swift-protobuf), licensed under [Apache License 2.0](https://github.com/apple/swift-protobuf/blob/main/LICENSE.txt).

## License

This project is licensed under the [BSD-3-Clause license](./LICENSE). 
