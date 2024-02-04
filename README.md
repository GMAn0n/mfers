bump
# syndicate-farcaster-frame-starter

A starter for using https://frame.syndicate.io/ with Farcaster Frames

This repository contains two important components:
`api/syndicate-syndicate-farcaster-frame-starter.ts`: An API for serving Farcaster Frames, already integrated with the API at frame.syndicate.io
`contracts/src/Use this contract.sol`: An example smart contract with flexible metadata options. It's simple to modify for the metadata you want.

Fork and enjoy! Setup should only take a few minutes if your NFT contract's mint function is formatted as `mint(address to)`

DM @will on Warpcast/@WillPapper on Telegram for an API key.

Gas is sponsored up to a shared max for everyone, so please be careful in your use and leave gas for others. We'll work on self-funding options for gas soon if the sponsored gas runs out! Your minting **will go down** if gas runs out, so use this for fun experiments, not production use cases.

To get started, I use Limewire to generate images, you can use my referral code to join their partner program, play with it a few days, fill out their contact form, you may get invited to a free year of premium (1k credits a month). https://limewire.com/studio?referrer=tkqwgkggxs

To generate metadata for the images, I have used Kredeum, it's a free service that does require some gas. I would however recommend Pinata if you are able to generate your own metadata (I do now know how yet, but am looking into this) https://app.kredeum.com/

contracts/src/Use this contract.sol will work pretty easily, you need to replace the contract name, and ipfs links (DYOR, trust but verify, there could be other things to correct here) such as replacing my wallet address with your own in authorized minters (important, its the last one on the list).
When you are ready, you need Remix IDE (https://remix.ethereum.org/) which allows you to compile your smart contract using version 0.8.20 (!important).

When you are confident you are ready, ALWAYS deploy to testnet first, sepholia is my go to, this way you can make sure everything is working correctly. 

Have a few wallets from friends to test out the randomization logic and ensure that the correct NFTs are getting distributed, in addition to requiring nobody can mint twice. 

Now that you are ready, link your github repo with Vercel https://vercel.com. 

You'll need to send a json payload or CURL as described by Will in the first document link. I use YARC (Yet another React Client). 
POST
URL: https://frame.syndicate.io/api/register
{"contractAddress":"0xSMARKc0nTRactaDDress"} <<<<<<< This goes in payload, replace with your smart contract from IDE. 
Authorization	Bearer SYNDICATE-API-KEY   <<<<<<<<<<<<< Replace this, it needs to post as a header	 This is an invalid API key.
Content-Type	application/json;charset=utf-8/

Now, deploy to vercel, and you should be ready to go. 
