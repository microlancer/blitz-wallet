# blitz-wallet

Blitz Wallet - A self-hosted mobile-friendly UI for Bitcoin Lightning Network payments

Blitz Wallet is a simple web application (like Wordpress) that provides a web-based front-end to your Lightning Wallet. It is designed for Lightning Network node operators (everyone) to be able to connect to their home node from anywhere, anytime. There is no need to download or use any mobile apps, or trust any 3rd party. You can make payments or receive payments using your node, through this interface.

To install:

The default install uses docker, but you can install it directly on your system if you have the proper packages. Also, you will need to be running either c-lightning or LND on the same server. You will also need to allow access to port 443 so that the service is reachable via a secure HTTPS connection.

To configure:

The first time you connect, it will ask you to create an account. The first account will be the administrator. You can create other accounts if you'd like (such as for trusted friends or family) by sending them an invite link.

You will then be prompted to select your node type: c-lightning or LND. Once selected, it will attempt to connect to your node. If it is unable to connect via local RPC, it will guide you through some troubleshooting steps.

If you don't have any channels yet, it will prompt you for this as well. Once everything is set up, you can then deposit BTC via on-chain or LN, or make payments via on-chain or LN.

How it works:

Each account has a balance being tracked by the web application. There is an on-chain balance and LN balance for each user. Although the balances are not separated at the node-level, they are completely separate at the web application level. In this way, each user has their own, personal wallet. However, the node operator has full control of all the funds, so this is intended to be used by only one person, or a highly trusted group (family, close friends). The administrator is able to see the  full balance of all accounts. However, non-admin accounts cannot see other account balances.


