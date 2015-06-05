# logging-store
[![Codacy status][codacy-image]][codacy-url]
[![Build status][travis-image]][travis-url]
[![License][license-image]][license-url]

[codacy-image]: https://www.codacy.com/project/badge/fe2c9325e1f34ecfb8dbc79012e2c719
[codacy-url]: https://www.codacy.com/public/marzelwidmer/logging-store
[travis-image]: https://img.shields.io/travis/marzelwidmer/logging-store.svg?style=flat-square
[travis-url]: https://travis-ci.org/marzelwidmer/logging-store
[license-image]: http://img.shields.io/:license-Apache2.0-blue.svg?style=flat-square
[license-url]: LICENSE



# POST a Log Message
```
curl -X POST  -H "Accept: Application/json" -H "Content-Type: application/json" http://localhost:8080/log -d '{
  "clientApplikation":"SPA1",
  "clientVersion":"1.0.1",
  "correlationId": "11212",
  "debugInformation":"Hello World",
  "faultMessage":"Message Hello World",
  "faultCode":"289-36",
  "faultType":"SYSTEM_UMGEBUNG",
  "severity":"DEBUG"
}'
```

# Start App with develpment profile
```
  java -jar  --spring.profiles.active=development target/
```

# Shutdown 
```
  curl -X POST localhost:9000/shutdown
```