---
layout: post
title:      "Redux Can Be A Devil"
date:       2019-09-17 16:52:55 +0000
permalink:  redux_can_be_a_devil
---


Redux is hard. At least... It's a hard concept to grasp initially, as it separates a lot of the tasks that are done within a React component into other a bunch of other different pieces.

First, I think it's appropriate to talk about THE STORE, because that's essentially the entire reason Redux exists. Redux exists to keep a repository of data--of your choosing--always at the ready for access. This is of course, alongside the normal rules of React where data is kept in a state in a component and can only be passed down to children components as props, should such communication of information be desired. So any component that one should want access to data in the store, you simply "connect" the component to the store using a line of code like this:

```
defaul export connect(mapStateToProps, mapDispatchToProps)([ComponentName]) 
```

That connect function's first argument, mapStateToProps, is  essentially a function that will take whatever state information is kept in THE STORE and passes it to your React component as props. From there, you can just access that bit of data (or function) by saying props.soandso or this.props.soandso--depending on whether you are using a functional component or a class component. Special note here: if you're using a functional component, you must go another step further to pass those state objects in by passing them in as arguments when declaring your component. Another helpful thing to know here, is that your STORE can have an awful lot of data in it, so you're going to have to tell mapStateToProps which particular data you're wanting to use in it.

What I personally wasn't familiar with when I started learning Redux was "dispatching," "actions," and "reducers." If you're like me, you'd have to admit these don't really have an intuitive feel to them. I like to start backwards here with "reducers." Reducers singular purpose is to update the STORE with whatever data you're wanting to put in, update, or delete (think the CUD, of CRUD). That's it, that's all. So essentially, a reducer takes the original state from your Redux STORE, **as well as whatever the deuce you want to do with it**--which most often requires that bit of new data--and makes the necessary changes to the Redux STORE. Now, keep in mind, this isn't making any changes whatsoever to any database you might have on the backend.

So as to that **whatever the deuce you want to do with it**, that's called an "action" and we pull it in the reducer as `action.type`.

Now actions are typically put in another file, separate from the reducer, for one reason is single-responsibility. You can also do a lot more with actions than just define what you want the reducer to do and what data you're sending. You can also accomplish front-end logic and execute fetch requests because sometimes you just want to make your STORE reflect a backend database and visa versa.

The last thing we haven't talked about is dispatching, and that's simply the process of getting your action and payload (the data you want to update the state with) over to the reducer to handle.

So I think that's pretty much the basics of it, as far as I understand. You or the app requests the store to be changed by dispatching an action which includes a type of action and the information with which it should update (the payload) to the reducer, and it updates THE STORE.


