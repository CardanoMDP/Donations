# Donations - Community Audited Donation Proofs

Agregate Leaderboards:
[USD](https://raw.githubusercontent.com/CardanoMDP/Donations/live/donations.usd) 
[ADA](https://raw.githubusercontent.com/CardanoMDP/Donations/live/donations.ada)

MDP Total:
[USD](https://raw.githubusercontent.com/CardanoMDP/Donations/live/totals.usd) 
[ADA](https://raw.githubusercontent.com/CardanoMDP/Donations/live/totals.ada)

## Motivation
We want to increase the credibility of published donations. This can be done in many ways, some fancy others simpler. The only bulletproof way is to make charities publish Cardano addresses so that SPOs can show that they actually sent money to that specific charity. Unfortunately this is a solution that is a very long way of. To have a standardized information pool about donations and at least enable some degree of trust and auditability in that, we created this repository.

## Methodology

You cannot merge on your own to this repository (even admins cannot), you need to submit a PR which will be reviewed by the CI and one member of the CardanoMDP github organization (see: [Members List](https://github.com/orgs/CardanoMDP/people)).

### Steps

1. Fork this repo
1. In your fork:
   1. Create a folder named like your pool's `Ticker`
   1. Add your donation files
      ![image](https://user-images.githubusercontent.com/1410379/111878164-598eb300-89a7-11eb-88bc-ee1294b3cf97.png)
   2. Create a `donations.yml` (see: [example.donations.yml](./example.donations.yml))
      If you are unfamiliar with Yaml check out [this 5 minute tutorial](https://gettaurus.org/docs/YAMLTutorial/)
   4. Submit a pull request.
1. Once a pull request is created the members of the `CardanoMDP` github organization will be notified
   1. If you want a specific member of that list to review your submission you can select a specific reviewer in the top left corener of the pull request view.
      ![image](https://user-images.githubusercontent.com/1410379/111878531-eafe2500-89a7-11eb-96f0-e4be590453ee.png)
1. Make suree the CI tests pass. If the middle check in your PR is red there are errors in your donations.yml that you need to fix
   ![image](https://user-images.githubusercontent.com/1410379/111880094-ab383d00-89a9-11eb-9e34-fdba9a43e14f.png)
   Click on `details` to see what check went wrong (typically either a file reference is incorrect or a required field is missing).


## Data Structure

This repository is meant to represent a dedicated space to each SPO. The intended folder structure is as follows

```
-| TICKER
    |- donations.yml (required)
    |- donation-proof-2020-12.jpg <- You will be referencing these images. You are free to name them as you like.
    |- donation-proof-2021-01.jpg
    |- donation-proof-2021-02.jpg
    |- Some_Folder <- you can also organize your extra files in folders, just don't forget to add the folder names to the paths in donations.json
 | TICKER
 | TICKER
 | TICKER
 | TICKER
 | TICKER
 | TICKER
```

## Examples

For a documented example see [example.donations.yml](./example.donations.yml).

For a realworld example see the [SPEC](./SPEC) folder.


## Validating Dontations

If you have been given write permissions to `CardanoMDP/Donations` you can now aprove Pull Requests. To do this, please keep the following things in mind.

* Check that the uploaded receipts identify the name of the operator or the pool
* Check that the dates match (timezone issue might arise here)
* Importantly Check the reported values that are being claimed

Some other things to keep in mind are:

* Is this receipt unique? Ideally a receipt should have some sort of official tx id
* Is the receiving party a real charity (they should have a website and ideally some sort of bank account info)
* Is there a possibility the operator is paying themselves?

Formating checks:

* Ensure that `ada` and `usd` values are `dot` denominated `42.1` is fine, ~`42,1`~ is not!



## Keeping your repository up to date with the upstream repository (CardanoMDP/Donations)

When you submit a PR, if your submitted branch isn't up to date with the `CardanoMDP/Donations` repository we will not be able to merge your PR. 
Because of that you need to make sure that your forked repo is up to date with with ours.

Two ways of doing this:

* Using the github page of your repository
* Using github CLI



1. Using the github page of your repository
   1. Go to the webpage of your repository (example: `https://github.com/github-name/forked-repository`) 
   2. Press Fetch Upstream
   3. Press Fetch and merge
![image](https://user-images.githubusercontent.com/38225333/129491626-c2f7742b-bfb7-492e-a51f-2be788856e1a.png)

2. Using the github CLI
   1. Navigate to the root of your repository with terminal
   2. Add the upstream repository `git remote add upstream git://github.com/CardanoMDP/Donations.git`
   3. Fetch upstream `git fetch upstream`
   4. Merge upstream main branch with your main branch `git merge upstream/main main` 



