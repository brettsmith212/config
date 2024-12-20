# Instructions

1. clone project into .config/
2. brew install koekeishiya/formulae/yabai

- brew services start yabai
- brew services stop yabai
- brew services restart yabai

or

- yabai --start-service
- yabai --stop-service
- yabai --restart-service

3. Change System Settings on Mac

- Create 7 Desktop Windows
- Keyboard -> Keyboard Shortcuts -> Mission Control
  - Expand `Mission Control` box
  - Select all `Switch to Desktop n` (should be 7 from creating earlier)
  - Now you can switch between the 7 desktops using Ctrl + 1, Ctrl + 2, etc
- Accessibility -> Display
  - Turn `Reduce motion` on
  - Allows instant transition between desktops
- Desktop & Dock -> Scroll to the bottom where it says `Mission Control`
  - Turn `Automatically rearrange Spaces based on most recent use` to off
  - Prevents desktops from rearranging when you move between applications

[Youtube Tutorial](https://www.youtube.com/watch?v=k94qImbFKWE)
