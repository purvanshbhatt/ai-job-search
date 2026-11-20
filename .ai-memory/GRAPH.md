# Knowledge Graph

```mermaid
graph LR
  "file:documents/README.md"["documents/README.md"]:::file
  "file:s://github.com"["s://github.com"]:::file
  "session:claude-code:17785521-8b14-4c89-abb4-dbe7fee97a3f"["<command-message>setup</command-message>"]:::session
  "topic:command-message"["command-message"]:::topic
  "topic:setup"["setup"]:::topic
  "topic:command-name"["command-name"]:::topic
  "topic:keep"["keep"]:::topic
  "topic:local"["local"]:::topic
  "session:claude-code:17785521-8b14-4c89-abb4-dbe7fee97a3f" -->|touched| "file:documents/README.md"
  "session:claude-code:17785521-8b14-4c89-abb4-dbe7fee97a3f" -->|touched| "file:s://github.com"
  "session:claude-code:17785521-8b14-4c89-abb4-dbe7fee97a3f" -->|discusses| "topic:command-message"
  "session:claude-code:17785521-8b14-4c89-abb4-dbe7fee97a3f" -->|discusses| "topic:setup"
  "session:claude-code:17785521-8b14-4c89-abb4-dbe7fee97a3f" -->|discusses| "topic:command-name"
  "session:claude-code:17785521-8b14-4c89-abb4-dbe7fee97a3f" -->|discusses| "topic:keep"
  "session:claude-code:17785521-8b14-4c89-abb4-dbe7fee97a3f" -->|discusses| "topic:local"
  classDef session fill:#4a90d9,color:#fff
  classDef file fill:#7ab648,color:#fff
  classDef decision fill:#e67e22,color:#fff
  classDef topic fill:#9b59b6,color:#fff
```
