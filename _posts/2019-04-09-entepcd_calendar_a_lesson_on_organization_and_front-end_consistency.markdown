---
layout: post
title:      "EntePCD Calendar: A Lesson on Organization and Front-End Consistency"
date:       2019-04-09 19:21:10 +0000
permalink:  entepcd_calendar_a_lesson_on_organization_and_front-end_consistency
---


I’ve just finished my first CLI Project with Flatiron Academy. **YOWZA**.

I can see the importance of organizing the flow of information ahead of time, perhaps in a visual way. Eons ago, in the dawn of time when languages like Pascal, C++, and QBasic were taught, flow charts were a common foundational step one learned before dabbling in the dark arts of functions, modules, and conditional statements. What ever happened to those? Are they now considered a waste of time? 

As with all things, I expect the ability to organize which calculations should go in which place, etc. will come through practice. I will, however, be on the lookout for resources that offer explanation on common conventions. As for now, Flatiron’s Avi created some lessons that were helpful in avoiding anti-patterns and refactoring my code. Here they are:

[o Video - Common Anti-Patterns in CLI Data Gem ](http://https://www.youtube.com/watch?v=cbMa87oWv08)

[o	Video- Student Example 1: Refactoring CLI Data Gem](http://https://www.youtube.com/watch?v=JEL_PXr74qQ)

[o	Video- Student Example 2: Refactoring CLI Data Gem](http://https://www.youtube.com/watch?v=Lt0oyHiKWIw)


While coding PCD Calendar, I found myself wondering if it would be best to only "open" files for use with Nokogiri once and generating new Group's from my scraper class to limit the amount of time it takes to process. Ultimately, I did, however because the calendar from pinellascountydemocrats.org leads to multiple event pages, the scraper has to open each of those URL’s to glean the details not only for the groups, but for the events themselves. When you have 20 events in a month, which means 20 URL’s to open, and that necessitates tons of time.

The most heinous aspect of putting this all together was scraping information from a website that has no consistency as far as the event or group details. While finding selectors with Nokogiri, I was surprised to find few patterns that the webpage developer used to input event information. Some details would be in a block after the event summary, which—in my opinion—should have been used more consistently. Other details were listed within the event summary itself. The tags failed to follow a consistent pattern as well. To be thorough, I found all of this to be an extremely tedious task for which to account, but it did teach me a valuable lesson on the importance of consistency when designing web pages.

