---
layout: post
title:      "JS Is a Doozy. Thank the Gods for Google."
date:       2019-08-14 10:43:15 -0400
permalink:  js_is_a_doozy_thank_the_gods_for_google
---


Can't figure it out? Keep googling it. JS is a mess, so someone has definitely been in your shoes before. The upside is that person has also had to ask the interweb hivemind for help, which means you can find the answer to your problem. The truth is out there. 

The best place to go for documentation on JavaScript is obviously Mozilla Developer Network (MDN), but I found one the place I like to peruse the most is W3 Schools at www.w3schools.com. W3 Schools provides a space where you can not only get examples on how code works, but you have a safe space to manipulate those examples at the same time.  If you're just getting started with JavaScript and wanting to poke around with the code, starting from https://www.w3schools.com/js/js_examples.asp is a fantastic idea! The way JS deals with Dates is pretty weird--without getting really into it--you can scroll down the examples page to JavaScript Dates, click on "Use Date() to display today's date and time," and experiment with how the date function works.

You'll see this on the left

```
<!DOCTYPE html>
<html>
<body>

<h2>JavaScript new Date()</h2>

<p id="demo"></p>

<script>
var d = new Date();
document.getElementById("demo").innerHTML = d;
</script>

</body>
</html>
```

and the results will be to the right, if you click on the green run button at the top of the screen. As you can see with JavaScript, a variable set to equal a new Date() will equal the moment in time that function is ran. Start experimenting with it by say, putting a number in the parenthesis and weird things start happening. 

Want to know what the devil is going on? I honestly wouldn't go back and sift through W3 Schools to find out, I'd go straight back to Google and search for "JavaScript Date function." Now you have some options here, you can see what W3 Schools has to offer--which when I check, the initial description isn't really what I'm looking for, it doesn't really tell me WHY what's happening in the parenthesis is happening. So I'll click on the MDN documentation site and see what they have to say, which is:

> Creates a JavaScript Date instance that represents a single moment in time in a platform-independent format. Date objects contain a Number that represents milliseconds since 1 January 1970 UTC.
> 

Now we have our answer. 

As you can see, MDN here has it's own tool you can use to experiment with the code. Often, however, I like to jump from one site to the next because some site present answers I'm looking for in a more simplistic way like W3 Schools. Sites like MDN are going to have the formal documentation and get really in depth, and sometimes I'm just not ready for all of that information. 

And sometimes sites don't have the answers to my questions at all, or the way it's presented doesn't really help me with my specific problem. Which is why I love google for being able to often lead me in the right direction if I straight up ask the specific question I have, like, "How do I find a date one year ago from today in JavaScript?" (I got used to typing in my internet searches like this when my friend Jeeves was still around, and I still do it today)

So go on.. try it.

The last source I really rely on (occasionally I'll find what I'm looking for on Medium or little known blog sites like Learn.co) is Stack Overflow. Stack Overflow is where developers of abilities spanning the spectrum come to ask for assistance and provide answers. This is truly where the answer to your personal question has probably already been asked and has probably already been answered. 

The first two search responses to our question are"How to determine one year from now in Javascript - Stack Overflow" and "Find out the previous year date from current date in javascript - Stac...." Now I'm betting you we could probably extrapolate how to find a year ago from now from the the first search response if we really needed to, but for now, the second response looks like the one we want.

I think it's important when Googling to have an open mind to results that may not look like the exact match to your quandry, but might have the answers within if you just think about it for a second.

With the answers you get on Stack Overflow, sometimes its best to open up the console and test out the responses for yourself before implementing them directly to your own code. It's also a good idea to see the comments others have made on the answers: Are they deprecated? Have they worked for others? How many upvotes has this response been given versus others? Does this code have any vulnerabilties?

The thing with coding is that you will always be searching for an answer. Troubleshooting seems to be the job almost in its entirety. Knowing there are resources out there that can help and knowing HOW to use them will speed along your own personal journey, and knowing is half the battle(?)



