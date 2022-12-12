# Welcome to [AptosPad](https://aptospad.app)
![AptosPad Banner](https://github.com/aptospad-app/.github/blob/main/assets/Aptospad-05.png)

AptosPad is the launchpad platform on Aptos blockchain that accelerates the future ideals by connecting the community, investors and builders. The creative ideals can become real with the fundraising and support from AptosPad platform

AptosPad is the first launchpad on Aptos that proposes and applies the SharePad mechanism. This mechanism allows projects to sell tokens not only on AptosPad but also on the whole sharing pool of AptosPad’s partners.

AptosPad will be the DAO and community-driven platform so that It creates the fair opportunity for any users to access the project's token sale from the early stage.

__Document Outlines:__

- [How AptosPad work](#how-aptospad-work)
- [The AptosPad functions](#the-aptospad-functions)
- [How to participate in token sales](#how-to-participate-in-token-sales)
    - [Whitelist mechanism ](#whitelist-mechanism)
    - [AptosPad ticket](#aptospad-ticket)
- [The refund mechanism](#the-refund-mechanism)
- [The Referential system](#the-referential-system)
    - [Users benefits](#users-benefits)
    - [How it works](#how-it-work)
- [How SharePad works](#how-sharepad-works)
- [APD - The utinity token on AptosPad](#atpp---the-utinity-token-on-aptospad)
    - [Token utinity](#token-utinity)
    - [Tokenomic](#tokenomic)
- [Become the early supporter](#become-the-early-supporters)
- [Frequently Asked Question](#frequently-asked-questions)

__Project resources:__

[Smart contract](https://github/aptospad-app/smart-contracts) | [Web application](https://aptospad.app) | [Discord Channel](https://discord/) | [Twitter](https://twitter.com/aptospad_dao) | [Contact us](mailto:contact@aptpospad.app)

## How AptosPad work

__AptosPad__ is the launchpad platform that helps the projects raise funds from the early stage. All fundraising is in the token (or coin) on Aptos blockchain. 

Projects that are listed on AptosPad must be qualified and verified by platform experts or through community voting process. All projects must publish the following information: 
- Project name and description 
- Project purpose, the problem solving 
- Website, media channel (discord, telegram, twitter …)
- Founder team  
- Whitepaper and source code (if open source)
- Fundraising target/hardcap, policy and refund terms/conditions

As supporters/investors, you can check for the project information, the potential and decide whether or not to participate in the token sales.

## The AptosPad functions
Like many other launchpad platforms, Aptos Pad has the following functions 
- Register new projects for early public sales
- List of current projects in sale progress and projects in the past
- Register users/investors by web2 or web3 methods
- KYC project owners/investors 
- Whitelist users for specific projects
- Buy early sales tokens and claim 
- SharePad mechanism
- Earn reward by Staking and farming 
- Daily task and leaderboard ranking 
- Earning by inviting/ref
- Voting for projects
- Other functions

## How to participate in token sales
Normally, token sale of projects listed on AptosPad is in the early stage (like the public IDO) and the amount of token is limited (3-5% of total supply). Token price is expected to increase several times in the next public sales on exchanges, that’s why not everyone can buy the token on platform. The project owner may restrict the sales and bring the opportunity to users who help the project in the long-term vision. To make It fair for every user to access the early sales, AptosPad has the ticket-based and whitelist mechanism. Users in the whitelist will have the opportunity to get the ticket and buy the project token.

### Whitelist mechanism 

Users that hold and stake the APD token in a staking pool at least 3 days before the token sale occurs will get the ticket. The number of tickets depends on the APD token that users deposit into the staking pool and the amount of project token will be based on the number of tickets that users have.
 ``` number_of_ticket = floor(APD/1000) + reward``` where  ```reward = floor(APD/5000)``` 
. That means users get 1 ticket for each 1000 APD staking token and get another 1 ticket for each other 5000 APD staking token. For example :
- If user stake 2000 APD, they get ```floor(2000/1000) = 2 tickets```
- If user stake 7000 APD, they get ```floor(7000/1000) + floor(7000/5000) = 9 tickets``` 
- If users stake 60.000 APD, they get ```floor(60000/1000) + floor(60000/5000) = 60 + 12 = 72 tickets```

Please note that the official ticket calculation will be define in smart contract at the time of deploying

### AptosPad ticket
AptosPad ticket is the fair way for users participating in the early token sale. To get the Aptospad tickets users can join the whitelist by taking the APD token which is described in the session above or participate in community activities on the platform such as share the event, retweet the post, win the lottery, … the first 100 users with the high ranking will get the tickets. The number of tickets that the leaderboard can archive will depend on the situation when launching the projects.

The token that a user will be allowed to by will be calculated by the formulation below:

![$$ amount_x = {ticket_x*totalSale \over \sum_{k=1}^n ticket_k}$$](https://github.com/aptospad-app/.github/blob/main/assets/ticket-equation.png)

Where:
- _amount(x)_: is the amount of token that user X can buy
- _ticket(x)_: is the number of tickets that user X has
- _totalSale_: is the total token of project in the early sale
- _sum of ticket(k)_: is the total tickets on the platform joined the early sale

Please note that the token that user X can buy will not exceed the maximum quota that a user can buy defined in each project policy

## The refund mechanism 
The projects on AptosPad should define the refund policy if some certain conditions are not met. It attracts investors and makes projects more credible. AptosPad has the basic built-in refund mechanism that can be customised.

### Refund if the fundraising target is not met
When a project is listed on AptosPad, the project owners should clarify the target (in  ATP or USD equivalent). The fundraising target is considered as the softcap, If It below the softcap, the refund process will be activated. Project owners can also define the maximum target in which the fund cannot exceed, otherwise, the refund will be triggered too.

![refund-mechanism](https://github.com/aptospad-app/.github/blob/main/assets/aptospad-refund.png)

When users buy a token, the user's fund goes directly to the smart contract pool rather than the project owners wallet. After the IDOs, the smart contract will check the fundraising status. If the condition does not meet, a refund process will be executed automatically, It creates a claimable vault that maps the investor’s account with the refund amount and after that users can claim their funds into their wallet. 

Please note that the _min target, max target, refund fee …_ will be set by project owners in AptosPad’s smart contract and displayed transparently on the platform before the IDOs started. 

### Refund in overbought case 
AptosPad allows users to buy more tokens than the tickets they have if the fundraising target is not met. The special thing is that It will be fair for all users while users can overbuy the token before the IDOs end. If the fundraising amount exceeds the _hardcap_, the refund process will be activated. The detailed steps below:

(1). Users need to be added to the whitelist to participate in early token sales

(2). Users can buy the token amount corresponding the tickets they have or overbuy the token

(3). At the end of IDO, the smart contract will check the result and the following cases may occur: 
- The total fundraising amount does not reach the softcap: the refund process will be triggered and all users can claim their funds 
- The total fundraising amount is between the _[softcap, hardcap]_: fundraising is considered as the success case. Token will be distributed to users wallet (TGE and vesting schedule depends on each project)
- The total fundraising amount exceeds the hardcap: All users receive the token corresponding to the number of tickets they have. To the users who overbought the token, a portion of the overbought amount will be refunded. This portion will depend on percentage of the total exceeded amount and is calculated as below:
```
    exceeded_amount = total_amount - hardcap 
    exceeded_percentage = exceeded_amount/hard_cap 
    refund_amount = (overbought_amout - allowed_amount)*exceeded_percentage 
```
The overbought creates a fair opportunity for all participants because the ticket system is the priority. It also helps projects to reach the target funds in somecase and also satisfy some early investors' demand. 

## The Referential system
AptosPad has a referential mechanism that allows users to refer to other users and get the reward. It is also the way to scale the community and also help IDOs projects to reach the target and potential investors/customers. 
### Users benefits 
When users refer to others users joining the AptosPad, they may receive the following benefits
- Receive retroactive token
- Get the tickets to be added to whitelist
- Become the listing agency 
- Get commission from F1 IDOs volume or staking volume

### How It work
Everyone in AptosPad can create the reference codes and invite their friends in their network to join the AptosPad. Users must connect to AptosWallet (Petra, Martian … for example) to create the ref codes, when other users login with their friend ref codes by Aptos wallet, they must sign the transaction and submit to AptosPad system. The information then gets verified and stored on both on-chain and chain for later incentive calculation. Please note that all addresses must exist on Aptos network in order to join the referential program. The picture below describes the referential flow in AptosPad.

![aptospad-ref](https://github.com/aptospad-app/.github/blob/main/assets/aptospad-ref.png)

## How SharePad works
When a project token is listed on AptosPad.app for the early token sales, The token will not only appear on AptosPad but also on other trusted launchpads that partnered with AptosPad. Users can buy the early token on all connected partners but the whitelist mechanism or policies depend on each launchpad partner.

![SharePad mechanism](https://github.com/aptospad-app/.github/blob/main/assets/aptos-sharepad.png)

There will be the _sharepad contract_ that all the partners will agree on and each launchpad partner can sell for a specific number of tokens (for example 10%). If the total of the fundraising on all launchpads exceeds the project target, the refund process on smart contract will be triggered and users can claim the corresponding amount of APT based on exceeded percentage.


## APD - The utinity token on AptosPad
APD is the token/coin of AptosPad on Aptos blockchain that is designed to leverage the AptosPad ecosystem
### Token utinity
With APD token/coin, users can:
- Get more opportunity to participate in early sale of any projects 
- Stake to add to whitelist, get ticket and buy tokens 
- Earn reward from staking tools 
- Vote for projects to be listed or delisted 
- Swap/exchange to another token 

### Tokenomic
There will be 1.000.000.000 (1B in word) token issued on Aptos mainet. The allocation and vesting schedule as following (draft)

| Token distribution           | Percentage  | Amount     | Vesting schedule                              |
| -----------------------      | ----------- |------------|-----------------------------------------------|
| Private round                | 8 %         |80.000.000  |Release 20% at TGE, linear vesting in 6 months |
| Public round (IDO)           | 4%          |40.000.000  |Release 100% at TGE                            |
| Advisor                      | 5%          |50.000.000  |Release 10% at TGE, linear vesting in the next 36 months|
| Founder/Core team            | 15%         |150.000.000 |Fully lock in 12 months then unlock over 36 months|
| Ecosystem growth             | 30%         |300.000.000 |Linear vesting over 5 years|
| Marketing                    | 15%         |150.000.000 |Release on each campaign, target in 2 years|
| Airdrop/Bounty               | 5%          |50.000.000  |Fully unlock                               |
| Treasury                     | 18%         |180.000.000 |Fully lock in the first 3 years, unlock over next 36 months|

## Become the early supporters
The early supporters, also known as __OG__ will have the high opportunity to buy the tokens because they will have the priority tickets (without staking the APD token) to access the project sales.
There are many ways to become early supporters (or OG) such as joining and sharing AptosPad social media channels, partnership or collaboration in projects … There will be a post on twitter of how to be the platform early supporters. Please follow us [AptosPad](https://twitter.com/Aptospad_DAO)


## Frequently Asked Questions
1. __What is AptosPad__

AptosPad is the launchpad on Aptos network that helps projects to raise funds from community in the early stage (IDO)

2. __What the special features of AptosPad__

AptosPad has almost all of the functions that other launchpads have, some features below make AptosPad special
    - Launch-fair
    - Ref mechanism
    - SharePad mechanism 
    - Overbuy mechanism 
    - Refund mechanism 

3. __What’s the launch-fair feature on AptosPad__

Unlike other launchpad, AptosPad has the fair-launch mechanism, that means everyone has the same opportunity to buy the IDO as long as they contribute for the projects in the long-term vision 

4. __Can I get reward when sharing the AptosPad__

Yes, We have the referential mechanism, please check more [detail here](#the-referential-system)

5. __What is the SharePad and how It works__

SharePad is the mechanism that allow a projects to sell their IDO tokens not only on AptosPad but also on others AptosPad’s launchpad partners. Please check more detail information [here](#how-sharepad-works)

6. __How can I buy AptosPad token__

You can buy AptosPad token on AptosPad.com when AptosPad opens the first IDO. The IDOs time and whitelist will be published on official media channels such as website, discord, twitter. 

7. __How can I buy IDO token__

You can buy IDOs tokens if you are in the whitelist and have enough tickets. The opening time, refund and other policies will depend on each project and public before the selling time.

8. __Can I buy more IDO token than my ticket__

Yes, but the actual token you can claim may be decided only after the IDOs end. The Overbuy mechanism allows you to buy more than the maximum number of allocation, this helps satisfy the users demand and also the project target. If the total fundraising does not exceed the maximum target (hardcap), you can keep your overbuy amount. If It exceeds the hardcap, the refund will be triggered. 
 
9. __How refund mechanism work__

The refund mechanism protects users in case the project cannot meet some certain condition (such as cannot reach the softcap). It may also be triggered incase of an overbuy process.

10. __When APD get listed on exchanges__

After the IDOs, APD will be listed on some Aptos DEX. The CEX will be listed later (2023) after We reach an agreement with the exchanges.


<!--

**Here are some ideas to get you started:**

🙋‍♀️ A short introduction - what is your organization all about?
🌈 Contribution guidelines - how can the community get involved?
👩‍💻 Useful resources - where can the community find your docs? Is there anything else the community should know?
🍿 Fun facts - what does your team eat for breakfast?
🧙 Remember, you can do mighty things with the power of [Markdown](https://docs.github.com/github/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax)
-->
