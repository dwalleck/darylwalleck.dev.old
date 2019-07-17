---
title: "What's in a name?: Test Types"
date: 2019-07-04T13:05:43-05:00
draft: true
---

I run into lots of hard problems every day, but there's one problem I can never
escape: naming things. Does this class name convey its purpose well? Will someone
read this function name and have no idea what validateBehaviorIsCorrect means?
If I had a magic pie chart that tracked how time I spend trying to will "good"
names into existence, the slice for naming would be at least 10-15%. Some of
those are probably me being too nit-picky, but most of the time the concern is
valid. Words matter, and if you have any desire for someone else, much less
yourself six months from now, to be able to understand your code, then spending
the time to pick class/function/variable names that provide meaningful context is
worth the investment. Now, if I could convince any group of three or more people
to agree on what "good" naming looks like, I'm sure I'd find myself a millionaire
before the year is up. Since there's no one "true" guide to naming things, we figure
out what makes the most sense to ourselves and hope that no misfits with their other
crazy ideas speak up. All joking aside, it can be a contentious problem, but finding
the line between nit-picking and standing your ground to try and get the point across
more clearly. And with that, we arrive at our topic of the day: the classifications/types of tests.

# An integration test is an integration test...except when it's not

This is where the contention could start. "But everyone knows that there's unit,
integration, and functional tests. How could anyone argue with that?". Those sentences
alone could easily start a vigorous debate that could last for hours. "Are we defining a
'unit' as one function or one 'behavior'? Integration tests are the ones where we use
mocks, right? No, that's when we integrate multiple components! But what testing
integrations between systems? No, those are system tests! Your system or my system?..."
This is somewhat of a silly example, but it's not too far from reality. Depending on the
type of application you're building or your role in a team, you may have varying opinions about
how to classify your tests. I've seen leaders within the same organization draw up
completely different diagrams for their groupings of types of tests. It can get even more
complicated if teams to try to decide who is responsible for which types of tests.
"No, don't automate that. It should be a unit test. But do we have that unit test? ...no,
but if we had a test, a developer would write it. Don't worry about it". I've watched
(and to be fair, participated in) teams grind to a halt while debating the semantics of test
classifications. But why? Nit-picky, pedantic arguments? Sometimes. However, it happens
enough that it feels like there is a misalignment between what we've seen and heard
versus the problem we're trying to solve. Let's start with a model that has seen quite a bit
of use over the last decade: the testing pyramid.

While the usual primary of testing pyramids is to describe the ratio of different test types
to another, they also leak a bit of perspective about the creator's views about the different
classifications of tests. From a quick search for "testing pyramid" on Google Images shows that
those opinions vary...a lot. Nearly everyone agrees on unit tests being the base of the pyramid,
but from there on, things are more contentious. Is the next tier of tests integration tests or
service tests? Is the top of the pyramid UI tests, system tests, or end-to-end tests? But wait,
I don't even have a UI! What about API tests? If you have the time, take a look for yourself
and scroll through a few dozen iterations. It's interesting to see how different individuals
have mapped their experiences back to a similar model. So which set of classifications is the
most "correct"? Technically, all of them. The perspective of someone testing a web application
is different from someone testing a set of microservices, which is also different from testing
a REST API for an IaaS platform. Words like integration, system, and component can take on very
different meanings based on the application architecture, outside services that it may use, and
even on how the work is distributed between teams. While I think most people can agree with what a unit test looks like, it's incredibly challenging to come up with other test
definitions that would always fit every situation. Is all hope lost? Not necessarily. If it did,
I might have already lost my mind. Here's my secret: ***the names don't matter***.

# If it walks like a functional test and talks like a functional test...

That's a bold statement, but I'll do my best to back it up with a reasonable argument. This is
one of the times when putting the "best names" practice down for a bit. "But naming is important
because it expresses intent!" Exactly! The challenge of trying to decide on classifications
is really a proxy for discussing characteristics the different types of tests should have. It
is much more productive to put naming discussions aside and talk in terms of your application
and its architecture about how different tests should behave. Part of the trick is to
**not** use the common testing terms while describing how tests need to behave, becoming almost
like the dev and test version of the game Taboo. I find that the most crucial conversations
occur around deciding when and when not to mock (both in-code mocks and live mocks of
external services). By discussing the behavior of tests, you build confidence that capabilities
that are not be tested thoroughly in one type of test will be covered in another. It also calls
out types of tests that may not work well for the given application type or architecture
and provides a chance to adjust your testing strategy accordingly. Once you've described the characteristics and behaviors of how different types of tests you need, it's then okay to
flip back on our good naming practices to pick ones that encompass your intent the best.
I find "integration" and "functional" to be two of the more problematic names due to their
loose interpretations. Pairing them up with a more meaningful descriptor like "component" or
"system" helps set the scope more clearly. That said, focus on describing tests in terms
that are the clearest and agreeable for your team. At the end of the day, they're just labels,
and if you're confident that you have enough buckets for types of tests and all the buckets
have labels, call it a win.

# A bit of sentiment as you head for the door

All joking aside, naming things is hard. You will certainly run into people in
your career who, rightfully or wrongfully so, have very different ideas about
testing in general and what the "right" types of tests are. Before jumping to
judgment or starting to correct them, remember that your experiences and theirs
with applications and projects may be wildly different. Try to connect on intent and
not labels. Instead of butting heads, you may end up hearing a story about a wildly
different set of challenges than you've previously experienced and leave with a bit
more perspective. Testing is too young of a field to have absolute or final answers.
Keep an open mind to letting your own practices and opinions evolve based on the
experience of others.

