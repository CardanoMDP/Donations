# Donations - Community Audited Donation Proofs

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

## Data Structure

This repository is meant to represent a dedicated space to each SPO. The intended folder structure is as follows

```
-| TICKER
    |- donations.json (required)
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

