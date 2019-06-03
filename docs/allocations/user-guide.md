<br>

## What does the Allocations app do?

The Allocations app is used to propose a financial allocation meant to be distributed to multiple parties. Allocation proposals are forwarded to the Dot Voting app. The percentage of the allocation amount distributed to each party is determined based on the results of the Dot Vote.

<br>

## What are the intended use cases?

If you want to set aside a portion of your DAOs tokens/budget for allocations, you can! Then on a regular interval members of the DAO can vote to allocate funds however they want. One example of this is rewarding outstanding community contributions. Think of it as an employee of the month program, but as often and as granular as you want. You could also have a charity that the DAO donates to on a regular basis, and the community could choose where to direct those funds. The options are limitless! If you think of a great usecase please let us know by opening an Issue :)

Your organization is determining how to allocate a predefined amount of funds to child organizations or departments. (If the child organizations are also part of Aragon, input the organization’s vault address in your Address Book)

Your organization has ongoing work areas that aren’t necessarily specific project issues that can be individually funded (e.g. participating on the forum, taking meeting notes, more general contributions). These contributors can be subjects of Allocation proposals meant to give back to community members that contribute in a noticeable manner (and usually on a voluntary basis).

<br>

## How do I use the Allocations app?

<img src='https://cdn-images-1.medium.com/max/2160/1*PRCNTHvTHvOJQajJq6SZOQ.png' />

- An account needs to be created via the “New Account” button before proposing an Allocation. Accounts are used to categorize allocation types that occur frequently.
- To propose an allocation, choose the “New Allocation” action from the Account’s context menu.
- In the New Allocation panel, enter an allocation amount which can be drawn from the ETH held in the account, or any of the token’s in your Organization’s vault.

<br>

## Tips
- Use the Address Book to manage Ethereum addresses you will be sending regular allocations to. Once you have added entries to your address book, you can select “Use address book for options” in the New Allocation panel to select the recipients.
- If categorizing by Account isn’t useful to you, feel free to create a “General” account and create your allocations from this account.

<br>

## Current Limitations

There is a current limitation with how Accounts currently function. An “Account” can hold ETH, but it can transfer tokens that are in the organization’s vault (yet not the Vault’s ETH). This can also be a bit confusing for the user experience. Due to these limitations, if tokens are sent to the Account address they will not be accessible.

<br>

## Future

Before launching to mainnet, we would like to resolve the above limitations. To do so, we plan on enhancing how accounts work so the user experience is more intuitive. One possible solution is:
- Instead of accounts holding/receiving ETH, they will instead function more as budget controls for specific initiatives.
- Accounts will have the following properties:
  - Name (e.g. Community Funding Initiative)
  - Budget cycle (e.g. Monthly)
  - Budget amount (e.g. 4,000 DAI/month)
- All accounts will withdraw from the vault and cannot be individually funded. Updating the budget will be protected by an organization role.
- Accounts cards will display amount spent and budget remaining per cycle.

Another possible solution, which may make the experience even smoother, is enhancing the current Finance app within Aragon to provide segmenting capital by accounts. Autark’s initial application development approach was to develop new apps, but now that we are a Flock team and have had a year to reflect, we think that this is a use case where the experience would be more seamless if both single party and multi-party financial allocations were managed in a unified app.

<br>

## Where can I learn more?

The [Aurark website](https://www.autark.xyz/) is a great start.
- [Allocations app](https://www.autark.xyz/allocations)

[This blog post](https://medium.com/@stellarmagnet/that-planning-suite-live-on-rinkeby-c2332e2e5e27) also explains how to use the app in more detail. 

<br>

## Still have questions?

[Ask the Autark team on Keybase!](https://keybase.io/team/autark.community)

<br>
