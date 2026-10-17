---
layout: post
title: "Internal Linking Strategy That Works (2026)"
date: 2026-10-17
---

An internal linking strategy comes down to two rules from Google: every page you care about should be linked from at least one other page on your site, and the link has to be a real `<a>` element with an `href`. This guide from [farmanrind.com](https://farmanrind.com/), written by Farman Rind, covers internal linking in the detail that actually changes results.

Most sites do not need more links. They need the right ones, pointing at the pages that earn money.

## What counts as a crawlable link?

Google generally follows only `<a>` elements that have an `href` attribute. That single sentence from Google's [crawlable links documentation](https://developers.google.com/search/docs/crawling-indexing/links-crawlable) rules out a surprising amount of what modern sites ship.

Links that work:

- Absolute URLs, relative paths and query-string URLs are all fine.
- Extra attributes such as `onclick` or `class` do not prevent crawling.
- JavaScript-inserted links are crawlable if they use the same `<a href>` markup.

Links that may not work:

- `<span href>`, `routerLink` and links that rely on `onclick` alone may not be parsed.
- Pseudo-URLs such as `javascript:goTo('products')` are not recommended, because the URL should resolve to a real web address.

Google says it may still attempt some of these, but that you should not depend on it. If a section of your site is built from button handlers rather than anchors, that is where to look first.

## How should you write anchor text?

Put descriptive text between the `<a>` tags. Google uses the `title` attribute only as a fallback when the link is empty, and for image links it uses the image's alt text as the anchor text.

Google's guidance on good anchor text is specific and easy to apply:

- Be specific and reasonably concise.
- Make it make sense when read out of context.
- Avoid generic phrases such as "click here" or "read more", which it names as weak.
- Write naturally. Do not stuff keywords into anchor text.
- Do not cluster several links side by side.

The out-of-context test is the useful one. If someone read your anchor text alone, with none of the sentence around it, would they know where the link goes?

## Which pages should you link to?

Link to the pages that make you money, from the pages that get traffic. That sounds obvious and it is routinely ignored, because most internal linking happens by accident through navigation and related-post widgets.

Work it out deliberately:

1. List your service or product pages. These are the destinations.
2. Open the Performance report in [Google Search Console](https://support.google.com/webmasters/answer/9128668) and list the pages getting the most impressions.
3. For each high-impression page, ask whether it links to a relevant destination.
4. Add that link in the body text, in a sentence, where it genuinely helps the reader.

Google's advice is to link to related resources in context, which is exactly this. A link inside a sentence a reader is already reading carries more weight with people than a row of links in a footer.

## How many internal links should a page have?

There is no ideal number. Google states this plainly, and adds that excessive linking is a sign to trim. So the answer is: as many as help the reader, and no more.

What I look for instead of a count:

- Does every link go somewhere relevant to the sentence it sits in?
- Could a reader finish the page without being pulled away three times?
- Is the most important link on the page easy to spot?

If a paragraph has four links competing for attention, none of them gets clicked. Cutting links often works better than adding them.

## What about orphan pages?

An orphan page is a page with no internal links pointing at it. Google's rule is that every page you care about should be linked from at least one other page on your site, which makes orphans a direct problem.

They appear for predictable reasons: a page built for a campaign and never added to navigation, an old service page dropped from a menu during a redesign, or content published straight from a CMS without an entry point.

Find them by comparing a crawl of your site against your sitemap and your analytics. Pages that appear in one but not the other are the candidates. Then either link them properly from a relevant page, or accept they are not needed and remove them.

## Does internal linking help with AI search?

It helps, and Google says so directly. Its guidance on [AI features in Search](https://developers.google.com/search/docs/appearance/ai-features) lists internal links among the standard practices that still apply for appearing in AI Overviews and AI Mode, alongside allowing crawling, good page experience and keeping important content in text form.

The logic is the same as for ordinary search. A page that nothing links to is hard to find, and a page that is hard to find cannot be cited.

## A monthly internal linking routine

Fifteen minutes a month keeps this healthy, and that beats a large one-off project that nobody repeats.

1. List any pages published since last month.
2. For each one, add at least one link from an older, relevant page.
3. Pick your top three money pages and check how many pages link to them.
4. Fix any link pointing at a redirect, so it points at the final URL instead.
5. Check that no important page has become an orphan.

## Want this looked at properly?

Send me your site address and the three pages that matter most commercially. I will tell you what is linking to them now and what should be.

## FAQs

**How many internal links should a page have?**

Google says there is no ideal number, and that excessive linking is a sign to trim. Judge by whether each link helps the reader at the point it appears. A handful of relevant links inside the text beats twenty scattered through a page, which compete with each other and dilute attention.

**Do internal links pass ranking value?**

Internal links help Google find and understand your pages, and Google's own guidance stresses that every page you care about should be linked from somewhere on your site. Rather than thinking in terms of value flowing, think about how pages are found and understood: links tell Google which pages exist and what they are about.

**What is the best anchor text for internal links?**

Specific, concise text that makes sense out of context. Google names "click here" and "read more" as weak examples. Describe the destination in the words a reader would use, write it naturally within the sentence, and avoid stuffing keywords or placing several links next to each other.

**Are JavaScript links crawlable?**

They can be. Google says JavaScript-inserted links are crawlable if they use standard `<a href>` markup. What is not reliable is `routerLink`, `<span href>` or links that work only through an `onclick` handler. If navigation depends on those, check the rendered HTML with the URL Inspection tool.

**What is an orphan page and does it matter?**

An orphan page has no internal links pointing to it. It matters, because Google's guidance is that every page you care about should be linked from at least one other page. Orphans are harder to find and easy to forget. Either link them from a relevant page or remove them deliberately.

---

Farman Rind is an SEO and GEO consultant with 7+ years of experience across 70+ websites, helping businesses get found in Google and in AI search.

*Last updated: 17 October 2026*
