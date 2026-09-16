# Glossary

Five terms. Not because five is a magic number, but because five is honest about how much anyone's actually agreed on so far.

Each entry follows the same shape: a plain definition, and a note on what it keeps getting confused with. If you don't see a worked example, that's the next thing worth arguing about.

---

### Chunk

A segment of source text split up for embedding and retrieval, small enough to embed with some semantic coherence, large enough to still mean something read on its own.

**Watch out for:** "chunk" gets used for both the piece as it was split and the piece as it was retrieved, and those aren't always the same size, boundary, or even the same text once overlap and reranking get involved. If you mean one specifically, say which.

### Grounding

The property of a generated answer being traceable to a specific, identifiable passage in the source corpus, not merely to a source document.

**Distinguished from:** *citation*, which can legitimately point at a whole document. Grounding can't get away with that. If your system says "grounded" and means "the source document is roughly relevant," it's not grounded, it's citing.

### Evidence

A piece of retrieved content being treated as support for an answer. Retrieved and relevant, not verified and true.

**Watch out for:** "evidence" quietly turning into a synonym for "fact" somewhere in the pipeline. It isn't one. Evidence can be wrong, outdated, or contradicted by other evidence, that's the whole reason ranking it matters.

### Authority

How much a given source deserves to be trusted, independent of how well it happens to match the query.

**Watch out for:** conflating authority with relevance. A source can be a near-perfect semantic match for the question and still be garbage. Those are two different axes, and most systems only score one of them.

### Freshness

How current a piece of content is relative to when the thing it describes was true, not just when it was published or last touched.

**Watch out for:** a newly published document summarizing old information isn't fresh in any sense that matters. Publish date and freshness are correlated, not the same thing.
