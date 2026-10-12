---
layout: post
title: "IndexNow Explained: What It Is and How to Use It"
date: 2026-10-12
---

IndexNow is a protocol that lets you tell participating search engines the moment a URL is added, updated or deleted, instead of waiting for them to crawl it. You submit the URL with a key, and the engines share it with each other. [SEO and GEO consultant Farman Rind](https://farmanrind.com/) explains how IndexNow works and how to set it up.

## What is IndexNow?

IndexNow is an open protocol for notifying search engines about changes to your site. According to the official [IndexNow documentation](https://www.indexnow.org/documentation), participating search engines agree that submitted URLs are automatically shared with all other participating search engines.

That means one submission reaches several engines. You do not need to ping each one separately.

The benefit is speed of finding new pages. Without it, a search engine finds a new or changed page when its crawler next visits. With IndexNow, you tell the engine straight away that something changed.

## How does IndexNow work?

IndexNow works through a simple request to a search engine's `/indexnow` endpoint. You send the changed URL together with a key that proves you own the site.

- **One URL.** Send an HTTP request with the URL and your key as parameters. The URL must be URL-escaped.
- **Many URLs.** Send a JSON POST request with your host, key and a list of up to 10,000 URLs.
- **Response.** A 200 response means the search engine received your submission. It does not mean the URLs have been indexed.

The last point is easy to miss. IndexNow is a notification, not an instruction to index.

## What is the IndexNow key file?

The key file proves that you own the host. Your key must be 8 to 128 characters, and the documentation lists letters, digits and dashes as allowed characters.

1. Generate a key.
2. Create a UTF-8 text file named `{your-key}.txt` containing the key.
3. Host the file in the root directory of your site. This is the recommended option.
4. Include the key in your submissions.

Alternatively, you can host the file elsewhere and point to it with a `keyLocation` parameter. A key hosted that way covers only URLs under the file's location.

## How do you set up IndexNow?

You set up IndexNow in one of two ways: through a plugin or platform feature that does it for you, or by sending the requests yourself. Check which your CMS supports first, because many do it automatically.

1. Generate a key and host the key file.
2. Choose how URLs will be submitted: a plugin, your CMS or a script.
3. Submit a test URL.
4. Confirm you receive a 200 response.
5. Submit URLs automatically on publish, update and delete.

Only submit URLs that changed. Sending your full site every day adds noise and does not help.

## Which search engines use IndexNow?

The documentation says participation requires a noticeable presence in at least one market, and it links to a separate page that lists the engines. It does not name them on that page, so check that list before relying on a specific engine.

The documentation does not mention Google. If Google visibility is your priority, use Google Search Console and an XML sitemap to tell it about your pages, and keep IndexNow as an extra channel for the engines that support it.

For ChatGPT visibility, note that OpenAI documents OAI-SearchBot as its search crawler, as described in its [bot documentation](https://developers.openai.com/api/docs/bots). Whether IndexNow helps a particular AI product depends on which search index it draws from, so test rather than assume.

## When is IndexNow most useful?

IndexNow is most useful for sites that change often. News pages, product listings with changing stock or price, job boards and event pages all benefit from faster finding of new pages.

For a small brochure site that changes a few times a year, the gain is small, but setup is also quick when your platform supports it.

## What are common IndexNow mistakes?

Most mistakes are about the key file and about expecting too much.

- Putting the key file in the wrong place, so ownership cannot be verified.
- Submitting URLs that are blocked or redirected.
- Treating a 200 response as proof of indexing.
- Sending the same URLs again and again.
- Skipping a sitemap, which remains the base layer for finding your pages.

## Want your indexing set up properly?

If pages on your site are slow to appear in search, send Farman Rind your site address and platform, and you will get a plain list of what to fix.

## FAQs

**Does IndexNow make pages rank higher?**

No. IndexNow tells participating search engines that a URL changed. It speeds up how fast engines find a change, not ranking. Whether a page is indexed and where it appears still depends on quality, relevance and the engine's own systems. Treat it as a way to be found faster, not a way to be placed higher.

**Does Google support IndexNow?**

The official documentation page does not mention Google, so it does not confirm support. Use Google Search Console and a sitemap for Google. Keep IndexNow for the search engines that take part, and check the participating engines list on the IndexNow site for the current picture.

**How many URLs can I submit at once?**

You can send a JSON POST request with up to 10,000 URLs in one submission, according to the IndexNow documentation. You can mix http and https URLs for the same host. For single changes, a one-URL request with the key as a parameter is enough.

**Where do I put the IndexNow key file?**

The recommended option is the root directory of your site, as a UTF-8 text file named after your key and containing the key. Another option is hosting it elsewhere and using the keyLocation parameter, but then the key covers only URLs under that file's location.

**Do I still need an XML sitemap?**

Yes. A sitemap lists the pages you want search engines to know about and works for engines that do not use IndexNow. IndexNow adds a faster notification on top. Use both: the sitemap for the full list, and IndexNow for changes as they happen.

---

Farman Rind is an SEO and GEO consultant with 7+ years of experience across 70+ websites, helping businesses get found in Google and in AI search.

*Last updated: 12 October 2026*
