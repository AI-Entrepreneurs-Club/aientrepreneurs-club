# Project: ClaimMiner

* This is a [[projects]] file.
* Founder: [[marc-antoine parent]]

ClaimMiner was designed for [[SocietyLibrary]], to automate their efforts to map public discourse. An example of a finished map can be found [here](https://papers.societylibrary.org/papers/diablo_canyon). Map curation happens in [DebateMap](https://debatemap.app), but ClaimMiner allows identifying claims in documents to be exported to DebateMap later.

ClaimMiner's repository is currently private, but this is expected to change very soon (details below.)

## Current Functionality

1. ClaimMiner stores a set of documents (currently HTML, PDF or text) which were provided as URLs or uploaded.
2. The documents are split in paragraphs, and various embeddings can be calculated for each paragraph, allowing for semantic or text search.
3. ClaimMiner also maintains lists of text statements (claims, questions, etc.) which are not associated with documents.
4. Statements and Documents can be grouped in collections, with corresponding access rights.
5. (WIP) Statements can be assembled into arbitrary frame structures (see [[HyperKnowledge]])
6. Operations can be applied to documents and statements:
   1. Paragraph extraction (core)
   2. Embeddings (core)
   3. Claim extraction from documents (developed by [[SocietyLibrary]])
   4. Claim clustering
   5. GDELT-based search (developed by [[SocietyLibrary]])
   6. DebateMap import/export (not yet full 2-way synchronization)

## Short-term goals

I am working on abstracting the notion of operations that can be applied to documents and statements, so we can create a marketplace of add-ons, with ClaimMiner as a substrate. The ClaimMiner core will be open-sourced as soon as the SocietyLibrary components are isolated as plug-ins.

## Technology stack

* Storage in PostgreSQL, with pgvector to hold embeddings
* Backend in Python, using FastAPI and SQLAlchemy
* Integration of other technologies is work in progress: Langchain, unstructured, etc.
* Plugin architecture with pluggy
