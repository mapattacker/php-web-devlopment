# Sitemap

[Sitemaps](https://www.sitemaps.org/protocol.html) are an easy way for webmasters to inform search engines about pages on their sites that are available for crawling. It is contained within the file `sitemap.xml`

## What It Is

> In its simplest form, a Sitemap is an XML file that lists URLs for a site along with additional metadata about each URL (when it was last updated, how often it usually changes, and how important it is, relative to other URLs in the site) so that search engines can more intelligently crawl the site.

> Web crawlers usually discover pages from links within the site and from other sites. Sitemaps supplement this data to allow crawlers that support Sitemaps to pick up all URLs in the Sitemap and learn about those URLs using the associated metadata. Using the Sitemap protocol does not guarantee that web pages are included in search engines, but provides hints for web crawlers to do a better job of crawling your site.

## Sample Sitemap

Below is a sample sitemap.xml file. There are 3 optional tags: `lastmod`, `changefreq` and `priority`.

```xml
<?xml version="1.0" encoding="UTF-8"?>

<urlset xmlns="http://www.sitemaps.org/schemas/sitemap/0.9">

   <url>

      <loc>http://www.example.com/</loc>

      <lastmod>2005-01-01</lastmod>

      <changefreq>monthly</changefreq>

      <priority>0.8</priority>

   </url>

   <url>

      <loc>http://www.example.com/catalog?item=12&amp;desc=vacation_hawaii</loc>

      <changefreq>weekly</changefreq>

   </url>

   <url>

      <loc>http://www.example.com/catalog?item=73&amp;desc=vacation_new_zealand</loc>

      <lastmod>2004-12-23</lastmod>

      <changefreq>weekly</changefreq>

   </url>

   <url>

      <loc>http://www.example.com/catalog?item=74&amp;desc=vacation_newfoundland</loc>

      <lastmod>2004-12-23T18:00:15+00:00</lastmod>

      <priority>0.3</priority>

   </url>

   <url>

      <loc>http://www.example.com/catalog?item=83&amp;desc=vacation_usa</loc>

      <lastmod>2004-11-23</lastmod>

   </url>

</urlset>
```

## Submitting the Sitemap

Google is the most dominate search engine in world, so it is a must to submit your sitemap to it. This is done through the [Google Search Console](https://search.google.com/search-console).

Bing is another search engine which has its [Webmaster Tools](https://www.bing.com/webmasters/) to submit your sitemap and do some analysis of your website.