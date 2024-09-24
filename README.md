# @arunvaradharajalu/common.cookies

[![npm version](https://badge.fury.io/js/%40arunvaradharajalu%2Fcommon.cookies.svg)](https://www.npmjs.com/package/@arunvaradharajalu/common.cookies)
[![GitHub issues](https://img.shields.io/github/issues/arunv11u/common.cookies)](https://github.com/arunv11u/common.cookies/issues)
[![GitHub license](https://img.shields.io/github/license/arunv11u/common.cookies)](https://github.com/arunv11u/common.cookies/blob/master/LICENSE)

## Overview

This package provides a Cookie Implementation class to handle setting, retrieving, and clearing cookies, including signed cookies, in an Express application.

## Installation

To install the package, run the following command:

```bash
npm install @arunvaradharajalu/common.cookies
```

## Usage

### Importing the Cookie Implementation

```bash
import { CookieImpl } from '@arunvaradharajalu/common.cookies';
```

### Setting a Cookie

```bash
const cookieImpl = new CookieImpl();
cookieImpl.setCookies(response, { name: Cookies.appnameCookieName, value: 'cookie_value' });
```

### Setting a Signed Cookie

```bash
cookieImpl.setSignedCookies(response, { name: SignedCookies.lifeverseChristmasEventAuthToken, value: 'signed_cookie_value' });
```

### Retrieving Cookies

```bash
const cookies = cookieImpl.getCookies(request);
console.log(cookies.appnameCookieName);
```

### Retrieving Signed Cookies

```bash
const signedCookies = cookieImpl.getSignedCookies(request);
console.log(signedCookies.lifeverseChristmasEventAuthToken);
```

### Clearing a Cookie

```bash
cookieImpl.clear(response, Cookies.appnameCookieName);
```

## Types
The package includes types for cookies and signed cookies:

- `Cookies`: Enum for standard cookies.
- `SignedCookies`: Enum for signed cookies.
- `CookieInput`: Interface for passing cookie name and value.
- `SignedCookieInput`: Interface for passing signed cookie name and value.

## Tests

Tests can be run using:

```bash
npm run test
```

Test results will be available in an HTML format using the jest-html-reporter.

## License

This project is licensed under the ISC License.

## Issues

For any issues or bug reports, please visit the GitHub Issues Page.

## Author

Arun Varadharajalu