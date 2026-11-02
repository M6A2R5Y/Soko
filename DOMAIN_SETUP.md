# Custom Domain Setup Guide for Soko Edit

Before launching Soko Edit publicly, connect your custom domain (for example: `sokoedit.co.ke` or `sokoedit.com`).

Follow these instructions to connect your custom domain:

---

## 1. If Hosting on GitHub Pages

1. **Add CNAME file:**
   Create a file named `CNAME` in the root of this repository containing your domain name (e.g., `sokoedit.co.ke` or `www.sokoedit.co.ke`).

2. **Configure DNS Records at your Registrar:**
   Log in to your domain registrar (e.g. Kenya Web Experts, Safaricom Domains, Namecheap, Cloudflare, or GoDaddy) and add the following records:

   **For Apex Domain (e.g. `sokoedit.co.ke`):**
   Add four `A` records pointing to GitHub Pages IP addresses:
   - Type: `A`, Host/Name: `@`, Value: `185.199.108.153`
   - Type: `A`, Host/Name: `@`, Value: `185.199.109.153`
   - Type: `A`, Host/Name: `@`, Value: `185.199.110.153`
   - Type: `A`, Host/Name: `@`, Value: `185.199.111.153`

   **For Subdomain / WWW (e.g. `www.sokoedit.co.ke`):**
   - Type: `CNAME`, Host/Name: `www`, Value: `m6a2r5y.github.io.`

3. **Enable Custom Domain & Enforce HTTPS in GitHub:**
   - Go to your repository settings: `Settings` > `Pages`.
   - Enter your domain in **Custom domain** and click **Save**.
   - Wait for DNS check to complete, then check **Enforce HTTPS**.

---

## 2. If Hosting on Cloudflare Pages or Vercel

1. In the dashboard (Cloudflare / Vercel), open the Soko project and select **Custom Domains**.
2. Enter your domain name.
3. Follow the automated DNS record prompts (Cloudflare handles SSL certificates automatically).

---

## Pre-Launch Verification Checklist

- [x] Favicon added (`favicon.svg` linked in `<head>` of all pages).
- [x] AI platform attribution removed (verified 0 instances).
- [x] Privacy Policy page live (privacy-policy.html).
- [x] Terms and Conditions page live (terms-and-conditions.html).
- [x] Zero fake reviews, zero fake counters, zero vague text.
- [x] Zero emoji icons (clean SVG vector icons only).
- [x] Zero em dashes (hyphens and colons only).
- [x] Clean architectural earth and forest color palette.
- [x] Modern rectangular button radius (4px, zero pill shapes).
- [ ] Connect custom domain and enforce HTTPS.
- [ ] Update `CONFIG.whatsapp` in `index.html` with your live business WhatsApp phone number.
- [ ] (Optional) Paste your direct M-Pesa / IntaSend / Paystack payment link into `CONFIG.paymentLink` in `index.html`.
