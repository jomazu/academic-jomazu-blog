---
# Course title, summary, and position.
linktitle: About Erlang and Elixir
summary: Why Erlang and Elixir.
weight: 4

# Page metadata.
title: Overview
date: "2019-10-01T00:00:00Z"
lastmod: "2019-10-01T00:00:00Z"
draft: false  # Is this a draft? true/false
toc: true  # Show table of contents? true/false
type: docs  # Do not modify.

# Add menu entry to sidebar.
# - name: Declare this menu item as a parent with ID `name`.
# - weight: Position of link in menu.
menu:
  elixir_fundamentals:
    name: Overview
    weight: 4
---

<br>
## About Erlang
[Erlang](https://www.erlang.org/) is a general-purpose development platform for building scalable and reliable systems that constantly provide service with little or no downtime.

>Conceived in the mid-1980s by [Ericsson](https://www.ericsson.com/en/news/2018/5/erlang-celebrates-20-years-as-open-source), a Swedish telecom giant, Erlang was driven by the needs of the company's own telecom systems, where properties like reliability, responsiveness, scalability, and constant availability were imperative (Juric, 2019, p. 1). 

The development of Erlang was led by [Joe Armstrong](https://en.wikipedia.org/wiki/Joe_Armstrong_(programmer)), [Robert Virding](https://codesync.global/speaker/robert-virding/) and [Mike Williams](https://codesync.global/speaker/mike-williams/) at the Ericsson Computer Science Labs.

As mentioned, Erlang was specifically created to support the development of highly available systems - working 24/7 without any downtime. To do so, the system had to address the following challenges:

- `Fault-tolerance` - keep working when something unforeseen happens.
- `Scalability` - handle any possible load, including the ability to respond to load increases by adding more hardware resources without any software intervention or a system restart.
- `Distribution` - scale horizontally by adding more machines without interruption.
- `Responsiveness` - always be reasonably fast and responsive.
- `Live update` - push new versions of software without restarting any servers.

Erlang provides the tools to address these challenges - that's what it was built for. 

<br>
## Erlang Concurrency
At the heart and sould of Erlang systems is concurrency. 

<br>
## References

Juric, S. (2019). Elixir in action (2nd ed.). Shelter Island, NY: Manning Publications.
