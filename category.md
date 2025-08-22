## 🔹 Final JSON-LD Schemas for Category Page (`/order/toyota`)

### **1. WebSite Schema**

```json
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "WebSite",
  "@id": "https://pqsjapan.jp/#website",
  "url": "https://pqsjapan.jp/",
  "name": "PQSJAPAN",
  "publisher": {
    "@id": "https://pqsjapan.jp/#organization"
  },
  "potentialAction": {
    "@type": "SearchAction",
    "target": {
      "@type": "EntryPoint",
      "urlTemplate": "https://pqsjapan.jp/search?q={search_term_string}"
    },
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

### **3. CollectionPage Schema**

```json
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "CollectionPage",
  "name": "Used Toyota Cars from Japan",
  "description": "Browse our inventory of used Toyota cars from Japan, including Toyota Vitz, Land Cruiser, Regiusace Van, and more. All cars are fully inspected and ready for worldwide export.",
  "url": "https://pqsjapan.jp/order/toyota",
  "isPartOf": {
    "@id": "https://pqsjapan.jp/#website"
  },
  "mainEntity": {
    "@id": "https://pqsjapan.jp/order/toyota/#itemlist"
  },
  "breadcrumb": {
    "@id": "https://pqsjapan.jp/order/toyota/#breadcrumb"
  }
}
</script>
```

---

### **4. BreadcrumbList Schema**

```json
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "BreadcrumbList",
  "@id": "https://pqsjapan.jp/order/toyota/#breadcrumb",
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
    }
  ]
}
</script>
```

---

### **5. ItemList Schema**

```json
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "ItemList",
  "@id": "https://pqsjapan.jp/order/toyota/#itemlist",
  "name": "Toyota Models",
  "itemListElement": [
    {
      "@type": "ListItem",
      "position": 1,
      "item": {
        "@type": "Product",
        "name": "Toyota Vitz",
        "url": "https://pqsjapan.jp/order/toyota/vitz",
        "image": "https://pqsjapan.jp/images/vitz.jpg",
        "offers": {
          "@type": "Offer",
          "priceCurrency": "USD",
          "price": "4500",
          "availability": "https://schema.org/InStock",
          "url": "https://pqsjapan.jp/order/toyota/vitz"
        }
      }
    },
    {
      "@type": "ListItem",
      "position": 2,
      "item": {
        "@type": "Product",
        "name": "Toyota Land Cruiser",
        "url": "https://pqsjapan.jp/order/toyota/land-cruiser",
        "image": "https://pqsjapan.jp/images/land-cruiser.jpg",
        "offers": {
          "@type": "Offer",
          "priceCurrency": "USD",
          "price": "15000",
          "availability": "https://schema.org/InStock",
          "url": "https://pqsjapan.jp/order/toyota/land-cruiser"
        }
      }
    },
    {
      "@type": "ListItem",
      "position": 3,
      "item": {
        "@type": "Product",
        "name": "Toyota Regiusace Van",
        "url": "https://pqsjapan.jp/order/toyota/regiusace-van",
        "image": "https://pqsjapan.jp/images/regiusace.jpg",
        "offers": {
          "@type": "Offer",
          "priceCurrency": "USD",
          "price": "6200",
          "availability": "https://schema.org/InStock",
          "url": "https://pqsjapan.jp/order/toyota/regiusace-van"
        }
      }
    }
  ]
}
</script>
```

---

✅ With this setup:

* Google recognizes PQSJAPAN as **the seller** (Organization).
* The Toyota category is a **CollectionPage** with proper breadcrumb hierarchy.
* **ItemList + Product** gives rich listing potential in SERPs (with name, price, availability).
