# wuff-sandbox

Hello guys,

This repo is a sandbox for incubating Wuff features.

All projects here use snapshot version of Wuff from local maven repository or from jfrog repository.

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

