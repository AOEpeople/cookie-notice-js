[![Build status — Travis-CI][travis-icon]][travis]
[![cookie-notice on Npmjs][npm-icon]][npm]
[![License][license-icon]][mit]
[![Total downloads ~ Npmjs][downl-icon]][npm]
[![Size of Javascript][size-icon]][build]

# CookieNotice

**CookieNoticeJS** is a very simple and small *(→ 2 kB gzip)* vanilla JS script with multi language support for [GDPR][]/[DSGVO][]‎ transparency and
notification purposes that provides an easy way to show a cookie notice on your website.

<img src="https://i.imgur.com/koDf1h0.png" alt="cookie notice working example" align="center"/>

**Available via [npm][]**

```shell
npm install cookie-notice
npm test
```


**To use in your project There are plenty ways for integration:**

**When installed via npm, include in any project by using path below:**
```html
<script src="node-modules/cookie-notice/dist/cookie.notice.min.js"></script>
```

**For usage with Angular2+ add line below in "scripts" section in angular-cli.json:**
```json
{
    "scripts": [
        "../node_modules/cookie-notice/dist/cookie.notice.js",
        "../optional/path/to/custom/cookie-notice-config.js"
    ]
}
```

**When cloned directly from gitHub use path below:**
```html
<script src="cookie-notice/dist/cookie.notice.min.js"></script>
```

## Behavior
You will get a dismissable banner on the bottom of your pages showing a default cookie audit like the following:

> We use cookies to make sure you can have the best experience on our website. If you continue to use this site we assume that you will be happy with it.

Check my website for a [DEMO](http://codeb.it/). Depending on the visitor browser language one of the preloaded translations will be shown. At the moment **CookieNoticeJS** supports *EN, IT, DE and FR*. If you want to contribute with an extra language do not hesitate to open an issue or a PR.

**CookieNoticeJS** has been successfully tested on IE9+, Chrome, Firefox and Safari.

## Customize CookieNoticeJS

For the most of you including the script should be enough but **CookieNoticeJS** comes with many customization options. Let's see an example:

```html
<script src="js/cookie.notice.min.js"></script>
<script>
    new cookieNoticeJS({

       // Localizations of the notice message
       'messageLocales': {
         'it': 'Custom localized message'
       },

       // Localizations of the dismiss button text
       'buttonLocales': {
         'it': 'Chiudi'
       },

       // Position for the cookie-notifier (default=bottom)
       'cookieNoticePosition': 'top',

       // Shows the "learn more button (default=false)
       'learnMoreLinkEnabled': false,

       // The href of the learn more link must be applied if (learnMoreLinkEnabled=true)
       'learnMoreLinkHref': '/learn/more/index.html',

       // Text for optional learn more button
       'learnMoreLinkText':{
           'en':'learn more'
       },

       // The message will be shown again in X days
       'expiresIn': 30,

      // Specify a custom font family and size in pixels
      'fontFamily': 'inherit',
      'fontSize': 12,

       // Dismiss button background color
       'buttonBgColor': '#d35400',  

       // Dismiss button text color
       'buttonTextColor': '#fff',

       // Notice background color
       'noticeBgColor': '#000',

       // Notice text color
       'noticeTextColor': '#fff',

       // the learnMoreLink color (default='#009fdd')
       'linkColor': '#f00',

       // The target of the learn more link (default='', or '_blank')
       'linkTarget': '',

       // Print debug output to the console (default=false)
       'debug': false
    });
</script>
```

## Configuration via `data-` attribute

Configuration options can be put in a `data-cookie-notice` HTML attribute in JSON format.
Note, you can include the Javascript from the [unpkg][] CDN ([browse][]).
For example:

```html
<script
  data-cookie-notice='{ "learnMoreLinkEnabled": true, "learnMoreLinkHref": "/privacy.html" }'
  src="https://unpkg.com/cookie-notice@^1/dist/cookie.notice.min.js"
></script>
```

#### Author
Alessandro Benoit

#### Contributors
[Bernhard Behrendt](mailto:bernhard.behrendt@aoe.com) [@AOEpeople](https://github.com/AOEpeople),
[Nick Freear](https://github.com/nfreear) [IET at the OU](https://github.com/IET-OU)

### License

License: [MIT][]


[MIT]: https://github.com/micc83/cookie-notice-js/blob/master/LICENSE
    "License: MIT | Copyright © 2018 Alessandro Benoit (micc83)."
[MIT-0]: https://mit-license.org/#2018
[travis-icon]: https://travis-ci.org/AOEpeople/cookie-notice.svg?branch=master
[travis]: https://travis-ci.org/AOEpeople/cookie-notice "Build status – Travis-CI"
[npm]: https://npmjs.com/package/cookie-notice "CookieNotice – on NPM"
[npm-icon]: https://badge.fury.io/js/cookie-notice.svg
[npm-i0]: https://img.shields.io/npm/v/cookie-notice.svg "(Timeout errors)"
[license-icon]: https://img.shields.io/npm/l/cookie-notice.svg
[downl-icon]: https://img.shields.io/npm/dt/cookie-notice.svg "Count of total downloads – NPM"
[build]: https://github.com/AOEpeople/cookie-notice/tree/master/dist
[size-icon]: https://img.shields.io/github/size/AOEpeople/cookie-notice/dist/cookie.notice.min.js.svg
    "Size of built Javascript, kilo-bytes (kB) – on GitHub"
[unpkg]: https://unpkg.com/ "unpkg is a fast, global content delivery network (CDN) for everything on npm."
[browse]: https://unpkg.com/cookie-notice@^1/ "Browse cookie-notice on unpkg"

[DSGVO]: https://de.wikipedia.org/wiki/Datenschutz-Grundverordnung "Datenschutz-Grundverordnung (DSGVO)"
[GDPR]: https://en.wikipedia.org/wiki/General_Data_Protection_Regulation "General Data Protection Regulation (GDPR)"

[End]: //.
