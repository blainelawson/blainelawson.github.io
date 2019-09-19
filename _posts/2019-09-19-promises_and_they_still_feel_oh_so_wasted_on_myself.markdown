---
layout: post
title:      "Promises, and they still feel oh so wasted on myself"
date:       2019-09-19 19:36:59 +0000
permalink:  promises_and_they_still_feel_oh_so_wasted_on_myself
---


So what exactly is  a promise in JavaScript?

A promise essentially exists as a placeholder, or proxy, for a value which is likely to be unknown when the promise is created--and this doesn't necessarily mean anything unless you realize why a promise is necessary. A promise is necessary as when an *asynchronous* request is made to another server. Perhaps this request is made to a backend we've created, or perhaps it's a third-party API endpoint for retrieving info from Spotify. You wouldn't want your page to render to the user before the relavant data has arrived, right? 'Cause this kind of action is going to take some time--more time than we want--so a promise is returned until the actual response we're looking for can be processed, sent through the interwebs, and arrive at our front-end's front porch.

While we're waiting, this placehold--the promise--exists with a *pending* state, which is neither fulfilled nor rejected. There are two other states that are actually more helpful that we'll end up with, on is *fulfilled*, meaning that the task at hand has actually been completed; the other, far more disappointing state is *rejected*, which will obviously ruin your day. Whether you the promise ends up as fulfilled or rejected, the promise is considered *settled* at this point.

With Redux, we use Thunk middleware to handle asynchronous actions, so you don't actually get to see the word promise used. However, the example provided by those guys at MDN show that you can use a promise anywhere you'd like to setup an asynchronous call. Their explanation is as follows:

```const myFirstPromise = new Promise((resolve, reject) => {
  // do something asynchronous which eventually calls either:
  //
  //   resolve(someValue); // fulfilled
  // or
  //   reject("failure reason"); // rejected
});```

Note the `resolve` and `reject` arguments in the Promise callback. Here, `resolve` should mean "fulfilled." You simply want to return the feedback from this Promis function to your parent function and you'll have successfully  implemented a promise. Like so:

```const myFirstPromise = new Promise((resolve, reject) => {
  // do something asynchronous which eventually calls either:
  //
  //   resolve(someValue); // fulfilled
  // or
  //   reject("failure reason"); // rejected
});```
