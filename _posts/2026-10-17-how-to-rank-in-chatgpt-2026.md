---
layout: post
title: "How to Rank in ChatGPT (2026)"
date: 2026-10-17
---

To rank in ChatGPT, let OAI-SearchBot crawl your site, publish pages that answer one question clearly, and get mentioned on other sites that ChatGPT already trusts. There is no ranking position to buy or claim. This guide from [this SEO and GEO consultant](https://farmanrind.com/), Farman Rind, sets out what actually controls whether ChatGPT names you.

Start with the crawler. Everything else is wasted if that part is wrong.

## Which crawler decides whether you appear in ChatGPT?

OAI-SearchBot is the one that matters. According to [OpenAI's bot documentation](https://developers.openai.com/api/docs/bots), OAI-SearchBot is used to surface websites in ChatGPT's search features. A site that opts out will not appear in ChatGPT search answers, though it can still show up as a navigational link.

OpenAI documents three separate user agents, and confusing them is the most common mistake I see:

- **OAI-SearchBot** surfaces sites in ChatGPT's search features. Block it and you disappear from ChatGPT search answers.
- **GPTBot** crawls content that may be used to train OpenAI's foundation models. Blocking it signals your content should not be used for training. It does not remove you from ChatGPT search.
- **ChatGPT-User** supports user-initiated actions, such as when someone asks a question or uses a GPT Action. Because a person triggers these visits, robots.txt rules may not apply.

Changes to robots.txt can take about 24 hours to affect search results, so do not judge a fix the same day you make it.

## How do you check you are not blocked?

Open your robots.txt and read it line by line before you do anything else. A single rule left over from a staging site is the most common reason a brand is absent from AI answers entirely.

1. Visit `yourdomain.com/robots.txt` and read every rule.
2. Confirm there is no `Disallow: /` applying to OAI-SearchBot or to all user agents.
3. Check whether a blanket "block all AI bots" rule is catching OAI-SearchBot along with the training crawlers.
4. Check each subdomain separately, because each one needs its own file.
5. Wait a day, then ask ChatGPT a question your site should answer.

If you want training opt-out without losing visibility, disallow GPTBot and allow OAI-SearchBot. Those are two different decisions and you can answer them differently.

## What kind of content gets cited?

Content that answers one question completely in a short span of text gets cited. AI systems assemble answers from passages, not from whole pages, so a page that buries its answer under 600 words of preamble is hard to quote even when it is the best page on the subject.

The research paper that named this field, [GEO: Generative Engine Optimization](https://arxiv.org/abs/2311.09735) by Pranjal Aggarwal and colleagues, reports visibility gains of up to 40 percent from content changes in its tests. Treat that as a research result rather than a promise for your site.

In practice, these are the changes that make a page quotable:

- Open every section with a direct answer in the first sentence.
- Give each question its own heading, in the words a person would use.
- Name your brand, product and people in full rather than writing "it" or "we".
- Put facts, numbers and prices in plain text, not inside images.
- Show an author and a last updated date.

## Does Google's guidance apply to ChatGPT too?

Partly, and the overlap is larger than most people assume. Google's own guidance on [AI features in Search](https://developers.google.com/search/docs/appearance/ai-features) says a page must be indexed and eligible to appear with a snippet, and that there are no additional requirements or special optimizations necessary.

The same fundamentals serve both systems: crawlable pages, content in text form, internal links so pages can be found, and structured data that matches what the visitor sees. Google also states you do not need new machine-readable files, AI text files or special schema markup. There is no evidence that a file of that kind changes what ChatGPT cites either, so treat any product sold on that basis with suspicion.

## Why do third-party mentions matter so much?

AI answers frequently cite sources that are not the brand's own website. Review sites, directories, community threads, news coverage and independent listicles all feed the picture an assistant builds of your category.

This is why a company with a perfect website can still be absent from answers. If nobody outside your own domain describes what you do, the assistant has only your marketing copy to work from, and it tends to prefer sources that are not trying to sell.

The work here is ordinary public relations and consistency:

- Keep your business name, description and category identical across every profile.
- Get listed on the directories and review sites your category actually uses.
- Answer questions in the communities where your buyers already are.
- Earn coverage that describes what you do in someone else's words.

## How do you measure whether it is working?

Test it by hand, monthly, with the same list of questions every time. No tool can promise you a citation, and answers vary between runs, so a single check tells you almost nothing.

1. Write 20 questions your buyers would genuinely ask an assistant.
2. Ask each one in ChatGPT and record whether your brand is named.
3. Record which sources are cited instead of you.
4. Repeat monthly and compare.

The list of sources cited instead of you is the most valuable output. It tells you exactly which third-party pages to go and influence.

## Ready to find out where you stand?

Send me your website and the three questions your buyers are most likely to ask an assistant. You will get a straight answer on whether you are visible and what to fix first.

## FAQs

**Can I pay to rank in ChatGPT?**

No. There is no paid placement in ChatGPT's organic answers and no submission process. What you control is whether OAI-SearchBot can crawl your site, how clearly your pages answer questions, and how often other trusted sites mention you. Anyone selling a promised ChatGPT ranking is selling something that does not exist.

**Does blocking GPTBot hurt my ChatGPT visibility?**

No. OpenAI documents GPTBot as the crawler for content that may train its foundation models, while OAI-SearchBot is what surfaces sites in ChatGPT's search features. You can disallow GPTBot and still allow OAI-SearchBot, which keeps you eligible for ChatGPT search answers while opting out of training use.

**How long does a robots.txt change take to work?**

OpenAI says changes to robots.txt can take about 24 hours to affect search results. Allow at least a day before you test, and avoid making repeated edits while you wait. Verify the file loads correctly at your domain root first, because a file that returns an error is worse than no change at all.

**Do I need an llms.txt file?**

There is no documented evidence that it changes what ChatGPT cites. Google states plainly that you do not need new machine-readable files or AI text files for its AI features. Spend the effort on crawler access, clear answers and third-party mentions, which are the things the documentation actually describes as mattering.

**How is this different from normal SEO?**

The foundations are the same: be crawlable, be indexed, write clearly. The differences are that AI systems pull short passages rather than ranking whole pages, and that they lean heavily on sources beyond your own site. So you optimise passages and entities rather than pages, and you spend more effort on being mentioned elsewhere.

---

Farman Rind is an SEO and GEO consultant with 7+ years of experience across 70+ websites, helping businesses get found in Google and in AI search.

*Last updated: 17 October 2026*
