# class13

# LOCAL STORAGE FOR WEB APPLICATIONS

The read-only localStorage property allows you to access a Storage object for the Document's origin; the stored data is saved across browser sessions. localStorage is similar to sessionStorage, except that while data stored in localStorage has no expiration time, data stored in sessionStorage gets cleared when the page session ends — that is, when the page is closed. (Data in a localStorage object created in a "private browsing" or "incognito" session is cleared when the last "private" tab is closed.)

Data stored in either localStorage or sessionStorage is specific to the protocol of the page. In particular, data stored by a script on a site accessed with HTTP is put in a different localStorage object from the same site accessed with HTTPS

The keys and the values are always in the UTF-16 DOMString format, which uses two bytes per character. (As with objects, integer keys are automatically converted to strings.)*

Persistent local storage is one of the factors why native client applications have held an advantage over web applications.

Cookies are used by web applications for persistent local storage of small amounts of data, but they have 3 main downsides

## Downsides of Cookies:

1. Slowing Cookies are included with every HTTP request, thereby slowing down your web application by needlessly transmitting the same data over and over

2. Sending unencrypted data Cookies are included with every HTTP request, thereby sending data unencrypted over the internet (unless your entire web application is served over SSL)

3. Limited storage Cookies are limited to about 4 KB of data — enough to slow down your application (see above), but not enough to be terribly useful

## HTML 5 Storage

HTML5 storage is a way for web pages to store named key/value pairs locally, within the client web browser.

**Thank you**