<p align="center">
  <picture><source media="(prefers-color-scheme: dark)" srcset="https://global.media.stux.design/logo-light.png"><source media="(prefers-color-scheme: light)" srcset="https://global.media.stux.design/logo-dark.png"><img src="https://global.media.stux.design/logo-dark.png" height="100" alt="Stux.Design Logo"></picture>
</p>

# Stux.Design GitHub Pages Redirect

Sends anyone who visits [stuxdesign.github.io](https://stuxdesign.github.io) to Stux.Design's GitHub organisation,
[github.com/StuxDesign](https://github.com/StuxDesign).

## How it works

`index.html` is a single page with a meta refresh and a canonical link, both pointing at
`https://github.com/StuxDesign`. `.github/workflows/pages.yml` deploys it to GitHub Pages. Stux.Design's own sites use
custom domains (stux.design, services.stux.design, status.stux.design and so on), so this address only needs to land
somewhere useful.

To point it somewhere else, change both URLs in `index.html`:

```html
<meta http-equiv="refresh" content="0;url=https://github.com/StuxDesign" />
<link rel="canonical" href="https://github.com/StuxDesign" />
```

## Versioning

This project uses [Date Versioning](https://datevers.ing): each release is numbered by its UTC release date as `YY.MM.DD` (for example `26.10.23`), with `-1`, `-2`… for later releases the same day. See [CHANGELOG.md](CHANGELOG.md) for what changed in each release.

Work happens on the `test` branch. Changes reach `main` only through a pull request from `test`, which needs CI to pass and is reviewed and merged by Leo. Release commits and tags are made on `test` (`git push origin test --tags`) and go live when the pull request is merged.

## License

&copy; 2026 Stux.Group. All rights reserved.

---

*Built & Maintained by <picture><source media="(prefers-color-scheme: dark)" srcset="https://global.media.stux.design/icon-light.png"><source media="(prefers-color-scheme: light)" srcset="https://global.media.stux.design/icon-dark.png"><img src="https://global.media.stux.design/icon-dark.png" height="14" alt="Stux.Design" valign="middle"></picture> [Stux.Design](https://github.com/StuxDesign), Hosted by <picture><source media="(prefers-color-scheme: dark)" srcset="https://global.media.stuxedo.com/icon-light.png"><source media="(prefers-color-scheme: light)" srcset="https://global.media.stuxedo.com/icon-dark.png"><img src="https://global.media.stuxedo.com/icon-dark.png" height="14" alt="Stuxedo" valign="middle"></picture> [Stuxedo](https://stuxedo.com).
Stux.Design is a part of the <picture><source media="(prefers-color-scheme: dark)" srcset="https://global.media.stux.group/icon-light.png"><source media="(prefers-color-scheme: light)" srcset="https://global.media.stux.group/icon-dark.png"><img src="https://global.media.stux.group/icon-dark.png" height="14" alt="Stux.Group" valign="middle"></picture> Stux.Group brand of businesses.*
