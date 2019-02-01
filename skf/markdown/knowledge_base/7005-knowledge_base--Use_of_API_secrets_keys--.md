## Description:

APIs static keys and secrets are widely used for authenticating the client before accepting the request in the endpoint. Even though it's  easy to implement, managing its secrets and keys is challenging. They should be securely transported from the server to the client, which is normally done in plain-text. Also, the API keys lack of granular controls and transfers the responsibility to the consumer to implement security controls for key protection. Yet, the keys can be accidently exposed and leaked in public cloud buckets and repository commits. Furthermore, the keys has no expiration, so if stolen they can used indefinetly.


## Solution:

For new implementations, API Secrets and Keys souldn't be solely relied for authentication purposes. They can be used for identification purposes in conjunction of a more robust authentication mechanis using JWT, OAuth or SAML for token based Session-Management.
