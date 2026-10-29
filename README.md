# JustTools / QR Code Generator

100% free, No ads, all happen on the browsers, 100% private, No uploads. No tricks. Just tools.

A static, browser-only QR code generator for HTTP and HTTPS URLs. Download codes
as PNG images or scalable SVGs. No backend, build step, API keys, or CDN required.
URLs are processed locally, not uploaded or stored by the app.

## Use locally

Open `index.html` in a modern browser. Paste a complete URL (including `https://`
or `http://`), select **Generate QR code**, and download either format.

The encoded URL is displayed under the preview. Standard browser URL
normalization applies, including percent-encoding non-ASCII paths and converting
international domain names to ASCII. Editing the URL clears the previous code
so you cannot accidentally download a code for an outdated link.

## Publish on GitHub Pages

1. Create a GitHub repository and upload `index.html`, `styles.css`, `app.js`,
   and the entire `vendor` directory to the repository root.
2. In the repository, open **Settings > Pages**.
3. Under **Build and deployment**, choose **Deploy from a branch**.
4. Select your branch (usually `main`), choose **/ (root)**, and save.
5. Once deployment finishes, open the site URL shown on the Pages settings page.

Relative asset paths support both `https://USERNAME.github.io/REPOSITORY/` and
custom domains. Keep the `vendor` directory alongside `index.html`.

## Notes

- QR codes are static and do not expire. The destination must remain available.
- Codes use medium error correction and a four-module white quiet zone.
- Very long URLs can exceed QR capacity; the page reports this instead of
  generating an invalid code.
- Scan the downloaded code before printing or distributing it.
- The app has no analytics or external runtime requests. GitHub Pages itself
  still receives normal hosting requests when someone visits the site.

## Third-party software

`vendor/qrcode.js` is [qrcode-generator 1.4.4](https://github.com/kazuhikoarase/qrcode-generator),
copyright Kazuhiko Arase, licensed under the MIT license. See `vendor/LICENSE`.
