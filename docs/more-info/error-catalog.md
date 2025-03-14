# Snyk Error Codes
  The error codes in the table below describe the codes that you may encounter while working with the [Snyk API](../snyk-api-info/README.md) or [CLI](../snyk-cli/README.md). When errors are encountered using the API, they will also have an appropriate [HTTP status code](https://en.wikipedia.org/wiki/List_of_HTTP_status_codes). If you encounter errors without an error code, use the HTTP status code to determine the appropriate action.
  
  
---
# [Snyk](https://docs.snyk.io/introducing-snyk)
### [SNYK-0001](#snyk-0001-too-many-requests) - Too many requests
  The service has received too many requests and will be throttled.

  **HTTP Status:** [429](https://developer.mozilla.org/en-US/docs/Web/HTTP/Status/429)

  **Exit Code:** N/A

  **Help Links:**

  
### [SNYK-0002](#snyk-0002-not-implemented) - Not implemented
  The server either does not recognize the request method, or it lacks the ability to fulfil the request.

  **HTTP Status:** [501](https://developer.mozilla.org/en-US/docs/Web/HTTP/Status/501)

  **Exit Code:** N/A

  **Help Links:**

  
### [SNYK-0003](#snyk-0003-bad-request) - Bad request
  The server cannot or will not process the request due to an apparent client error (e.g. malformed request syntax, size too large, invalid request message framing, or deceptive request routing).

  **HTTP Status:** [400](https://developer.mozilla.org/en-US/docs/Web/HTTP/Status/400)

  **Exit Code:** N/A

  **Help Links:**

  
### [SNYK-004](#snyk-004-timeout-error) - Timeout error
  The server did not receive a timely response from the upstream server.

  **HTTP Status:** [504](https://developer.mozilla.org/en-US/docs/Web/HTTP/Status/504)

  **Exit Code:** N/A

  **Help Links:**

  
### [SNYK-005](#snyk-005-unauthorised-error) - Unauthorised error
  Authentication failed or has not been provided.

  **HTTP Status:** [401](https://developer.mozilla.org/en-US/docs/Web/HTTP/Status/401)

  **Exit Code:** N/A

  **Help Links:**

  
### [SNYK-9999](#snyk-9999-server-error) - Server error
  An unexpected server error was encountered.

  **HTTP Status:** [500](https://developer.mozilla.org/en-US/docs/Web/HTTP/Status/500)

  **Exit Code:** N/A

  **Help Links:**

  
---
# OpenAPI
### [SNYK-OPENAPI-001](#snyk-openapi-001-bad-request) - Bad request
  The request sent to the server is invalid or corrupt.

  **HTTP Status:** [400](https://developer.mozilla.org/en-US/docs/Web/HTTP/Status/400)

  **Exit Code:** N/A

  **Help Links:**

  
### [SNYK-OPENAPI-002](#snyk-openapi-002-forbidden) - Forbidden
  Access to the requested resource is forbidden.

  **HTTP Status:** [403](https://developer.mozilla.org/en-US/docs/Web/HTTP/Status/403)

  **Exit Code:** N/A

  **Help Links:**

  
### [SNYK-OPENAPI-003](#snyk-openapi-003-not-acceptable) - Not acceptable
  The server cannot provide a response which matches the provided accept headers.

  **HTTP Status:** [406](https://developer.mozilla.org/en-US/docs/Web/HTTP/Status/406)

  **Exit Code:** N/A

  **Help Links:**

  
### [SNYK-OPENAPI-004](#snyk-openapi-004-not-found) - Not found
  The server cannot find the requested resource.

  **HTTP Status:** [404](https://developer.mozilla.org/en-US/docs/Web/HTTP/Status/404)

  **Exit Code:** N/A

  **Help Links:**

  
### [SNYK-OPENAPI-005](#snyk-openapi-005-method-not-allowed) - Method not allowed
  The endpoint does not support the request method.

  **HTTP Status:** [405](https://developer.mozilla.org/en-US/docs/Web/HTTP/Status/405)

  **Exit Code:** N/A

  **Help Links:**

  
### [SNYK-OPENAPI-006](#snyk-openapi-006-request-entity-too-large) - Request entity too large
  The request entity exceeds server limitations.

  **HTTP Status:** [413](https://developer.mozilla.org/en-US/docs/Web/HTTP/Status/413)

  **Exit Code:** N/A

  **Help Links:**

  
### [SNYK-OPENAPI-007](#snyk-openapi-007-unauthorized) - Unauthorized
  The request lacks authentication credentials for the requested resource.

  **HTTP Status:** [401](https://developer.mozilla.org/en-US/docs/Web/HTTP/Status/401)

  **Exit Code:** N/A

  **Help Links:**

  
### [SNYK-OPENAPI-008](#snyk-openapi-008-unsupported-media-type) - Unsupported media type
  The media format of the request is not supported.

  **HTTP Status:** [415](https://developer.mozilla.org/en-US/docs/Web/HTTP/Status/415)

  **Exit Code:** N/A

  **Help Links:**

  
---
# [Open Source Languages & Package Managers](https://docs.snyk.io/products/snyk-open-source/language-and-package-manager-support)
### [SNYK-OS-0001](#snyk-os-0001-unsupported-ecosystem) - Unsupported Ecosystem
  The language or package manager is not supported.

  **HTTP Status:** [400](https://developer.mozilla.org/en-US/docs/Web/HTTP/Status/400)

  **Exit Code:** N/A

  **Help Links:**

  - [https://docs.snyk.io/products/snyk-open-source/language-and-package-manager-support](https://docs.snyk.io/products/snyk-open-source/language-and-package-manager-support)
### [SNYK-OS-0002](#snyk-os-0002-unable-to-parse-manifest-file) - Unable to parse manifest file
  The provided manifest file could not be parsed.

  **HTTP Status:** [400](https://developer.mozilla.org/en-US/docs/Web/HTTP/Status/400)

  **Exit Code:** N/A

  **Help Links:**

  
### [SNYK-OS-0003](#snyk-os-0003-lock-file-out-of-sync-with-manifest-file) - Lock file out of sync with manifest file
  Some of the dependencies that are expected to be in the lock file are missing - this usually indicates that the lock file is out of sync with the provided manifest file. Please re-sync the lock file and try again.

  **HTTP Status:** [400](https://developer.mozilla.org/en-US/docs/Web/HTTP/Status/400)

  **Exit Code:** N/A

  **Help Links:**

  
---
# Builds
### [SNYK-OS-8001](#snyk-os-8001-invalid-request) - Invalid request
  The provided request payload is not valid for the selected ecosystem. Please review the API documentation.

  **HTTP Status:** [400](https://developer.mozilla.org/en-US/docs/Web/HTTP/Status/400)

  **Exit Code:** N/A

  **Help Links:**

  - [https://apidocs.snyk.io/](https://apidocs.snyk.io/)
### [SNYK-OS-8002](#snyk-os-8002-build-environment-not-found) - Build environment not found
  The build environment for the provided context could not be found. Please ensure you have created the build environment first.

  **HTTP Status:** [404](https://developer.mozilla.org/en-US/docs/Web/HTTP/Status/404)

  **Exit Code:** N/A

  **Help Links:**

  
---
# [PURL Vulnerabilities](https://docs.snyk.io/introducing-snyk/getting-started-snyk-intel-vuln-db-access#about-the-snyk-vulnerability-database)
### [SNYK-OSSI-1040](#snyk-ossi-1040-your-organisation-is-not-authorised-to-perform-this-action) - Your organisation is not authorised to perform this action
  You likely don’t have access to the Beta. To get access, you can request access to the Beta through your account manager or team.

  **HTTP Status:** [403](https://developer.mozilla.org/en-US/docs/Web/HTTP/Status/403)

  **Exit Code:** N/A

  **Help Links:**

  
### [SNYK-OSSI-1050](#snyk-ossi-1050-authorization-request-failure) - Authorization request failure
  Unexpected error when authenticating. Please try again, and if you continue to experience issues please contact support.

  **HTTP Status:** [500](https://developer.mozilla.org/en-US/docs/Web/HTTP/Status/500)

  **Exit Code:** N/A

  **Help Links:**

  
### [SNYK-OSSI-2010](#snyk-ossi-2010-invalid-purl-has-been-provided) - Invalid PURL has been provided
  Please make sure that the purl you’ve provided is valid. Please see the Package URL specification link for further information.

  **HTTP Status:** [400](https://developer.mozilla.org/en-US/docs/Web/HTTP/Status/400)

  **Exit Code:** N/A

  **Help Links:**

  - [https://github.com/package-url/purl-spec/blob/master/PURL-SPECIFICATION.rst](https://github.com/package-url/purl-spec/blob/master/PURL-SPECIFICATION.rst)
### [SNYK-OSSI-2011](#snyk-ossi-2011-ensure-you-specify-a-namespace-in-the-purl-and-then-try-again) - Ensure you specify a namespace in the purl and then try again
  You have requested a package type which requires a namespace (eg. maven group id). Please supply the namespace in order to retrieve the package correctly.

  **HTTP Status:** [400](https://developer.mozilla.org/en-US/docs/Web/HTTP/Status/400)

  **Exit Code:** N/A

  **Help Links:**

  - [https://github.com/package-url/purl-spec/blob/master/PURL-SPECIFICATION.rst](https://github.com/package-url/purl-spec/blob/master/PURL-SPECIFICATION.rst)
### [SNYK-OSSI-2020](#snyk-ossi-2020-ecosystem-is-not-supported) - Ecosystem is not supported
  Ensure that the package type is a supported type.

  **HTTP Status:** [400](https://developer.mozilla.org/en-US/docs/Web/HTTP/Status/400)

  **Exit Code:** N/A

  **Help Links:**

  
### [SNYK-OSSI-2021](#snyk-ossi-2021-purl-components-required) - Purl components required
  Currently we require a list of components of the package url specification. The purl supplied by the user did not specify all the components which we currently require.

  **HTTP Status:** [400](https://developer.mozilla.org/en-US/docs/Web/HTTP/Status/400)

  **Exit Code:** N/A

  **Help Links:**

  
### [SNYK-OSSI-2022](#snyk-ossi-2022-you-have-submitted-a-purl-with-components-which-are-not-supported) - You have submitted a purl with components which are not supported
  Please remove the component which is not supported, and try to make the request again. The endpoint only accepts particular components.

  **HTTP Status:** [400](https://developer.mozilla.org/en-US/docs/Web/HTTP/Status/400)

  **Exit Code:** N/A

  **Help Links:**

  
### [SNYK-OSSI-2030](#snyk-ossi-2030-requested-package-not-found) - Requested package not found
  The package you’ve specified in the purl can not be found in our vulnerability database. Please check that the package name, ecosystem and version are correct and then try again.

  **HTTP Status:** [404](https://developer.mozilla.org/en-US/docs/Web/HTTP/Status/404)

  **Exit Code:** N/A

  **Help Links:**

  
### [SNYK-OSSI-2031](#snyk-ossi-2031-vulnerability-service-is-currently-not-available) - Vulnerability service is currently not available
  This issue is unexpected, and the service should recover quickly. If not, please contact support.

  **HTTP Status:** [503](https://developer.mozilla.org/en-US/docs/Web/HTTP/Status/503)

  **Exit Code:** N/A

  **Help Links:**

  
### [SNYK-OSSI-2032](#snyk-ossi-2032-this-issue-is-unexpected-and-the-service-should-recover-quickly-if-not-please-contact-support) - This issue is unexpected and the service should recover quickly if not please contact support
  An unexpected error occurred. Please try again, and if you continue to experience issues please contact support.

  **HTTP Status:** [500](https://developer.mozilla.org/en-US/docs/Web/HTTP/Status/500)

  **Exit Code:** N/A

  **Help Links:**

  
### [SNYK-OSSI-2033](#snyk-ossi-2033-this-issue-is-unexpected-and-the-service-should-recover-quickly-if-not-please-contact-support) - This issue is unexpected and the service should recover quickly if not please contact support
  An unexpected error occurred with the vulnerability service. Please try again, and if you continue to experience issues please contact support.

  **HTTP Status:** [500](https://developer.mozilla.org/en-US/docs/Web/HTTP/Status/500)

  **Exit Code:** N/A

  **Help Links:**

  
### [SNYK-OSSI-2040](#snyk-ossi-2040-an-error-was-experienced-by-the-service-when-processing-the-request) - An error was experienced by the service when processing the request
  This issue is unexpected, and the service should recover quickly. If not, please contact support.

  **HTTP Status:** [500](https://developer.mozilla.org/en-US/docs/Web/HTTP/Status/500)

  **Exit Code:** N/A

  **Help Links:**

  
### [SNYK-OSSI-2041](#snyk-ossi-2041-invalid-pagination-parameters) - Invalid pagination parameters
  Please ensure the supplied pagination limit is > 1 and <= 1000, and that the offset is >= 0.

  **HTTP Status:** [400](https://developer.mozilla.org/en-US/docs/Web/HTTP/Status/400)

  **Exit Code:** N/A

  **Help Links:**

  
---
# OpenSourceProjectIssues
### [SNYK-OSSI-OSPI-1001](#snyk-ossi-ospi-1001-invalid-request) - Invalid request
  Please check the body of your request and try again.

  **HTTP Status:** [400](https://developer.mozilla.org/en-US/docs/Web/HTTP/Status/400)

  **Exit Code:** N/A

  **Help Links:**

  
### [SNYK-OSSI-OSPI-1002](#snyk-ossi-ospi-1002-unable-to-return-valid-api-response) - Unable to return valid API response
  This should resolve, however please contact support if you continue to experience issues.

  **HTTP Status:** [500](https://developer.mozilla.org/en-US/docs/Web/HTTP/Status/500)

  **Exit Code:** N/A

  **Help Links:**

  
### [SNYK-OSSI-OSPI-2001](#snyk-ossi-ospi-2001-failed-to-process-data) - Failed to process data
  This should resolve, however please contact support if you continue to experience issues.

  **HTTP Status:** [500](https://developer.mozilla.org/en-US/docs/Web/HTTP/Status/500)

  **Exit Code:** N/A

  **Help Links:**

  
### [SNYK-OSSI-OSPI-3001](#snyk-ossi-ospi-3001-failed-to-store-issue-data) - Failed to store issue data
  Please check your inputs and try again. If you continue to experience issues please contact support.

  **HTTP Status:** [500](https://developer.mozilla.org/en-US/docs/Web/HTTP/Status/500)

  **Exit Code:** N/A

  **Help Links:**

  
### [SNYK-OSSI-OSPI-4001](#snyk-ossi-ospi-4001-internal-server-error) - Internal server error
  This issue is unexpected, and the service should recover quickly. If not, please contact support.

  **HTTP Status:** [500](https://developer.mozilla.org/en-US/docs/Web/HTTP/Status/500)

  **Exit Code:** N/A

  **Help Links:**

  
---
# Open Source Project Snapshots
### [SNYK-OSSI-OSPSS-1001](#snyk-ossi-ospss-1001-invalid-request) - Invalid request
  Please check the body of your request and try again.

  **HTTP Status:** [400](https://developer.mozilla.org/en-US/docs/Web/HTTP/Status/400)

  **Exit Code:** N/A

  **Help Links:**

  
### [SNYK-OSSI-OSPSS-1002](#snyk-ossi-ospss-1002-unable-to-return-valid-api-response) - Unable to return valid API response
  This should resolve, however please contact support if you continue to experience issues.

  **HTTP Status:** [500](https://developer.mozilla.org/en-US/docs/Web/HTTP/Status/500)

  **Exit Code:** N/A

  **Help Links:**

  
### [SNYK-OSSI-OSPSS-2001](#snyk-ossi-ospss-2001-failed-to-process-data) - Failed to process data
  This should resolve, however please contact support if you continue to experience issues.

  **HTTP Status:** [500](https://developer.mozilla.org/en-US/docs/Web/HTTP/Status/500)

  **Exit Code:** N/A

  **Help Links:**

  
### [SNYK-OSSI-OSPSS-3001](#snyk-ossi-ospss-3001-failed-to-store-snapshot-data) - Failed to store snapshot data
  Please check your inputs and try again. If you continue to experience issues please contact support.

  **HTTP Status:** [500](https://developer.mozilla.org/en-US/docs/Web/HTTP/Status/500)

  **Exit Code:** N/A

  **Help Links:**

  
### [SNYK-OSSI-OSPSS-4001](#snyk-ossi-ospss-4001-internal-server-error) - Internal server error
  This issue is unexpected, and the service should recover quickly. If not, please contact support.

  **HTTP Status:** [500](https://developer.mozilla.org/en-US/docs/Web/HTTP/Status/500)

  **Exit Code:** N/A

  **Help Links:**

  
---

Genererated at 2022-10-28T13:03:48.777Z