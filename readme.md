 
```
   __            __  ____          
  / /____  _  __/ /_/ __/___  _  __
 / __/ _ \| |/_/ __/ /_/ __ \| |/_/
/ /_/  __/>  </ /_/ __/ /_/ />  <  
\__/\___/_/|_|\__/_/  \____/_/|_|  
```

_a port of spotify tui to firefox_

## Preview

## Prequisites

- Sidebery (optional)

## Installation

### Manual

1. Download the files
2. Go to `about:profiles`
3. Find your profile -- ( _„This is the profile in use and it cannot be deleted.”_ )
4. Open the profile's root directory
5. Move the files chrome directory and user.js there
6. Restart firefox

## Sidebery

Sidebery css is being set from within `content/sidebery` (applied as content to
the sidebery url). If you have any prexisting css set from within the sidebery
settings, they might clash or make it so that the sidebery style does not match
the example.

#### Settings

The theme was made using a reset sidebery config, so there should not be
anything crazy needed here, notable settings being set is using the **plain**
theme and **firefox** color scheme. If you want to you can import the sidebery
settings provided.

> [!IMPORTANT]
> **Importing sidebery settings overwrites your current settings, do this at
> your own risk.**

## Customization

The icon configuration utilizes code that is originally from ShyFox, therefore
the same settings are used (these can be set in about:config).
| Setting | true | false (default) |
| -------------------------------------- | --------------------------------------------------------------------- | ------------------------- |
| `shyfox.enable.ext.mono.toolbar.icons` | Supported extensions get monochrome icons as toolbar buttons | Standard icons used |
| `shyfox.enable.ext.mono.context.icons` | Supported extensions get monochrome icons as context menu items | Standard icons used |
| `shyfox.enable.context.menu.icons` | Many context menu items get icons | No icons in context menus |

### CSS configurations
The theme ships with a `defaults.css`, this file can be overriden by creating a
`config.css` inside the chrome directory. For instance if I'd want to change the
border radius it would look like this:

```css
/* path: chrome/config.css */
:root {
  --tf-rounding: 4px;
}
```

#### Defaults
```css
:root {
  --tf-font-family: "SF Mono", Consolas, monospace; /* Font family of config */
  --tf-font-size: 14px; /* Font size of config */
  --tf-accent: var(--toolbarbutton-icon-fill); /* Accent color used, eg: color when hovering a container  */
  --tf-bg: var(--lwt-accent-color, -moz-dialog); /* Background color of all elements, tab colors derive from this */
  --tf-border: var(--arrowpanel-border-color, --toolbar-field-background-color); /* Border color when not hovered */
  --tf-border-transition: 0.2s ease; /* Smooth color transitions for borders */
  --tf-border-width: 2px; /* Width of borders */
  --tf-rounding: 0px; /* Border radius used through out the config */
  --tf-margin: 0.8rem; /* Margin used between elements in sidebery */
  --tf-display-horizontal-tabs: none; /* If horizontal tabs should be shown, none = hidden, block = shown */
  --tf-display-nav-buttons: none; /* If the navigation buttons (back, forward) should be shown, none = hidden, block = shown */
  --tf-newtab-logo: "   __            __  ____          \A   / /____  _  __/ /_/ __/___  _  __\A  / __/ _ \\| |/_/ __/ /_/ __ \\| |/_/\A / /_/  __/>  </ /_/ __/ /_/ />  <  \A \\__/\\___/_/|_|\\__/_/  \\____/_/|_|  ";
}
```

### Changing the new tab logo

The new tab logo can be any string you want, to create a string with line breaks
add a `\A` at every line break, also make sure to break any backslashes, eg. if
you want a `\`, you need to write `\\`. I used [this tool](https://www.patorjk.com/software/taag/#p=display&f=Slant&t=textfox)
to create the current logo.

Wanna hide the logo? Simply pass an empty string as the logo.

## Acknowledgements

[original textfox github repo](https://github.com/adriankarlen/textfox)

[Naezr](https://github.com/Naezr) - Icon logic and some sideberry logic.

изз - starting working on a similar project in the glazewm discord, prompted me
to get started on the work.

