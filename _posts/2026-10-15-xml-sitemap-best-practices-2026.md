---
layout: post
title: "XML Sitemap Best Practices (2026)"
date: 2026-10-15
---

XML sitemap best practices are simple: list only the URLs you want indexed, use full absolute URLs, keep each file under 50,000 URLs and 50MB, and set lastmod only when it is accurate. This guide by Farman Rind of [farmanrind.com](https://farmanrind.com/) follows Google's sitemap documentation, checked on 15 October 2026.

## What is an XML sitemap?

An XML sitemap is a file that lists the URLs on your site that you want search engines to know about. It helps crawlers find pages, especially on large sites or sites with weak internal linking.

Google's [sitemap documentation](https://developers.google.com/search/docs/crawling-indexing/sitemaps/build-sitemap) says it accepts XML sitemaps, RSS 2.0 and Atom 1.0 feeds, and plain text files, and has no format preference. It also says submitting a sitemap is a hint: Google does not promise to download or use it for crawling.

A sitemap supports good internal linking. It does not replace it.

## What are the size limits?

A single sitemap can hold up to 50,000 URLs and be up to 50MB uncompressed. Larger sets must be split across several sitemaps, which you can group under a sitemap index file.

| Item | Limit or rule |
|---|---|
| URLs per sitemap | 50,000 |
| File size | 50MB uncompressed |
| Encoding | UTF-8 |
| URL form | Fully qualified absolute URLs |
| Many sitemaps | Group under a sitemap index file |

For a large site, split by type, such as products, categories and articles. This makes problems easier to find in Search Console.

## What should you include?

Include only canonical, indexable URLs that return a normal page. A sitemap is a statement of which pages you want in search, so every URL in it should be one you would be happy to see ranking.

- Pages that return a 200 status.
- Canonical versions only.
- Pages you want indexed.

Leave out:

- Redirected URLs.
- Pages that return errors.
- Pages with a `noindex` tag.
- Parameter and duplicate versions.
- Internal search results and thin pages.

Google lists a sitemap URL as a weak signal for the canonical, so keep it consistent with your canonical tags.

## How should you use lastmod?

Use lastmod only if you can keep it accurate. Google says it uses `<lastmod>` only if it is consistently and verifiably accurate, and that it should reflect the last significant update, such as changes to main content, structured data or links. Updating a copyright year does not count.

A common mistake is setting lastmod to the current date on every build. Google then learns to ignore the field for your site.

## What does Google ignore?

Google ignores priority and changefreq. The documentation states that Google ignores both values. You can leave them out, which also makes your files smaller.

Many plugins still add them by default. They do no harm, but they do no good, and time spent tuning them is wasted.

## How do you submit a sitemap?

You can submit a sitemap in three ways. Choose one and be consistent.

1. **Search Console.** Use the Sitemaps report to submit the file and see whether it was read.
2. **Search Console API.** Useful if you manage many properties.
3. **robots.txt.** Add a `Sitemap:` line with the full URL. There is no limit on how many you list.

Google's [Search Console overview](https://support.google.com/webmasters/answer/9128668) explains what the service reports. After submitting, check the Sitemaps report for errors and compare submitted URLs with indexed URLs.

## What are common sitemap mistakes?

Most sitemap problems come from automation that nobody checks. Review your file each quarter.

- Including URLs that redirect or return errors.
- Listing relative URLs instead of absolute ones.
- Mixing http and https versions of the same page.
- Leaving staging or test URLs in the file.
- Letting a plugin add noindexed pages.
- Using an inaccurate lastmod.

## How do you check that your sitemap works?

Check your sitemap by comparing what you submitted with what Google indexed. The gap tells you where to look. Follow this short routine each quarter.

1. Open the Sitemaps report in Search Console and confirm the file was read without errors.
2. Open the Page indexing report and filter by the sitemap.
3. List the submitted URLs that are not indexed, and note the reason for each.
4. Decide for each group: should this page be indexed? If not, remove it from the sitemap.
5. If it should be indexed, fix the cause, such as a noindex tag, a redirect or thin content.

A sitemap with 5,000 URLs where only 2,000 are indexed is a sign that the list needs cleaning, not that Google is broken.

## Need a sitemap review?

If your sitemap lists pages that are not indexed, send Farman Rind your sitemap URL and you will get a short list of what to remove and fix.

## FAQs

**Do I need an XML sitemap?**

Not always. Small sites with good internal linking can be crawled without one. A sitemap helps most on large, new or frequently changing sites. It costs little to add, and the Sitemaps report in Search Console gives you useful feedback, so most sites should have one.

**How many URLs can an XML sitemap contain?**

Up to 50,000 URLs, and up to 50MB uncompressed, according to Google. If you need more, split the URLs across several sitemap files and list them in a sitemap index file. Splitting by content type also makes it easier to spot problems.

**Does Google use priority and changefreq?**

No. Google's documentation states that it ignores the priority and changefreq values. You can omit them. Spend your effort on the accuracy of the URL list and on lastmod instead, because Google does use lastmod when it is consistently and verifiably accurate.

**Should I include noindex pages in my sitemap?**

No. A sitemap should list pages you want indexed. Including noindex pages sends mixed signals and makes it harder to read the Sitemaps report. Keep only canonical, indexable URLs that return a normal page, and remove redirects, errors and duplicates.

**How do I submit my sitemap to Google?**

Submit it in the Sitemaps report in Search Console, through the Search Console API, or by adding a Sitemap line to your robots.txt file. Any of these works. After submitting, check the report for read errors and compare the number of submitted pages with those indexed.

---

Farman Rind is an SEO and GEO consultant with 7+ years of experience across 70+ websites, helping businesses get found in Google and in AI search.

*Last updated: 15 October 2026*
