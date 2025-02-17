---
layout: default
title: fabric-ca
parent: Hyperledger
grand_parent: Releases
has_children: false
permalink: /releases/hyperledger/fabric-ca
---

# fabric-ca <span class="fs-3 right-align">[GitHub](https://github.com/hyperledger/fabric-ca){: .btn .mr-4 }</span>


<div>
    <table>
        <tr>
            <td colspan="2">
                <b>
                    v1.5.7
                </b>
            </td>
        </tr>
        <tr>
            <td>
                <span class="chip">
                    v1.5.7
                </span>
            </td>
            <td>
                v1.5.7 Release Notes - August 29, 2023
======================================

Improvements
------------

**SignerConfig struct now exports the RevocationHandle**

SignerConfig struct now exports the RevocationHandle.
The way the revocation handle is encoded has changed to align to what the Idemix library expects.
[#363](https://github.com/hyperledger/fabric/pull/363)

Dependencies
------------

Fabric CA v1.5.7 has been tested with the following dependencies:
- Go 1.20.5
- Ubuntu 20.04 (for Docker images)


Changes, Known Issues, and Workarounds
--------------------------------------

None.

Known Vulnerabilities
---------------------
- FABC-174 Commands can be manipulated to delete identities or affiliations

  This vulnerability can be resolved in one of two ways:

    1) Use HTTPS (TLS) so that the authorization header is not in clear text.

    2) The token generation/authentication mechanism was improved to optionally prevent
       token reuse. As of v1.4 a more secure token can be used by setting environment variable:

  FABRIC_CA_SERVER_COMPATIBILITY_MODE_V1_3=false

  However, it cannot be set to false until all clients have
  been updated to generate the more secure token and tolerate
  FABRIC_CA_SERVER_COMPATIBILITY_MODE_V1_3=false.
  The Fabric CA client has been updated in v1.4 to generate the more secure token.
  The Fabric SDKs will be updated by v2.0 timeframe to generate the more secure token,
  at which time the default for Fabric CA server will change to:
  FABRIC_CA_SERVER_COMPATIBILITY_MODE_V1_3=false

Resolved Vulnerabilities
------------------------
None.

            </td>
        </tr>
    </table>
    <a href="https://github.com/hyperledger/fabric-ca/releases/tag/v1.5.7" class=".btn">
        View on GitHub
    </a>
    <span class="right-align">
        Created At 2023-08-29 18:23:17 +0000 UTC
    </span>
</div>

