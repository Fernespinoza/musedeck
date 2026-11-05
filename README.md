# Muse Deck

Fernando's personal Jarvis deck: the real muse.ai chat in a WebView2 pane,
a daily ribbon (clock, Houston weather, headlines, battery), a Board with
notes and a whiteboard, and a Stage for full-detail views - all summoned
by Win+Shift+D. WPF on .NET 8, portable single folder, no installer.

Releases in this repo power the app's built-in auto-updater (Phase 2.5):
the Deck checks the latest release on launch, downloads the zip asset in
the background, and applies it from the tray menu. All user data lives in
%LocalAppData%\MuseDeck, never in the program folder.
