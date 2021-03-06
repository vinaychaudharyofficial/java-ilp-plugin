# Java Interledger Plugin Interface [![join the chat on gitter][gitter-image]][gitter-url] [![circle-ci][circle-image]][circle-url] [![codecov][codecov-image]][codecov-url]

[gitter-image]: https://badges.gitter.im/interledger/java.svg
[gitter-url]: https://gitter.im/interledger/java
[circle-image]: https://circleci.com/gh/interledger/java-ilp-plugin.svg?style=shield
[circle-url]: https://circleci.com/gh/interledger/java-ilp-plugin
[codecov-image]: https://codecov.io/gh/interledger/java-ilp-plugin/branch/master/graph/badge.svg
[codecov-url]: https://codecov.io/gh/interledger/java-ilp-plugin


Java implementation of the [Plugin Interface](https://github.com/interledger/rfcs/blob/master/0004-plugin-interface/0004-plugin-interface.md), typically used by ILP Connectors.

* v0.1.0-SNAPSHOT Initial commit of interfaces and abstract classes.
 
## Usage

### Requirements
This project uses Maven to manage dependencies and other aspects of the build. 
To install Maven, follow the instructions at [https://maven.apache.org/install.html](https://maven.apache.org/install.html).

### Get the code

``` sh
git clone https://github.com/interledger/java-ilp-plugin
cd java-ilp-plugin
```

### Build the Project
To build the project, execute the following command:

```bash
$ mvn clean install
```

#### Checkstyle
The project uses checkstyle to keep code style consistent. All Checkstyle checks are run by default during the build, but if you would like to run checkstyle checks, use the following command:


```bash AbstractLedgerPluginTest
$ mvn checkstyle:checkstyle
```

### Step 3: Extend
This project is meant to be extended with your own implementation. There are two concrete 
implementations of a LedgerPlugin in this project, `MockLedgerPlugin`, which is a demonstration 
implementation that simulates an underlying ledger while handling events from the underlying ledger in 
synchronous manner. 

Additionally, `QueuedMockLedgerPlugin` is a demonstration implementation that simulates an underlying ledger 
while handling events from that ledger in a a queued fashion manner. 


## Contributors
Any contribution is very much appreciated! 

[![gitter][gitter-image]][gitter-url]

## TODO
See the issues here: [https://github.com/interledger/java-ilp-plugin/issues](https://github.com/interledger/java-ilp-plugin/issues).

## License
This code is released under the Apache 2.0 License. Please see [LICENSE](LICENSE) for the full text.
