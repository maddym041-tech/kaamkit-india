# KaamKit India

A beginner-friendly, static website and installable Progressive Web App (PWA) starter for an Indian everyday-tools platform. It uses plain HTML, CSS and JavaScript so you can edit and publish it without installing a framework or running a backend.

## Included in this first release

- Responsive landing page, tool search and category filters
- Installable PWA support for compatible Android/desktop browsers
- App icons, web app manifest, service worker and cached app shell for repeat/offline opening
- PDF re-save (basic optimisation attempt), PDF merge, image-to-PDF and image resize
- EMI, salary take-home, gratuity and GST estimators
- Resume preview and print-to-PDF
- Application letter and professional email draft templates (no AI API)
- Simple invoice preview and print-to-PDF

## Run on Windows

1. Download and extract `kaamkit-india.zip`.
2. Open the extracted `kaamkit-india` folder.
3. Double-click `index.html` to open it in Chrome or Edge.
4. Internet is needed the first time to load the PDF libraries from cdnjs and the optional Google Font. After the app shell has been opened online, the service worker caches the main app files. PDF libraries are cached after a successful online load. Some features may still need internet until their dependencies have been cached.
5. For a local web-server preview, install Visual Studio Code and its free **Live Server** extension, open this folder, right-click `index.html`, then choose **Open with Live Server**.

No Node.js, API key, database or paid service is required for this starter release.

## Install on an Android phone (PWA)

1. Publish the complete project folder to an HTTPS host such as GitHub Pages or Netlify (steps below).
2. Open the published KaamKit website in Chrome on Android.
3. Wait for the page to finish loading once while online.
4. Tap the **Install app** prompt if it appears. Alternatively, open Chrome's three-dot menu and choose **Install app** or **Add to Home screen**.
5. Confirm. KaamKit will appear on the phone's home screen and open in an app-style window.

On iPhone/iPad, open the website in Safari, tap **Share**, then **Add to Home Screen**. On desktop Chrome/Edge, use the install icon in the address bar or browser menu when available.

This package is a PWA, not an Android APK and not yet a Google Play Store release. A PWA must be hosted over HTTPS (or localhost for testing) for service-worker installation and offline caching. Opening `index.html` directly by double-clicking will not enable PWA installation.

## Publish free with GitHub Pages

1. Create or sign in to a GitHub account.
2. Create a new **public** repository named `kaamkit-india`.
3. Upload `index.html`, `styles.css`, `app.js` and `README.md` to the repository root.
4. Open repository **Settings → Pages**.
5. Under **Build and deployment**, choose **Deploy from a branch**.
6. Choose branch `main` and folder `/ (root)`, then Save.
7. Wait for GitHub Pages to publish. The site address will appear on the Pages settings screen.

A custom domain is optional and normally costs money. Do not buy one until you have tested demand.

## Alternative: Netlify Drop

You can also sign up for Netlify and drag the extracted project folder into its manual deploy/drop area. Netlify will provide a hosted preview URL. Its interface and free-tier limits may change.

## Project structure

```text
kaamkit-india/
├── index.html   # Page structure and tool dialogs
├── styles.css   # Layout, colours and responsive styling
├── app.js       # Tool logic, filters and interactions
└── README.md    # Setup and deployment guide
```

## Important accuracy and privacy notes

- EMI is a mathematical estimate; lender fees, rate changes and rounding are not included.
- Salary estimator subtracts only the deductions entered by the visitor. It is not a tax engine or payroll advice.
- Gratuity uses the custom formula requested for this version: (Basic + DA) × years of service ÷ 2. This is not presented as the statutory gratuity formula. Users must verify the rules applicable to their employment before relying on an estimate.
- GST tool calculates total tax only. It does not determine the correct rate, place of supply, exemptions, HSN/SAC or invoice compliance.
- The invoice tool is a simple template, not a certified GST invoice generator.
- PDF re-saving is not guaranteed to compress every file. Scanned PDFs may not shrink. Encrypted or unusual PDFs may fail.
- Browser file tools process files locally in the page using third-party libraries fetched from cdnjs. Review dependencies and security before using sensitive documents. A CDN outage or no internet connection can prevent PDF features from loading.
- Resume, letter and email content is stored only in the current page while it is open; this version has no account or cloud save feature.
- The email/letter generators use templates, not generative AI. Do not represent them as AI-generated.
- Replace the sample `hello@kaamkit.in` contact address with an address you control before public launch.

## Recommended next steps

1. Test every tool with sample data and different browsers/devices.
2. Add a real contact address, terms, privacy policy and an accessibility review before promotion.
3. Add individual search-engine-friendly guide pages, with original instructions and verified sources.
4. Collect user feedback before building login, saved history, paid plans or AI features.
5. Keep legal, tax, pension and government-service information dated and linked to official sources. Never promise eligibility or outcomes based only on a calculator.

## Licence

Starter project code may be adapted for your project. Check the licences and terms of any external libraries, fonts, hosting services and APIs you add.
