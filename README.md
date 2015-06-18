# Maths Concept Graph

The idea is to build a graph whose vertices are words in (common) use in mathematics with two words connected by an edge if there is a context in which the words are interchangeable.  Ideally, the context should not be too esoteric.

The main file is a `dot` file suitable for feeding into Graphviz to create the graph.  Or at least, it is the core of a `dot` file consisting of the node and edge declarations.

The format is straightforward: a node declaration looks like:

~~~
vector [label="Vector"];
~~~

So it starts with the node name, which should be a lowercased, no spaces version of the word (which could be a phrase, or word with adjective, hence the no spaces rule in this part).  The `label` is the real version of the word which will be displayed in the graph.  The line ends with a semi-colon.

The node declaration section should be kept in alphabetical order to make it easier to avoid duplicates.

The edges look like:

~~~
point -- vector;
~~~

So this is using the node name.  The order doesn't matter as the edges are not directed.  To make searching easier, let's make the convention that the alphabetically first name goes first.

Please contribute.  When you make an addition, please add the context(s) where the equivalence(s) hold as part of the commit message.
