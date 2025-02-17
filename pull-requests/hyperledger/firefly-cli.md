---
layout: default
title: firefly-cli
parent: Hyperledger
grand_parent: Pull Requests
has_children: false
permalink: /pull-requests/hyperledger/firefly-cli
---

# firefly-cli <span class="fs-3 right-align">[GitHub](https://github.com/hyperledger/firefly-cli){: .btn .mr-4 }</span>


<div>
    <table>
        <tr>
            <td>
                PR <a href="https://github.com/hyperledger/firefly-cli/pull/272" class=".btn">#272</a>
            </td>
            <td>
                <b>
                    Resloves #271 info command gives more information on stack
                </b>
            </td>
        </tr>
        <tr>
            <td>
                
            </td>
            <td>
                Resolves #271  info command now output information about the stack not container.
            </td>
        </tr>
    </table>
    <div class="right-align">
        Created At 2023-10-06 06:28:47 +0000 UTC
    </div>
</div>

<div>
    <table>
        <tr>
            <td>
                PR <a href="https://github.com/hyperledger/firefly-cli/pull/270" class=".btn">#270</a>
            </td>
            <td>
                <b>
                    feature: upgrade the Fabric version to v2.5 TLS
                </b>
            </td>
        </tr>
        <tr>
            <td>
                
            </td>
            <td>
                Related to: #https://github.com/hyperledger/firefly-cli/issues/268

I've run the E2E tests locally as @nguyer mentioned:
`DOWNLOAD_CLI=false STACK_TYPE=fabric TEST_SUITE=TestFabricMultipartyE2ESuite  MULTIPARTY_ENABLED=true  ./run.sh`

--- PASS: TestFabricMultipartyE2ESuite (137.02s)
    --- PASS: TestFabricMultipartyE2ESuite/TestE2EBroadcast (3.97s)
    --- PASS: TestFabricMultipartyE2ESuite/TestE2EBroadcastBlob (34.51s)
    --- PASS: TestFabricMultipartyE2ESuite/TestE2EPrivate (3.74s)
    --- PASS: TestFabricMultipartyE2ESuite/TestE2EPrivateBlobDatatypeTagged (3.71s)
    --- PASS: TestFabricMultipartyE2ESuite/TestE2EWebhookExchange (7.61s)
    --- PASS: TestFabricMultipartyE2ESuite/TestE2EWebhookRequestReplyNoTx (4.78s)
    --- PASS: TestFabricMultipartyE2ESuite/TestStrongDatatypesBroadcast (7.58s)
    --- PASS: TestFabricMultipartyE2ESuite/TestStrongDatatypesPrivate (7.29s)
    --- PASS: TestFabricMultipartyE2ESuite/TestCustomChildIdentityBroadcasts (7.88s)
    --- PASS: TestFabricMultipartyE2ESuite/TestCustomChildIdentityPrivate (11.26s)
    --- PASS: TestFabricMultipartyE2ESuite/TestInvalidIdentityAlreadyRegistered (9.39s)
    --- PASS: TestFabricMultipartyE2ESuite/TestE2EContractEvents (2.69s)
PASS
ok  	github.com/hyperledger/firefly/test/e2e/runners	137.028s

But some changes are needed in Firefly main project also. I added those in the PR: #https://github.com/hyperledger/firefly/pull/1415
            </td>
        </tr>
    </table>
    <div class="right-align">
        Created At 2023-10-04 11:53:43 +0000 UTC
    </div>
</div>

