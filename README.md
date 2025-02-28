# Citizen
![](https://github.com/StarCitizenTools/mediawiki-skins-Citizen/workflows/MediaWiki%20CI/badge.svg) [![License: GPL v3](https://img.shields.io/badge/License-GPLv3-blue.svg)](https://www.gnu.org/licenses/gpl-3.0) [![MediaWiki: >=1.35.0](https://img.shields.io/badge/MediaWiki-%3E%3D1.35.2-%2336c)](https://www.mediawiki.org)

Citizen is a responsive skin for [MediaWiki](https://www.mediawiki.org) built by the [Star Citizen Wiki](https://starcitizen.tools) team. Although it is specifically built for the Star Citizen Wiki, the skin is designed to be flexible to run on any Mediawiki installation that is **1.35.2 or higher**. Due to resource constraints, we might not be able to provide full support for setups that are vastly different than us, but please feel free to submit patches or bug report!

Live demo can be seen at the [Star Citizen Wiki](https://star-citizen.wiki), more avaliable [here](https://wikiapiary.com/wiki/Skin:Citizen).

## Notable features
- **Fully responsive skin**: Responsive and able to adapt to different screen sizes. 📱💻🖥️
- **Light/dark mode support**: Switch between light and dark mode. ***Require JS*** ☀️🌙
- **Adjustable font size and page width**: Read the article the way you wanted. ***Require JS*** 👀📃
- **Collapsible sections**: Collapse and expand article sections. ***Require JS*** 📖📕
- **Persistent ToC**: Access ToC anywhere in the article. ***Tracking require JS*** 🔍📖
- **Rich search suggestions**: More helpful search suggestions with images and descriptions. ***Require JS*** 🔍👀
- **Webapp manifest**: Give a more app-like experience when users add your wiki to their home screen. 📱
- **HTTP security response headers**: Enhance the security of your wiki from HTTP response headers. 🔒🔑

## SkinStyles
Citizen includes numerous skinStyles that applies custom styling to extensions and core libraries. Please feel free to submit PRs if you want to add support for more extensions! Unless the extension has never supported the current minimum required MediaWiki version of the skin, the skinStyles are based on the latest version of the said MW release branch (e.g. `REL1_35` for MediaWiki 1.35).

- **Grade A - Overhaul** - Major adjustments to UI, plus Grade B. 
- **Grade B - Dynamic** - Colors are converted into CSS variables, little to none style adjustments.
- **Grade C - Legacy overhaul**  Major adjustments to UI but using legacy CSS variables.
- **Grade D - Legacy dynamic** - Color are converted into CSS variables but in old standards (`background-color-dp-XX`). These should be updated to at least Grade B support.
- **Grade E - Legacy static** - Dark mode colors are hardcored as LESS variables. These should be updated to at least Grade B support.

### Core
Name | Grade | Version | Last updated
:--- | :--- | :--- | :---
MediaWiki UI | B | 1.35.3 | 2021-07-27
OOUI | B | 0.39.3 `086b4f1` | 2021-07-26

### Extensions
Name | Grade | Version | Last updated
:--- | :--- | :--- | :---
[AdvancedSearch](https://www.mediawiki.org/wiki/Extension:AdvancedSearch) | E | N/A | N/A
[ApprovedRevs](https://www.mediawiki.org/wiki/Extension:Approved_Revs) | B | N/A | N/A
[Babel](https://www.mediawiki.org/wiki/Extension:Babel) | B | MLEB 2021.07 | 2021-07-29
[Capiunto](https://www.mediawiki.org/wiki/Extension:Capiunto) | E | N/A | N/A
[CategoryTree](https://www.mediawiki.org/wiki/Extension:CategoryTree) | B | N/A | N/A
[Cite](https://www.mediawiki.org/wiki/Extension:Cite) | A | N/A | N/A
[CleanChanges](https://www.mediawiki.org/wiki/Extension:CleanChanges) | B | MLEB 2021.07 | 2021-07-29
[CodeMirror](https://www.mediawiki.org/wiki/Extension:CodeMirror) | D | N/A | N/A
[CookieWarning](https://www.mediawiki.org/wiki/Extension:CookieWarning) | A | N/A | N/A
[DismissableSiteNotice](https://www.mediawiki.org/wiki/Extension:DismissableSiteNotice) | A | N/A | N/A
[Echo](https://www.mediawiki.org/wiki/Extension:Echo) | E | N/A | N/A
[Flow (StructuredDiscussions)](https://www.mediawiki.org/wiki/Extension:StructuredDiscussions) | E | N/A | N/A
[Graph](https://www.mediawiki.org/wiki/Extension:Graph) | D | N/A | N/A
[Lingo](https://www.mediawiki.org/wiki/Extension:Lingo) | E | N/A | N/A
[MultimediaViewer](https://www.mediawiki.org/wiki/Extension:MultimediaViewer) | C | N/A | N/A
[OAuth](https://www.mediawiki.org/wiki/Extension:OAuth) | D | N/A | N/A
[Popups](https://www.mediawiki.org/wiki/Extension:Popups) | D | N/A | N/A
[RelatedArticles](https://www.mediawiki.org/wiki/Extension:RelatedArticles) | D | N/A | N/A
[Semantic MediaWiki](https://www.mediawiki.org/wiki/Extension:Semantic_MediaWiki) | E | N/A | N/A
[Semantic Result Formats](https://www.mediawiki.org/wiki/Extension:Semantic_Result_Formats) | E | N/A | N/A
[Tabber](https://www.mediawiki.org/wiki/Extension:Tabber) | A | N/A | N/A
[TabberNeue](https://www.mediawiki.org/wiki/Extension:TabberNeue) | A | 1.0.1 `0dc1b34` | 2021-06-21
[TimedMediaHandler](https://www.mediawiki.org/wiki/Extension:TimedMediaHandler) | D | N/A | N/A
[Translate](https://www.mediawiki.org/wiki/Extension:Translate) | B | MLEB 2021.07 | 2021-07-29
[UniversalLanguageSelector](https://www.mediawiki.org/wiki/Extension:UniversalLanguageSelector) | B | MLEB 2021.07 | 2021-07-29
[UploadWizard](https://www.mediawiki.org/wiki/Extension:UploadWizard) | C | N/A | N/A
[VisualEditor](https://www.mediawiki.org/wiki/Extension:VisualEditor) | C | N/A | N/A
[WikiEditor](https://www.mediawiki.org/wiki/Extension:WikiEditor) | E | N/A | N/A

Some of the field are tagged as N/A because the information was not tracked before.

## Installation
1. [Download](https://github.com/StarCitizenTools/mediawiki-skins-Citizen/archive/main.zip) place the file(s) in a directory called `Citizen` in your `skins/` folder.
2. Add the following code at the bottom of your LocalSettings.php:
```php
wfLoadSkin( 'Citizen' );
```
3. **✔️Done** - Navigate to Special:Version on your wiki to verify that the skin is successfully installed.

## Configurations
**The skin works out of the box without any configurations.** 
The config flags allow more customization on the specific features in the skin. 

Note that:
* By default, all security-related features are turned off to ensure maximum compatibility.

### Appearance
Name | Description | Values | Default
:--- | :--- | :--- | :---
`$wgCitizenThemeDefault` | The default theme of the skin | `auto` - switch between light and dark according to OS/browser settings; `light`; `dark` | `auto`
`$wgCitizenEnableCollapsibleSections` | Enables or disable collapsible sections on content pages | `true` - enable; `false` - disable | `true`
`$wgCitizenShowPageTools` | The condition of page tools visibility | `true` - always visible; `login` - visible to logged-in users; `permission` - visible to users with the right permissions | `true`
`$wgCitizenEnableDrawerSiteStats` | Enables the site statistics in drawer menu | `true` - enable; `false` - disable | `true`
`$wgCitizenEnableDrawerSubSearch` | Enables the drawer search box for menu entries | `true` - enable; `false` - disable | `false`
`$wgCitizenPortalAttach` | Label of the portal to attach links to upload and special pages to | string | `first`
`$wgCitizenThemeColor` | The color defined in the `theme-color` meta tag | Hex color code | `#131a21`

### Search suggestions
Name | Description | Values | Default
:--- | :--- | :--- | :---
`$wgCitizenEnableSearch` | Enable or disable rich search suggestions |`true` - enable; `false` - disable | `true`
`$wgCitizenSearchGateway` | Which gateway to use for fetching search suggestion |`mwActionApi`; `mwRestApi` | `mwActionApi`
`$wgCitizenSearchDescriptionSource` | Source of description text on search suggestions (only takes effect if `$wgCitizenSearchGateway` is `mwActionApi`) | `wikidata` - Use description provided by [WikibaseLib](Extension:WikibaseLib) or [ShortDescription](https://www.mediawiki.org/wiki/Extension:ShortDescription); `textextracts` - Use description provided by [TextExtracts](https://www.mediawiki.org/wiki/Extension:TextExtracts); `pagedescription` - Use description provided by [Description2](https://www.mediawiki.org/wiki/Extension:Description2) or any other extension that sets the `description` page property | `textextracts`
`$wgCitizenMaxSearchResults` | Max number of search suggestions | Integer > 0 | `6`

### Security-related
#### Content Security Policy (CSP)
Name | Description | Values | Default
:--- | :--- | :--- | :---
`$wgCitizenEnableCSP` | Enable or disable [Content Security Policy](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Content-Security-Policy), as an alternative to [`$wgCSPHeader`](https://www.mediawiki.org/wiki/Manual:$wgCSPHeader) in Mediawiki 1.32+ | `true` - enable; `false` - disable | `false`
`$wgCitizenEnableCSPReportMode` | Enable or disable [CSP report only mode](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Content-Security-Policy-Report-Only), overrides `$wgCitizenEnableCSP` | `true` - enable; `false` - disable | `false`
`$wgCitizenCSPDirective` | The string of yourr CSP directive | See the [Content Security Policy](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Content-Security-Policy) page | 

#### HTTP Strict Transport Security (HSTS)
Name | Description | Values | Default
:--- | :--- | :--- | :---
`$wgCitizenEnableHSTS` | Enable or disable [HTTP Strict Transport Security](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Strict-Transport-Security) | `true` - enable; `false` - disable | `false`
`$wgCitizenHSTSMaxAge` | Time in second that the browser should remember that a site is only to be accessed using HTTPS | Integer > 0 | `300`
`$wgCitizenHSTSIncludeSubdomains` | Apply HSTS to all of the site's subdomains | `true` - enable; `false` - disable | `false`
`$wgCitizenHSTSPreload` | Enable or disable [HSTS preload](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Strict-Transport-Security#Preloading_Strict_Transport_Security) | `true` - enable; `false` - disable | `false`

#### Other security headers
Name | Description | Values | Default
:--- | :--- | :--- | :---
`$wgCitizenEnableDenyXFrameOptions` | Enable or disable the deny [X-Frame-Options](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/X-Frame-Options) header | `true` - enable; `false` - disable | `false`
`$wgCitizenEnableXXSSProtection` | Enable or disable the [X-XSS-Protection header](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/X-XSS-Protection) | `true` - enable; `false` - disable | `false`
`$wgCitizenEnableStrictReferrerPolicy` | Enable or disable `strict-origin-when-cross-origin` [referrer policy](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Referrer-Policy) header, should be used in conjunction with [`$wgReferrerPolicy`](https://www.mediawiki.org/wiki/Manual:$wgReferrerPolicy) as that only outputs the meta tags | `true` - enable; `false` - disable | `false`
`$wgCitizenEnableFeaturePolicy` | Enable or disable [Feature Policy](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Feature-Policy) | `true` - enable; `false` - disable | `false`
`$wgCitizenFeaturePolicyDirective` | The string of your Feature Policy directive | See the [Feature Policy](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Feature-Policy) page | 
`$wgCitizenEnablePermissionsPolicy` | Enable or disable Permissions Policy | `true` - enable; `false` - disable | `false`
`$wgCitizenPermissionsPolicyDirective` | The string of your Permissions Policy directive | | 

### Webapp manifest
Name | Description | Values | Default
:--- | :--- | :--- | :---
`$wgCitizenEnableManifest` | Enable or disable [web app manifest](https://developer.mozilla.org/en-US/docs/Web/Manifest) | `true` - enable; `false` - disable | `true`
`$wgCitizenManifestThemeColor` | [Theme color](https://developer.mozilla.org/en-US/docs/Web/Manifest/theme_color) of the web app manifest | Hex color code | `#131a21`
`$wgCitizenManifestBackgroundColor` | [Background color](https://developer.mozilla.org/en-US/docs/Web/Manifest/background_color) of the web app manifest | Hex color code | `#131a21`

### Miscellaneous
Name | Description | Values | Default
:--- | :--- | :--- | :---
`$wgCitizenEnablePreconnect` | Enable or disable [preconnect to required origin](https://web.dev/uses-rel-preconnect/) | `true` - enable; `false` - disable | `false`
`$wgCitizenPreconnectURL` | The URL for preconnect to required origin | URL | 
`$wgCitizenThemeColor` | The color defined in the `theme-color` meta tag | Hex color code | `#11151d`

## Requirements
* [MediaWiki](https://www.mediawiki.org) 1.35.2 or later
* For the legacy versions, check the other release branches.

