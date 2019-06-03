<br>

## How do you run it locally?
- instructions on how to run the app

> Node.js LTS or greater required.

> @aragon/cli and truffle npm deps are automatically installed when bootstrapping.

```bash
# Bootstrap project dependencies:
$ npm i

# Start a local blockchain and deploy
# aragon dao kit with all apps:
$ npm start

# Develop single app react frontend:
$ npm run dev:rewards

# Develop single app with backend and aragon wrapper:
$ npm run start:rewards
```

<br>

### Extra tips

- Individual development is ultra-fast thanks to parcel and hot module replacement.
- Start the dao kit to manage smart contracts interactions between all "planning apps" and aragon official apps (token manager and voting right now)
- The start script spawns a local blockchain, needed to publish the apps before deploying the dao kit template with all them.

**Detailed information can be found in the [DEVELOPMENT_NOTES.md](https://github.com/AutarkLabs/planning-suite/blob/dev/docs/DEVELOPMENT_NOTES.md) document.**

<br>

## How do you install it in a pre-existing DAO?
- instructions on deployment & installation on an Aragon DAO

https://github.com/AutarkLabs/planning-suite/blob/master/docs/GETTING_STARTED.md#install-the-rewards-app

<br>

## Technical Breakdown 
- explanation of each function/feature, what it does, and how to use it. 

<br>

## Show me the code!

[Here's the GitHub](https://github.com/AutarkLabs/planning-suite/tree/dev/apps/projects)

[Here's where you can roll your own TPS enables DAO on Rinkeby to explore the Projects app](https://rinkeby.autark.xyz/)

[Here's a live working DAO that's set up with TPS apps already enabled](https://rinkeby.aragon.org/#/dune.aragonid.eth)

<br>

## Still have questions?

[Ask the Autark team on Keybase!](https://keybase.io/team/autark.community)

<br>
