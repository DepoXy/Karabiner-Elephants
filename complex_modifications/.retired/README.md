Retired Karabiner-Elephants Modifications
=========================================

## RETIRED BINDINGS

  The author has migrated many bindings to
  [`skhd`](https://github.com/koekeishiya/skhd), whose
  ``~/.config/skhd/skhdrc`` file makes it even easier to create
  and update the more simple keybindings.

  - See the related
    [`macOS-skhibidirc`](https://github.com/DepoXy/macOS-skhibidirc)
    project:

    https://github.com/DepoXy/macOS-skhibidirc#👤

    - Many of the bindings listed below were migrated to
      that project's ``skhdrc``:

      https://github.com/DepoXy/macOS-skhibidirc/blob/release/.config/skhd/skhdrc

### Chrome bindings

  - [0310-applcn-chrome.json](complex_modifications/0310-applcn-chrome.json)

    Chrome-specific bindings.

    - *#0311.t — Google Chrome — New Window (Cmd-t)*

      Systemwide: &lt;`Cmd-t`&gt; opens new Chrome window

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

### Slack bindings

  - [0410-applcn-slack.json](complex_modifications/0410-applcn-slack.json)

    - *#0411 — Slack — Systemwide — Foreground (Shift-Ctrl-Cmd-S)*

      Systemwide: &lt;`Shift-Ctrl-Cmd-S`&gt; brings Slack to foreground

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

### Keyboard-specific Systemwide Modifier Key Swaps

  The author has not used their Logitech Ergo K860 in a spell,
  so, which these bindings still work, they're no longer "supported",
  and scarce few people might care about them.

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

