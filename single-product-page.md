# **Single product page schema**, separated into **individual script tags**:

---

### **1. WebSite Schema**

```json
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "WebSite",
  "@id": "https://pqsjapan.jp/#website",
  "url": "https://pqsjapan.jp/",
  "name": "PQSJAPAN",
  "potentialAction": {
    "@type": "SearchAction",
    "target": "https://pqsjapan.jp/search?q={search_term_string}",
    "query-input": "required name=search_term_string"
  }
}
</script>
```

---

### **2. Organization Schema**

```json
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "Organization",
  "@id": "https://pqsjapan.jp/#organization",
  "name": "PQSJAPAN",
  "url": "https://pqsjapan.jp/",
  "logo": "https://pqsjapan.jp/logo.png",
  "sameAs": [
    "https://www.facebook.com/pqsjapan",
    "https://twitter.com/pqsjapan",
    "https://www.linkedin.com/company/pqsjapan"
  ],
  "contactPoint": {
    "@type": "ContactPoint",
    "telephone": "+81-123-456-789",
    "contactType": "customer service",
    "areaServed": "Worldwide",
    "availableLanguage": ["en", "ja"]
  }
}
</script>
```

---

### **3. BreadcrumbList Schema**

```json
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "BreadcrumbList",
  "@id": "https://pqsjapan.jp/order/toyota/regiusace-van/102194#breadcrumb",
  "itemListElement": [
    {
      "@type": "ListItem",
      "position": 1,
      "name": "Home",
      "item": "https://pqsjapan.jp/"
    },
    {
      "@type": "ListItem",
      "position": 2,
      "name": "Toyota",
      "item": "https://pqsjapan.jp/order/toyota"
    },
    {
      "@type": "ListItem",
      "position": 3,
      "name": "Regiusace Van",
      "item": "https://pqsjapan.jp/order/toyota/regiusace-van"
    },
    {
      "@type": "ListItem",
      "position": 4,
      "name": "Stock #102194",
      "item": "https://pqsjapan.jp/order/toyota/regiusace-van/102194"
    }
  ]
}
</script>
```

---

### **4. Product / Vehicle Schema**

```json
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": ["Product", "Vehicle"],
  "@id": "https://pqsjapan.jp/order/toyota/regiusace-van/102194#product",
  "name": "Toyota Regiusace Van 2015",
  "description": "Used 2015 Toyota Regiusace Van in excellent condition. Exported directly from Japan by PQSJAPAN. Fully inspected, low mileage, and ready for worldwide shipping.",
  "sku": "102194",
  "mpn": "REGI-102194",
  "brand": {
    "@type": "Brand",
    "name": "Toyota"
  },
  "url": "https://pqsjapan.jp/order/toyota/regiusace-van/102194",
  "image": [
    "https://pqsjapan.jp/images/regiusace-102194-front.jpg",
    "https://pqsjapan.jp/images/regiusace-102194-side.jpg",
    "https://pqsjapan.jp/images/regiusace-102194-interior.jpg"
  ],
  "vehicleModelDate": "2015",
  "mileageFromOdometer": {
    "@type": "QuantitativeValue",
    "value": "65000",
    "unitCode": "KMT"
  },
  "fuelType": "Diesel",
  "vehicleTransmission": "Automatic",
  "bodyType": "Van",
  "driveWheelConfiguration": "https://schema.org/RearWheelDriveConfiguration",
  "offers": {
    "@type": "Offer",
    "@id": "https://pqsjapan.jp/order/toyota/regiusace-van/102194#offer",
    "priceCurrency": "USD",
    "price": "6200",
    "availability": "https://schema.org/InStock",
    "itemCondition": "https://schema.org/UsedCondition",
    "url": "https://pqsjapan.jp/order/toyota/regiusace-van/102194",
    "seller": {
      "@id": "https://pqsjapan.jp/#organization"
    }
  }
}
</script>
```

---

✅ Each schema is in its own `<script>` block.
✅ This keeps things modular, easier to maintain, and still Google-compliant.
