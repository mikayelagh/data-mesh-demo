# Data Mesh Demo

An example implementation of Data Mesh on top of Confluent Cloud.

### Prerequisties
* Java 8 or 11
* Gradle

### Instructions (WIP during development)

* Clone the repository locally and change directories
  ```
  git clone https://github.com/confluentinc/data-mesh-demo
  cd data-mesh-demo
  ```

* Run the web service with
   ```
   ./gradlew bootRun
   ```

  It is successful and will wait for requests when you see this:
  ```
  <==========---> 80% EXECUTING [30s]
  > :bootRun
  ```

* Use endpoint `localhost:8080` to interact with the REST API, for example with `curl` and `jq`
  ```
  curl -s localhost:8080/data-products | jq
  [
    {
      "qualifiedName": "lsrc-78xpp:.:pageviews-value:1",
      "name": "pageviews",
      "owner": "@web",
      "version": 1
    },
    {
      "qualifiedName": "lsrc-78xpp:.:users-value:1",
      "name": "users",
      "owner": "@web",
      "version": 1
    }
  ]
  ```
