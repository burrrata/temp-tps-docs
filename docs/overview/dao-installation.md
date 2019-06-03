- source: https://github.com/AutarkLabs/planning-suite/blob/master/docs/GETTING_STARTED.md

<br>

# Installing That Planning Suite to an Existing DAO
The following are instructions to install That Planning Suite. 

<br>

## aragonCLI primer
We will be using aragonCLI.
The basic command to install an app is:

#### App with no initialization parameters

```
dao install <dao-addr> <app-apm-repo> 
```

#### App with initialization parameters (two for example)
```
dao install <dao-addr> <app-apm-repo> --app-init-args <param1> <param2>
```

Be sure to also pass the `--environment aragon:rinkeby` flag since these apps are on rinkeby.

### Permissions
In order to make the apps appear in the UI, you need to initialize at least one permissions per app via the cli. Once you setup at least one permission via the cli, you can do the rest in the UI via Permissions.


The command to set permissions is:

```
dao acl create <dao-address> <app-proxy-address> <permission-name> <grantee> <manager>
```

In order to get the proxy address of apps that do not have permissions, you need to run the following command:
```
dao apps <dao-address> --all
```
You should see a list of apps, and freshly installed apps will be listed at the bottom, in the "permissionless apps" section, in the order in which they were installed.


Read about acl commands on the [Aragon wiki](https://hack.aragon.org/docs/cli-dao-commands#dao-acl-create), and refer to the end of this document for the initial permissions that we set via the Planning Suite template / kit that you may want to consider as well.

### Additional Vault
In the early mainnet phases, you may want to consider installing a second (or third) vaults that will be used for Planning Suite apps such as Projects, Rewards, or Allocations -- until the contracts have been fully audited. You can transfer funding from the Finance app / your primary vault into smaller funding pools in these additional vault(s).

### Learn more about aragonCLI
Refer to these links for more information: 
* https://hack.aragon.org/docs/guides-custom-deploy
* https://hack.aragon.org/docs/cli-dao-commands

<br>

## Install Address Book
#### tps-address-book.open.aragonpm.eth

The Address Book is for maintaining a list of Ethereum addresses mapped to human-readable names, on-chain. The Address Book will enable a more user-friendly way to access and review common addresses a DAO uses for Allocations and Dot Voting.

The address book does not require passing any initialization parameters.

#### Sample install command

```
dao install <dao-address> tps-address-book.open.aragonpm.eth --environment aragon:rinkeby
```

<br>

## Install Dot Voting App
#### tps-dot-voting.open.aragonpm.eth

The Dot Voting app is used by both the Allocations app and Projects app. Dot Voting allows token holders to prioritize between multiple options by distributing votes across these options.

The Dot Voting app requires the following initialization parameters:

* `AddressBook`: proxy address of the Address Book app (must be installed before initializing Dot Voting)
* `MinimeToken`: address of a minime token
* `minParticipationPct`: percentage of total votes required for a vote to succeed (expressed as a percentage of 10^18; eg. 10^16 = 1%, 10^18 = 100%)
* `candidateSupportPct`: minimum percentage required for an option to be valid. This feature is not fully enabled yet, so set this to 0 otherwise the app may behave unexpectedly.
* `voteDuration`: Seconds that a vote will be open for token holders to vote


#### Sample install command
This will install a Dot Voting instance with a participation requirement of 50% and a voting period of 7 days.
```
dao install <dao-address> tps-dot-voting.open.aragonpm.eth --app-init-args [AddressBook] [MinimeToken] 500000000000000000 0 604800 --environment aragon:rinkeby
```

<br>

## Install the Projects app
#### tps-projects.open.aragonpm.eth

Proects allows an organization to manage a bounties workflow using Github and the Standard Bounties contract. Issue Curation proposals can also be created via the Projects app, which are forwarded to the Dot Voting app to collectively determine project priorities.

The Projects app requires the following initialization parameters:
* `registry`: The Standard Bounties registry address. Use 0xcac024cb2ad5f22c3e92053b95c89f69442952d8
* `Vault`: proxy address of the Vault you want to connect with the app
* `paymentToken`: the default token that bounties will be paid in. This can always be changed via the Settings tab.

#### Sample install command
```
dao install <dao-address> tps-projects.open.aragonpm.eth --app-init-args 0xcac024cb2ad5f22c3e92053b95c89f69442952d8 [Vault] [paymentToken] --environment aragon:rinkeby 
```

<br>

## Install the Rewards app
#### tps-rewards.open.aragonpm.eth

With Rewards, you can distribute payments to token holders based on the number of tokens one has earned in a specific cycle of time (one-time reward) or based on the total tokens one holds (dividend).

The Rewards app requires the following initialization parameter:
* `Vault`: proxy address of the Vault you want to connect with the app


#### Sample install command
```
dao install <dao-address> tps-rewards.open.aragonpm.eth --app-init-args [Vault] --environment aragon:rinkeby 
```

<br>

## Install the Allocations app
#### tps-allocations.open.aragonpm.eth

Allocations is used to propose a financial allocation meant to be distributed to multiple parties or options. Proposals are forwarded to the Dot Voting app for an organization to collectively determine the distribution of funds. The percentage of the allocation amount distributed to each party is determined based on the results of the Dot Vote.

The Allocations app requires the following initialization parameter:
* `AddressBook`: proxy address of the Address Book app (must be installed before initializing Dot Voting)
* `Vault`: proxy address of the Vault you want to connect with the app


#### Sample install command
```
dao install <dao-address> tps-allocations.open.aragonpm.eth --app-init-args [AddressBook] [Vault] --environment aragon:rinkeby 
```

<br>

## Notes

More info and troubleshooting tips can be found here:
- https://github.com/AutarkLabs/planning-suite/blob/dev/docs/DEVELOPMENT_NOTES.md

<br>
