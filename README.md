# Revolt-Mono

Disruption

## Getting Started

This is a [Next.js](https://nextjs.org/) project bootstrapped with Vercel Speed Insights integration.

### Development

First, install dependencies:

```bash
npm install
# or
yarn install
# or
pnpm install
```

Then, run the development server:

```bash
npm run dev
# or
yarn dev
# or
pnpm dev
```

Open [http://localhost:3000](http://localhost:3000) with your browser to see the result.

## Vercel Speed Insights

This project includes [Vercel Speed Insights](https://vercel.com/docs/speed-insights) integration for monitoring web performance metrics.

### Features

- Real User Monitoring (RUM) for Core Web Vitals
- Performance tracking for:
  - First Contentful Paint (FCP)
  - Largest Contentful Paint (LCP)
  - Cumulative Layout Shift (CLS)
  - First Input Delay (FID)
  - Time to First Byte (TTFB)
  - Interaction to Next Paint (INP)

### Setup

The `@vercel/speed-insights` package is already integrated in the root layout (`app/layout.tsx`):

```tsx
import { SpeedInsights } from '@vercel/speed-insights/next'

export default function RootLayout({ children }) {
  return (
    <html lang="en">
      <body>
        {children}
        <SpeedInsights />
      </body>
    </html>
  )
}
```

### Enabling Speed Insights on Vercel

1. Deploy your app to Vercel
2. Go to your project dashboard
3. Navigate to the **Speed Insights** tab
4. Click **Enable**

After enabling and deploying, the `/_vercel/speed-insights/script.js` script will be automatically injected and performance data will be collected.

### Viewing Data

Once deployed and after users visit your site, you can view performance metrics in the Vercel dashboard under the Speed Insights tab.

## Deployment

Deploy this project to Vercel:

```bash
vercel deploy
```

Or connect your Git repository to enable automatic deployments on push.

## Learn More

- [Next.js Documentation](https://nextjs.org/docs)
- [Vercel Speed Insights Documentation](https://vercel.com/docs/speed-insights)
- [Speed Insights Package Reference](https://vercel.com/docs/speed-insights/package)
