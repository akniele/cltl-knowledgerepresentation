# cltl-knowledgerepresentation

A knowledge representation service (aka Leolani's Brain). This service expects structures data and outputs an RDF graph.

### Description

This package contains the necessary functionality for creating an RDF episodic knowledge graph. It features:

- Representation of experiences and their context
- Storing of learned facts, their mentions/references, and the perspectives expressed
- Querying of the graph as a way of accessing memories created during previous experiences
- Typing of incoming information through querying of external knowledge sources like DBpedia and Wikidata
- Location reasoning for guessing where a new experience is taking place, based on previous locations
- Thoughts and drives that arise from new information added to the graph. For example
    - conflicts resulting from learned facts,
    - curiosity based on knowledge gaps,
    - generalization via shared characteristics across people or objects
- Trust calculation of agents as sources of information. The trust value is based on:
    - the number of interaction with this agent,
    - the number of new content the agent has provided,
    - the number of conflicting information it has provided

## Installation

This repository uses Python >= 3.7

Be sure to run in a virtual python environment (e.g. conda, venv, mkvirtualenv, etc.)

### Prerequisites

1. In the root directory of this repo run

    ```python
    pip install -e .
    python -c "import nltk; nltk.download('wordnet')"
    ```

2. Additionally, you need to install [GraphDB Free](http://graphdb.ontotext.com/) with a repository named `sandbox`. You
   will need to launch this before running the package.

### Examples

Please take a look at the example scripts provided to get an idea on how to run and use this package. For these example
scripts, you need a repository on GraphDB called `sandbox`. To run any example script you first have to launch GraphDB,
and you can run them.

Change your current directory to `./examples/` and run some examples (e.g. `python brain_base_cases.py`)

## To Do

- Fix logging