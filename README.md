# Not a framework

In my opinion, the JavaScript ecosystem had gotten out of hand.
One of the biggest challenges I've faced in this situation is choosing
a frontend framework based on availability of developers who understand that
framework.
A problem with this approach is that you often end up with developers
( including yourself ), who are Angular developers, React developers,
Vue.js developers, etc., etc., who have a strong understanding of the
implementation, ecosystem, and idioms of that particular framework,
but a poor understanding of the underlying principles of JavaScript
and general software engineering.

Common design patterns, state managment, performance and tooling are
offloaded to libraries over which you have very little say in the philosophy,
roadmap, and popularity ( hence availabilty of developers to hire ).

Furthermore, frontend developers often find themselves with "frontend fatigue",
trying to figure out which framework will make them more employable and which
framework will be the next big thing, without having the time to explore other
areas of good software practice ( including the fundamentals of JavaScript
and Web APIs ).

As the name of this project suggests, this is not a framework. The classes, tooling,
and philosophy are merely designed as a suggestion on how to augment the native
JavaScript and browser environments to match the functionality of modern frontend
frameworks while getting you and your team as close to the "metal" as possible,
preventing "frontend fatigue", making the hiring process about finding good developers
rather than framework specific developers, and hopefully making the process of
builing web applications fun.

Throughout the exploration of this project, I urge you to explore the
[MDN web docs](developer.mozilla.org) to dive deeper into the native behaviour
used.

## Functions of modern frontend frameworks to be matched:

Don't get me wrong, modern frontend frameworks do amazing things.
If you and a team of developers have domain knowledge pertaining to the
framework already, you can build complex applications very quickly.

With that in mind, this might be a pointless exercise in terms of affecting
choices around how to build modern frontend applications.

But let's do it anyway.

In my mind, this is the core functionality of frontend frameworks that needs to
be matched:

### Dynamically rendering data

Interpolation of scoped variables, conditional rendering, and a way of
mapping elements of an array so that each of them are represented in the
desired manner.

### Dynamically updating data

When data changes, the view should represent that change

### Routing

A way of linking between views, starting on a particular view if that's where
the user navigates to first, rendering the same data for a given url.

### Server side rendering

Many frameworks have a built in way of sending down raw HTML and CSS and then
replacing it with an interactive virtual DOM. This reduces the time to paint.
The time to interactivity remains similar.

## Functions that aren't intended to be matched:

### Complex tooling

The idea is to work with native functionality in a way that using a cli to generate
complex folder structures and dependency injection becomes unnecessary.

When it comes to compilations, some recommendations will be made around how to
handle sourcemaps, assets, compression, etc. But this will not be part of
an opinionated cli.

### Complex debugging tools

If we stick with standard functionality, we'll be able to plug in to standard
browser debugging tools.

### Automated configuration for PWA

Progressive web apps shouldn't be seen as some sort of strange witchcraft that
wizards conjur up while building frontend frameworks. I'll include some details
on how to handle this functionality when building your application.


