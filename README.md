# FHCookieGuard

A set of hooks to use to save a user's cookie preferences in a cookie(🥲).

The cookie settings are stored as follows:

`'["functional","analytics","marketing"]'`

## Usage

You can use the build in cookieguard to get up and running quickly or use the provided hooks to make your own.

The cookiebanner makes use of Context to share the cookie state throughout the app.

-   Wrap your app with the Provider:

    ```jsx
    import { CookieGuardContextProvider } from '@freshheads/cookie-guard';

    <CookieGuardContextProvider>
        <App />
    </CookieGuardContextProvider>;
    ```

-   The provider optionally accepts:

    -   onCookiesChange
    -   onCookiesSet
    -   onCookiesCleared

    e.g. If you want to change the Google consent options based on the cookie settings

-   Add the premade Cookie Banner to your app

    ```jsx
    import {
    CookieGuard,
    CookieGuardContextProvider,
    CookieGuardProps
    } from '@freshheads/cookie-guard';
    import '@freshheads/cookie-guard/dist/style.css';

    const CookieGuardProps = {
        title: 'Onze site maakt gebruik van cookies.',
        description:
            'Wij gebruiken cookies voor de werking van de website, analyse en verbetering en marketingdoeleinden.',
        acceptAllLabel: 'Alle cookies accepteren',
        saveLabel: 'Opslaan',
        functionalLabel: 'Noodzakelijke cookies',
        analyticsLabel: 'Analytische cookies',
        marketingLabel: 'Marketing cookies',
    }
     <CookieGuardContextProvider>
        <App/>
        <CookieGuard {...CookieGuardProps}>
    </CookieGuardContextProvider>

    ```

-   To style look at the source code `/src/popupstyles.css` and import your own css.

-   You can also use the hooks to make your own custom cookiebanner

TODO: explain hooks with chakraui example

```jsx

```
