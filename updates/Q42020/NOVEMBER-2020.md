# SKALE Network Product Updates (NOVEMBER 2020)

These updates are posted in: 

-   <https://github.com/skalenetwork/skale-network/tree/master/updates>
-   <https://forum.skale.network/>
-   [SKALE Discord](https://discord.gg/vvUtWJB)

If you would like to suggest changes, please post, discuss, or open a GitHub issue respective of the channels listed above.

## Month focus

During November, the team was mostly focused on:

-   Schains performance and stability testing, enabling Medium schains 1/32 of a node configuration
-   Consensus, skaled performance optimizations, and stability improvements
-   SGX wallet memory usage optimizations, performance improvements, load testing
-   SKALE Manager Bounty algorithm updates
-   IMA beta release preparations, enabling SGX wallet and Transaction manager support, outstanding bug fixes, and general enhancements
-   Various bug fixes


## Code changes

November:

**SKALE Manager (1.6.2-develop.0)**

-   Fixed Bounty V2 migration issue [\[PR#419\]](https://github.com/skalenetwork/skale-manager/pull/419)
-   Added independent audits references to the documentation[\[PR#420\]](https://github.com/skalenetwork/skale-manager/pull/420)
-   Added name check as a part of the IMA improvements [\[PR#423\]](https://github.com/skalenetwork/skale-manager/pull/423)
-   Merged release artifacts to the develop branch [\[PR#426\]](https://github.com/skalenetwork/skale-manager/pull/426)
-   Added range check as part of the Crypto audit enhancements [\[PR#427\]](https://github.com/skalenetwork/skale-manager/pull/427)
-   Added support of 1/32 of a node configuration for the schains launch [\[PR#431\]](https://github.com/skalenetwork/skale-manager/pull/431)
-   Fixed Bounty formula [\[PR#435\]](https://github.com/skalenetwork/skale-manager/pull/435), [\[PR#438\]](https://github.com/skalenetwork/skale-manager/pull/438)
-   Updated dependencies

**SKALE Consensus**

-   Added BLAKE3 hashing as a part of the performance improvements [\[PR#282\]](https://github.com/skalenetwork/skale-consensus/pull/282), [\[PR#283\]](https://github.com/skalenetwork/skale-consensus/pull/283), [\[PR#284\]](https://github.com/skalenetwork/skale-consensus/pull/284), [\[PR#286\]](https://github.com/skalenetwork/skale-consensus/pull/286)
-   Fixed libBLS build after latest libff update [\[PR#285\]](https://github.com/skalenetwork/skale-consensus/pull/285)
-   Updated libBLS [\[PR#288\]](https://github.com/skalenetwork/skale-consensus/pull/288)
-   Removed incorrect warning [\[PR#289\]](https://github.com/skalenetwork/skale-consensus/pull/289)
-   Fixed stop after assert in BlockProposalClientAgent[\[PR#290\]](https://github.com/skalenetwork/skale-consensus/pull/290)
-   Fixed busy wait in NetworkReadLoop if there are no messages [\[PR#291\]](https://github.com/skalenetwork/skale-consensus/pull/291)
-   Fixed sending too many rebroadcasts [\[PR#292\]](https://github.com/skalenetwork/skale-consensus/pull/292), [\[PR#293\]](https://github.com/skalenetwork/skale-consensus/pull/293)
-   Fixed: don't do an ECDSA signature check on a default block[\[PR#294\]](https://github.com/skalenetwork/skale-consensus/pull/294)
-   Fixed retry to SGX when the server is down [\[PR#295\]](https://github.com/skalenetwork/skale-consensus/pull/295)
-   Fixed empty block time is consensus [\[PR#296\]](https://github.com/skalenetwork/skale-consensus/pull/296)
-   Updated CODEOWNERS [\[PR#297\]](https://github.com/skalenetwork/skale-consensus/pull/297)
-   Added libcurl error 35 handling and print unexpected exception when reconnecting to SGX server [\[PR#298\]](https://github.com/skalenetwork/skale-consensus/pull/298)

**SGXWallet (1.59.1-develop.8)**

-   Fixed memory leak in BLS [\[PR#194\]](https://github.com/skalenetwork/SGXWallet/pull/194)
-   Extended tests for DKG procedure [\[PR#195\]](https://github.com/skalenetwork/SGXWallet/pull/195)
-   Added ECDSA key import [\[PR#196\]](https://github.com/skalenetwork/SGXWallet/pull/196)
-   Updated libBLS [\[PR#197\]](https://github.com/skalenetwork/SGXWallet/pull/197), [\[PR#199\]](https://github.com/skalenetwork/SGXWallet/pull/199)
-   Performance improvements: added fast ECDSA signatures [\[PR#200\]](https://github.com/skalenetwork/SGXWallet/pull/200)
-   Updated SGX wallet to always use signed enclave for SGX hardware builds [\[PR#201\]](https://github.com/skalenetwork/SGXWallet/pull/201)
-   Fixed SGX init crash on GitHub actions [\[PR#208\]](https://github.com/skalenetwork/SGXWallet/pull/208)
-   Removed SetDKGPoly call [\[PR#210\]](https://github.com/skalenetwork/SGXWallet/pull/210)
-   GitHub actions CI process improvements [\[PR#213\]](https://github.com/skalenetwork/SGXWallet/pull/213), [\[PR#215\]](https://github.com/skalenetwork/SGXWallet/pull/215)
-   Fixed SGX_ERROR_OUT_OF_TCS  [\[PR#219\]](https://github.com/skalenetwork/SGXWallet/pull/219)
-   Added nightly tests  [\[PR#224\]](https://github.com/skalenetwork/SGXWallet/pull/224), [\[PR#225\]](https://github.com/skalenetwork/SGXWallet/pull/225)
-   Secure enclave updates [\[PR#226\]](https://github.com/skalenetwork/SGXWallet/pull/226), [\[PR#227\]](https://github.com/skalenetwork/SGXWallet/pull/227), [\[PR#228\]](https://github.com/skalenetwork/SGXWallet/pull/228), [\[PR#229\]](https://github.com/skalenetwork/SGXWallet/pull/229), [\[PR#230\]](https://github.com/skalenetwork/SGXWallet/pull/230), [\[PR#231\]](https://github.com/skalenetwork/SGXWallet/pull/231), [\[PR#232\]](https://github.com/skalenetwork/SGXWallet/pull/232), [\[PR#233\]](https://github.com/skalenetwork/SGXWallet/pull/233), [\[PR#234\]](https://github.com/skalenetwork/SGXWallet/pull/234), [\[PR#237\]](https://github.com/skalenetwork/SGXWallet/pull/237), [\[PR#238\]](https://github.com/skalenetwork/SGXWallet/pull/238), [\[PR#239\]](https://github.com/skalenetwork/SGXWallet/pull/239), [\[PR#241\]](https://github.com/skalenetwork/SGXWallet/pull/241), [\[PR#242\]](https://github.com/skalenetwork/SGXWallet/pull/242), [\[PR#243\]](https://github.com/skalenetwork/SGXWallet/pull/243), [\[PR#244\]](https://github.com/skalenetwork/SGXWallet/pull/244), [\[PR#245\]](https://github.com/skalenetwork/SGXWallet/pull/245), [\[PR#246\]](https://github.com/skalenetwork/SGXWallet/pull/246)

**SKALED (3.1.1-develop.0)**

-   Fixed snapshots issue [\[PR#370\]](https://github.com/skalenetwork/skaled/pull/370)
-   Fixed skaled build after latest libff update [\[PR#371\]](https://github.com/skalenetwork/skaled/pull/371)
-   Fixed download snapshot if one of 15 nodes are offline [\[PR#373\]](https://github.com/skalenetwork/skaled/pull/373)
-   Fixed skaled build [\[PR#374\]](https://github.com/skalenetwork/skaled/pull/374)
-   Fixed skaled crash due to skale_nodesRpcInfo call [\[PR#376\]](https://github.com/skalenetwork/skaled/pull/376)
-   Updated IMA messages verification [\[PR#379\]](https://github.com/skalenetwork/skaled/pull/379)
-   Renamed snapshotInterval parameter [\[PR#380\]](https://github.com/skalenetwork/skaled/pull/380)
-   Updated skaled container workflow [\[PR#381\]](https://github.com/skalenetwork/skaled/pull/381), [\[PR#382\]](https://github.com/skalenetwork/skaled/pull/382)
-   Fixed skaled tests [\[PR#385\]](https://github.com/skalenetwork/skaled/pull/385)
-   Updated skaled with the most recent fixes from consensus [\[PR#386\]](https://github.com/skalenetwork/skaled/pull/386), [\[PR#388\]](https://github.com/skalenetwork/skaled/pull/388)
-   Added downloading snapshot from a random node [\[PR#387\]](https://github.com/skalenetwork/skaled/pull/387)
-   Fixed IMA transfer for ERC20 and ERC721 tokens [\[PR#389\]](https://github.com/skalenetwork/skaled/pull/389)
-   Generated new built-in IMA contracts for S-Chain [\[PR#390\]](https://github.com/skalenetwork/skaled/pull/390)
-   Fixed default level logs [\[PR#391\]](https://github.com/skalenetwork/skaled/pull/391)
-   Closed debug interface [\[PR#393\]](https://github.com/skalenetwork/skaled/pull/393)
-   Added features fir built-in IMA on schain [\[PR#394\]](https://github.com/skalenetwork/skaled/pull/394)

**SKALE Admin (1.1.0-develop.22)**

-   Fixed dry run disabling [\[PR#327\]](https://github.com/skalenetwork/skale-admin/pull/327)
-   Restructured allocation file, refactored containers limits [\[PR#328\]](https://github.com/skalenetwork/skale-admin/pull/328)
-   Added IMA supporting SGX wallet [\[PR#331\]](https://github.com/skalenetwork/skale-admin/pull/331)
-   Fixed schain block mining [\[PR#332\]](https://github.com/skalenetwork/skale-admin/pull/332)
-   Moved wallet send API to RPC [\[PR#333\]](https://github.com/skalenetwork/skale-admin/pull/333)
-   Renamed snapshotInterval parameter [\[PR#335\]](https://github.com/skalenetwork/skale-admin/pull/335)
-   Added sChain blocks check, refactored SChainChecks, added tests [\[PR#336\]](https://github.com/skalenetwork/skale-admin/pull/336)
-   Temporary commented out IMA [\[PR#337\]](https://github.com/skalenetwork/skale-admin/pull/337)
-   Filtered empty schains structures [\[PR#338\]](https://github.com/skalenetwork/skale-admin/pull/338)
-   Fixed ALLOWED_TIMESTAMP_DIFF type [\[PR#339\]](https://github.com/skalenetwork/skale-admin/pull/339)
-   Fix IMA container execution in creator [\[PR#340\]](https://github.com/skalenetwork/skale-admin/pull/340)
-   Fixed IMA cleaner [\[PR#341\]](https://github.com/skalenetwork/skale-admin/pull/341)
-   Changed cleaner time during DKG process [\[PR#342\]](https://github.com/skalenetwork/skale-admin/pull/342)
-   Removed deprecated set-env syntax form publish workflow [\[PR#343\]](https://github.com/skalenetwork/skale-admin/pull/343)
-   Added catch failure after type 2 complaint (DKG process)  [\[PR#344\]](https://github.com/skalenetwork/skale-admin/pull/344)
-   Changed SchainType for medium schain [\[PR#345\]](https://github.com/skalenetwork/skale-admin/pull/345)
-   Temporary commented out IMA  [\[PR#346\]](https://github.com/skalenetwork/skale-admin/pull/346)
-   Updated CODEOWNERS  [\[PR#348\]](https://github.com/skalenetwork/skale-admin/pull/348)
-   Restructured Telegram notifications  [\[PR#349\]](https://github.com/skalenetwork/skale-admin/pull/349)
-   Added option to sepcify gas price  [\[PR#350\]](https://github.com/skalenetwork/skale-admin/pull/350)
-   Updated skale.py to 4.1dev18  [\[PR#352\]](https://github.com/skalenetwork/skale-admin/pull/352)
-   Turned on IMA [\[PR#354\]](https://github.com/skalenetwork/skale-admin/pull/354)

**IMA (1.0.0-develop.57)**

-   Added SGX Wallet support [\[PR#299\]](https://github.com/skalenetwork/ima/pull/299)
-   Added OZ upgradable structure [\[PR#300\]](https://github.com/skalenetwork/ima/pull/300)
-   Updated IMA Docker part [\[PR#302\]](https://github.com/skalenetwork/ima/pull/302)
-   Moved to solidity 0.6.0 and added try/catch support [\[PR#303\]](https://github.com/skalenetwork/ima/pull/300)
-   Improved IMA agent command line for invoking tests [\[PR#307\]](https://github.com/skalenetwork/ima/pull/307)
-   Changed IMA protocol preference to contact skaled (JSON RPC)  [\[PR#308\]](https://github.com/skalenetwork/ima/pull/308)
-   Added docs to IMA LockAndData contracts[\[PR#309\]](https://github.com/skalenetwork/ima/pull/309)
-   Added additional IMA improvements [\[PR#311\]](https://github.com/skalenetwork/ima/pull/311)
-   Fixed tests coverage [\[PR#312\]](https://github.com/skalenetwork/ima/pull/312)
-   Added docs to ERC20ModuleForMainnet [\[PR#313\]](https://github.com/skalenetwork/ima/pull/313)
-   Removed run.js script [\[PR#314\]](https://github.com/skalenetwork/ima/pull/314)
-   removed redundant and test contracts from coverage reports [\[PR#315\]](https://github.com/skalenetwork/ima/pull/315)
-   Updated TokenManager.sol  [\[PR#316\]](https://github.com/skalenetwork/ima/pull/316)
-   Fixed run register only on sChain side [\[PR#317\]](https://github.com/skalenetwork/ima/pull/317)
-   Added transaction manager support [\[PR#318\]](https://github.com/skalenetwork/ima/pull/318)
-   Set up semver versioning process [\[PR#320\]](https://github.com/skalenetwork/ima/pull/320)
-   Fixed link node addresses [\[PR#321\]](https://github.com/skalenetwork/ima/pull/321)
-   Fixed IMA data generator script  [\[PR#322\]](https://github.com/skalenetwork/ima/pull/322)
-   Changed registration step “Add schain in LockAndData” [\[PR#325\]](https://github.com/skalenetwork/ima/pull/325)
-   Fixed wait feature and names [\[PR#326\]](https://github.com/skalenetwork/ima/pull/326)
-   Replaced deprecated set-env in publish pipeline [\[PR#327\]](https://github.com/skalenetwork/ima/pull/327)
-   Added registration step Mainnet on schain [\[PR#329\]](https://github.com/skalenetwork/ima/pull/329)
-   Fixed incorrectly handled chain ID [\[PR#330\]](https://github.com/skalenetwork/ima/pull/330)
-   Fixed registration [\[PR#331\]](https://github.com/skalenetwork/ima/pull/331)
-   Updated ownable contracts [\[PR#339\]](https://github.com/skalenetwork/ima/pull/339)
-   Updated CODEOWNERS [\[PR#340\]](https://github.com/skalenetwork/ima/pull/340)
-   Updated dependencies

**SKALE Node CLI (1.1.0-develop.22)**

-   Turned off dry run env [\[PR#337\]](https://github.com/skalenetwork/skale-node-cli/pull/337)
-   Restructured resource allocation file, added IMA limits [\[PR#338\]](https://github.com/skalenetwork/skale-node-cli/pull/338)
-   Added IMA limits [\[PR#339\]](https://github.com/skalenetwork/skale-node-cli/pull/339)
-   Customized gas limit and gas price, removed deps [\[PR#345\]](https://github.com/skalenetwork/skale-node-cli/pull/345)
-   Fixed resource allocation file init [\[PR#346\]](https://github.com/skalenetwork/skale-node-cli/pull/346)
-   Handling script error [\[PR#347\]](https://github.com/skalenetwork/skale-node-cli/pull/347)
-   Set node-cli to save metadata about current versions and versions history [\[PR#348\]](https://github.com/skalenetwork/skale-node-cli/pull/348)
-   Hiding log folder init message [\[PR#353\]](https://github.com/skalenetwork/skale-node-cli/pull/353)
-   Updated README.md [\[PR#354\]](https://github.com/skalenetwork/skale-node-cli/pull/354)
-   Added node cli command for contracts abi validation [\[PR#355\]](https://github.com/skalenetwork/skale-node-cli/pull/355)
-   Fixed backup and restore [\[PR#358\]](https://github.com/skalenetwork/skale-node-cli/pull/358)
-   Fixed publish workflow [\[PR#360\]](https://github.com/skalenetwork/skale-node-cli/pull/360)
-   Fixed set versions Github Actions script [\[PR#361\]](https://github.com/skalenetwork/skale-node-cli/pull/361)
-   Enabled 1/32 of a node configurations for schains [\[PR#362\]](https://github.com/skalenetwork/skale-node-cli/pull/362)
-   Added skaled RPC and blocks checks to checks cmd to node-cli [\[PR#365\]](https://github.com/skalenetwork/skale-node-cli/pull/365)
-   Updated CODEOWNERS [\[PR#366\]](https://github.com/skalenetwork/skale-node-cli/pull/366)
-   Added --gas-price --gas-limit for skale node register [\[PR#367\]](https://github.com/skalenetwork/skale-node-cli/pull/367)
-   Added gas price env config option [\[PR#371\]](https://github.com/skalenetwork/skale-node-cli/pull/371)
-   Updated dependencies

**Validator CLI (1.2.0-develop.5)**

-   Replaced deprecated set-env in publish pipeline  [\[PR#239\]](https://github.com/skalenetwork/validator-cli/pull/239)
-   Updated dependencies

**sla-agent (1.0.2-develop.2)**

-   no updates

**bounty-agent (1.1.0-develop.1)**

-   Used getNodeNextRewardDate for sending getBounty transaction [\[PR#92\]](https://github.com/skalenetwork/bounty-agent/pull/92)
-   Updated to skale manager with a new getBounty procedure [\[PR#94\]](https://github.com/skalenetwork/bounty-agent/pull/94)
-   Fixed set-env for publishing docker image [\[PR#97\]](https://github.com/skalenetwork/bounty-agent/pull/97)
-   Updated dependencies

**SKALE.py (4.1dev18)**

-   Fixed DEFAULT_GAS_LIMIT env [\[PR#319\]](https://github.com/skalenetwork/skale.py/pull/319)
-   Added function to send ETH with skale.wallet [\[PR#324\]](https://github.com/skalenetwork/skale.py/pull/324)
-   Removed print  [\[PR#325\]](https://github.com/skalenetwork/skale.py/pull/325)
-   Updated CODEOWNERS [\[PR#329\]](https://github.com/skalenetwork/skale.py/pull/329)
-   Added DEFAULT_GAS_PRICE env config option  [\[PR#330\]](https://github.com/skalenetwork/skale.py/pull/330)
-   Removed deprecated set-env usage  [\[PR#331\]](https://github.com/skalenetwork/skale.py/pull/331)
-   Updated dependencies


**Transaction-manager (1.0.0-develop.8)**

-   Increased http timeout [\[PR#123\]](https://github.com/skalenetwork/transaction-manager/pull/123)
-   Fixed crop dict for tx without data [\[PR#124\]](https://github.com/skalenetwork/transaction-manager/pull/124)
-   Fixed Transaction manager exceeds connection limit [\[PR#125\]](https://github.com/skalenetwork/transaction-manager/pull/125)
-   Added customizable blocks limit, dropped skale.py init [\[PR#128\]](https://github.com/skalenetwork/transaction-manager/pull/128)
-   Updated dependencies

**sgx.py (0.6dev15)**

-   no updates
