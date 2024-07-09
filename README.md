Parade of Karabiner-Elements Modifications
==========================================

## DESCRIPTION

  Keyboard customization config for
  [Karabiner-Elements](https://karabiner-elements.pqrs.org/)
  (using [complex_modifications](https://karabiner-elements.pqrs.org/docs/json/complex-modifications-manipulator-definition/) JSON)
  that'll make your Mac feel like Linux.

  Basically, it swaps `Ctrl-` and `Cmd-` key combos for
  the whole system, and for specific apps.

  For less complex bindings that simply call an app
  (e.g., to open a new browser window), check out
  [skhd](https://github.com/koekeishiya/skhd)
  and our related config project,
  [`macOS-skhibidirc`](https://github.com/DepoXy/macOS-skhibidirc)

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

  There may also be additional bindings for other interesting effects.

## JSON FILES

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

    - *#0414 — Slack — Delete Back-Word like readline (Cmd-w)*

      Slack &lt;`Cmd-w`&gt; deletes back-word, like `readline`

## SEE ALSO

  This project tackles more advanced modifications that simpler, yet
  easier to config, applications do not support.

  - Consider using [skhd](https://github.com/koekeishiya/skhd) for
    basic action bindings.

    E.g., if a modification is only `to: [ { shell_command: ... } ]`,
    then you might find `skhd` easier.

    - `skhd` uses one or more flat config files, starting at
      `~/.config/skhd/skhdrc`, that, as soon as they change,
      `skhd` reloads. I.e., no more opening Karabiner
      Elements, finding the rule, clicking the trash can,
      then adding the rule back. Also the `skhdrc` config
      supports comments, unlike Karabiner Elements JSON.

  - See the related
    [`macOS-skhibidirc`](https://github.com/DepoXy/macOS-skhibidirc)
    project for lots of (opinionated) `skhdrc` config ideas:

    https://github.com/DepoXy/macOS-skhibidirc#👤

  This project also complements
  [`macOS-Onboarder`](https://github.com/DepoXy/macOS-onboarder),
  which remaps application menu items using `defaults write`
  to configure `NSUserKeyEquivalents` for each app:

  https://github.com/DepoXy/macOS-onboarder#🏂

  - Specifically, see the defaults script:

    https://github.com/DepoXy/macOS-onboarder/blob/release/bin/slather-defaults.sh

  This project is part of the DepoXy Development Environment Orchestrator

  https://github.com/DepoXy/depoxy#🍯

## AUTHOR

Copyright (c) 2020-2023 Landon Bouma &lt;depoxy@tallybark.com&gt;

This software is released under the MIT license (see `LICENSE` file for more)

## REPORTING BUGS

&lt;https://github.com/DepoXy/Karabiner-Elephants/issues&gt;

