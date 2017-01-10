# Flex Java Example

A minimalist java/spring-boot example integration using Flex-API tokenization.

## Prerequisites

- [Java 8](http://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html)
- [JCE unlimited policy files](http://www.oracle.com/technetwork/java/javase/downloads/jce8-download-2133166.html)
- [Maven](https://maven.apache.org/install.html)

## Setup Instructions

1. Modify `./src/main/resources/application.properties` with the credentials created through [VISA Developer Portal](https://developer.visa.com/).

  ```properties
  vdp.api-key=_YOUR_APPLICATION_SPECIFIC_API_KEY_
  vdp.shared-secret=_YOUR_APPLICATION_SPECIFIC_SHARED_SECRET_
  ```

2. Build and run the application using maven
  ```bash
  mvn clean spring-boot:run
  ```
  This will serve the application from [https://localhost:8443](https://localhost:8443).

## Tips

- If you are having issues, checkout the full [FLEX documentation](https://developer.visa.com/products/cybersource/reference#cybersource__cybersource_flex_api).

- To change the port the application is served on, update `server.port=8443` in `application.properties`, replacing `8443` with your desired port number.

- If the application throws `java.security.InvalidKeyException: Illegal key size` you have probably not installed the [JCE unlimited policy files](http://www.oracle.com/technetwork/java/javase/downloads/jce8-download-2133166.html).

## Browser Support

- Chrome 37+
- Firefox 34+
- Edge 12+
- Opera 24+

*NB: IE11 and Safari support could be achieved through the use of polyfills for promises and Web Crypto API such as [webcrypto-shim](https://github.com/vibornoff/webcrypto-shim) and [promiz](https://github.com/Zolmeister/promiz). However, these are not included in the examples.*

## Disclaimer

This respository is provided as a learning aid for merchants wishing to integrate with the Flex API.  The code samples are not production ready and are intended for illustrative purposes only. As such, any use of these code samples in a production setting is strongly discouraged. Any usage of these code samples must comply with the license agreement as defined in `LICENSE.md` at the root level of this repository.