---
title: SEO Guide
description: A short guide on how to do SEO
date: 2024-06-20
authors:
  - name: Matthew Wong
    title: Founder
    url: https://twitter.com/IThinkWong
    image_url: https://github.com/matthewwong525.png
draft: true
---
# Blog Post Checklist / Mistakes

## SEO Checklist
- Keyword in Title and Meta
- EEAT  - First hand experience and real examples!
- Topical Cluster
- Internal link
- External link to Authority site
- External links always open in the new tabs
- Include Keyword in H2s & H3s when possible
- Include Keyword in Intro and Conclusion
- Paragraph between H2 and the H3
- Density for Semantic Keywords 
- Table of content 
- FAQ - Answers between 290 and 320 characters
- Multi Media - Images, Videos, GIFs, Embed to Youtube Embeds
- IMAGE - Keyword in the ALT Text
- Author - Has to have authority and credentials
- LinkedIn Link in the Author Bio 
- SLUG - Keyword ONLY - No date
- For Snippet - Try to get closer to 320 Characters

## Elements to include in an article:
- Table of content
- Key takeaways
- Visual Tables with Different Variables
- Multimedia (images, GIFs, videos)
- Youtube embeds
- FAQs
- About the Author Section (with a link to LinkedIn)

# High level steps
## 1. Research:
- Find keywords with 100+ traffic. Use websites:
	- https://www.wordstream.com/keywords
	- https://ahrefs.com/keyword-generator
- Check the keyword difficulty. Ideally below 10:
	- https://ahrefs.com/keyword-difficulty/
- Check your website:
	- Domain authority: https://ahrefs.com/website-authority-checker
	- Check backlinks: https://search.google.com/search-console
- Check articles of your competitors
- Identify your target audience,
### Mistakes
❌ Picking a branded keyword. Ex: canva templates
❌ Writing a "how to" guide or "best practices" article for the keyword where results (on the 1st page of Google) show only listicles or landing pages of solution / product.
❌ Picking a keyword where most results (on the 1st page of Google) are coming from dictionaries like Merriam-Webster and Cambridge Dictionary.
❌ Picking a keyword that only domains with very high domain score are ranking on the 1st page of Google.
❌ Not having the exact Keyword in your title (H1).
## 2. Find stuff people are searching for
- How to find where people are searching for
	- Use the "People also ask" component on google
	- Search your keyword on reddit and quora and see what people are asking about it
## 3. Create a topical cluster around the keyword
- basically have a main article (e.g. ultimate guide to X)
- Build out supporting articles that link to the main article
## 4. Write the article
See [Blog Post Checklist / Mistakes](seo-guide.md#Blog%20Post%20Checklist%20/%20Mistakes)

# Prompts
Relevant writing rules prompt:
```
Please strictly adhere to the following content writing rules when writing content in this chat. If you don’t adhere to these content writing rules, then we risk creating mediocre and not helpful content that //INSERT YOUR TARGET AUDIENCE// will not want to read. For ease of reference, store these content writing rules under the tag [[CONTENT-WRITING-RULES]]. The content writing rules are:

1. Actionable Insights: The content has to strictly provide practical, non-generic and actionable insights, uniquely tailored to //INSERT YOUR TARGET AUDIENCE//.

2. LSI Optimization: Incorporate LSI terms from the [[KEYPHRASES-KEYWORDS]] list when writing content as often as needed while maintaining context relevance. E.g., instead of saying “//INSERT YOUR TERM//” use the term “//INSERT TERM VARIATION//” or “//INSERT TERM VARIATION//” from the [[KEYPHRASES-KEYWORDS]] list.

3. Stay True to the Main Topic: The main topic of this article is “//INSERT ARTICLE NAME//“.

4. Aim for Conversational Style: Just like a good teacher who engages students through conversation, your content should foster a two-way interaction. Use personal pronouns like ‘you’ and ‘I’ to establish a direct connection with the reader.

5. Pose Questions: Incorporate questions to stimulate curiosity and provoke thought. This encourages the reader to ponder and engage more deeply with the content.

6.Brevity is Key: Keep paragraphs short, concise, and to the point. Avoid long, tedious blocks of text that can overwhelm or bore the reader.

7. Simplicity Over Complexity: Use simple, clear language that’s easily understandable. You don’t need complex vocabulary to be effective. Approachable language broadens your content’s appeal.

8. Be Intriguing Yet Accessible: While the content must be interesting, ensure it’s also conversational. Avoid falling into the trap of being interesting without being engaging. Remember, even the most fascinating content can be overlooked if it doesn’t connect with the reader conversationally.
```

SEO titles and meta description prompt:
```
Please give me top 10 SEO optimized Titles and Meta descriptions for the keyword phrase “INSERT KEYWORD” and use the following criteria:

Up to 12 words and 70 characters long

< 8th-grade reading level

Clear and concise

Skimmable

Give me some variations targeting specific emotions like intellectual, empathetic, and spiritual

Title and meta description have to include the key phrase “INSERT KEYWORD”

Goal is to increase the article CTR on GoogleGrade the Titles and Meta descriptions on a scale of 1-10 based on clickability and relevance in a table. Add a third column that averages the two scores together.

Below is the table of contents of this article.

[INSERT OUTLINE]
```
