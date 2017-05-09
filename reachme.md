ReachMe
=======

Conferencing application.

Current state
=============

Source code is a bit outdated.

Long-term goals
===============

1. To have an independend (of sipX) conferencing application able to integrate with various SIP entities. 
2. Scalability. Application should be scalable horizontally by adding more servers to handle more load.

Short-term goals
================

1. Have a dockerized version for testing and development. It should be possibe to do changes
and test them locally.

2. Make statistic work. Currenlty it seems broken by design. There is an attempt to re-create
functionality of time-series database using Erlang and MongoDB, and it is easier to use existing
time-series database to handle this kind of data.

3. Make dialyzer work and applied systematically (on each pull request). Most of function
specs are in place, but I'm not sure about regular runs.

4. Have an automated functional test suite. It should be possible to make calls to ReachMe, and
check the results in terms of functionality, e.g. call gets to the queue, call is delivered to agent,
etc.