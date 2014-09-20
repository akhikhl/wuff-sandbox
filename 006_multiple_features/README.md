Here we demonstrate how to configure multiple eclipse features in the same project.

Notes:

1. You should use "features" section for configuring multiple eclipse features.

2. "features" section has type [EclipseFeaturesExtension](https://github.com/akhikhl/wuff/blob/master/libs/wuff-plugin/src/main/groovy/org/akhikhl/wuff/EclipseFeaturesExtension.groovy) and supports a single function: 
  ```groovy
  void feature(String id = null, Closure closure)
  ```

3. Closure passed to "feature" function gets instance of [EclipseFeatureExtension](https://github.com/akhikhl/wuff/blob/master/libs/wuff-plugin/src/main/groovy/org/akhikhl/wuff/EclipseFeatureExtension.groovy) class as a delegate.

4. Separation of dependencies for multiple features can be achieved with multiple gradle configurations. The property EclipseFeatureExtension.configuration associates dependencies of gradle configuration with given feature.
