---
title: "knowledge ingest"
---
## knowledge ingest

Ingest a file/directory into a dataset

### Synopsis

Ingest a file or directory into a dataset.

## Important Note

The first time you ingest something into a dataset, the embedding function (model provider) you chose will be attached to that dataset.
After that, the client must always use that same embedding function to ingest into this dataset.
Usually, this only concerns the choice of the model, as that commonly defines the embedding dimensionality.
This is a constraint of the Vector Database and Similarity Search, as different models yield differently sized embedding vectors and also represent the semantics differently.


```
knowledge ingest [--dataset <dataset-id>] <path> [flags]
```

### Options

```
      --auto-migrate string                 Auto migrate database ($KNOW_DB_AUTO_MIGRATE) (default "true")
      --concurrency int                     Number of concurrent ingestion processes ($KNOW_INGEST_CONCURRENCY) (default 10)
  -c, --config-file string                  Path to the configuration file ($KNOW_CONFIG_FILE)
  -d, --dataset string                      Target Dataset ID ($KNOW_DATASET) (default "default")
      --dedupe-func string                  Name of the deduplication function to use ($KNOW_INGEST_DEDUPE_FUNC)
      --embedding-model-provider string     Embedding model provider ($KNOW_EMBEDDING_MODEL_PROVIDER) (default "openai")
      --err-on-unsupported-file             Error on unsupported file types ($KNOW_INGEST_ERR_ON_UNSUPPORTED_FILE)
      --flow string                         Flow name ($KNOW_FLOW)
      --flows-file string                   Path to a YAML/JSON file containing ingestion/retrieval flows ($KNOW_FLOWS_FILE) (default "blueprint:default")
  -h, --help                                help for ingest
      --ignore-extensions string            Comma-separated list of file extensions to ignore ($KNOW_INGEST_IGNORE_EXTENSIONS)
      --ignore-file string                  Path to a .gitignore style file ($KNOW_INGEST_IGNORE_FILE)
      --include-hidden                      Include hidden files and directories ($KNOW_INGEST_INCLUDE_HIDDEN)
      --index-dsn string                    Index Database Connection string (relational DB) (default "sqlite://$XDG_DATA_HOME/gptscript/knowledge/knowledge.db") ($KNOW_INDEX_DSN)
      --no-create-dataset                   Do NOT create the dataset if it doesn't exist ($KNOW_INGEST_NO_CREATE_DATASET)
      --no-recursive                        Don't recursively ingest directories ($KNOW_NO_INGEST_RECURSIVE)
      --prune                               Prune deleted files ($KNOW_INGEST_PRUNE)
      --server string                       URL of the Knowledge API Server ($KNOW_SERVER_URL)
      --textsplitter-chunk-overlap int      Textsplitter Chunk Overlap ($KNOW_TEXTSPLITTER_CHUNK_OVERLAP) (default 256)
      --textsplitter-chunk-size int         Textsplitter Chunk Size ($KNOW_TEXTSPLITTER_CHUNK_SIZE) (default 1024)
      --textsplitter-encoding-name string   Textsplitter Encoding Name ($KNOW_TEXTSPLITTER_ENCODING_NAME) (default "cl100k_base")
      --textsplitter-model-name string      Textsplitter Model Name ($KNOW_TEXTSPLITTER_MODEL_NAME) (default "gpt-4o")
      --vector-dsn string                   DSN to the vector database (default "chromem:$XDG_DATA_HOME/gptscript/knowledge/vector.db") ($KNOW_VECTOR_DSN)
```

### SEE ALSO

* [knowledge](knowledge.md)	 - 

