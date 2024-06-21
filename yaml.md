### YAML Basics

YAML, a human-readable data serialization format, is often used for configuration files and data exchange. Its structure, based on indentation with spaces, organizes data into lists, maps and objects, supporting types such as strings, numbers, data and booleans. To promote data reuse, YAML uses anchors to define blocks of data and aliases to reference them, avoiding repetition. The language offers flexibility in representing multiline strings, with styles that preserve or modify line breaks. The examples demonstrate the use of anchors and aliases to prevent data reproduction and the different styles for representing multiline strings.

```yml
# YAML Basics

YAML:
  - human-readable data serialization format
  - commonly used for:
    - configuration files
    - data exchange

Practices:
  - organization # group related data
  - indentation  # spaces not tabs, two spaces
  - comments     # short and clearly comments
  - lines        # 80-100 characters
  - long strings # use folded style (>)
  - quotes
    - quotes strings only when necessary # "unnecessary_quote"
    - quotes special characters to avoid parsing issues # "@special&characters"

Types:
  - strings    # singleline, multiline
  - numbers    # {int: 42, float: 3.14, hexa: 0xff, scifi: 1e+12, z: 3+4i}
  - timestamps # {date: 2024-02-05, time: 16:32:48, datetime: 2001-12-15T02:59:43.1Z}
  - booleans   # true/false, yes/no, on/off
  - nulls      # null, undefined
  - tags       # explicitly_typed: !!python/tuple [5, 7]

Structures:
  - list   # [item, item, ...]
  - map    # { k: v, k: v, ... }
  - object # { name: bob, age: 42, hobbies: [reading, hiking]}

DRY: # Don’t Repeat Yourself
  - anchors # & define a block
  - aliases # * refer back to the anchored content
```

Example demonstrating YAML anchors and aliases:

```yml
# Define a server configuration block with an anchor named &server_config
server: &server_config
  host: my-server.com
  port: 8080

# Use the alias *server_config to reference the defined block for web server
web_server:
  <<: *server_config

# Use the alias again (with slight modification) for the database server
database_server:
  <<: *server_config
  port: 3306
```

Example demonstrating YAML multiline strings:

```yml
# Folded Style ('>') - removes all newlines except the last
description: >
  This is a long description of my configuration 
  that spans multiple lines. It will be treated as 
  a single string with a newline at the end.

# Literal Style ('|') - preserves all newlines
long_poem: |
  Roses are red,
  Violets are blue,
  This poem is long,
  And uses literal style too.
```
