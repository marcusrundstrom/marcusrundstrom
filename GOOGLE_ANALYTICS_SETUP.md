# Google Analytics Setup Instructions

This website now includes Google Analytics tracking code on all pages. To complete the setup, follow these steps:

## Step 1: Create a Google Analytics Account

1. Go to [Google Analytics](https://analytics.google.com/)
2. Sign in with your Google account
3. Click "Start measuring" to create a new property
4. Follow the setup wizard to create your property

## Step 2: Get Your Measurement ID

1. In Google Analytics, go to **Admin** (bottom left)
2. Under the **Property** column, click **Data Streams**
3. Select your web data stream (or create one if it doesn't exist)
4. Copy your **Measurement ID** (format: G-XXXXXXXXXX)

## Step 3: Update Your Website Files

Replace the placeholder `G-XXXXXXXXXX` with your actual Measurement ID in the following files:

- `index.html` (lines 10 and 15)
- `research.html` (lines 8 and 13)
- `teaching.html` (lines 8 and 13)
- `spare-time.html` (lines 8 and 13)

Search for `G-XXXXXXXXXX` and replace both occurrences in each file with your actual Measurement ID.

## Step 4: Verify Tracking

After deploying your changes:

1. Visit your website
2. Go to Google Analytics > Reports > Realtime
3. You should see your visit appear in real-time (it may take a few seconds)

## What's Included

The Google Analytics integration includes:

- **Page view tracking**: Automatically tracks when visitors view each page
- **Event tracking**: Ready for custom event tracking if needed in the future
- **Standard metrics**: Time on page, bounce rate, traffic sources, etc.

## Privacy Considerations

Google Analytics collects user data. Consider adding a privacy policy to your website and potentially a cookie consent banner depending on your jurisdiction and audience (e.g., GDPR for European visitors).
