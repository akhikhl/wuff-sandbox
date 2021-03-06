This is the simplest example of Wuff-driven Eclipse repository.

Notes:

1. Repository generation is enabled by applying plugin 'org.akhikhl.wuff.eclipse-repository'.

2. 'java' and 'groovy' plugins are neither required nor prohibited.

3. The repository automatically includes features from special configuration 'repository' (see dependencies section).

4. 'repository' configuration is not transitive. That means: Wuff will include exactly those features you mentioned, without their dependencies. You can enable transitive dependencies by code:
  ```
  configurations.repository.transitive = true
  ```
  
5. The repository is generated by invoking `gradle build`.

6. The generated repository is located in directory `"${buildDir}/repository-output"`.

7. By default repository gets the same name and version, as gradle project. This can be changed (see further examples).

8. By default repository gets single category with the same name, as gradle project. This can be changed (see further examples).

9. Currently Wuff understands only feature projects (i.e. the projects where 'org.akhikhl.wuff.eclipse-feature' was applied) as features. File-level features are not yet supported.
