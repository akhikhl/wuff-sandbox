Here we demonstrate, how feature properties can be configured in build.gradle.

Notes:

1. All feature properties are fields of the class [EclipseFeatureExtension](https://github.com/akhikhl/wuff/blob/master/libs/wuff-plugin/src/main/groovy/org/akhikhl/wuff/EclipseFeatureExtension.groovy).

2. All feature properties are optional. When they are omitted, Wuff still generates the feature with reasonable defaults.

3. The only required part is dependencies. Feature must include at least one dependency. If there are no dependencies, Wuff does not generate the feature (should we give warning message in such case?).
