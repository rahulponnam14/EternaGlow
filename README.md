# EternaGlow — Static Dropshipping Storefront

A beautiful, mobile-responsive static storefront for EternaGlow beauty tech products. Built with **Tailwind CSS** and **vanilla JavaScript** — no backend required!

## ✨ Features

- 📱 **Mobile-first responsive design**
- 🛒 **LocalStorage shopping cart** (persists between sessions)
- 💬 **WhatsApp checkout** with pre-filled order messages
- 💳 **Stripe & PayPal integration** (payment links)
- 🎨 **Modern UI** with smooth animations and glass morphism
- ⚡ **Fast loading** - optimized static files
- 🌍 **Deploy anywhere** - GitHub Pages, Netlify, Vercel

## 🚀 Quick Setup

### 1. Configure Your Settings

Open `index.html` and update the configuration object:

```javascript
const config = {
  // Replace with your WhatsApp number (country code + number, no + sign)
  phone: '919876543210', // Example for Indian number
  
  // Replace with your actual payment links
  stripeLink: 'https://buy.stripe.com/your-payment-link', 
  paypalLink: 'https://paypal.me/your-paypal-username',
  
  currency: 'USD', // Change to your preferred currency
  currencySymbol: '$'
};
```

### 2. Deploy to GitHub Pages

1. **Create a new repository** on GitHub
2. **Upload all files** to your repository
3. **Enable GitHub Pages**:
   - Go to repository Settings → Pages
   - Source: Deploy from a branch
   - Branch: main (or master)
   - Folder: / (root)
4. **Your site will be live** at: `https://yourusername.github.io/repository-name`

### 3. Alternative Deployment Options

**Netlify:** 
- Drag and drop the folder to [netlify.com/drop](https://netlify.com/drop)

**Vercel:**
- Connect your GitHub repo at [vercel.com](https://vercel.com)

**Any web host:**
- Upload files via FTP to your hosting provider

## 💰 Payment Setup

### WhatsApp Checkout (Recommended)
- Update the `phone` number in the config
- Orders will open WhatsApp with pre-filled product details
- Handle payments via WhatsApp Pay, bank transfer, etc.

### Stripe Payment Links
1. Create a Stripe account at [stripe.com](https://stripe.com)
2. Go to Products → Payment Links
3. Create payment links for each product
4. Update the `stripeLink` in config and individual product `pay_link` values

### PayPal
1. Create payment links at [paypal.me](https://paypal.me)
2. Update `paypalLink` in config

## 🎨 Customization

### Products
Edit the `products` array in `index.html` to add/modify products:

```javascript
const products = [
  {
    "id": "product-id",
    "name": "Product Name",
    "price": 99.99,
    "compare_at": 149.99,
    "desc": "Product description...",
    "bullets": ["Feature 1", "Feature 2"],
    "img": "https://images.pexels.com/photos/...",
    "pay_link": "https://buy.stripe.com/..."
  }
];
```

### Styling
- The site uses **Tailwind CSS** via CDN
- Modify colors, spacing, and components directly in the HTML
- Custom styles are in the `<style>` section

### Images
- Uses **Pexels** stock photos by default
- Replace with your product photos
- Recommended size: 1600×1600px for product images

## 📱 Mobile Optimization

- Responsive grid layouts
- Touch-friendly buttons and modals
- Optimized for mobile shopping experience
- Fast loading on slow connections

## 🛍️ Cart Features

- **Persistent cart** (survives browser refresh)
- **Quantity controls** (increase/decrease/remove)
- **Real-time totals** and item counts
- **Multiple checkout options**

## 📊 Analytics (Optional)

Add Google Analytics by including this before `</head>`:

```html
<!-- Google Analytics -->
<script async src="https://www.googletagmanager.com/gtag/js?id=GA_MEASUREMENT_ID"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());
  gtag('config', 'GA_MEASUREMENT_ID');
</script>
```

## 🔧 Troubleshooting

**Cart not working?**
- Check browser console for JavaScript errors
- Ensure localStorage is enabled

**WhatsApp not opening?**
- Verify phone number format (country code + number, no + sign)
- Test the WhatsApp link manually

**Images not loading?**
- Check image URLs are accessible
- Consider hosting images on your own domain

## 📄 License

This template is free to use for commercial projects. Attribution appreciated but not required.

## 🤝 Support

For questions or issues:
- Check the browser console for error messages
- Test on different devices/browsers
- Ensure all configuration values are updated

---

**Ready to launch your beauty tech store? 🚀**

Update the config, upload to GitHub Pages, and start selling!