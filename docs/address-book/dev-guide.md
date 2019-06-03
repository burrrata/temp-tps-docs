## How do you run it locally?

### Aragon CLI Deployment 

> Node.js LTS or greater required.

> @aragon/cli and truffle npm deps are automatically installed when bootstrapping.

```bash
# Bootstrap project dependencies:
$ npm i

# Start a local blockchain and deploy
# aragon dao kit with all apps:
$ npm start

# Develop single app react frontend:
$ npm run dev:address

# Develop single app with backend and aragon wrapper:
$ npm run start:address
```

### Tips
- Individual development is ultra-fast thanks to parcel and hot module replacement.
- Start the dao kit to manage smart contracts interactions between all "planning apps" and aragon official apps (token manager and voting right now)
- The start script spawns a local blockchain, needed to publish the apps before deploying the dao kit template with all them.
- 

<br>

## How do you install it in a pre-existing DAO?
- instructions on deployment & installation on an Aragon DAO

https://github.com/AutarkLabs/planning-suite/blob/master/docs/GETTING_STARTED.md#install-address-book

<br>

## Technical Breakdown 
- explanation of each function/feature, what it does, and how to use it. 

TBD 

<br>

## Show me the code!

[Here's the Address Book GitHub repo.](https://github.com/AutarkLabs/planning-suite/tree/dev/apps/address-book)

<br>

## Still have questions?

[Ask the Autark team on Keybase!](https://keybase.io/team/autark.community)

<br>

