## 0.0.7

* Split core Dart models and controller code into focused source files.
* Split Windows and Linux native rendering into dedicated renderer and resource units.
* Fixed Windows CMake after the native source split.
* Fixed desktop lyrics slider state sync and background opacity rendering.
* Centered desktop lyrics text by default and fixed default alignment behavior.
* Fixed macOS opacity clamping to allow fully transparent values.
* Resolved Linux overlay build warnings.

## 0.0.6

* Added macOS native implementation with AppKit overlay window support.
* Added macOS example host project and XCTest coverage.
* Added an extra Windows native unit test for `updateLyricFrame`.

## 0.0.5

* Refactored `DesktopLyrics` to default to a shared singleton instance.
* Prevented state split between `apply` and `render` when called from different app layers.
* Added singleton lifecycle tests (`same instance`, `dispose -> recreate`, `shared state across references`).

## 0.0.4

* Changed default visibility to disabled (`enabled: false`) to avoid showing overlay during app startup.
* Aligned Windows/Linux native default `enabled` behavior with Dart-side default.
* Updated README usage notes for explicit enable flow.
* Added tests for default disabled state and adjusted toggle tests.

## 0.0.3

* Added GitHub Actions tag-based publish workflow for pub.dev.
* Added public API dartdoc comments to improve pub.dev documentation score.
* Updated README with Trusted Publisher + tag release instructions.

## 0.0.1

* Initial desktop floating lyrics implementation (Windows/Linux).
* Added public Dart API:
  * `DesktopLyricsFrame`
  * `DesktopLyricsConfig`
  * `DesktopLyrics.apply`
  * `DesktopLyrics.state` (read-only, single state entry)
  * `DesktopLyrics.render`
  * `DesktopLyrics.dispose`
* Added desktop overlay behavior:
  * top-most transparent layered window
  * click-through toggle
  * drag and double-click reset position
  * text/shadow/stroke style controls
