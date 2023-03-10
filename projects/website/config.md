---
label: Config
title: Website Config and ENVs
icon: note
order: 5
---

## ENV

This project currently supports 3 environments:

- `local` - For development
- `localproduction` - For development but with prod API
- `production` - For production

## Config

App config can be found in `config/appConfig.ts` file.

### config.global

| Key                                  | Description                                                                                                                                                                                                                                                                                                                    |
| ------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `global.app`                         | Few app related information.                                                                                                                                                                                                                                                                                                   |
| `global.domain`                      | Domain. For eg. `own-store-demo.vercel.app` OR `localhost:3000`                                                                                                                                                                                                                                                                |
| `global.baseUrl`                     | Base URL. For eg. `https://own-store-demo.vercel.app` or `http://localhost:3000`                                                                                                                                                                                                                                               |
| `global.assetBaseUrl`                | Base URL of static assets. If you want to push your static assets (stored in `/public`) and build files generated by NextJs to a CDN, update this URL. If you have a CDN for production, this is how you will map: <ul><li>`http://localhost:3000` - (On local)</li><li>`https://www.your-cdn.com` - (On production)</li></ul> |
| `global.imageBaseUrl`                | Cloudinary image base URL. For eg. `https://res.cloudinary.com/your-store/image/upload`. If you have mapped AWS S3 with Cloudinary, put that URL here. `imageBaseUrl + image path (from DB)` will render the image. **Note:** This is not for static images.                                                                   |
| `global.apiBaseUrl`                  | API base URL to connect to. For eg. `http://localhost:3001`.                                                                                                                                                                                                                                                                   |
| `global.infiniteScrollFetchLimit`    | How many items should be shown be fetched and shown per page during infinite scroll.                                                                                                                                                                                                                                           |
| `global.scrollToTopDisplayThreshold` | When to show scroll-to-top UI.                                                                                                                                                                                                                                                                                                 |
| `global.minSecurityQuestions`        | How many security questions should be shown to user to set?                                                                                                                                                                                                                                                                    |
| `global.openBlogsInNewTab`           | Should blogs open in a new tab?                                                                                                                                                                                                                                                                                                |

### config.seo

Learn more [here](./seo.md)

| Key                    | Description                                                        |
| ---------------------- | ------------------------------------------------------------------ |
| `seo.facebook.pageId`  | Facebook page ID. For eg. `1223xxxx`. Get this from page settings. |
| `seo.twitter.username` | Twitter page username.                                             |

### config.pwa

Learn more [here](./pwa.md)

| Key                          | Description                                                                                                                                                                                                             |
| ---------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `pwa.shortcuts[]`            | Users can directly open a page through shortcuts. Few properties are required: <ul><li>name (Eg. `Search`)</li><li>short_name (Eg. `search`)</li><li>url (Eg. `/search?utm_source=pwa&utm_medium=shortcut`)</li></ul>   |
| `pwa.startUrl`               | PWA's start URL. Eg. `/?utm_source=pwa&utm_medium=homescreen`                                                                                                                                                           |
| `pwa.icons.maskable`         | Set this to true if PWA icons can be masked. **Note:** Make sure icons can be masked before setting to true. Otherwise, the installability criteria will not be met. [Masked icons ref](https://web.dev/maskable-icon/) |
| `pwa.preferNativeAppOverPWA` | If you have a native app in store and want the app to have a higher preference, set this to true.                                                                                                                       |

### config.app

| Key                    | Description                                                                                         |
| ---------------------- | --------------------------------------------------------------------------------------------------- |
| `app.android`          | Android app information                                                                             |
| `app.android.name`     | App name.                                                                                           |
| `app.android.id`       | App ID. For eg. (`com.android.chrome`)                                                              |
| `app.android.storeUrl` | Store URL for the app. For eg. (`https://play.google.com/store/apps/details?id=com.android.chrome`) |
| `app.ios`              | iOS app information                                                                                 |
| `app.android.name`     | App name.                                                                                           |
| `app.android.id`       | App ID. For eg. (`535886823`)                                                                       |
| `app.android.storeUrl` | Store URL for the app. For eg. (`https://apps.apple.com/in/app/google-chrome/id535886823`)          |

### config.search

| Key                         | Description                                                                                         |
| --------------------------- | --------------------------------------------------------------------------------------------------- |
| `search.placeholder.header` | Search placeholder on the header.                                                                   |
| `search.placeholder.page`   | Search placeholder on the page.                                                                     |
| `search.sectionFetchLimit`  | Results count to show for each section. For eg. if set 10, show 10 products, catalogues and combos. |

### config.features

| Key                               | Description                                                                                          |
| --------------------------------- | ---------------------------------------------------------------------------------------------------- |
| `features.enableLandscapeMode`    | Enable landscape mode.                                                                               |
| `features.enablePageTransition`   | Enable transition when navigation changes.                                                           |
| `features.enableScrollToTop`      | Show scroll to top UI.                                                                               |
| `features.enablePWAPromotions`    | Enable PWA promotions.                                                                               |
| `features.enableAppPromotions`    | Enable app promotions.                                                                               |
| `features.enablePagesPrefetching` | If enabled, link pages will be prefetched. [Reference](https://web.dev/route-prefetching-in-nextjs/) |

### config.build

Learn more [here](./build-strategy.md)

| Key                             | Description                                                                         |
| ------------------------------- | ----------------------------------------------------------------------------------- |
| `build.pageRevalidateTimeInSec` | When should the pages be re-validated? This is mapping for each static page.        |
| `build.initialPageBuildCount`   | For pages that are public and dynamic, how many versions should be built initially? |

### config.integrations

#### config.integrations.googleOneTapLogIn

For Google one-tap login integration.

| Key                                      | Description                                                               |
| ---------------------------------------- | ------------------------------------------------------------------------- |
| `integrations.googleOneTapLogIn.enabled` | Use this flag to disable.                                                 |
| `integrations.googleOneTapLogIn.code`    | Get this code from your app's credentials page from Google cloud console. |

#### config.integrations.googleLogIn

For Google login integration.

| Key                                | Description                                                               |
| ---------------------------------- | ------------------------------------------------------------------------- |
| `integrations.googleLogIn.enabled` | Use this flag to disable.                                                 |
| `integrations.googleLogIn.code`    | Get this code from your app's credentials page from Google cloud console. |

#### config.integrations.facebookLogIn

For Facebook login integration.

| Key                                  | Description                                   |
| ------------------------------------ | --------------------------------------------- |
| `integrations.facebookLogIn.enabled` | Use this flag to disable.                     |
| `integrations.facebookLogIn.code`    | Get this code from Facebook's developer page. |

#### config.integrations.stripePayment

For Stripe payments integration.

| Key                                     | Description                                 |
| --------------------------------------- | ------------------------------------------- |
| `integrations.stripePayment.code`       | Stripe secret key. Get this from dashboard. |
| `integrations.stripePayment.publicCode` | Stripe public key. Get this from dashboard. |

#### config.integrations.googleAnalytics

For Google analytics integration.

| Key                                    | Description                       |
| -------------------------------------- | --------------------------------- |
| `integrations.googleAnalytics.enabled` | Use this flag to disable.         |
| `integrations.googleAnalytics.webCode` | GA code. Get this from dashboard. |

#### config.integrations.googleSiteVerification

For site verification on Google search console.

| Key                                           | Description                   |
| --------------------------------------------- | ----------------------------- |
| `integrations.googleSiteVerification.enabled` | Use this flag to disable.     |
| `integrations.googleSiteVerification.code`    | Get this from search console. |

#### config.integrations.sentryErrorReporting

For Sentry integration.

| Key                                           | Description               |
| --------------------------------------------- | ------------------------- |
| `integrations.googleSiteVerification.enabled` | Use this flag to disable. |
| `integrations.googleSiteVerification.dsn`     | Get this from dashboard.  |

#### config.integrations.imageTransformation

Image transformation integration. For eg. if you use `Cloudinary` and want to use their transformation parameters.

| Key                                         | Description                                             |
| ------------------------------------------- | ------------------------------------------------------- |
| `integrations.imageTransformation.enabled`  | Use this flag to disable.                               |
| `integrations.imageTransformation.variants` | A mapping of app-specific key and transform parameters. |

### config.company

| Key                     | Description                                                                                                                                                                                                                                                                        |
| ----------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `company.name`          | Legal company name.                                                                                                                                                                                                                                                                |
| `company.contactNumber` | Company's contact number.                                                                                                                                                                                                                                                          |
| `company.contactEmail`  | Company's contact email.                                                                                                                                                                                                                                                           |
| `company.address`       | Company address.                                                                                                                                                                                                                                                                   |
| `company.socialLinks[]` | Company social links. Following properties are required: <ul><li>type: Type of the icon ([Reference](./faq/#which-social-icons-are-supported))</li><li>url: Social URL</li><li>name: Name of the social platform</li><li>isExternal: Should this link open in a new tab?</li></ul> |

### config.footer

| Key                    | Description               |
| ---------------------- | ------------------------- |
| `footer.links`         | Links to show on footer.  |
| `footer.copyrightText` | Copyright text on footer. |

### config.share

| Key                   | Description                                                                                             |
| --------------------- | ------------------------------------------------------------------------------------------------------- |
| `share.section.title` | Title to show when user shares the app from section.                                                    |
| `share.product.title` | Title to show when user shares the product. Dynamic keywords allowed: `PRODUCT_NAME` and `PRODUCT_URL`. |
