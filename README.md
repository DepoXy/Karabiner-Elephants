Parade of Karabiner-Elements Modifications
==========================================

## DESCRIPTION

  Keyboard customization config for
  [Karabiner-Elements](https://karabiner-elements.pqrs.org/)
  (using [complex_modifications](https://karabiner-elements.pqrs.org/docs/json/complex-modifications-manipulator-definition/) JSON)
  that'll make your Mac feel like Linux.

  Also other bindings, like systemwide commands to bring specific
  applications to the foreground.

## USAGE

  Copy or symlink the JSON files you like to your local
  Karabiner-Elements config directory.

  E.g., copy them to:

      ~/.config/karabiner/assets/complex_modifications

## OVERVIEW

  Take a look around the [complex_modifications](complex_modifications/)
  directory to see if there's anything appealing.

  - Each file is labeled by the application it affects,
    and each JSON rule is descriptively titled.

  - See [JSON FILES](#json-files) below for an overview of each file.

## PURPOSE

  The main goal of this project is to make macOS behave
  like a Linux desktop (MATE).

  - You'll find rules to swap Command and Alt keys, for example.

  - Also many of the Cmd-key bindings are rebound to Ctrl-key.

  You'll also find a number of bindings to front specific apps
  by using a global binding.

  - E.g., &lt;`Cmd-a`&gt; brings forward the email application (which
    could be the Outlook app, or Outlook in a Chrome browser tab).

    - In this example, note that &lt;`Cmd-a>`&gt; is not Select All.
      Select All is remapped to &lt;`Ctrl-a>`&gt;, because Linux.

  There are also additional bindings for other interesting effects.

## JSON FILES

### Systemwide Modifier Key Swaps

  - [0110-system-swap-mods-ergo.json](complex_modifications/0110-system-swap-mods-ergo.json)

    Contains one rule for Logitech Ergo K860 keyboards that
    swaps the left Command and left Option keys.

    - *#0111 — Systemwide — Swap Keys: Command ↔ Option (Left)*

      - Systemwide: Swaps &lt;`Left-Command`&gt; and &lt;`Left-Option`&gt;

    This rule could be updated to support additional keyboards (although
    many keyboards nowadays have programmable firmware that let you make
    this same modification).

  - [0130-system-alt-r-to-ctl-l.json](complex_modifications/0130-system-alt-r-to-ctl-l.json)

    Six rules to remap &lt;`Right-Option`&gt; to &lt;`Left-Control`&gt;
    when using Up, Down, Page Up, Page Down, Home and End motions.

    These rules are currently restricted to Logitech Ergo K860 keyboards,
    because many keyboards let you remap this at the firmware level (and
    if you have both an Ergo K860 and a mechanical keyboard, you might
      want different KE bindings for each).

    - *#0131 — Syswide — Ergo K480 — Forward Keys: Up/Down-RightOption*

      - Systemwide: Forwards &lt;`Right-Option-Up`&gt; to &lt;`Left-Control-Up`&gt;

      - Systemwide: Forwards &lt;`Right-Option-Down`&gt; to &lt;`Left-Control-Down`&gt;

    - *#0132 — Syswide — Ergo K480 — Forward Keys: Home/End-RightOption*

      - Systemwide: Forwards &lt;`Right-Option-Home`&gt; to &lt;`Left-Control-Home`&gt;

      - Systemwide: Forwards &lt;`Right-Option-End`&gt; to &lt;`Left-Control-End`&gt;

    - *#0133 — Syswide — Ergo K480 — Forward Keys: PageUp/PageDown-RightOption*

      - Systemwide: Forwards &lt;`Right-Option-PageUp`&gt; to &lt;`Left-Control-PageUp`&gt;

      - Systemwide: Forwards &lt;`Right-Option-PageDown`&gt; to &lt;`Left-Control-PageDown`&gt;

    The Control-Home/End/PageUp/PageDown motions are especially useful for
    right-handed motions in certain text editors.

### Systemwide Cut/Copy/Paste/Select-All Key Swaps

  - [0150-system-cmd-2-ctl-cxva.json](complex_modifications/0150-system-cmd-2-ctl-cxva.json)

    Swaps edit command bindings (&lt;`Cmd-key`&gt; ↔ &lt;`Ctrl-key`&gt;).

    E.g., Copy is remapped from &lt;`Cmd-c`&gt; to &lt;`Ctrl-c`&gt;.

    - *#0151 — Systemwide — Remap Cut: Control-X → Command-X*

      *#0152 — Systemwide — Remap Copy: Control-C → Command-C*

      *#0153 — Systemwide — Remap Paste: Control-V → Command-V*

      *#0154 — Systemwide — Remap Select All: Control-A → Command-A*

      - Systemwide: Forwards &lt;`Ctrl-[xcva]`&gt; to &lt;`Cmd-[xcva]`&gt;
        (with only these rules, you could copy with either
        &lt;`Ctrl-c`&gt; or &lt;`Cmd-c`&gt;).

    - *#0155 — Systemwide — Remap Cut: Control-X ← Command-X*

      *#0156 — Systemwide — Remap Copy: Control-C ← Command-C*

      *#0157 — Systemwide — Remap Paste: Control-V ← Command-V*

      *#0158 — Systemwide — Remap Select All: Control-A ← Command-A*

      - Systemwide: Forwards &lt;`Cmd-[xcva]`&gt; back to &lt;`Ctrl-[xcva]`&gt;,
        so that if an app has a menu item at, e.g.,
        &lt;`Cmd-c`&gt;, it's now at &lt;``Ctrl-c``&gt;.
   
### Application Left-Right Modifier Motions

  - [0170-apphoc-ctl-and-alt-lr.json](complex_modifications/0170-apphoc-ctl-and-alt-lr.json)

    Swaps cursor movement bindings:

    &lt;`Ctrl-left`&gt; ↔ &lt;`Alt-left`&gt;

    &lt;`Ctrl-right`&gt; ↔ &lt;`Alt-right`&gt;

    If you're used to Linux, &lt;`Ctrl-left/right`&gt; jumps the cursor by
    word, and &lt;`Alt-left/right`&gt; by line. On macOS, it's the reverse.
    These rules reverse that reverse.

    Note these rules only apply to certain apps: Finder, Chrome, Teams,
    Outlook, and Slack. Please PR if you want to add additional apps.

    - *#0171 — Finder↔/Chrome↔/Teams↔/½Outlook — Remap Control+LeftArrow ↔ Alt+LeftArrow*

      Apps: Swaps &lt;`Ctrl-left`&gt; ↔ &lt;`Alt-left`&gt;

    - *#0172 — Finder↔/Chrome↔/Teams↔/½Outlook→ — Remap Control+RightArrow ↔ Alt+RightArrow*

      Apps: Swaps &lt;`Ctrl-right`&gt; ↔ &lt;`Alt-right`&gt;

    - *#0173 — Outlook — Remap Alt+LeftArrow → Command+LeftArrow*

      Outlook-only: Forwards &lt;`Alt-left`&gt; → &lt;`Cmd-left`&gt;

    - *#0174 — Outlook — Remap Alt+RightArrow → Command+RightArrow*

      Outlook-only: Forwards &lt;`Alt-right`&gt; → &lt;`Cmd-right`&gt;

### Chrome bindings

  - [0310-applcn-chrome.json](complex_modifications/0310-applcn-chrome.json)

    Chrome-specific bindings.

    - *#0311.t — Google Chrome — New Window (Cmd-t)*

      Systemwide: &lt;`Cmd-t`&gt; opens new Chrome window

    - *#0314 — Google Chrome — (Shift-)F5 (Hard) Reload (maps to (Shift-)Ctrl-R)*

      Chrome: &lt;`F5`&gt; reloads

    - *#0315 — Google Chrome — Remap Command+Click → Control+Click*

      Chrome: Forwards &lt;`Cmd-click`&gt; → &lt;`Ctrl-click`&gt;
      (which sends a clicked link to a new tab)

    - *#0316 — Google Chrome — Remap Command+Click ← Control+Click*

      Chrome: Forwards &lt;`Ctrl-click`&gt; → &lt;`Cmd-click`&gt;
      (reverse of previous rule)

    - *#0317 — Google Chrome — Delete Back-Word like readline (Cmd-w)*

      Chrome: &lt;`Cmd-w`&gt; deletes back-word, like `readline`

### iTerm2 bindings (and one for Terminal.app)

  - [0330-applcn-iterm2.json](complex_modifications/0330-applcn-iterm2.json)

    - *#0331 — iTerm2 — New Window (Cmd-m)*

      Systemwide: &lt;`Cmd-m`&gt; opens a new `iTerm2` window (terminal session)

    - *#0332 — iTerm2 — Foreground (Shift-Cmd-M)*

      Systemwide: &lt;`Shift-Cmd-M`&gt; brings the topmost `iTerm2` window to foreground

    - *#0333 — Terminal.app — New Window (Ctrl-Cmd-M)*

      Systemwide: &lt;`Ctrl-Cmd-M`&gt; opens a new `Terminal.app` window (terminal session)

  - [0340-applcn-iterm2-fronter.json](complex_modifications/0340-applcn-iterm2-fronter.json)

    `iTerm2` numbers its windows, and &lt;`Cmd-1`&gt; through &lt;`Cmd-9`&gt;
    brings the `iTerm2` window with the corresponding number to the foreground.

    - *#0341 — iTerm2 — Foreground Window Numbered “1.” (Cmd-1)*

    - *#0342 — iTerm2 — Foreground Window Numbered “2.” (Cmd-2)*

    - *#0343 — iTerm2 — Foreground Window Numbered “3.” (Cmd-3)*

    - *#0344 — iTerm2 — Foreground Window Numbered “4.” (Cmd-4)*

    - *#0345 — iTerm2 — Foreground Window Numbered “5.” (Cmd-5)*

    - *#0346 — iTerm2 — Foreground Window Numbered “6.” (Cmd-6)*

    - *#0347 — iTerm2 — Foreground Window Numbered “7.” (Cmd-7)*

    - *#0348 — iTerm2 — Foreground Window Numbered “8.” (Cmd-8)*

    - *#0349 — iTerm2 — Foreground Window Numbered “9.” (Cmd-9)*

### MacVim foregrounder

  - [0350-applcn-macvim.json](complex_modifications/0350-applcn-macvim.json)

    - *#0351 — MacVim — Foreground (Cmd-`)*

      Systemwide: &lt;`` Cmd-` ``&gt; brings MacVim to foreground

### Meld bindings

  - [0370-applcn-meld.json](complex_modifications/0370-applcn-meld.json)

    Remaps Meld &lt;`Cmd-key`&gt; menu items to their &lt;`Ctrl-key`&gt; equivalent
    (because Meld does not respect `defaults write ... NSUserKeyEquivalents`).

    - *#0371 — Meld — Remap Meld > Quit Meld: Control-Q → Command-Q*

    - *#0372 — Meld — Remap File > New Comparison...: Control-N → Command-N*

    - *#0373 — Meld — Remap File > Save: Control-S → Command-S*

    - *#0374 — Meld — Remap File > Save As...: Control-S → Command-S*

    - *#0375 — Meld — Remap File > Close: Control-W → Command-W*

    - *#0376 — Meld — Remap Edit > Undo: Control-Z → Command-Z*

    - *#0378 — Meld — Remap Edit > Redo: Shift-Control-Z → Shift-Command-Z*

    - *#0379 — Meld — Remap Edit > Find...: Control-F → Command-F*

    - *#0380 — Meld — Remap Edit > Find Next: Control-G → Command-G*

    - *#0381 — Meld — Remap Edit > Find Previous: Shift-Control-G → Shift-Command-G*

    - *#0382 — Meld — Remap Edit > Go to Line: Control-I → Command-I*

    - *#0383 — Meld — Remap View > Refresh: Control-R → Command-R*

### GIMP bindings

  - [0390-applcn-gimp.json](complex_modifications/0390-applcn-gimp.json)

    Remaps GIMP &lt;`Cmd-key`&gt; menu items to their &lt;`Ctrl-key`&gt; equivalent
    (because GIMP does not respect `defaults write ... NSUserKeyEquivalents`).

    - *#0391 — Gimp — Remap GIMP-2.10 > Quit GIMP-2.10: Control-Q → Command-Q*

    - *#0392 — Gimp — Remap File > New...: Control-N → Command-N*

    - *#0393 — Gimp — Remap File > Create > From Clipboard (aka Edit > Paste as > New Image): Shift-Control-V → Shift-Command-V*

    - *#0394 — Gimp — Remap File > Open...: Control-O → Command-O*

    - *#0395 — Gimp — Remap File > Open as Layers...: Shift-Control-O → Shift-Command-O*

    - *#0396 — Gimp — Remap File > Save...: Control-S → Command-S*

    - *#0397 — Gimp — Remap File > Save As...: Shift-Control-S → Shift-Command-S*

    - *#0398 — Gimp — Remap File > Export...: Control-E → Command-E*

    - *#0399 — Gimp — Remap File > Export As...: Shift-Control-E → Shift-Command-E*

    - *#0400 — Gimp — Remap File > Close View: Control-W → Command-W*

    - *#0401 — Gimp — Remap File > Close All: Shift-Control-W → Shift-Command-W*

### Slack bindings

  - [0410-applcn-slack.json](complex_modifications/0410-applcn-slack.json)

    - *#0411 — Slack — Systemwide — Foreground (Shift-Ctrl-Cmd-S)*

      Systemwide: &lt;`Shift-Ctrl-Cmd-S`&gt; brings Slack to foreground

    - *#0412 — Slack — Remap Control → Alt+Click*

      Slack: Forwards &lt;`Ctrl-click`&gt; → &lt;`Alt-click`&gt;

    - *#0413 — Slack — Remap Alt+Click ← Control+Click*

      Slack: Forwards &lt;`Alt-click`&gt; → &lt;`Ctrl-click`&gt;
      (reverse of previous rule)

    - *#0414 — Slack — Delete Back-Word like readline (Cmd-w)*

      Slack &lt;`Cmd-w`&gt; deletes back-word, like `readline`

### Outlook bindings

  - [0430-applcn-outlook-or-tab.json](complex_modifications/0430-applcn-outlook-or-tab.json)

    - *#0431.b — Microsoft Outlook — Foreground (Shift-Ctrl-Cmd-A)*

      Systemwide: &lt;`Shift-Ctrl-Cmd-A`&gt; brings Outlook to foreground

### OpenLens foregrounder

  - [0470-applcn-openlens.json](complex_modifications/0470-applcn-openlens.json)

    - *#0471 — OpenLens — Systemwide — Foreground (Shift-Ctrl-Cmd-Q)*

      Systemwide: &lt;`Shift-Ctrl-Cmd-Q`&gt; brings OpenLens to foreground

### DBeaver foregrounder

  - [0490-applcn-dbeaver.json](complex_modifications/0490-applcn-dbeaver.json)

    - *#0491 — DBeaver — Systemwide — Foreground (Shift-Ctrl-Cmd-E)*

      Systemwide: &lt;`Shift-Ctrl-Cmd-E`&gt; brings DBeaver to foreground

### Webex foregrounder

  - [0510-vidapp-webex-teams-zoom.json](complex_modifications/0510-vidapp-webex-teams-zoom.json)

    - *#0511.b — Webex — Systemwide — Foreground (Shift-Ctrl-Cmd-W)*

      Systemwide: &lt;`Shift-Ctrl-Cmd-W`&gt; brings Webex to foreground

    - *#0511.c — Microsoft Teams — Foreground (Shift-Ctrl-Cmd-T)*

      Systemwide: &lt;`Shift-Ctrl-Cmd-T`&gt; brings Teams to foreground

### Postman foregrounder

  - [0530-applcn-postman.json](complex_modifications/0530-applcn-postman.json)

    - *#0531 — Postman — Systemwide — Foreground (Shift-Ctrl-Cmd-P)*

      Systemwide: &lt;`Shift-Ctrl-Cmd-P`&gt; brings Postman to foreground

## SEE ALSO

  This project complements *macOS-Onboarder*, which remaps application
  menu items the easy way (using `default write` to configure
  `NSUserKeyEquivalents` for each app):

  https://github.com/DepoXy/macOS-onboarder#🏂

  - Specifically, see the defaults script:

    https://github.com/DepoXy/macOS-onboarder/blob/release/slather-defaults.sh

  This project is part of the DepoXy Development Environment Orchestrator

  https://github.com/DepoXy/depoxy#🍯

## AUTHOR

Copyright (c) 2020-2023 Landon Bouma &lt;depoxy@tallybark.com&gt;

This software is released under the MIT license (see `LICENSE` file for more)

## REPORTING BUGS

&lt;https://github.com/DepoXy/Karabiner-Elephants/issues&gt;

