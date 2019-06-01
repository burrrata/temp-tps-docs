> Node.js LTS or greater required.

> @aragon/cli and truffle npm deps are automatically installed when bootstrapping.

```bash
# Bootstrap project dependencies:
$ npm i

# Start a local blockchain and deploy
# aragon dao kit with all apps:
$ npm start

# Develop single app react frontend:
$ npm run dev:projects

# Develop single app with backend and aragon wrapper:
$ npm run start:dot

# current app name aliases: {address, allocations, dot, projects, rewards}
```

<br>

### Extra tips

- Individual development is ultra-fast thanks to parcel and hot module replacement.
- Start the dao kit to manage smart contracts interactions between all "planning apps" and aragon official apps (token manager and voting right now)
- The start script spawns a local blockchain, needed to publish the apps before deploying the dao kit template with all them.

**Detailed information can be found in the [DEVELOPMENT_NOTES.md](https://github.com/AutarkLabs/planning-suite/blob/dev/docs/DEVELOPMENT_NOTES.md) document.**

<br>
