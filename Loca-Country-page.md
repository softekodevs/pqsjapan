This page is more specific than the `/local` overview:

* It shows **used car listings filtered by country** (Zimbabwe in this case).
* It should include **CollectionPage + ItemList + BreadcrumbList + Organization**.
* We can also enrich it with **Place / Country** properties to reinforce the geographic targeting.

---

## ✅ Local Country Page Schema (separated blocks)

---

### **1. CollectionPage Schema**

```json
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "CollectionPage",
  "@id": "https://pqsjapan.jp/local/zimbabwe#collectionpage",
  "name": "Used Cars for Zimbabwe - PQSJAPAN",
  "description": "Explore PQSJAPAN's selection of used cars available for export to Zimbabwe. Browse Toyota, Nissan, Honda and other top brands ready for import.",
  "url": "https://pqsjapan.jp/local/zimbabwe",
  "isPartOf": {
    "@id": "https://pqsjapan.jp/#website"
  },
  "breadcrumb": {
    "@id": "https://pqsjapan.jp/local/zimbabwe#breadcrumb"
  },
  "mainEntity": {
    "@id": "https://pqsjapan.jp/local/zimbabwe#itemlist"
  }
}
</script>
```

---

### **2. Organization Schema (site-wide, reused here)**

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
    "areaServed": "Zimbabwe",
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
  "@id": "https://pqsjapan.jp/local/zimbabwe#breadcrumb",
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
      "name": "Local Markets",
      "item": "https://pqsjapan.jp/local"
    },
    {
      "@type": "ListItem",
      "position": 3,
      "name": "Zimbabwe",
      "item": "https://pqsjapan.jp/local/zimbabwe"
    }
  ]
}
</script>
```

---

### **4. ItemList Schema (cars available for Zimbabwe)**

👉 Keep this **dynamic**, auto-generated from your stock for that country.

```json
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "ItemList",
  "@id": "https://pqsjapan.jp/local/zimbabwe#itemlist",
  "name": "Used Cars Available for Zimbabwe",
  "itemListOrder": "https://schema.org/ItemListOrderAscending",
  "numberOfItems": 2,
  "itemListElement": [
    {
      "@type": "ListItem",
      "position": 1,
      "item": {
        "@type": "Product",
        "name": "Toyota Corolla 2015",
        "url": "https://pqsjapan.jp/order/toyota/corolla/12345",
        "image": "https://pqsjapan.jp/images/corolla-2015.jpg",
        "offers": {
          "@type": "Offer",
          "priceCurrency": "USD",
          "price": "6500",
          "availability": "https://schema.org/InStock",
          "url": "https://pqsjapan.jp/order/toyota/corolla/12345"
        }
      }
    },
    {
      "@type": "ListItem",
      "position": 2,
      "item": {
        "@type": "Product",
        "name": "Nissan X-Trail 2017",
        "url": "https://pqsjapan.jp/order/nissan/x-trail/67890",
        "image": "https://pqsjapan.jp/images/xtrail-2017.jpg",
        "offers": {
          "@type": "Offer",
          "priceCurrency": "USD",
          "price": "9800",
          "availability": "https://schema.org/InStock",
          "url": "https://pqsjapan.jp/order/nissan/x-trail/67890"
        }
      }
    }
  ]
}
</script>
```

---

### **5. (Optional) Place Schema for Zimbabwe**

👉 This reinforces **regional targeting** for SEO.

```json
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "Place",
  "@id": "https://pqsjapan.jp/local/zimbabwe#place",
  "name": "Zimbabwe",
  "address": {
    "@type": "PostalAddress",
    "addressCountry": "ZW"
  }
}
</script>
```

---

✅ With this:

* **Google understands `/local/zimbabwe` is a country-specific collection page**.
* **Vehicles are clearly marked with `ItemList → Product → Offer`**.
* **Breadcrumb navigation + Place schema reinforce Zimbabwe targeting**.

---

👉 Do you also want me to prepare a **dynamic schema template** (where variables auto-fill product name, ID, image, price, country) so it can be integrated into PQSJAPAN’s backend for **all countries automatically**?
