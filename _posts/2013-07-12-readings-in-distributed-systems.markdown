---
layout: post
title:  "Readings in distributed systems"
date:   2013-07-12 12:00:35 -0400
categories: distributed systems
---

_This post is a work in progress._

Inspired by a recent purchase of the [Red Book][redbook], which provides
a curated list of important papers around database systems, I've decided
to begin assembling a list of important papers in distributed systems.
Similar to the Red Book, I've broken each group of papers out into a
series of categories.

## Consensus

The problems of establishing consensus in a distributed system.

* [In Search of an Understandable Consensus Algorithm][raft] -
    Diego Ongaro, John Ousterhout - 2013
* [A Simple Totally Ordered Broadcast Protocol][zab] - Benjamin Reed,
  Flavio P. Junqueira - 2008
* [Paxos Made Live - An Engineering Perspective][paxoslive] -
    Tushar Deepak Chandra, Robert Griesemer, Joshua Redstone - 2007
* [Paxos Made Simple][paxossimple] - Leslie Lamport - 2001
* [Impossibility of Distributed Consensus with One Faulty Process][flp]
  - Michael Fischer, Nancy Lynch, Michael Patterson - 1985
* [The Byzantine Generals Problem][generals] - Leslie Lamport - 1982

#

## Consistency

Types of consistency, and practical solutions to solving ensuring atomic
operations across a set of replicas.

* [HAT, not CAP: Highly Available Transactions][hat] - Peter Bailis,
  Alan Fekete, Ali Ghodsi, Joseph M. Hellerstein, Ion Stoica - 2013
* [Linearizability: A Correctness Condition for Concurrent
  Objects][linearizability] - Maurice P. Herlihy, Jeannette M. Wing -
  1990

#

## Conflict-free data structures

Studies on data structures which do not require coordination to ensure
convergence to the correct value.

* [A Comprehensive Study of Convergent and Commutative Replicated Data
    Types][crdt1] - Mark Shapiro, Nuno Preguiça, Carlos Baquero, Marek
    Zawirski - 2011
* [A Commutative Replicated Data Type For Cooperative Editing][treedoc]
  - Nuno Preguica, Joan Manuel Marques, Marc Shapiro, Mihai Letia, 2009

#

## Distributed programming

Languages aimed towards disorderly distributed programming as well as
case studies on problems in distributed programming.

* [Logic and Lattices for Distributed Programming][blooml] - Neil Conway, William Marczak, Peter Alvaro, Joseph M. Hellerstein, David Maier - 2012
* [Dedalus: Datalog in Time and Space][dedalus] - Peter Alvaro, William R. Marczak, Neil Conway, Joseph M. Hellerstein, David Maier, Russell Sears - 2011
* [A Note On Distributed Computing][computing] - Samuel C. Kendall, Jim Waldo, Ann Wollrath, Geoff Wyant - 1994

#

## Systems

Implemented distributed systems.

* [Dynamo: Amazon’s Highly Available Key-Value Store][dynamo] -
    Giuseppe DeCandia, Deniz Hastorun, Madan Jampani, Gunavardhan
    Kakulapati, Avinash Lakshman, Alex Pilchin, Swaminathan
    Sivasubramanian, Peter Vosshall and Werner Vogels - 2007

#

I'm hoping to make this into a living document, so please submit [pull
requests][pull] or leave comments!

[pull]: https://github.com/cmeiklejohn/cmeiklejohn.github.io
[redbook]: http://www.amazon.com/Readings-Database-Systems-Joseph-Hellerstein/dp/0262693143
[raft]: https://ramcloud.stanford.edu/wiki/download/attachments/11370504/raft.pdf
[paxoslive]: http://research.google.com/pubs/pub33002.html
[dynamo]: http://www.read.seas.harvard.edu/~kohler/class/cs239-w08/decandia07dynamo.pdf
[crdt1]: http://hal.upmc.fr/docs/00/55/55/88/PDF/techreport.pdf
[hat]: http://arxiv.org/pdf/1302.0309.pdf
[linearizability]: http://cs.brown.edu/~mph/HerlihyW90/p463-herlihy.pdf
[paxossimple]: http://www.cs.utexas.edu/users/lorenzo/corsi/cs380d/past/03F/notes/paxos-simple.pdf
[generals]: http://www.cs.cornell.edu/courses/cs614/2004sp/papers/lsp82.pdf
[flp]: http://macs.citadel.edu/rudolphg/csci604/ImpossibilityofConsensus.pdf
[treedoc]: http://hal.inria.fr/docs/00/44/59/75/PDF/icdcs09-treedoc.pdf
[zab]: http://www.research.yahoo.com/pub/3274
[computing]: http://dl.acm.org/citation.cfm?id=974938
[blooml]: http://db.cs.berkeley.edu/papers/UCB-lattice-tr.pdf
[dedalus]: http://db.cs.berkeley.edu/papers/datalog2011-dedalus.pdf