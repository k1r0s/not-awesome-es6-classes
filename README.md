# Not Awesome: ES6 Classes

A curated list of resources on why ES6 (aka ES2015) classes are NOT awesome

Reverse-inspired by all of the awesome lists on GitHub, like [Awesome](https://github.com/sindresorhus/awesome), [Awesome Awesomeness](https://github.com/bayandin/awesome-awesomeness), [Awesome JavaScript](https://github.com/sorrycc/awesome-javascript), [Awesome React](https://github.com/enaqx/awesome-react), [Awesome Cycle.js](https://github.com/vic/awesome-cyclejs), [Awesome Go](https://github.com/avelino/awesome-go), [Awesome Elixir](https://github.com/h4cc/awesome-elixir), [Awesome Elm](https://github.com/isRuslan/awesome-elm), etc.



## Table of Contents

- [Introduction](#introduction)
- [TL;DR](#tldr)
- [Reading](#reading)
- [Videos](#videos)
- [ES6 Classes in React](#es6-classes-in-react)
- [Don't Want to Use ES6 Classes in React?](#dont-want-to-use-es6-classes-in-react)
- [Addendum (About Functional Programming)](#addendum-about-functional-programming)
- [People You Should Follow](#people-you-should-follow)
- [Contribution Guidelines](https://github.com/joshburgess/not-awesome-es6-classes/blob/master/CONTRIBUTING.md)
- [License](https://github.com/joshburgess/not-awesome-es6-classes/blob/master/LICENSE.md)



## Introduction

While ES6 brings several useful and syntactically pleasing new features to JavaScript, there are many people in the JS community who feel that adding class syntax to the language was a mistake. I share this sentiment, but I have encountered quite a few programmers in the wild who don't agree or simply don't seem to understand why some of us have this opinion. So, I wanted to create an online reference where people could come to learn specifically about this issue and why they __might not actually need class syntax in JavaScript__.



## TL;DR

`DISCLAIMER: This is an opinionated summary of the core points made throughout the linked content. I am only providing this as a convenience for people who requested it. If you're looking for technical depth, skip this section. Please, take the time to dive into the content before drawing any conclusions.`

- JavaScript is a class-free, object-oriented, & functional programming language. It eschews [classical inheritance](https://en.wikipedia.org/wiki/Class-based_programming) in favor of [prototypal inheritance](https://en.wikipedia.org/wiki/Prototype-based_programming). Although it is possible to emulate classical inheritance patterns in JS, classical inheritance is not built directly into the language, and many people believe prototypal inheritance to be a more flexible and freeing paradigm due to its less rigid nature. For more, first, read [this](http://www.crockford.com/javascript/inheritance.html). Then, read [this](http://javascript.crockford.com/prototypal.html).
- The ES6 class syntax, constructors, the `new` keyword, etc. are ideas taken from the classical inheritance model to make programmers coming from languages like C++, Java, C#, etc. more comfortable and do not really belong in JavaScript. ES6 class syntax is essentially syntactic sugar that will end up obfuscating the true nature of JavaScript and confusing the next generation of programmers learning it.
- While prototypal inheritance is very powerful in its own right, it is important to know that there is a growing movement among developers, both within and outside of the JS community (Ex: [Composition in Golang](https://talks.golang.org/2012/splash.article#TOC_15.)), to shift away from inheritance in favor of object composition.
- Whether you choose to use prototypal inheritance, composition, or some combination of the two, you should __consider using factory functions, object literals, prototypes, Object.create(), Object.assign(), etc.__ while avoiding ES6 classes, constructors, and the `new` keyword altogether.

> If a feature is sometimes dangerous, and there is a better option, then always use the better option.
> &mdash; Douglas Crockford



## Reading

#### Articles & Blog Posts

- [10 Interview Questions Every JavaScript Developer Should Know](https://medium.com/javascript-scene/10-interview-questions-every-javascript-developer-should-know-6fa6bdf5ad95)
- [Class Teacher](https://adactio.com/journal/11012)
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
- [Prototypes Are Not Classes](http://raganwald.com/2014/01/19/prototypes-are-not-classes.html)
- [The Many Talents of JavaScript for Generalizing Role Oriented Programming Approaches Like Traits and Mixins](http://peterseliger.blogspot.de/2014/04/the-many-talents-of-javascript.html#the-many-talents-of-javascript)
- [The Two Pillars of JavaScript -- Part 1: How to Escape the 7th Circle of Hell](https://medium.com/javascript-scene/the-two-pillars-of-javascript-ee6f3281e7f3)
- [The Open Minded Explorer’s Guide to Object Composition](https://medium.com/javascript-scene/the-open-minded-explorer-s-guide-to-object-composition-88fe68961bed)
- [Think Twice About ES6 Classes](http://christianalfoni.github.io/javascript/2015/01/01/think-twice-about-classes.html)
- [Web Reflection: Better JavaScript Classes](http://webreflection.blogspot.com/2010/01/better-javascript-classes.html)
- [Web Reflection: \[ES5\] Classes As Descriptor Objects](http://webreflection.blogspot.com/2010/01/es5-es5-classes-as-descriptor-objects.html)
- [We Don’t Need a Standard for Single Inheritance. Single Inheritance Taxonomies Are an Anti-Pattern.](https://medium.com/@_ericelliott/we-don-t-need-a-standard-for-single-inheritance-single-inheritance-taxonomies-are-an-anti-pattern-5d58ad7107d0)
- [Why Prototypal Inheritance Matters](https://aaditmshah.github.io/why-prototypal-inheritance-matters/)

#### Books

- [Design Patterns: Elements of Reusable Object-Oriented Software](http://www.amazon.com/gp/product/0201633612)
- [Eloquent JavaScript](http://eloquentjavascript.net/)
- [JavaScript Allongé](https://leanpub.com/javascriptallongesix/) 
- [JavaScript: The Good Parts](http://shop.oreilly.com/product/9780596517748.do)
- [Professor Frisby's Mostly Adequate Guide to Functional Programming](https://drboolean.gitbooks.io/mostly-adequate-guide/content/)
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
- [JavaScript Air Episode 01: Learning and Developing JavaScript](https://www.youtube.com/watch?v=uDtkEEIBsz4)
- [Nordic.js 2014 • Douglas Crockford - The Better Parts](https://www.youtube.com/watch?v=PSGEjv3Tqo0)
- [Professor Frisby Introduces Composable Functional JavaScript](https://egghead.io/courses/professor-frisby-introduces-composable-functional-javascript)
- [Source Decoded: Composition vs. Inheritance](https://www.youtube.com/watch?v=dYUZiJEy0JE)
- [Source Decoded 3: Javascript -- Prototypes, Prototypal Inheritance Done Right](https://www.youtube.com/watch?v=Yvf_kUBZmXg)



## ES6 Classes in React
#### A Reasonable, Limited Approach to Using ES6 Class Syntax in React

Dan Abramov (creator of [react-hot-loader](https://github.com/gaearon/react-hot-loader), [react-dnd](https://github.com/gaearon/react-dnd), [redux](https://github.com/rackt/redux), and [redux-devtools](https://github.com/gaearon/redux-devtools)) has written an article on how to approach the use of ES6 classes in React in a limited & controlled way:

[How to Use Classes and Sleep at Night](https://medium.com/@dan_abramov/how-to-use-classes-and-sleep-at-night-9af8de78ccb4)

I'm not convinced that using ES6 class syntax in this fashion is the best long term solution for React, and you should be aware of the alternatives: __React.createClass(), [react-stamp](https://github.com/stampit-org/react-stamp), and pure (stateless) functions__. However, Dan has established a solid, __reasonable set of guidelines__ to follow in the meantime. So, __if you must use ES6 classes in React, please follow his lead__:

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

With that said, we should think about why needing to use `class` and `extends` in such a limited fashion, to establish sane & maintainable practices for the specific purpose of creating a React Component (through 1-level deep inheritance), is necessary in the first place. It probably means that there should be a better solution and/or a better syntactical approach to solving this problem. I’d like to see a syntax focusing on what the conceptual thing actually is, i.e., a __component__, not a __class__… Why was __createClass()__ not originally named __createComponent()__? Why do we think that classes are the right tool for modeling components in the first place?

Also, read Dan's previous article on composition:

[Mixins Are Dead. Long Live Composition](https://medium.com/@dan_abramov/mixins-are-dead-long-live-higher-order-components-94a0d2f9e750)

## Don't Want to Use ES6 Classes in React?

Currently, it is not all that practical to completely avoid using ES6 classes in React due to the fact that functional components lack the lifecycle methods of ES6 class components (or the deprecated `createClass` factory function). However, it is possible to avoid them by using Andrew Clark's [recompose](https://github.com/acdlite/recompose), a React utility belt for function components and higher-order components. Using recompose, you are able to use methods like `componentDidMount`, `shouldComponentUpdate`, etc. with functional components via the `lifecycle` helper utility. However, `lifecycle` currently uses React's `createClass` under the hood, and many of recompose's other API methods are implemented using classes... So, you will probably still be using them if you use recompose in your project, depending on the specific methods you are using. However, they will be abstracted away from the code __you__ are writing, which you might still find nice enough to consider.

Alternatively, if you are not 100% married to React, look into Dominic Gannaway's [Inferno](https://github.com/trueadm/inferno), which Dominic describes as "an extremely fast, React-like JavaScript library for building modern user interfaces." Although Inferno offers ES6 class style components through the optional [inferno-component](https://www.npmjs.com/package/inferno-component) package, many users find they don't need them, because the library [gives functional components access to all of the important lifecycle events](https://github.com/infernojs/inferno#functional-component-lifecycle-events). Some members of the React team have suggested that React's functional components might one day receive a similar feature, but this is not a top priority for them at the moment. If you choose to check out Inferno but still want access to the wealth of 3rd party React components out there, look into [inferno-compat](https://github.com/trueadm/inferno/tree/59fb20b106307656e04f0f153d28000da040cc70/packages/inferno-compat), a module which provides a compatibility layer that makes React-based modules work with Inferno without any code changes.

Otherwise, if you are willing to abandon React compatibility & a React-like API altogether, look into [snabbdom](https://github.com/paldepind/snabbdom), a virtual DOM library focused on simplicity, modularity, & performance. Like Inferno, Snabbdom is extremely fast and features a powerful [hooks API](https://github.com/paldepind/snabbdom#hooks). Also, if you are a fan of JSX, you can keep using it via [snabbdom-jsx](https://github.com/yelouafi/snabbdom-jsx). You may be surprised how similar what you can accomplish when using a minimal virtual DOM library is to when using a larger view library like React, especially if you are already heavily using a state container like Redux. 

## Addendum (About Functional Programming)

Since writing this not-awesome-list I've really jumped into learning functional programming core concepts/principles, and, honestly, I don't really use prototypal inheritance or object composition anymore either, because I really believe FP is the way to go. However, I do still think that if you're going to do OOP in JS, then using prototypes & the OLOO (Objects Linked to Other Objects) concept + object composition is a much better idea than emulating Java with class syntax, the constructor pattern, & inheritance. Embrace simple! OO composition is better than classical inheritance by a long shot, but functional composition is even better.

## People You Should Follow

### The People Who Initially Inspired Me to Create This Repo
- Ashley G. Williams
    - GitHub: [ashleygwilliams](https://github.com/ashleygwilliams)
    - Medium: [@ag_dubs](https://medium.com/@ag_dubs)
    - Twitter: [@ag_dubs](https://twitter.com/@ag_dubs)
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

### Awesome Functional Programming in JavaScript People
- Aldwin Vlasblom
    - GitHub: [@Avaq](https://github.com/Avaq)
- Ali Sharif
    - GitHub: [@busypeoples](https://github.com/busypeoples)
    - Medium: [@sharifsbeat](https://medium.com/@sharifsbeat)
    - Twitter: [@sharifsbeat](https://twitter.com/sharifsbeat)
- André Medeiros (aka André Staltz)
    - GitHub: [@staltz](https://github.com/staltz)
    - Twitter: [@andrestaltz](https://twitter.com/andrestaltz)
    - Website: [staltz.com](https://staltz.com/)
- Brian Cavalier
    - GitHub: [@briancavalier](https://github.com/briancavalier)
    - Twitter: [@briancavalier](https://twitter.com/briancavalier)
- Brian Lonsdorf
    - GitHub: [@DrBoolean](https://github.com/DrBoolean)
    - Medium: [@drboolean](https://medium.com/@drboolean)
    - Twitter: [@drboolean](https://twitter.com/drboolean)
- Buzz de Cafe
    - GitHub: [@buzzdecafe](https://github.com/buzzdecafe)
    - Twitter: [@buzzdecafe](https://twitter.com/buzzdecafe)
    - Website: [buzzdecafe.com](http://buzzdecafe.github.io/)
 - Christoph Hermann
    - GitHub: [@stoeffel](https://github.com/stoeffel)
    - Twitter: [@schtoeffel](https://twitter.com/schtoeffel)
- David Chambers
    - GitHub: [@davidchambers](https://github.com/davidchambers)
    - Twitter: [@davidchambers](https://twitter.com/davidchambers)
- David Chase
    - GitHub: [@davidchase](https://github.com/davidchase)
    - Twitter: [@lazyeval](https://twitter.com/lazyeval)
- Gleb Bahmutov
    - GitHub: [@bahmutov](https://github.com/bahmutov)
    - Twitter: [@bahmutov](https://twitter.com/bahmutov)
    - Website: [glebbahmutov.com](https://glebbahmutov.com/)
- Ian Hofmann-Hicks
    - GitHub: [@evilsoft](https://github.com/evilsoft)
    - Twitter: [@evilsoft](https://twitter.com/evilsoft)
    - Youtube: [TheEvilSoft](https://www.youtube.com/user/TheEvilSoft)
- James Forbes
    - GitHub: [@JAForbes](https://github.com/JAForbes)
    - Twitter: [@james_a_forbes](https://twitter.com/james_a_forbes)
    - Website: [james-forbes.com](https://james-forbes.com/?/)
- James Sinclair
    - GitHub: [@jrsinclair](https://github.com/jrsinclair)
    - Twitter: [@jrsinclair](https://twitter.com/jrsinclair)
    - Website: [jrsinclair.com](http://jrsinclair.com/)
- Jon Gold
    - GitHub: [@jongold](https://github.com/jongold)
    - Twitter: [@jongold](https://twitter.com/jongold)
- Juan Soto
    - GitHub: [@sotojuan](https://github.com/sotojuan)
- Luke Westby
    - GitHub: [@lukewestby](https://github.com/lukewestby)
    - Twitter: [@luke_dot_js](https://twitter.com/luke_dot_js)
- Reginald Braithwaite
    - GitHub: [@raganwald](https://github.com/raganwald)
    - Twitter: [@raganwald](https://twitter.com/raganwald)
    - Website: [raganwald.com](http://raganwald.com/)
- Roman Pominov
    - GitHub: [@rpominov](https://github.com/rpominov)
    - Twitter: [@rpominov](https://twitter.com/rpominov)
- Simon Friis Vindum
    - GitHub: [@paldepind](https://github.com/paldepind)
    - Twitter: [@paldepind](https://twitter.com/paldepind)
- Tom Harding
    - GitHub: [@i-am-tom](https://github.com/i-am-tom)
    - Twitter: [@am_i_tom](https://twitter.com/am_i_tom)
- Tylor Steinberger
    - Github: [@TylorS](https://github.com/TylorS)
    - Twitter: [@TylorS167](https://twitter.com/TylorS167)
- Yassine Elouafi
    - GitHub: [@yelouafi](https://github.com/yelouafi)
    - Medium: [@yelouafi](https://medium.com/@yelouafi)
    - Twitter: [@YassineElouafi2](https://twitter.com/YassineElouafi2)
