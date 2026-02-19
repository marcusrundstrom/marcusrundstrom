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

Replace the placeholder `G-XXXXXXXXXX` with your actual Measurement ID in **all four HTML files**:

- `index.html`
- `research.html`
- `teaching.html`
- `spare-time.html`

**How to update:**
1. Open each file in a text editor
2. Use Find & Replace to search for `G-XXXXXXXXXX`
3. Replace **both occurrences** in each file with your actual Measurement ID
4. Save all files

Alternatively, you can use this command to replace all instances at once:
```bash
# Replace G-XXXXXXXXXX with your actual ID
find . -name "*.html" -type f -exec sed -i 's/G-XXXXXXXXXX/YOUR-MEASUREMENT-ID/g' {} \;
```

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

Google Analytics collects user data. Consider the following privacy best practices:

### Required Actions
- **Privacy Policy**: Add a privacy policy page explaining what data you collect and how it's used
- **Cookie Consent**: For European visitors (GDPR) or California residents (CCPA), implement a cookie consent banner

### Optional GA4 Privacy Features
You can enhance privacy by enabling these Google Analytics 4 features:

1. **IP Anonymization**: GA4 anonymizes IP addresses by default
2. **Data Retention**: Configure data retention periods in GA4 Admin > Data Settings
3. **Opt-out**: Provide users a way to opt-out (use browser extensions like "Google Analytics Opt-out")

### Resources
- [Google Analytics Privacy Documentation](https://support.google.com/analytics/topic/2919631)
- [GDPR Compliance Guide](https://support.google.com/analytics/answer/9019185)
- Simple cookie consent solutions: [Cookie Consent](https://www.cookieconsent.com/), [CookieBot](https://www.cookiebot.com/)
