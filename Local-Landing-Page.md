# The key schemas here are:

* **CollectionPage** → represents the “Local Markets” overview page itself.
* **Organization** → links PQSJAPAN as the seller/exporter tied to that local market.
* **BreadcrumbList** → navigation trail (Home → Local → Country).
* *(Optional)* **ItemList** → if you’re listing multiple countries/markets inside `/local`.
* *(Optional)* **Place / Country** → if each local landing links to a specific region.

---

## ✅ Local Landing Page Schema (separated blocks)

---

### **1. CollectionPage Schema**

```json
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "CollectionPage",
  "@id": "https://pqsjapan.jp/local#collectionpage",
  "name": "Local Markets - PQSJAPAN",
  "description": "Explore PQSJAPAN local landing pages by country. Find region-specific used car listings, import details, and export support for your market.",
  "url": "https://pqsjapan.jp/local",
  "isPartOf": {
    "@id": "https://pqsjapan.jp/#website"
  },
  "breadcrumb": {
    "@id": "https://pqsjapan.jp/local#breadcrumb"
  }
}
</script>
```

---

### **2. Organization Schema (linked again for this context)**

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
  "@id": "https://pqsjapan.jp/local#breadcrumb",
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
    }
  ]
}
</script>
```

---

### **4. (Optional) ItemList for Countries**

👉 If `/local` lists countries (e.g. `/local/zimbabwe`, `/local/kenya`, `/local/uganda`), you can add this:

```json
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "ItemList",
  "@id": "https://pqsjapan.jp/local#itemlist",
  "name": "Local Market Pages",
  "itemListElement": [
    {
      "@type": "ListItem",
      "position": 1,
      "item": {
        "@type": "WebPage",
        "name": "Zimbabwe Local Market",
        "url": "https://pqsjapan.jp/local/zimbabwe"
      }
    },
    {
      "@type": "ListItem",
      "position": 2,
      "item": {
        "@type": "WebPage",
        "name": "Kenya Local Market",
        "url": "https://pqsjapan.jp/local/kenya"
      }
    }
  ]
}
</script>
```

---

✅ With this setup:

* **Google understands `/local` as a category/collection hub**.
* **Each country page can later get its own `CollectionPage + BreadcrumbList + Organization` schema**.
