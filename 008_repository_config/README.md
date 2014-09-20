Here we demonstrate, how repository properties can be configured in build.gradle.

Notes:

1. All repository properties are fields of the class [EclipseRepository](https://github.com/akhikhl/wuff/blob/master/libs/wuff-plugin/src/main/groovy/org/akhikhl/wuff/EclipseRepository.groovy).

2. All repository properties are optional. When they are omitted, Wuff still generates the repository with reasonable defaults.

3. The only required part is dependencies. Repository must include at least one dependency (referring a feature). If there are no dependencies, Wuff does not generate the repository (should we give warning message in such case?).

