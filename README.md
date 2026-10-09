# Merchigo

A site theme for [Modulento](https://github.com/alex01at/modulento): a calm,
warm retail look - a sand and off-white ground, charcoal ink, a terracotta
accent, generous rounded shapes. Built for the [shop
extension](https://github.com/alex01at/modulento-ext-shop), but works with
any extension that lists offers.

It brings a layout, a home page (a quiet hero with search, category tiles,
the newest products, and an editable feature band), card partials for
offers and providers, a stylesheet and its font. Every other page comes
from Modulento's `default` theme and only looks different.

Like the rest of the home page, every block is edited in place
(**Administration → Home page**, or directly on the page itself when
signed in with that permission): click into a heading or text to change
it, add pictures, reorder or remove blocks, or add a new one. Nothing
about this theme changes how that editor works - it only draws the blocks
differently.

The theme has a dark scheme. It follows the device, unless an account has
chosen "light" or "dark" in its settings. Every colour in `assets/theme.css`
is a variable; the dark values are in the two blocks below `:root`.

A logo uploaded under **Administration → Themes → Branding** replaces the
decorative mark and the site's name in the header and footer; a separate
logo for the dark scheme, where there is one, is swapped in by CSS. A
favicon and the description set under **Administration → Settings** are
linked and tagged (including Open Graph and Twitter tags) without any
further setup.

## Installing

In Modulento, open **Administration → Packages**, enter
`alex01at/modulento-theme-merchigo` and install. Then choose "Merchigo"
under **Administration → Themes**. New versions appear on the Packages
page.

By hand: unpack a release into `themes/merchigo/` of the installation.

## Changing the wording

The texts of the home page itself (heading, lead text, the feature band)
are edited in place as described above. A handful of smaller theme texts -
the search placeholder, the small "just arrived" badge above the hero
heading, the subtitle under the site name - are in `lang/de.php` and
`lang/en.php`, with keys starting `theme.`. Do not edit them here - an
update would replace the file. Put your own wording into
`lang/<language>.php` of the installation:

```php
<?php

return [
    'theme.brand.subtitle' => 'Keramik & Wohnaccessoires',
];
```

## Releasing

Set `version` in `theme.json`, commit, then tag and push:

```
git tag v0.1.0 && git push origin v0.1.0
```

The workflow checks that tag and `theme.json` agree, builds
`modulento-theme-merchigo-<version>.zip` with its SHA-256 and publishes
both as a GitHub Release.

## Licence

The theme is licensed under GPL-3.0-or-later, see `LICENSE`. The font Plus
Jakarta Sans in `assets/fonts/` is licensed under the SIL Open Font License,
see `assets/fonts/OFL.txt`.
