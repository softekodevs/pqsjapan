# PQSJAPAN Homepage Schema Documentation

This document provides the structured data (JSON-LD) schemas for the **PQSJAPAN** homepage. These code snippets are designed to be copied and pasted directly into the `<head>` section of the homepage's HTML file to improve SEO and search engine visibility.

-----

### How to Use

1.  **Copy the code:** Select and copy the entire `<script>` block for each schema you want to implement.
2.  **Paste into HTML:** Paste the code into the `<head>` section of your `index.html` or homepage file.
3.  **Validate:** After deployment, use Google's [Rich Results Test](https://search.google.com/test/rich-results) to ensure the schemas are free of errors and correctly recognized.

-----

### **1. WebSite Schema**

This schema defines your website as a whole. It includes the `potentialAction` property to enable the **sitelinks search box** in search results, allowing users to search your site directly from Google.

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

-----

### **2. Organization Schema**

This schema provides details about the **PQSJAPAN** brand. It helps Google understand your company's official name, logo, and social media profiles.

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
    "contactType": "Customer Service",
    "areaServed": "Worldwide",
    "availableLanguage": ["en", "ja"]
  }
}
</script>

```

-----

### **3. BreadcrumbList Schema**

Use this schema to define the breadcrumb trail for the homepage. It helps search engines understand the page's position in the site hierarchy.

```json
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "BreadcrumbList",
  "itemListElement": [
    {
      "@type": "ListItem",
      "position": 1,
      "name": "Home",
      "item": "https://pqsjapan.jp/"
    }
  ]
}
</script>
```

-----

### **4. SiteNavigationElement Schema**

This schema provides structured data for the main navigation menu. It helps search engines understand your key site links, which may improve the quality of **sitelinks** in SERPs.

```json
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "SiteNavigationElement",
  "name": "Main Navigation",
  "itemListElement": [
    {
      "@type": "SiteNavigationElement",
      "position": 1,
      "name": "All Stock",
      "url": "https://pqsjapan.jp/all-stock"
    },
    {
      "@type": "SiteNavigationElement",
      "position": 2,
      "name": "Truck Stock",
      "url": "https://pqsjapan.jp/truck-stock"
    },
    {
      "@type": "SiteNavigationElement",
      "position": 3,
      "name": "Back Order",
      "url": "https://pqsjapan.jp/stock-list"
    },
    {
      "@type": "SiteNavigationElement",
      "position": 4,
      "name": "Local",
      "url": "https://pqsjapan.jp/local"
    },
    {
      "@type": "SiteNavigationElement",
      "position": 5,
      "name": "Contact Us",
      "url": "https://pqsjapan.jp/contact"
    }
  ]
}
</script>
```
