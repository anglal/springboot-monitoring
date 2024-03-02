# Introduction 
Micrometer and Prometheus

```
base-path: /aazaa
Exposes only prometheus
include: ['prometheus']
If you want to expose all endpoints
include: *
```


# Console Output

```
: Starting SpringMicrometerApplication using Java 17.0.1 
: No active profile set, falling back to default profiles: default
: Tomcat initialized with port(s): 8080 (http)
: Starting service [Tomcat]
: Starting Servlet engine: [Apache Tomcat/9.0.56]
: Initializing Spring embedded WebApplicationContext
: Root WebApplicationContext: initialization completed in 398 ms
: Exposing 1 endpoint(s) beneath base path '/aazaa'
: Tomcat started on port(s): 8080 (http) with context path ''
: Started SpringMicrometerApplication in 0.824 seconds (JVM running for 1.271)
: Initializing Spring DispatcherServlet 'dispatcherServlet'
: Initializing Servlet 'dispatcherServlet'
: Completed initialization in 0 ms

```


### Actuator
http://localhost:8080/aazaa

```json
{
"_links": {
"self": {
"href": "http://localhost:8080/aazaa",
"templated": false
},
"prometheus": {
"href": "http://localhost:8080/aazaa/prometheus",
"templated": false
}
}
}
```


# Prometheus

```
http://localhost:8080/aazaa/prometheus
```

# Get Prometheus locally using Docker

```
docker pull prom/prometheus
```

# Add prometheus.yml file in resources

# Run prometheus image 
```
docker run -p 9090:9090 -v /pathTo/resources/prometheus.yml prom/prometheus

```
# Access prometheus

```
http://localhost:9090

```

# Run Grafana Docker image

```
docker run -d --name=grafana -p 3000:3000 grafana/grafana

```
# Access Grafana

```
http://localhost:3000

```
