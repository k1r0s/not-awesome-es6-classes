# Not Awesome: ES6 Classes

A curated list of resources on why ES6 (aka ES2015) classes are NOT awesome

Reverse-inspired by all of the awesome lists on GitHub, like [Awesome](https://github.com/sindresorhus/awesome), [Awesome Awesomeness](https://github.com/bayandin/awesome-awesomeness), [Awesome JavaScript](https://github.com/sorrycc/awesome-javascript), [Awesome React](https://github.com/enaqx/awesome-react), [Awesome Go](https://github.com/avelino/awesome-go), [Awesome Elm](https://github.com/isRuslan/awesome-elm), etc.



## Table of Contents

- [Introduction](#introduction)
- [Too Long; Didn't Read](#tldr)
- [Reading](#reading)
- [Videos](#videos)
- [ES6 Classes in React](#es6-classes-in-react)
- [People You Should Follow](#people-you-should-follow)
- [Contribution Guidelines](#contribution-guidelines)
- [License](#license)



## Introduction

While ES6 brings several useful and syntactically pleasing new features to JavaScript, there are many people in the JS community who feel that adding class syntax to the language was a mistake. I share this sentiment, but I have encountered quite a few programmers in the wild who don't agree or simply don't seem to understand why some of us have this opinion. So, I wanted to create an online reference where people could come to learn specifically about this issue and why they __might not actually need__ class syntax in JavaScript.



## TLDR

`DISCLAIMER: This is an opinionated summary of the core points made throughout the linked content. I am only providing this as a convenience for people who requested it. If you're looking for technical depth, skip this section. Please, take the time to dive into the content before drawing any conclusions.`

- JavaScript is a class-free, object-oriented, & functional programming language. It eschews [classical inheritance](https://en.wikipedia.org/wiki/Class-based_programming) in favor of [prototypal inheritance](https://en.wikipedia.org/wiki/Prototype-based_programming). Although it is possible to emulate classical inheritance patterns in JS, classical inheritance is not built directly into the language, and many people believe prototypal inheritance to be a more flexible and freeing paradigm due to its less rigid nature. For more, first, read [this](http://www.crockford.com/javascript/inheritance.html). Then, read [this](http://javascript.crockford.com/prototypal.html).
- The ES6 class syntax, constructors, the `new` keyword, etc. are ideas taken from the classical inheritance model to make programmers coming from languages like C++, Java, C#, etc. more comfortable and do not really belong in JavaScript. ES6 class syntax is essentially syntactic sugar that will end up obfuscating the true nature of JavaScript and confusing the next generation of programmers learning it.
- While prototypal inheritance is very powerful in its own right, it is important to know that there is a growing movement among developers, both within and outside of the JS community (Ex: [Composition in Golang](https://talks.golang.org/2012/splash.article#TOC_15.)), to shift away from inheritance in favor of object composition. 
- Whether you choose to use prototypal inheritance, composition, or some combination of the two, you should __consider__ using factory functions, object literals, prototypes, Object.create(), Object.assign(), etc. while avoiding ES6 classes, constructors, and the `new` keyword altogether.

> If a feature is sometimes dangerous, and there is a better option, then always use the better option. 
> &mdash; Douglas Crockford



## Reading

#### Articles & Blog Posts

- [10 Interview Questions Every JavaScript Developer Should Know](https://medium.com/javascript-scene/10-interview-questions-every-javascript-developer-should-know-6fa6bdf5ad95)
- [Common Misconceptions About Inheritance in JavaScript](https://medium.com/javascript-scene/common-misconceptions-about-inheritance-in-javascript-d5d9bab29b0a)
- [Composition Over Inheritance](https://medium.com/humans-create-software/composition-over-inheritance-cb6f88070205)
- [Constructors Are Bad for JavaScript](https://tsherif.wordpress.com/2013/08/04/constructors-are-bad-for-javascript/)
- [Delegation vs Inheritance in JavaScript](https://javascriptweblog.wordpress.com/2010/12/22/delegation-vs-inheritance-in-javascript)
- [Factory Functions in JavaScript](https://medium.com/humans-create-software/factory-functions-in-javascript-video-d38e49802555)
- [How to Fix the ES6 `class` Keyword](https://medium.com/javascript-scene/how-to-fix-the-es6-class-keyword-2d42bb3f4caf)
- [Inside the Dev Team Death Spiral](https://medium.com/javascript-scene/inside-the-dev-team-death-spiral-6a7ea255467b)
- [Introducing the Stamp Specification -- Move Over, `class`: Composable Factory Functions Are Here](https://medium.com/javascript-scene/introducing-the-stamp-specification-77f8911c2fee)
- [Javascript OO Without Constructors](http://tobyho.com/2012/10/21/javascript-OO-without-constructors/)
- [JS Objects -- Part 1: Inherited a Mess](http://davidwalsh.name/javascript-objects)
- [JS Objects -- Part 2: Distractions](http://davidwalsh.name/javascript-objects-distractions)
- [JS Objects -- Part 3: De"construct"ion](http://davidwalsh.name/javascript-objects-deconstruction)
- [Myth: JavaScript Needs Classes](http://www.2ality.com/2011/11/javascript-classes.html)
- [Prototypal Inheritance in JavaScript (Douglas Crockford)](http://javascript.crockford.com/prototypal.html)
- [The Many Talents of JavaScript for Generalizing Role Oriented Programming Approaches Like Traits and Mixins](http://peterseliger.blogspot.de/2014/04/the-many-talents-of-javascript.html#the-many-talents-of-javascript)
- [The Two Pillars of JavaScript -- Part 1: How to Escape the 7th Circle of Hell](https://medium.com/javascript-scene/the-two-pillars-of-javascript-ee6f3281e7f3)
- [The Open Minded Explorer’s Guide to Object Composition](https://medium.com/javascript-scene/the-open-minded-explorer-s-guide-to-object-composition-88fe68961bed)
- [Think Twice About ES6 Classes](http://christianalfoni.github.io/javascript/2015/01/01/think-twice-about-classes.html)
- [Web Reflection: Better JavaScript Classes](http://webreflection.blogspot.com/2010/01/better-javascript-classes.html)
- [Web Reflection: \[ES5\] Classes As Descriptor Objects](http://webreflection.blogspot.com/2010/01/es5-es5-classes-as-descriptor-objects.html)
- [We Don’t Need a Standard for Single Inheritance. Single Inheritance Taxonomies Are an Anti-Pattern.](https://medium.com/@_ericelliott/we-don-t-need-a-standard-for-single-inheritance-single-inheritance-taxonomies-are-an-anti-pattern-5d58ad7107d0)

#### Books

- [Design Patterns: Elements of Reusable Object-Oriented Software](http://www.amazon.com/gp/product/0201633612)
- [JavaScript: The Good Parts](http://shop.oreilly.com/product/9780596517748.do)
- [Programming JavaScript Applications](http://shop.oreilly.com/product/0636920033141.do)
- [You Don't Know JS](https://github.com/getify/You-Dont-Know-JS)
    - [You Don't Know JS: Up & Going](http://shop.oreilly.com/product/0636920039303.do)
    - [You Don't Know JS: Scope & Closures](http://shop.oreilly.com/product/0636920026327.do)
    - [You Don't Know JS: this & Object Prototypes](http://shop.oreilly.com/product/0636920033738.do)
    - [You Don't Know JS: Types & Grammar](http://shop.oreilly.com/product/0636920033745.do)
    - [You Don't Know JS: Async & Performance](http://shop.oreilly.com/product/0636920033752.do)
    - [You Don't Know JS: ES6 & Beyond](http://shop.oreilly.com/product/0636920033769.do)



## Videos

- [Ashley Williams: If You Wish to Learn ES6/2015 From Scratch, You Must First Invent the Universe](https://www.youtube.com/watch?v=DN4yLZB1vUQ)
- [Atmosphere 2013: "JavaScript, the Real Bad Parts" John Paul (Conde Nast)](https://www.youtube.com/watch?v=j1arKpV1wlg)
- [Composition Over Inheritance](https://www.youtube.com/watch?v=wfMtDGfHWpA)
- [Douglas Crockford: The Better Parts - JSConfUY 2014](https://www.youtube.com/watch?v=bo36MrBfTk4)
- [Factory Functions in JavaScript](https://www.youtube.com/watch?v=ImwrezYhw4w)
- [Fluent 2013 - Eric Elliott, "Classical Inheritance is Obsolete: How to Think in Prototypal OO"](https://www.youtube.com/watch?v=lKCCZTUx0sI)
- [Nordic.js 2014 • Douglas Crockford - The Better Parts](https://www.youtube.com/watch?v=PSGEjv3Tqo0)
- [Source Decoded: Composition vs. Inheritance](https://www.youtube.com/watch?v=dYUZiJEy0JE)
- [Source Decoded 3: Javascript -- Prototypes, Prototypal Inheritance Done Right](https://www.youtube.com/watch?v=Yvf_kUBZmXg)



## ES6 Classes in React
#### A Reasonable, Limited Approach to Using ES6 Class Syntax in React

Dan Abramov (creator of [react-hot-loader](https://github.com/gaearon/react-hot-loader), [react-dnd](https://github.com/gaearon/react-dnd), [redux](https://github.com/rackt/redux), and [redux-devtools](https://github.com/gaearon/redux-devtools)) has written an article on how to approach the use of ES6 classes in React in a limited & controlled way:

[How to Use Classes and Sleep at Night](https://medium.com/@dan_abramov/how-to-use-classes-and-sleep-at-night-9af8de78ccb4)

I'm __not convinced that using ES6 class syntax in this fashion is the best long term solution for React__, and you should __be aware of the__: __React.createClass()__, __[react-stampit](https://github.com/stampit-org/react-stampit)__, and __pure (stateless) functions__. However, Dan has established a solid, __reasonable set of guidelines__ to follow in the meantime. So, if you feel that you __must use ES6 classes__ to create React components, please __follow his lead__:

__Key Points__
- Resist making classes your public API.
- Don’t inherit more than once.
- Don’t expect people to use your classes.
- Learn functional programming.

__Recommendations__
- You can use class in your JS if you don’t inherit twice and don’t use super.
- Prefer to write React components as pure functions when possible.
- Use ES6 classes for components if you need the state or lifecycle hooks.
- In this case, you may only extend React.Component directly.
- Give your feedback to the React team on the functional [state](https://github.com/reactjs/react-future/tree/master/07%20-%20Returning%20State) [proposals](https://github.com/reactjs/react-future/tree/master/09%20-%20Reduce%20State).

With that said, we should think about why needing to use `class` and `extends` in such a limited fashion, in order to establish sane & maintainable practices for the specific purpose of creating a React Component (through 1-level deep inheritance), is necessary in the first place. It probably means that there should be a better solution and/or a better syntactical approach to solving this problem. I’d like to see a syntax focusing on what the conceptual thing actually is, a __Component__ rather than a __class__… For example, why was __createClass()__ not originally named __createComponent()__?

Also, read Dan's previous article on composition:

[Mixins Are Dead. Long Live Composition](https://medium.com/@dan_abramov/mixins-are-dead-long-live-higher-order-components-94a0d2f9e750)



## People You Should Follow

- Dan Abramov
    - GitHub: [gaeron](https://github.com/gaearon)
    - Medium: [@dan_abramov](https://medium.com/@dan_abramov)
    - Twitter: [@dan_abramov](https://twitter.com/dan_abramov)
- Douglas Crockford
    - GitHub: [douglascrockford](https://github.com/douglascrockford)
    - Website: [Douglas Crockford's Wrrrld Wide Web](http://www.crockford.com/)
- Eric Elliott
    - GitHub: [ericelliott](https://github.com/ericelliott)
    - Medium: [@_ericelliott](https://medium.com/@_ericelliott) & [JavaScript Scene](https://medium.com/javascript-scene)
    - Twitter: [@_ericelliott](https://twitter.com/@_ericelliott)
- Kyle Simpson
    - GitHub: [getify](https://github.com/getify)
    - Medium: [@getify](https://medium.com/@getify)
    - Twitter: [@getify](https://twitter.com/@getify)
- Mattias P Johansson
    - GitHub: [mpj](https://github.com/mpj)
    - Medium: [@mpjme](https://medium.com/@mpjme)
    - Twitter: [@mpjme](https://twitter.com/@mpjme)
    - YouTube Channel: [mpjme](https://www.youtube.com/channel/UCO1cgjhGzsSYb1rsB4bFe4Q)



## Contribution Guidelines

Please, ensure your pull request adheres to the following guidelines:

- Search previous suggestions before making a new one, as yours may be a duplicate.
- Make an individual pull request for each suggestion.
- Titles should be [capitalized](http://grammar.yourdictionary.com/capitalization/rules-for-capitalization-in-titles.html).
- Use the following format: `[Content Title](content link)`
- New categories or improvements to the existing categorization are welcome. I would like to add a Tutorials/Examples section at some point. Feel free to get started on that if you have the time.
- The pull request and commit should have clear and useful titles.
- Each section's list, after your addition, should be sorted alphabetically.



## License

[![Creative Commons License](http://i.creativecommons.org/l/by/4.0/88x31.png)](http://creativecommons.org/licenses/by/4.0/)

This work is licensed under a [Creative Commons Attribution 4.0 International License](http://creativecommons.org/licenses/by/4.0/).
