# Absolutely AC - Remaining Steps and TODO

This checklist tracks what is already implemented and what is still needed before go-live.

## Done

- [x] Updated core site copy to Tampa Bay / Odessa focus (75-mile radius from 33556)
- [x] Replaced phone CTAs with (727) 475-0284
- [x] Added SEO basics: title, meta description, canonical, robots meta
- [x] Added social tags: Open Graph + Twitter card tags
- [x] Added structured data: HVACBusiness schema + FAQ schema
- [x] Added Get a Quote lead form on-page
- [x] Added click tracking hooks for call, email, and CTA buttons
- [x] Added quote form submit tracking event hook
- [x] Added sitemap.xml
- [x] Added robots.txt

## Immediate TODO (Required Before Launch)

- [ ] Replace placeholder GA4 Measurement ID in HTML (`G-XXXXXXXXXX`)
- [ ] Replace placeholder Zapier webhook URL in HTML (`PASTE_ZAPIER_WEBHOOK_URL_HERE`)
- [x] Replace placeholder HVAC license number (`CAC1828298`)
- [ ] Confirm business street address (needed for LocalBusiness schema and Google Business Profile)
- [ ] Verify all assets and links load correctly in production domain

## Analytics and Lead Tracking TODO

- [ ] Create GA4 property for absolutelyac.com
- [ ] Mark these events as Conversions in GA4:
  - `phone_call_click`
  - `quote_form_submit`
- [ ] Confirm event firing with GA4 DebugView (call link, email link, quote submit)
- [ ] Build Zapier Catch Hook trigger
- [ ] Connect Zap to Google Sheets and map fields:
  - timestamp
  - name
  - phone
  - email
  - service
  - zip
  - message
  - source
  - page
- [ ] Add optional client alert action (email or Slack) in Zapier
- [ ] Submit 3 test leads and confirm rows appear in Google Sheets

## Cloudflare TODO

- [ ] Add domain to Cloudflare
- [ ] Update nameservers at GoDaddy to Cloudflare nameservers
- [ ] Set SSL/TLS mode to Full (strict)
- [ ] Enable Always Use HTTPS
- [ ] Configure redirect rule: www -> non-www (or non-www -> www, pick one canonical)
- [ ] Enable WAF managed rules
- [ ] Enable Bot Fight Mode
- [ ] Enable Auto Minify (HTML/CSS/JS)
- [ ] Enable Brotli compression
- [ ] Verify DNS proxy status (orange cloud) for public records

## Deployment TODO (GitHub Demo -> GoDaddy Prod)

- [ ] Push latest changes to GitHub main branch
- [ ] Enable GitHub Pages for demo preview
- [ ] QA demo URL on mobile + desktop
- [ ] Deploy production files to GoDaddy hosting for absolutelyac.com
- [ ] Verify domain DNS records after switch
- [ ] Re-test phone links, form, and tracking on production URL

## SEO and Local Growth TODO

- [ ] Create/claim Google Business Profile
- [ ] Set service area to 75-mile radius from 33556
- [ ] Ensure NAP consistency across website and listings
- [ ] Add business to local directories (Yelp, BBB, Angi, HomeAdvisor, Nextdoor)
- [ ] Publish at least 3 local service pages or posts (Odessa, Tampa, Clearwater)
- [ ] Request first 10 customer reviews and respond to each review

## QA and Sign-Off TODO

- [ ] Run Lighthouse on production (SEO >= 95 target)
- [ ] Validate schema in Google Rich Results Test
- [ ] Validate robots.txt and sitemap.xml in Google Search Console
- [ ] Add domain property in Google Search Console
- [ ] Submit sitemap in Search Console
- [ ] Create simple monthly lead report view for client (GA4 + Sheets)

## Client Reporting Cadence

- [ ] Weekly: leads generated, phone clicks, form submits, cost per lead (if ads used)
- [ ] Monthly: traffic trend, conversion trend, top landing pages, SEO progress summary

## Notes

- Current code is framework-free by design for speed, simplicity, and SEO.
- If business later needs a portal or booking app, then evaluate SvelteKit or React.
