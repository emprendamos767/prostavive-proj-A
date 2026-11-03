# PROSTAVIVE — A5 EVIDENCE-FOCUSED BRIDGE PAGE
Updated: 03 November 2026

## Project Structure
- [`index.html`](file:///c:/Users/JaimeH/Documents/Bridge%20Page%20PROST%20A/index.html) — Standard web root entry point (HTML, responsive CSS, and JS inline).
- [`prostavive_a5_bridge.html`](file:///c:/Users/JaimeH/Documents/Bridge%20Page%20PROST%20A/prostavive_a5_bridge.html) — Dedicated named standalone bridge page file.
- [`README.md`](file:///c:/Users/JaimeH/Documents/Bridge%20Page%20PROST%20A/README.md) — Documentation, deployment instructions, and affiliate configuration.

---

## Deployment & Setup Instructions

1. **Set your affiliate tracking link**:
   - Open [`index.html`](file:///c:/Users/JaimeH/Documents/Bridge%20Page%20PROST%20A/index.html) (and/or `prostavive_a5_bridge.html`).
   - Near the bottom script section, find:
     ```javascript
     const AFFILIATE_URL = "https://prostavive.org/";
     ```
   - Replace `"https://prostavive.org/"` with your verified ClickBank hoplink generated at [https://prostavive.org/affiliates](https://prostavive.org/affiliates).
   - All CTA buttons decorated with `data-affiliate-cta` dynamically route to this hoplink.

2. **Publishing / Hosting**:
   - Upload `index.html` to your web server, CDN, or landing page host (Netlify, Vercel, cPanel, S3, etc.).
   - Alternatively, recreate the structure in your landing page builder (e.g. Konverly).

3. **Privacy, Compliance & Legal**:
   - Add your legal entity/contact details and privacy/cookie policy matching the regulations in your targeted advertising regions.
   - The default page code sets zero analytics or persistent tracking cookies.

4. **Tracking Pixels (Optional)**:
   - If using Meta Pixel or Google Tag Manager, insert your pixel snippet in the `<head>` tag.
   - The CTA click handler contains a helper event trigger `BridgeOutboundClick`:
     ```javascript
     if (typeof window.fbq === 'function') window.fbq('trackCustom', 'BridgeOutboundClick');
     ```

5. **Search Engine Indexing**:
   - The `<meta name="robots" content="noindex, nofollow">` tag is set to avoid search engine index pollution for direct-response paid ad campaigns. If organic search traffic is desired, remove or alter this tag.

---

## Visual Assets & Remote URLs
- **Hero bottle image**: `https://prostavive.org/home-assets/images/product.png`
- **Supplement Facts panel**: `https://prostavive.org/images/Supplement-Facts-prostavive.png?v2=`

*Note: The images currently reference official remote assets. For production stability and resilience against upstream asset changes, consider downloading authorized local copies into an `assets/` or `images/` directory.*

---

## Reference Sources & Checks
- Seller: [https://prostavive.org/](https://prostavive.org/)
- Supplement Facts: [https://prostavive.org/images/Supplement-Facts-prostavive.png?v2=](https://prostavive.org/images/Supplement-Facts-prostavive.png?v2=)
- Seller Refund Policy: [https://prostavive.org/refunds.php](https://prostavive.org/refunds.php)
- Affiliate Program: [https://prostavive.org/affiliates](https://prostavive.org/affiliates)
- Vascular Physiology: [NCBI Bookshelf — NBK537010](https://www.ncbi.nlm.nih.gov/books/NBK537010/)
- Ingredient Safety: [NIH/NCCIH — Ashwagandha](https://www.nccih.nih.gov/health/ashwagandha)
