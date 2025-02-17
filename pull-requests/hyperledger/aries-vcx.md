---
layout: default
title: aries-vcx
parent: Hyperledger
grand_parent: Pull Requests
has_children: false
permalink: /pull-requests/hyperledger/aries-vcx
---

# aries-vcx <span class="fs-3 right-align">[GitHub](https://github.com/hyperledger/aries-vcx){: .btn .mr-4 }</span>


<div>
    <table>
        <tr>
            <td>
                PR <a href="https://github.com/hyperledger/aries-vcx/pull/1061" class=".btn">#1061</a>
            </td>
            <td>
                <b>
                    refactor: Move agents to new root (aries) as per #1045
                </b>
            </td>
        </tr>
        <tr>
            <td>
                
            </td>
            <td>
                <nil>
            </td>
        </tr>
    </table>
    <div class="right-align">
        Created At 2023-11-13 16:35:33 +0000 UTC
    </div>
</div>

<div>
    <table>
        <tr>
            <td>
                PR <a href="https://github.com/hyperledger/aries-vcx/pull/1060" class=".btn">#1060</a>
            </td>
            <td>
                <b>
                    Cleanup logging dependencies
                </b>
            </td>
        </tr>
        <tr>
            <td>
                
            </td>
            <td>
                Incrementally addressing https://github.com/hyperledger/aries-vcx/issues/1012 (considering file reorg PR)

Outstanding:
- `libvcx_logger` should not exists, each top level crate such as `libvcx_core`, `uniffi` or backchannel shall setup env logger (or other log macro implementations) themselves.
            </td>
        </tr>
    </table>
    <div class="right-align">
        Created At 2023-11-12 22:56:11 +0000 UTC
    </div>
</div>

<div>
    <table>
        <tr>
            <td>
                PR <a href="https://github.com/hyperledger/aries-vcx/pull/1059" class=".btn">#1059</a>
            </td>
            <td>
                <b>
                    Reorganize crates
                </b>
            </td>
        </tr>
        <tr>
            <td>
                
            </td>
            <td>
                First incremental shot at https://github.com/hyperledger/aries-vcx/issues/1045

Trying to move what's not currently being worked on / shouldn't cause trouble. 
            </td>
        </tr>
    </table>
    <div class="right-align">
        Created At 2023-11-12 22:48:46 +0000 UTC
    </div>
</div>

<div>
    <table>
        <tr>
            <td>
                PR <a href="https://github.com/hyperledger/aries-vcx/pull/1058" class=".btn">#1058</a>
            </td>
            <td>
                <b>
                    Uniffi demo holder
                </b>
            </td>
        </tr>
        <tr>
            <td>
                
            </td>
            <td>
                <nil>
            </td>
        </tr>
    </table>
    <div class="right-align">
        Created At 2023-11-11 19:23:07 +0000 UTC
    </div>
</div>

<div>
    <table>
        <tr>
            <td>
                PR <a href="https://github.com/hyperledger/aries-vcx/pull/1057" class=".btn">#1057</a>
            </td>
            <td>
                <b>
                    fix(aries_vcx): make tests run in parallel
                </b>
            </td>
        </tr>
        <tr>
            <td>
                
            </td>
            <td>
                fixes #1050
            </td>
        </tr>
    </table>
    <div class="right-align">
        Created At 2023-11-10 13:16:49 +0000 UTC
    </div>
</div>

<div>
    <table>
        <tr>
            <td>
                PR <a href="https://github.com/hyperledger/aries-vcx/pull/1056" class=".btn">#1056</a>
            </td>
            <td>
                <b>
                    WIP: Refactor/mediator/mediation (use integrated aries-vcx structs)
                </b>
            </td>
        </tr>
        <tr>
            <td>
                
            </td>
            <td>
                <nil>
            </td>
        </tr>
    </table>
    <div class="right-align">
        Created At 2023-11-09 13:24:44 +0000 UTC
    </div>
</div>

<div>
    <table>
        <tr>
            <td>
                PR <a href="https://github.com/hyperledger/aries-vcx/pull/1055" class=".btn">#1055</a>
            </td>
            <td>
                <b>
                    Indifferent to b64url padding in indy-utils
                </b>
            </td>
        </tr>
        <tr>
            <td>
                
            </td>
            <td>
                it was found that recent updates to base64 in indy-utils made the codebase less resilient to b64url padding when decoding. Previously we were indifferent to padding when decoding, then a regression was made which made indy-utils REQUIRE padding. This PR fixes the regression such that indy-utils will decode with or without padding.

this is important for utils such as `unpack_message`. 

according to encryption envelope: https://github.com/hyperledger/aries-rfcs/blob/main/features/0019-encryption-envelope/README.md

> NOTE: In the unpack algorithm, the base64url decode implementation used MUST correctly decode padded and unpadded base64URL encoded data.
            </td>
        </tr>
    </table>
    <div class="right-align">
        Created At 2023-11-09 11:54:38 +0000 UTC
    </div>
</div>

<div>
    <table>
        <tr>
            <td>
                PR <a href="https://github.com/hyperledger/aries-vcx/pull/1054" class=".btn">#1054</a>
            </td>
            <td>
                <b>
                    fix(aries_vcx): make integration tests run
                </b>
            </td>
        </tr>
        <tr>
            <td>
                
            </td>
            <td>
                This should make the tests run again, next step is to fix the failing cases.
            </td>
        </tr>
    </table>
    <div class="right-align">
        Created At 2023-11-08 14:54:04 +0000 UTC
    </div>
</div>

<div>
    <table>
        <tr>
            <td>
                PR <a href="https://github.com/hyperledger/aries-vcx/pull/1052" class=".btn">#1052</a>
            </td>
            <td>
                <b>
                    Add mediator coordination messages to aries-vcx messages crate
                </b>
            </td>
        </tr>
        <tr>
            <td>
                
            </td>
            <td>
                Ref: https://github.com/hyperledger/aries-rfcs/blob/main/features/0211-route-coordination/README.md
            </td>
        </tr>
    </table>
    <div class="right-align">
        Created At 2023-11-07 15:50:59 +0000 UTC
    </div>
</div>

