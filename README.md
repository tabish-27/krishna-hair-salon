# Krishna Hair Salon

A mobile-first, bilingual salon page built as one static `index.html` file. There is no build step or package install.

## Edit the shop details

Open `index.html` and edit the `SALON` object near the bottom of the file:

- `phone` is used for call and WhatsApp links. Keep the country code and digits, such as `+918800966984`.
- `phoneDisplay` controls how the number looks on the page.
- `address` and `timings` are shown in the location section. Replace the prompts with the real shop details before sharing the QR code. The Google Maps button automatically searches the salon name and updated address.
- `services` contains each service name, English label, and price. Change the `price` numbers in rupees. The list is also marked `<!-- EDIT PRICES HERE -->` in the HTML.
- `images` contains the gallery image URL, alt text, and captions. Keep meaningful alt text when replacing photos.
- `whatsappMessage` controls the prefilled booking message.

The three reviews are clearly labeled sample reviews. Replace them with real customer feedback and get permission before publishing names or photos. The Paytm name is set to Govind Kumar.

## Deploy with Vercel CLI

1. Install Node.js if it is not already installed.
2. Open a terminal in this folder and install the Vercel CLI: `npm install --global vercel`.
3. Sign in: `vercel login`.
4. Preview a deployment: `vercel` and follow the prompts.
5. Publish to production: `vercel --prod`.

The production command prints the live URL. Open it on a phone and test Call, WhatsApp, directions, and the image gallery before printing the QR code.

## Deploy from GitHub

1. Create a GitHub repository and upload `index.html`, `vercel.json`, and `README.md` to its root.
2. Sign in at [vercel.com](https://vercel.com), choose **Add New → Project**, and import the repository.
3. Choose **Other** as the framework preset. Leave the build command and output directory empty; this site has no build step.
4. Select **Deploy**. Vercel will provide a URL and redeploy when you push later changes to the connected branch.

## Make a QR code

1. Copy the deployed production URL, for example `https://your-project.vercel.app`.
2. In Chrome, open that URL, use **Share → Create QR code**, then download the QR image. A reputable QR-code generator that exports a print-quality PNG or SVG also works.
3. Scan the printed code with a phone before putting it up. Keep the QR code pointed at the stable Vercel production URL, not a preview deployment URL.

The page uses externally hosted Google Fonts and Unsplash images, so those need an internet connection to load. Each selected Unsplash image URL was checked during setup; the page also hides a failed image gracefully.