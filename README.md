# wuff-sandbox

This repo is a sandbox for testing incubating features of [Wuff project](https://github.com/akhikhl/wuff).

All projects represented here use snapshot version of Wuff from local maven repository or from jfrog repository.

Currently all projects in the sandbox are demonstrating one new feature of Wuff: Eclipse Feature and Repository generation. Please note that this feature is in it's infancy. Many things could be (and will be) done better, simpler or differently in a future.

Your critique, comments and test results are very much welcome.


## Usage

```
git clone git@github.com:akhikhl/wuff-sandbox.git
cd wuff-sandbox
gradle build
```

## Tight loop

You can setup "tight loop" with Wuff in order to modify Wuff sources and see effects in the sandbox:

```
git clone git@github.com:akhikhl/wuff.git
cd wuff
gradle build
cd ..
git clone git@github.com:akhikhl/wuff-sandbox.git
cd wuff-sandbox
gradle build
```

Each time you build Wuff (or just wuff-plugin), it gets installed to local maven repository, so that wuff-sandbox can immediately use modified code (without publishing to jfrog).

## How to run/study examples

Best of all - in alphabetical order. Every example is supplied with README.md, explaining the purpose, the syntax and the effects.
