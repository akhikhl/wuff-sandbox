Here we demonstrate how to build multiple repositories in the same project, using category configurations.

Category configuration is a property of category object, allowing to bind one or more features to the category:

```groovy
configurations {
  c1 { transitive = false }
}

dependencies {
  c1 project(':feature1')
  c1 project(':feature2')
}

wuff {
  repository('myrepository1') {
    // ...
    category('categoryA') {
      // ...
      configuration = 'c1' // categoryA contains feature1 and feature2
    }
  }
}
```

