# Project: HyperKnowledge

* This is a [[projects]] file.
* Founder: [[marc-antoine parent]]
* Where: [HyperKnowledge](https://hyperknowledge.org/)
* Repository: https://github.com/conversence/hyperknowledge

HyperKnowledge has been in planning for a long time, what we have now is a prototype of a fraction of planned functionality. Let us instead focus on the goals.

## Aspirations

1. A meta-model for a structured representation of ideas. Anything that can be expressed in natural language should be representable using that meta-model.
2. Idea snapshots are represented as frames. Inspired by [topic mapping](http://www.isotopicmaps.org/TMMM/tmrm.1.33.pdf), [linguistic frames](https://framenet.icsi.berkeley.edu), [conceptual graphs](http://www.jfsowa.com/cg/cg_hbook.pdf)
3. Any idea can refer to any other idea, including ideas that link other ideas. As such, idea frames form a recursive hypergraph.
4. Ideas are continuously evolving in conversations, and those conversations are represented as cross-referencing event streams.
5. As continuously evolving entities, ideas are represented by frames but are not equivalent to them. Idea references need to be continually updated.
6. Idea identity is not fixed either, as ideas may split or merge as they are evolving. Also, idea references are essentially ambiguous, as we discover new distinctions and precisions.
7. Anything that is asserted by an individual is held to be locally true in that event stream, and the federation will try to maintain a "social truth" value for the statement given how it is accepted or contested in a given community.

## The current prototype

The current prototype allows experimentations with event sourcing, as the foundation for HyperKnowledge. It gives an OpenAPI interface where one can define event streams, dynamically define schemas for events and projections, and store folding functions to maintain those projections according to the events. The system allows subscriptions to event streams, maintains the projections using the given folding functions, and makes them accessible through OpenAPI. The OpenAPI interface evolves as schemas are added.

