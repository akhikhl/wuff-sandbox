Here we demonstrate how to include eclipse-plugin projects into the feature.

Notes:

1. The generated eclipse plugins are located in directories `"${buildDir}/libs"` of their projects.

2. The generated feature is located in directory `"${buildDir}/feature-output"`.

3. Wuff correctly determines the build sequence: first it builds the plugins, then the feature.

