# Smart-App-Banner
SmartApp Banner for ioS and Android

Based on 'Smart App Banner' by [Ain Tohvri](https://github.com/ain/smartbanner.js)

## Difference
- Fully customisable info
- Close button that
  - closes the banner
  - sets cookie to keep banner closed for number of days
- Platform-specific app icon URL
- User Agent specific targeting

![smartbanner.js screenshot](https://github.com/hardweezy/Smart-App-Banner/raw/development/screenshot.png)

## Basic Usage

`smartbanner.js` works automagically given following meta tags:

```html
<!-- Start SmartBanner configuration -->
<meta name="smartbanner:title" content="Smart Application">
<meta name="smartbanner:author" content="SmartBanner Contributors">
<meta name="smartbanner:price" content="FREE">
<meta name="smartbanner:price-suffix-apple" content=" - On the App Store">
<meta name="smartbanner:price-suffix-google" content=" - In Google Play">
<meta name="smartbanner:icon-apple" content="https://url/to/apple-store-icon.png">
<meta name="smartbanner:icon-google" content="https://url/to/google-play-icon.png">
<meta name="smartbanner:button" content="VIEW">
<meta name="smartbanner:button-url-apple" content="https://ios/application-url">
<meta name="smartbanner:button-url-google" content="https://android/application-url">
<meta name="smartbanner:enabled-platforms" content="android,ios">
<meta name="smartbanner:days-to-hide" content="Number of Days">
<!-- End SmartBanner configuration -->
```

Additionally, JavaScript and CSS has to be included:

```html
<link rel="stylesheet" href="path/to/component/dist/smartbanner.min.css">
<script src="path/to/component/dist/smartbanner.min.js"></script>
```

## Advanced usage

### Hide the smartbanner for certain User Agents

There are cases where you do not want to show the smart app banner on all Android and/or all iOS devices. For example:
* your app is availabe only for some Android/iOS versions
* your app is only availabe on iPhone, but not iPad
* your app is a web app which also shows this website, but of course should not show the smart app banner.

In this case you can define a regular expression, which matches all user agent strings that should be excluded. Just add another `meta` tag like the following:
```html
<meta name="smartbanner:exclude-user-agent-regex" content="^.*My Example Webapp$">
```
This regular expression would match any user agent string, that ends with *My Example Webapp*.

### Show the smartbanner for certain User Agents

In addition to blacklisting certain user agents using the regex explained in the previous section, you can also whitelist certain user agents:
```html
<meta name="smartbanner:include-user-agent-regex" content="iPhone 7">
```

**Note:** You can define `enabled-platforms`, `exclude-user-agent-regex` and `include-user-agent-regex` at the same time. `enabled-platforms` has the lowest priority, `exclude-user-agent-regex` the highest priority.

### Disable Positioning

If you want to position smart app banner yourself (e.g. in CSS), you can disable built-in positioning with following option:
```html
<meta name="smartbanner:disable-positioning" content="true">
```

## Contributing

Contributions are welcome and will be fully credited.

We accept contributions via Pull Requests on [Github](https://github.com/hardweezy/Smart-App-Banner/tree/development).

Improvements would be appreciated on the following:
* Customize smart app banner for Windows Mobile

## Credits
* [Ain Tohvri](https://github.com/ain/smartbanner.js) - Super Awesome
* [Dima Yv](https://github.com/kudago/smart-app-banner) - Awesome


## Licence

Licenced under [MIT](https://raw.githubusercontent.com/hardweezy/Smart-App-Banner/development/LICENSE).
