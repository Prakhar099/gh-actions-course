
1. YAML Structure:
YAML files consist of key-value pairs, lists, and nested structures. Here's a basic structure example:
Special characters in YAML have specific meanings and uses within the language. Here's a breakdown of the characters you mentioned and their typical uses or roles within YAML:
key1: value1
key2: 
  - item1
  - item2
key3:
  subkey1: subvalue1
  subkey2: subvalue2

Key-Value Pairs: key1: value1 assigns value1 to key1.
Lists: key2: followed by - item1 and - item2 creates a list under key2.
Nested Structures: key3: with subkey1 and subkey2 nested under it.

Indentation:
YAML uses indentation to indicate structure, with each level indented by two spaces. For example:
key:
  subkey1:
    - item1
    - item2
  subkey2: value
 Scalars and Types:
YAML supports various data types:
 Comments:
Comments in YAML start with # and continue to the end of the line:
Scalars: Strings ("quoted" or unquoted), numbers (42), booleans (true/false), null (null).
4. Comments:
Comments in YAML start with # and continue to the end of the line:
# This is a comment
key: value  # Comment after a line

5. Special Characters:
Certain characters like :, {, }, [, ], &, *, #, -, !, > have special meanings in YAML. To include such characters as plain text, use quotes (' or ") around the value.

6. YAML in GitHub Actions:
In GitHub Actions workflows, YAML is used to define jobs and steps:
name: CI Pipeline

on:
  push:
    branches:
      - main

jobs:
  build:
    runs-on: ubuntu-latest

    steps:
      - name: Checkout repository
        uses: actions/checkout@v2

      - name: Set up Node.js
        uses: actions/setup-node@v2
        with:
          node-version: '14'

      - name: Install dependencies
        run: npm install

      - name: Build project
        run: npm run build

Collections: Lists (- item1, - item2), maps (key: value pairs), and combinations (key: [item1, item2]).

Colon (:): Used to separate keys from values in key-value pairs.

Left Curly Brace ({) and Right Curly Brace (}): Not directly used in YAML; they are typically used in data structures or expressions within other programming languages.

Left Square Bracket ([) and Right Square Bracket (]): Used to denote lists or arrays in YAML.

Ampersand (&): Used for anchors in YAML, which are references to nodes within the document. Anchors allow you to duplicate nodes or refer to them elsewhere.

Asterisk (*): Used for aliases in YAML, referencing an anchor to reuse its content at the alias location.

Hash/Pound (#): Used to start comments in YAML, providing explanatory notes that are ignored during parsing.

Hyphen/Minus (-): Used to denote elements of a list in YAML or as a prefix for negative numbers.

Exclamation Mark (!): Has various uses, including specifying YAML tags (e.g., !str for a string) or as part of the !include directive for file inclusion.

Greater Than Sign (>): Used for block scalar style in YAML, allowing multiline strings with control over line breaks.


