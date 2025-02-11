# Changelog

## UNRELEASED

- If defined, use url of the piece as canonical link over the page url, and use the page url if `seoCanonical` is not set.

## 1.6.1 (2023-03-06)

- Removes `apostrophe` as a peer dependency.

## 1.6.0 (2021-08-03)

- Add `seo-page-scan` permission to fine tune access to the SEO page scan feature for non-`admin` users. Thanks to [Harouna Traoré](https://harounatraore.com/) for contributing this code.

## 1.5.0 (2021-05-12)
- Adds possibility to set headers in config, if requesting the page needs authentication.

## 1.4.1 (2021-03-24)
- Adds a peer dependency for `apostrophe^2.116.1` to support the latest SEO page scan feature.

## 1.4.0 - 2021-02-11
- Adds the SEO page scan feature

## 1.3.3 - 2020-11-04
- Updates `eslint` to `^7.1.0`

## 1.3.2 - 2020-10-26
- Republishing to address npm issue. No changes.

## 1.3.1 - 2020-10-07
- Adds a note about setting the `baseUrl` option in the README.

## 1.3.0 - 2020-07-01

- Adds Google Tag Manager support.

## 1.2.4

- Updates eslint configuration to use `eslint-config-apostrophe`.

## 1.2.3

- Building on 1.2.2, we also should not output the robots meta tag at all if neither box was checked, although there is no harm in an empty one.

## 1.2.2

- Prior to this release there were separate checkboxes for "index, follow", "noindex" and "nofollow", even though checkboxes are nonexclusive, so it was possible to pick "index, follow" and "noindex" simultaneously — an invalid combination. Beginning with this release, there is no "index, follow" option because that is the default behavior of Google and never has to be explicitly chosen. If you want your page to be crawled and indexed normally, just leave the "noindex" and "nofollow" checkboxes alone.

- However, for bc reasons, if you are already using this module you may note that "index, follow" is explicitly output on pages for which you haven't edited the settings yet. That's fine and will have no ill effects. The only case you might want to look into is anywhere you chose an invalid combination of options as described above.

## 1.2.1

- The hard limits placed on seoTitle and seoDescription in version 1.2.0 are now just warnings, but still pop up when appropriate, calling attention to the fact that you are outside Google's guidelines. This is helpful if you are in no rush to shorten your `title` tags.
