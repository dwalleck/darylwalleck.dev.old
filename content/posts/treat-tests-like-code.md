---
title: "Treat Tests Like Code"
date: 2020-03-15T14:40:18-05:00
draft: true
---

During a somewhat heating meeting about test automation, I remember one of
my leaders blurting out "No one pays for pretty test code!". I imagine that
there are a number of people who would quietly nod to this opinion. Tests
are not product code. Technically, they're not a feature that users interact
with. However, there's subtle point being made: your test code isn't as
valuable code. Less valuable code means less investment, which ends up with
"just get it done" tests versus "tests that grow with you". I wouldn't argue
that tests should get as much development time as features, but there are some
practices that test code should share with feature code.

## Code Reviews

Code reviews are not only a great way

## Code standards

No magic strings, etc

## Practice code reuse

## Rely on community driven projects

One pitfall common with test suites is that some developers see it is an
opportunity to "do testing right" or "fix testing". In that self-righteous
light, they set off to write their own test framework that follows the
practices that they think are most important.

The downside is that no developer or tester you hire will know these tools,
and they will have to be trained from scratch, which means more ramp up time.
Some developers may also see this as a barrier to writing new tests because
it means more "work" learning something new.

As tempting as it can be to do something new, it's often best to look at
the existing landscape of libraries and frameworks before setting off on
your own. Sometimes you may have a unique problem that isn't solved by
the existing tooling, but often there's someone who's encountered the same
problem as you and built a solution. Innovation in testing shouldn't be
discouraged, but keep in mind the problem you're trying to solve. If your
team needs automated test coverage and the existing libraries and frameworks
solve your problem well enough, it's better to stand on the shoulders of
giants and get your testing done.'
:Pp[[[[[[[[[[[[[[[[]]]]]]]]]]]]]]]]

## Don't call your tests "scripts"


