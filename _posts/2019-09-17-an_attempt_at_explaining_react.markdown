---
layout: post
title:      "An Attempt at Explaining React"
date:       2019-09-17 15:46:48 +0000
permalink:  an_attempt_at_explaining_react
---


React is a fun ride. You don't have to worry about the everything on the screen updating, if your state has updated, your components will update as well as the natural reaction. But what is "state?" What is a component?

From my perspective, React is fully modular--pretty much like all programming--and the best place to begin is that a component is the bit of code in charge of rendering content to the screen. Now, we can apply other tasks within a component, like conditionals, but a component's main job is establishing a connection to you the user. Some components are called containers, and their responsibilities are really only different in that they typicallly are in charge of rendering other components.

Now a component can have attributes of its very own, but it can also have attributes that are provided from a parent container. These attributes are either props or state attributes. If you look at these attributes individually, they can be the same exact thing. That is, a state attribute can be a function like holdMyBeer(), and a prop can be an identical function holdMyBeer(). In fact, they can even refer to the same function--but that might be confusing. We really want state attributes to be involving an interchange between the user and the application whereas props are primarily used to pass information between components.

It's actually a great environment in which to work. You can build out applications rather quickly. My next blog, I'll be talking about connecting a React app to Redux, which is a method of having a state stored in the background, kind of like a backbone from which to collect data, functions, we just have to "connect" to it.
