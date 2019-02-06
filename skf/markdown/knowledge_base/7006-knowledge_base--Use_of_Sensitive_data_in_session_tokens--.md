## Description:

Depending on how the token based session management is implemented, the session token may contain sensitive information which should only be read at the server. For instance, JWT by default, does not provide the confidentiality of the payload as it's transmitted Base64 encoded. Thus, anyone with access to the token can decode it and read the content of its headers and claims. Also, if the server does not enforce a signature algorithm, an attacker can undertake null cipher, key substitution and brute force on weak keys attacks and thereafter tamper token's content.  


## Solution:

Verify that stateless session tokens, which contain sensitive session data, are digitally signed or encrypted. Implement server side validation and enforcement of the digital signature ciphers.
