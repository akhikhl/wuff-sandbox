Here we demonstrate, how to configure feature ID.

Notes:

1. Feature ID is a unique string distinguishing one feature from another in the same project.

2. Feature ID, when specified, must be passed as a parameter to feature function:

  ```groovy
  wuff {
    feature('myfeature') { 
      // ...
    }
  }
  ```

3. Feature without explicitly specified ID gets the default ID: `project.name.replace('-', '.')`.

  ```groovy
  wuff {
    feature { 
      // ...
    }
  }
  ```

4. You can configure the same feature multiple times:

  ```groovy
  wuff {
    feature('myfeature') { 
      // ...
    }
    feature('myfeature') { 
      // still the same feature
    }
  }
  ```
  
5. Every feature jar gets the name `"${id}_${version}.jar"`. where "id" and "version" are taken from feature configuration.

