# Technology Stack

This document describes the full "Technology Stack"
we use for dwyl products and services (clients).

_If **anything** is **unclear** or you have **any questions** please_
[***ask***](https://github.com/dwyl/technology-stack/issues).

## Why?

It's ~~good~~ _essential_ to be _unambiguous_
about the technology we use for our work.

## What?


# "PETE" Stack

"PETE" is an acronym<sup>1</sup> for the following elements:

+ **Phoenix** is a Web Application Framework that does not compromise
on speed, reliability or maintainability!
Phoenix is the "_successor_"
to the incredibly popular "Ruby-on-Rails" framework.
Built _from scratch_ by highly experienced engineers
who worked on/with Rails. It _solves_
all of the speed/socket/scaling/concurrency, issues
people felt when building/using Rails apps.
The list of ***benefits*** Phoenix has over
(_vertually every_) other Web Frameworks is _extensive_.<br />
Please see:
[github.com/dwyl/learn-phoenix-framework#our-**top-10-reasons**-why-phoenix](https://github.com/dwyl/learn-phoenix-framework#our-top-10-reasons-why-phoenix) <br />

+ **Elixir** is the _functional_ programming language used to
build using the Phoenix framework. Elixir is a _beautiful_ language
written _from scratch_ to be ***friendly, concise and efficient***.
***Yes***, Elixir not a "_popular_" as JavaScript, Java, C# or PHP,
but its' adoption is growing rapidly and most importantly its'
what many _experienced_ developers are gravitating towards and
described as their ["most wanted"]()
Also a language's popularity has more
to do with the intellectual inertia people/companies have because
they allow existing (_legacy_) codebases to dictate future development;
i.e.
[***sunk cost bias***](http://www.investopedia.com/terms/s/sunk-cost-trap.asp).
see: [github.com/dwyl/learn-elixir#key-advantages](https://github.com/dwyl/learn-elixir#**key-advantages**)

+ **Tachyons** is the most _sane_ way of creating a _beatiful_ web app UI
that can _easily_ be extended by a team of people
without fear of one person's change "_breaking_" another feature.
Unlike "_traditional_" CSS which - _as it's name implies_ - encourages
"_cascading_" of styles, Tachyons makes the style of each component _specific_
and _local_ to that component.
see: https://github.com/dwyl/learn-tachyons

+ **Elm** is a front-end developer's _dream_
made _reality_ by a community of unbelievably
brilliant and dedicated developers. <br />
While Elm is
[***incredibly fast***](http://elm-lang.org/blog/blazing-fast-html-round-two)
the _reason_ we love elm is _nothing_ to do
with "_benchmarks_" and everything to do
with the _experience_ of writing/reading/maintaining
an app built with elm; _that experience is like
a **reassuring hug** from a loved one_.
Elm has [**_considerably_ better performance**](http://elm-lang.org/blog/blazing-fast-html-round-two)
than similar/alternative front-end frameworks
e.g: Angular, Ember, React, Vue.js etc.
so _hopefully_ the "performance" discussion can "_go away_"!
When you discover elm, things that used
to be _difficult_ or "_error-prone_" become easy and ***reliable***.
See: [github.com/dwyl/learn-elm#why](https://github.com/dwyl/learn-elm#**why**)

<br />
<sup>1</sup><small>Thanks to [**Jimmy Ruts**](https://github.com/dwyl/technology-stack/issues/37#issuecomment-278282619)
for _coining_ the "PETE" acronym. He's the guy we go to for _naming_
and other
["***hard things***"!](https://twitter.com/codinghorror/status/506010907021828096)
;-)</small>

## Database?

The _reason_ we do not _specify_ our Database in the "PETE" Acronym is
that Phoenix allows us to use **_any_ Relational Database**.

By _abstracting_ the data layer using "Ecto" the application is "_decoupled_"
from the database. <br />
This means that if a client _asks_ us to deploy to MySQL or
Microsoft SQL Server <br />
(_e.g. because they already have in-house capability
  for maintaining one of these databases_) <br />
we can easily accommodate that without re-writing _any_ of the Phoenix app!

### We _Prefer_ PostgreSQL (Postgres)

![postgresql logo](https://cloud.githubusercontent.com/assets/194400/22939394/6cc00918-f2d6-11e6-8400-77886d70b520.png)


Our "_standard_" (_preference_) @dwyl is for Postgres. <br />
Postgres is the most "_mature_" Open Source Relational Database.


>_**Many** well-known/successful apps rely
on Postgres as their `main` database_. <br />
_**NOT** that you should adopt a particular technology
based on who `else` is using it, <br />
but it's **good to know** that **plenty** of teams
are getting **excellent results** with PostgreSQL!
<br />
See:_ [List of Organizations Using PostgreSQL](https://github.com/dwyl/learn-postgresql/issues/31)


We have used MySQL, MS SQL Server, Oracle and Aurora; all
[RDBMS](https://en.wikipedia.org/wiki/Relational_database_management_system)
have their pros/cons. <br />
The ***reason*** we like/use Postgres is because the ***community***
is _superb_. There is a great "_bank_" of _answered_ questions on
[StackOverflow](http://stackoverflow.com/questions/tagged/postgresql)
and new questions get answered _fast_.

> If we were to _consider_ an alternative to SQL, we
would use RethinkDB:
https://rethinkdb.com <br />
But we are _relieved_ that the Phoenix team
is _focussed_ on PostgreSQL because that _eliminates_ <br />
the "ambiguity" or "discussion" of "_which database_" to use!
Postgres is a _fantastic_ "_general purpose_" <br />
store that has a _rich_ ("_structured_") query language
that lets you JOIN data!! <br />
Also, now that [Citus DB is Open Source](https://www.citusdata.com/blog/2016/03/24/citus-unforks-goes-open-source)
we _know_ that Postgres can _easily_ handle billions of writes per day!


<br /> <br />

# Node.js Stack

<!-- We refer to our Node.js Stack as "Classic". -->
We have deployed our Node.js stack for many clients
and internal apps and achieved great results! <br />
It works _really_ well and we have not had any issues with "_performance_"
or "_scaling_" using AWS, and there's no "_reason_" to "_rewrite_"
any of our _existing_ projects to _any_ other "_stack_".
See: "tl;dr" section if you _interested_ in ***why*** we decided to "_evolve_".

## Overview

The following diagram is an overview of our Node.js stack:  

![dwyl-stack-with-postgres](https://cloud.githubusercontent.com/assets/194400/18927934/e5a9d0a4-85b5-11e6-9c59-4d5052d09053.png)

> <small>Note: To edit/improve this diagram: https://github.com/dwyl/technology-stack/issues/1 </small>

We have produced a ***complete beginners guide*** for *each* of the components in our stack. (see below)

## Open Source Projects We Use

### For Us *By* Us

We ***craft code*** to [***scratch our own itch***](https://github.com/dwyl/start-here#our-approach-scratching-your-own-itch) and ***everything*** we do is ***always Open Source***

| Project | Used For | Build Status | Test Coverage | Dependency Status | Tutorial |
| --------|----------|:-----:|:--------:|:------------:|-------|
| [**env2**](https://github.com/dwyl/env2) | Loading Environment Variables | [![Build Status](https://travis-ci.org/dwyl/env2.svg?branch=master)](https://travis-ci.org/dwyl/env2) | [![Test Coverage](https://img.shields.io/codecov/c/github/dwyl/env2.svg?maxAge=2592000)](https://codecov.io/github/dwyl/env2?branch=master) | [![dependencies Status](https://david-dm.org/dwyl/env2/status.svg)](https://david-dm.org/dwyl/env2) | [learn-environment-variables](https://github.com/dwyl/learn-environment-variables) |
| [**esta**](https://github.com/dwyl/esta) | ElasticSearch CRUD | [![Build Status](https://travis-ci.org/dwyl/esta.svg?branch=master)](https://travis-ci.org/dwyl/esta) | [![Test Coverage](https://img.shields.io/codecov/c/github/dwyl/esta.svg?maxAge=2592000)](https://codecov.io/github/dwyl/esta?branch=master) | [![dependencies Status](https://david-dm.org/dwyl/esta/status.svg)](https://david-dm.org/dwyl/esta) | [learn-elasticsearch](https://github.com/dwyl/learn-elasticsearch) |
| [**goodparts**](https://github.com/dwyl/goodparts) | Consistent Code (Linting & Style) | [![Build Status](https://travis-ci.org/dwyl/goodparts.svg?branch=master)](https://travis-ci.org/dwyl/goodparts) | [![Test Coverage](https://img.shields.io/codecov/c/github/dwyl/goodparts.svg?maxAge=2592000)](https://codecov.io/github/dwyl/goodparts?branch=master) | [![dependencies Status](https://david-dm.org/dwyl/goodparts/status.svg)](https://david-dm.org/dwyl/goodparts) | [goodparts#why](https://github.com/dwyl/goodparts#why) |
| [**hapi-auth-jwt2**](https://github.com/dwyl/hapi-auth-jwt2) | Authentication & Sessions | [![Build Status](https://travis-ci.org/dwyl/hapi-auth-jwt2.svg?branch=master)](https://travis-ci.org/dwyl/hapi-auth-jwt2) | [![Test Coverage](https://img.shields.io/codecov/c/github/dwyl/hapi-auth-jwt2.svg?maxAge=2592000)](https://codecov.io/github/dwyl/hapi-auth-jwt2?branch=master) | [![dependencies Status](https://david-dm.org/dwyl/hapi-auth-jwt2/status.svg)](https://david-dm.org/dwyl/hapi-auth-jwt2) | [learn-json-web-tokens](https://github.com/dwyl/learn-json-web-tokens) |
| [**hapi-error**](https://github.com/dwyl/hapi-error) | Human-Friendly Error Messages | [![Build Status](https://travis-ci.org/dwyl/hapi-error.svg?branch=master)](https://travis-ci.org/dwyl/hapi-error) | [![Test Coverage](https://img.shields.io/codecov/c/github/dwyl/hapi-error.svg?maxAge=2592000)](https://codecov.io/github/dwyl/hapi-error?branch=master) | [![dependencies Status](https://david-dm.org/dwyl/hapi-error/status.svg)](https://david-dm.org/dwyl/hapi-error) | [hapi-error#why](https://github.com/dwyl/hapi-error#why) |
| [**hapi-login**](https://github.com/dwyl/hapi-login) | User Login | [![Build Status](https://travis-ci.org/dwyl/hapi-login.svg?branch=master)](https://travis-ci.org/dwyl/hapi-login) | [![Test Coverage](https://img.shields.io/codecov/c/github/dwyl/hapi-login.svg?maxAge=2592000)](https://codecov.io/github/dwyl/hapi-login?branch=master) | [![dependencies Status](https://david-dm.org/dwyl/hapi-login/status.svg)](https://david-dm.org/dwyl/hapi-login) | [learn-hapi](https://github.com/dwyl/learn-hapi) |
| [**hapi-postgres-connection**](https://github.com/dwyl/hapi-postgres-connection) | Postgres Connection Pooling | [![Build Status](https://travis-ci.org/dwyl/hapi-postgres-connection.svg?branch=master)](https://travis-ci.org/dwyl/hapi-postgres-connection) | [![Test Coverage](https://img.shields.io/codecov/c/github/dwyl/hapi-postgres-connection.svg?maxAge=2592000)](https://codecov.io/github/dwyl/hapi-postgres-connection?branch=master) | [![dependencies Status](https://david-dm.org/dwyl/hapi-postgres-connection/status.svg)](https://david-dm.org/dwyl/hapi-postgres-connection) | [learn-postgresql](https://github.com/dwyl/learn-postgresql) |
| [**hapi-redis-connection**](https://github.com/dwyl/hapi-redis-connection) | Simplify Redis Connection | [![Build Status](https://travis-ci.org/dwyl/hapi-redis-connection.svg?branch=master)](https://travis-ci.org/dwyl/hapi-redis-connection) | [![Test Coverage](https://img.shields.io/codecov/c/github/dwyl/hapi-redis-connection.svg?maxAge=2592000)](https://codecov.io/github/dwyl/hapi-redis-connection?branch=master) | [![dependencies Status](https://david-dm.org/dwyl/hapi-redis-connection/status.svg)](https://david-dm.org/dwyl/hapi-redis-connection) | [learn-redis](https://github.com/dwyl/learn-redis) |
| [**hapi-register**](https://github.com/dwyl/hapi-register) | User Registration | [![Build Status](https://travis-ci.org/dwyl/hapi-register.svg?branch=master)](https://travis-ci.org/dwyl/hapi-register) | [![Test Coverage](https://img.shields.io/codecov/c/github/dwyl/hapi-register.svg?maxAge=2592000)](https://codecov.io/github/dwyl/hapi-register?branch=master) | [![dependencies Status](https://david-dm.org/dwyl/hapi-register/status.svg)](https://david-dm.org/dwyl/hapi-register) | [learn-hapi](https://github.com/dwyl/learn-hapi) |
| [**hapi-riot**](https://github.com/dwyl/hapi-riot) | Server-side (Fast) Rendering of Riot Tags | [![Build Status](https://travis-ci.org/dwyl/hapi-riot.svg?branch=master)](https://travis-ci.org/dwyl/hapi-riot) | [![Test Coverage](https://img.shields.io/codecov/c/github/dwyl/hapi-riot.svg?maxAge=2592000)](https://codecov.io/github/dwyl/hapi-riot?branch=master) | [![dependencies Status](https://david-dm.org/dwyl/hapi-riot/status.svg)](https://david-dm.org/dwyl/hapi-riot) | [learn-riot](https://github.com/dwyl/learn-riot) |

> <small>Note: to update this table, use the script: `generate_dependency_table.js`</small>

### Dependencies <small>(*projects built by people we trust*)</small>

+ **Node.js** - the most popular JavaScript runtime for easily building fast,
~~scalable~~ simple network applications. Lightweight and efficient, perfect for
data-intensive real-time apps. http://nodejs.org/
+ **Hapi.js** - A rich web framework for building applications and services.
https://github.com/dwyl/learn-hapi
+ **Socket.io** - a JavaScript library for realtime web applications.
It enables realtime, bi-directional communication between web clients and
server. Socket.io lets us send data to/from everyone connected to our app(s)
without having to refresh the web page. http://socket.io/
+ **Riot.js** - is the most ***light-weight*** user-interface (UI) framework
available which is compatible with IE 8/9 and has good
server-side rendering (*which means pages load faster for slow devices like budget smart phones*).
see: https://github.com/dwyl/learn-riot
+ **Redis** - the most popular *in-memory* data store which is *essential*  
for building the ***fastest possible*** apps.
read more: https://github.com/dwyl/learn-redis
+ **ElasticSearch** - the most feature-rich search engine. we use
it to find things fast. Learn more: https://github.com/dwyl/learn-elasticsearch


### Development Dependencies

We *carefully* select and only use *well-maintained* "*pure*" JavaScript modules
in our development toolchain:

+ **Tape** for testing: https://github.com/dwyl/learn-tape
+ **Istanbul** for Code Coverage: https://github.com/dwyl/learn-istanbul
+ **Pre-commit** for ensuring all commits pass strict quality checks before being pushed to GitHub. see: https://github.com/dwyl/learn-pre-commit
+ **GoodParts** "_linting_" and checking code style is _consistent_:
https://github.com/dwyl/goodparts
+ **CodeCov** for *detailed* test/code coverage stats
https://github.com/dwyl/learn-istanbul#tracking-coverage-as-a-service
+ **CodeClimate** for tracking code quality:
https://github.com/dwyl/learn-codeclimate

### Continuous Integration

We use and *recommend* Travis-CI for Continuous Integration (CI).
If you or anyone on your team are *new* to Travis-CI,
checkout our beginners guide: https://github.com/dwyl/learn-travis

<br /> <br /> <br /> <br />


## tl;dr

There is _no shortage_ of options available for
Technology Stack: https://www.google.co.uk/search?q=technology+stack&tbm=isch
How did we _arrive_ at the conclusion that "PETE"
was "_the **one**_" for us?

### *Contextualising* Technology Adoption (Mini History Lesson)

In 2006 _nobody_ was making/buying "smart" mobile phones
with glass touch screens that ran "apps" ...
in [January 2007 Steve Jobs introduced the iPhone](https://www.youtube.com/results?search_query=Steve+Jobs+iPhone+Introduction+2007)
and _litterally_ changed the industry!

![Steve Jobs introduces iphone](https://cloud.githubusercontent.com/assets/194400/22934275/4bc76090-f2c6-11e6-9b90-91226e39ea09.png)

The dominant/incumbent devices maker **Nokia**
(_which had_ [***49% market share in 2007***](http://www.bbc.co.uk/news/technology-23947212))
_mocked_ Apple's lack of features, poor battery life and high price.
By 2013 Nokia had 3% Market Share and was sold off "for parts" to Microsoft
while Apple was the [most valuable company](https://www.statista.com/statistics/263264/top-companies-in-the-world-by-market-value/)
on the planet!

> _Many **people still buy** "**feature phones**"
(the polite name a device that does not have any
  "smart" functionality!) <br />
but few people can **convincingly** argue that the **reason**
they **don't have** a smart phone is because they **don't want** one; <br />
[**over 90% 16-24 year olds own a smart phone**](https://www.ofcom.org.uk/about-ofcom/latest/media/media-releases/2015/cmr-uk-2015) ...
ask someone in their 20's if they would go "**back**"
to using a non-smart phone <br />
and see what they say ... "**No Way**!!" they laugh uncomfortably and
admit that: "**My Smartphone is my Life**!" <br />
We feel **exactly** the same about "**old technology**".
Sure the "**old way still works**",
but if you can **inexpensively switch** <br />
to something **demonstrably better** in **every dimension**,
why would you stick with the "feature phone" of web frameworks...?_

We are not _suggesting_ that _everyone_
is going to _suddenly_ flock to the "PETE" stack
the way people adopted smart phones.
This is merely an _illustration_ that when a technology
has a _specific_ advantage to it's users the adoption _can_ be fast.

In the case of programming languages or application frameworks,
moving one framework to another is a _much_ more difficult decision.

But one thing is for _sure_ we are going to use the "_smart phone_"
even if other people insist on using the

<!--
### Availabilility Bias

When we started using Node.js in 2010 _almost nobody_ was using it.
In fact there were _many_ blog posts & tweets asserting that
using JavaScript "on the server" was a "***terrible idea***".
At the time
But
The reason we aren't using Node.js for any new projects
-->

### But Phoenix Uses Node.js for Static Asset Compilation ...

***Yes***, if you are using the (http://brunch.io/)
"_static asset compilation_".
We _aren't_ using it for our project(s) because our only
"_static assets_" are the Elm files which we compile using `elm-compiler`.
The [`elm` compiler](https://github.com/elm-lang/elm-compiler)
is written in Haskell so technically we aren't writing _any_ JS
in our PETE projects.

<!--
Our _reasoning_ for
_considering_ an alternative approach was fueled
by the _maturity_ of Elixir, Phoenix and Elm!
-->

### Does it Scale?!?

If you are new to web development,
_please focus on UX and forget about "**scale**"_! <br />

> _Unless you work somewhere that
  **already** has "**millions of users**" and <br />
your team **cannot consider** anything that
does not support a million concurrent connections...!_ <br />

> _But let's face it, **most** people have [**imaginary scaling
issues**](https://twitter.com/ThePracticalDev/status/800752571497545729)
not **real** ones. <br />
discussing "scalability" before you have 10,000 paying customers is
a waste of time!!_ <br />

Stop worrying about "scalability"
and instead **focus** on building something **useful** <br />
**focus** on **User Experience** not "backend" **scalability**!

The _good_ news is that Phoenix was _does_ "***scale***" _really well_! <br />
see: http://www.phoenixframework.org/blog/the-road-to-2-million-websocket-connections

Forget about "_scaling_" until you have _made_
[***something people want***](http://paulgraham.com/good.html)
and are _paying_ for! <br />
Then _use_ the pile of cash you got from your product
to hire "_engineers_" to make it _available_ to more people!!

<br /> <br />

### _No JavaScript_ in "PETE"...?

![no-javascript](https://cloud.githubusercontent.com/assets/194400/22939705/88d3e524-f2d7-11e6-91c6-47513f6b4fa7.jpg)

This not the place to "diss" JavaScript;
_plenty_ of people have written blog posts/tweets "_ranting_"
about the
["_State of Web Development_"](https://medium.com/@wob/the-sad-state-of-web-development-1603a861d29f).
<br />
e.g: Douglas Crockford (_the authority on JS_) recently gave a presentation on
The **Post JavaScript _Apocalypse_**: https://youtu.be/6Fg3Aj9GzNw <br />
(_in which he describes all the "features" of JS that are "**unnecessary**"..._)
<br />

The **fact** is: we _only_ use JavaScript because it is the
["***Lingua Franca***"](https://en.wikipedia.org/wiki/Lingua_franca)
that _all_ web browsers "_understand_".<br />
It's _definately_ not because it's a "_better_" language than Python or Lisp;
we write JS out of _necessity_ not by _choice_. <br />


With Elm we no longer _need_ to write our Client-side code in JS,
we can write in a beautiful/functional language <br />
and "_compile_" it to JS for running in Browsers.
The JS that is produced by the Elm compiler
is almost _always_ more efficient/faster <br />
than "_hand-written_" JS,
so _why_ would we waste our _time_ with writing JavaScript...?!

> _If you aren't `.ready()` to try something (way) **more productive**
than **JavaScript**, `.then` please just **ignore** `this`! <br />
We have written this "Technology Stack" description for **ourselves**
and not because we want to "**convince**" anyone. <br />
But ... we wanted to put down our thoughts
in `case` anyone is
["**on the fence**"](https://en.wikipedia.org/wiki/Sitting_on_the_fence)!
If you're in any doubt, ***Just Do it***._

![just-do-it-nike-log](https://cloud.githubusercontent.com/assets/194400/22940322/63db1308-f2d9-11e6-8d84-e024b00e37a4.png)

### What About _Full Stack JavaScript_?

We still think that "***Full Stack JavaScript***"
is a ***compelling proposition***
_especially_ for people who are just starting out!
If you are learning programming and want a "_quick start_"
try Meteor.js!!
