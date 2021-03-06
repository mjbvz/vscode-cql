# CQL support for VS Code 

## This is a language extension for the Cassandra CQL language. 

This is an extension for working with Cassandra CQL. This extension supports syntax highlighting. Table definitions found will allow intellisense to work. This extension will find symbols for tables and columns. All keywords have intellisense. There are snippets for basic CQL statements.

### Features
   - Currently Supports:
    - Syntax Highlighting
    - Brackets
    - Comments
    - Intellisense 
    - Keywords *(SELECT, ALTER, UUID, etc)*
    - Table Names* 
    - Column Names*
    - Snippets (SELECT, CREATE TABLE|KEYSPACE|TRIGGER|TYPE|INDEX, UPDATE)
    - CQL Statement Execution
    - Keybinding for CQL Statement Execution
    - Scanning for objects
    - View schema
     - Tree view
     - Static tree
 
### CQL Statement Execution
**Execute SQL Statement:**

Pressing [Shift+F5] to execute a CQL statement or pressing [F1] and then typing 'exec' to find the "Execute CQL Statement" command. In either case, if text has been highlighted that text will be sent to the configured Cassandra endpoint; if there is no text selected then the entire document will be sent to Cassandra to run. Below you will find instructions to configure the extension to connect to your Cassandra endpoint.  

### Configuration: 
If your Cassandra endpoint is at 127.0.0.1:9042 (or localhost), then there is nothing to configure. If you have a remote endpoint then you will want to set the following keys in your [user configuration](https://code.visualstudio.com/Docs/customization/userandworkspace).
- Configuration Keys
 - **cql.address** *(string)*: IPAddress or hostname of Cassandra endpoint for the Execute command. *Default is 127.0.0.1.*
 - **cql.port**: *(integer)*: Port of the Cassandra endpoint for the Execute command. *Default is 9024.*
 - **cql.scanOnStartup**: *(boolean)*: Scan the cluster in the *cql.connection* value for non-system objects at startup. *Default is false.*
 - **cql.connection** *(object)*: Connection configuraiton object. This overrides cql.address and cql.port and is the new default configuration. ***Example*** 
 `{
     "contactPoints": ["127.0.0.1"],
     "hosts": ["127.0.0.1"]
 }`
 - **cql.resultStyle** *(object)*: Configures where and how you will view results. There are two options:
  - format: *json* or *tabular*
  - location: If set to *output* results are routed to the CQL Output window instead of a pane.

### For more information
* [project on github](https://github.com/lawrencekgrant/vscode-cql)

### Shout Outs:
 - Shout out to Jacob Gardner for fixing [Issue #3](https://github.com/lawrencekgrant/vscode-cql/issues/3) with [PR #4](https://github.com/lawrencekgrant/vscode-cql/pull/4)

### Build Status
[![Build Status](https://travis-ci.org/lawrencekgrant/vscode-cql.svg?branch=master)](https://travis-ci.org/lawrencekgrant/vscode-cql)
### Have fun!