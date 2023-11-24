# Project: OpenSherlock
* Founder: [[jack park]]
* Where:  <https://opensherlock.github.io/>
* 
OpenSherlock is a third generation exploration of the capabilities augmentation space where AI-backed software interacts with humans for research and discovery.

Earlier experiments led to a project TSC (short for *The Scholar's Companion*), written in Forth  beginning in the late 1980s and culminated in the mid 1990s when the program was used in a PhD dissertation defense on the topic of process control discovery, and in another experiment to discover appropriate diving chamber protocols when the topic is anaerobic wound healing. Both projects engaged deep domain model discovery, both in terms of processes, but one in the field of polymer curing, and one strictly in the biomedical domain.

By 2010, just following a defense of a PhD thesis proposal (my own), a goal of which was to use *topic maps* technology to curate online conversations about climate change, a rethinking of the earlier TSC experiments led to a new - possibly novel - framework for machine reading and processing.

The project was originally named SolrSherlock, because it relied on the Apache Solr database. The database was subsequently changed to Elasticsearch, so the project name was generalized to OpenSherlock.  Of course, he database has since been changed to PostgreSql.
## Aspirations
Overall: an ecosystem which *federates* disparate information resources and organizes those resources in the same process.

* An ecosystem which supports  machine reading of literature and other information resources, harvesting significant claims, and organizing those claims into a topic map and other high-level software structures
* An ecosystem which supports *literature-based discovery*, where claims made in one literature domain could be connected to claims in another domain, but which have not been connected
* An ecosystem which supports *deep question answering*

## The Current Prototype
OpenSherlock is a project with many different components, including:
* A Topic Map
* A Conceptual Graph
* ASR: (Anticipatory story reader) for machine reading
* future components for question answering and more
The present codebase is that of the ASR agent, which includes sub-components for:
* Document processing
* Paragraph, Sentence, and Triple processing
* Information ingestion: reading PDF files, etc
* future components to interface with the TopicMap and Conceptual Graph

That codebase is in the OpenSherlock repo:
At this writing, the code is in such high-evolution rate that it is in private repositories; that is soon to change.
