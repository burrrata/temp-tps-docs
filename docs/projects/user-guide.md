<br>

## What does the app do?

Projects is integrated with Github and allows organizations to allocate tokens or ETH against multiple issues in a single action, with the possibility to require DAO approval before funding is allocated. Additionally, Issue Curation proposals can be created via the Projects app, which are forwarded to the Dot Voting app to collectively determine project priorities.

<br>

## What are the intended use cases?

Projects can be added by connecting a Github repo, which will then display the repo's issues within an Aragon DAO. Members of the DAO can then use the TPS Projects app to curate issues to prioritize a roadmap or collectively allocate bounties to multiple issues in a single action.

<br>

## How do you use it?

<img src='https://cdn-images-1.medium.com/max/2160/1*1jsxao_cOo4t7GeHgLsNPA.png' />

- Once you have authorized Github, you can create a “New Project” which is essentially a Github repo. When you connect a repo with your organization, anyone else who accesses your DAO’s projects app and authorizes Github will see the repos you have connected.
- On the Issues tab, you can select multiple issues and then either choose “Curate Issues” or “Fund Issues” from the actions menu.
- On the Settings tab, you can set defaults and parameters used for calculating how many tokens are allocated to issue funding proposals, which is calculated based on: # hours * base rate * experience level
- Use Aragon’s Permissions system to restrict who can add repos, remove repos, fund issues, approve work, etc. Review the limitations below before deciding to give the Voting app power over these roles.

Note: while the Projects app is currently integrated with Github, we don’t see this as always being the case. We plan to roll out features as they are demanded, and [eventually integrate with Pando for a more fully decentralized solution](https://forum.aragon.org/t/pando-live-on-rinkeby/712).

<br>

## Limitations

- If funding issues requires a DAO vote for approval, the Voting app will have little context on the proposed funding amounts unless the description for the funding proposal contains a link that outlines the funding per issue (although this would have to be trusted). This is due to current limitations in the type of data that can be forwarded to the voting app.
- If funding issues requires a DAO vote for approval, the Projects app does not have any knowledge on the issues that were selected for potential funding until the vote is approved. [This is due to a current limitation with how Aragon works.](https://forum.aragon.org/t/showing-pending-forwarded-actions-in-apps/709)
- Even though it is integrated with Github, we do not have a Github bot for Github.com that comments if an issue has been funded by the organization. The way our system is implemented is catered more towards DAO members that want to help contribute to its tasks.
- If authorizing Github is slow or finicky, [please let us know](https://keybase.io/team/autark.community).

<br>

## Future

- It is a must to ultimately develop a solution that will provide more context to both the Voting and Projects apps of Funding proposals that have yet to be approved. There are various technical limitations that need to be overcome and we intend to contribute to the solutions as part of our [Cross Application UX Efforts](https://forum.aragon.org/t/cross-application-ux-initiative-part-1/742).
- An item on our near-term roadmap which was in our original Flock proposal is [implementing a way to fund project issues with non-transferable tokens](https://github.com/AutarkLabs/flock/blob/autark-proposal/teams/Autark/2019Q1-2.md#i04---expanding-governance-possibilities).
- We want to provide the ability to review the results of issue curation proposals within the Projects app, making it easier to take action on these priority lists by generating funding proposals.
- We want to eventually release a Projects app that can be used for general task management, which doesn’t require Github, has kanban, and discussion with all data stored on IPFS.
- We want to make it easier for people who are working on a Project’s issues to see what is assigned to them and to have notifications when due dates are approaching.

<br>

## Where can you learn more?

The [Aurark website](https://www.autark.xyz/) is a great start.
- [Projects app](https://www.autark.xyz/projects-app)

[This blog post](https://medium.com/@stellarmagnet/that-planning-suite-live-on-rinkeby-c2332e2e5e27) also explains how to use the app in more detail. 

<br>

## Still have questions?

[Ask the Autark team on Keybase!](https://keybase.io/team/autark.community)

<br>
