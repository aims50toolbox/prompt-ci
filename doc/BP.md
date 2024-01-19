- [Context injection - best practices](#context-injection---best-practices)
  - [RAG is just a *workaround*](#rag-is-just-a-workaround)
  - [Selecting chunk size](#selecting-chunk-size)
  - [Number of injected chunks](#number-of-injected-chunks)
  - [Metrics and embedding models](#metrics-and-embedding-models)
  - [Injecting huge amount of data](#injecting-huge-amount-of-data)
  - [Selecting proper vector indices](#selecting-proper-vector-indices)


# Context injection - best practices

## RAG is just a *workaround*
Please be aware, that RAG is just a workaround! Please see e.g. [this](https://dev.to/maximsaplin/gpt-4-128k-context-it-is-not-big-enough-1h02) entry.

## Selecting chunk size
It is very important to keep eye on the size of the chunks in the database. Using *small chunks* results in missing information in the context prompt, since nearby text around sentences can bear meaningful information to react a specific prompt. *Big chunks* however fill the context window of the LLM. Huge models, like GPT-4 has enermous context window (128K), but smaller models, like Falcon 7B has only 2048 sized window. So compromise between huge and small chunks is an issue, and depends on the use-case. Commonly, in a plain text, a chunk can be one or two sentence long, however, different applications might require bigger windows.

## Number of injected chunks
...

## Metrics and embedding models
...

## Injecting huge amount of data
...

## Selecting proper vector indices
..