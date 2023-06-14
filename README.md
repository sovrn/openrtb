Google OpenRTB Libraries - SOVRN fork
----------------------------------------------------------------------

This library supports the OpenRTB specification and providing
bindings for all protobuf-supported languages.

See our [wiki](https://github.com/google/openrtb/wiki) to get started!
Use the Github issue tracker for bugs, RFEs or any support. Check the
[changelog](CHANGELOG.md) for detailed release notes.


WHEN TO ARCHIVE THE REPO
----------------------------------------------------------------------

This fork exists only because [the original google protobuf](https://github.com/google/openrtb/blob/76961915396c842cf0a0940e9bfdbaee997cba3e/openrtb-core/src/main/protobuf/openrtb.proto) doesn't support 
- the `site.content.data` field which is in the Open RTB standard.
- custom No Bid reason codes for the Trade Desk
  ```
  TTD_ADS_TXT_AUTH_VIOLATION = 12;
  TTD_INCOMPLETE_SUPPLY_CHAIN = 16;
  TTD_BLOCKED_SUPPLY_CHAIN_NODE = 17;
  TTD_BLOCKED_PUBLISHER = 500;
  TTD_BLOCKED_SITE = 501;
  TTD_NO_MATCHING_DEAL = 502;
  TTD_FLOOR_TOO_HIGH = 503;
  ```

As soon as it's not the case, please use the original library and archive this repo.  


BUILDING NOTES
----------------------------------------------------------------------

You need: JDK 8, Maven 3.2, Protocol buffers (protoc) 3.5.1.
Building is supported from the command line with Maven and
from any IDE that can load Maven projects.

On Eclipse, the latest m2e is recommended but it can't run the code
generation step, so you need to run a "mvn install" from the command
line after checkout or after any mvn clean.

ARTIFACT NOTES
----------------------------------------------------------------------

Currently, there is no CI/CD pipeline for this fork as it hopefully won't change until very short period of time when it is removed. 
Please, publish the artifact manually.