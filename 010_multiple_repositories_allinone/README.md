Here we demonstrate how to build multiple repositories and features in the same project.

When repositories and features reside in the same project, it is necessary to use alternative category-to-feature binding mechanism:

```groovy
wuff {
  feature('feature1') {
    // ...
  }
  repository('myrepository1') {
    // ...
    category('category1') {
      // ...
      feature 'feature1' // this binds feature1 to category1
    }
  }
}
```
