---
layout: post
title: "URL Structure Best Practices for SEO"
date: 2026-10-15
---

The best URL structure uses short, readable words separated by hyphens, keeps parameters to a minimum and sticks to one letter case. Google's guidance is plain and easy to follow. This guide from an [SEO and GEO consultant](https://farmanrind.com/), Farman Rind, covers URL structure best practices and how to fix a messy site.

## What makes a good URL?

A good URL describes the page in words a person can read. Google's [URL structure guidance](https://developers.google.com/search/docs/crawling-indexing/url-structure) says to use readable words instead of long ID numbers. Its example prefers `example.com/wiki/Aviation` to a URL packed with IDs and query strings.

Use your audience's language in the path. If your readers search in another language, use it in the URL, and percent-encode non-ASCII characters where needed.

A good URL is easy to read aloud, easy to share and tells a visitor what to expect before they click.

## Should you use hyphens or underscores?

Use hyphens. Google advises separating words with hyphens and advises against underscores, which are commonly used in programming to join terms that belong together. It also lists joining words with no separator as not recommended.

| Style | Example | Recommended |
|---|---|---|
| Hyphens | `/seo-audit-checklist` | Yes |
| Underscores | `/seo_audit_checklist` | No |
| No separator | `/seoauditchecklist` | No |

If your site already uses underscores, changing them needs 301 redirects and updated internal links. Weigh the effort against the benefit before you start.

## How should you handle parameters?

Keep parameters to a minimum and remove any that do not change the page's content. Google says to use `=` for key-value pairs and `&` to add parameters, and notes that commas can list several values for one key.

Avoid session IDs in URLs where possible, and use cookies instead. Google also warns that overly complex URLs, especially those with many parameters, can create huge numbers of URLs and cause crawling problems.

This matters most for shops with filters and sorting. Decide which combinations deserve their own page, and control the rest with canonical tags or by limiting crawlable links.

## Does letter case matter?

Yes. Google treats URL paths as case-sensitive, so `/APPLE` and `/apple` are different URLs. If your server treats them as the same page, you create duplicates for no reason.

The fix is simple:

1. Choose lowercase for all paths.
2. Redirect uppercase variants to the lowercase version.
3. Link internally to the lowercase URL only.

## How long should a URL be?

Google's guidance does not give a length limit, so there is no official number. Keep URLs as short as they can be while staying clear. A short path with the main topic words is easier to read, and it avoids the problems that long, complicated URLs cause.

Do not stuff the URL with keywords. One clear phrase is enough.

## What about changing existing URLs?

Change existing URLs only when there is a real problem, and always redirect the old address. A URL change is a migration, even a small one.

1. List the old and new URLs.
2. Set 301 redirects from each old URL to its new URL.
3. Update internal links, canonical tags and sitemap entries.
4. Check that the redirects work and avoid chains.
5. Monitor Search Console for errors.

Google describes permanent redirects as a strong signal that the target should be processed, as explained in its [guide to consolidating duplicate URLs](https://developers.google.com/search/docs/crawling-indexing/consolidate-duplicate-urls).

## A short URL checklist

Use this list for every new page.

- Readable words, no ID numbers.
- Hyphens between words.
- Lowercase only.
- Few or no parameters.
- A clear topic in the path.
- One URL per page, with redirects for old versions.

## What does a before and after look like?

A before and after comparison shows the rules in action. These examples are made up to illustrate the pattern.

| Before | After | What changed |
|---|---|---|
| `/index.php?id=4821&cat=17` | `/services/technical-seo` | ID numbers replaced with readable words |
| `/Our_Services/SEO_Audit` | `/services/seo-audit` | Underscores and capitals removed |
| `/blog/post?session=a8f3&sort=new` | `/blog/post` | Session ID and sort parameter removed |
| `/seoauditchecklist` | `/seo-audit-checklist` | Hyphens added between words |

Each change makes the address easier to read, easier to share and less likely to create duplicates. When you make them on a live site, redirect every old URL to its new version.

## Need a URL audit?

If your URLs are messy and you are unsure whether changing them is worth the risk, send Farman Rind a sample of 20 URLs and you will get a clear recommendation.

## FAQs

**Do URLs affect rankings?**

Google's guidance treats URL structure mainly as a matter of clarity and crawling. Readable URLs help people and make crawling simpler. Do not expect a large ranking change from rewriting URLs alone, and do not change working URLs without a good reason and proper redirects.

**Should I include keywords in my URL?**

Yes, where they describe the page in natural words. A path such as `/seo-audit-checklist` tells people and search engines what to expect. Do not stuff several keywords into the URL, because it reads as spam to visitors and gives no extra benefit for search.

**Are underscores bad in URLs?**

Google advises using hyphens to separate words and advises against underscores. Both are crawlable, but hyphens are the recommended choice. If you have existing underscore URLs that work, changing them needs redirects, so only do it as part of a wider clean-up.

**Is uppercase a problem in URLs?**

It can be. Google treats URL paths as case-sensitive, so `/APPLE` and `/apple` are different URLs. If both load, you have duplicate pages competing with each other. Pick lowercase, redirect the other variants to it with a 301 and link only to the lowercase version.

**How many parameters are too many?**

Google gives no number. The advice is to keep parameters to a minimum and remove any that do not change the page content. Complex URLs with many parameters can create excessive URLs and crawling problems, so review filters, sorting and tracking parameters.

---

Farman Rind is an SEO and GEO consultant with 7+ years of experience across 70+ websites, helping businesses get found in Google and in AI search.

*Last updated: 15 October 2026*
