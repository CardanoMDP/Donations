# Donations - Community Audited Donation Proofs

We want to increase the credibility of published donations. While this can be done in many fancy ways and the only bulletproof way is to make charities publish Cardano addresses so that SPOs can show that they actually sent money to that specific charity this is a solution that is a very long way of. To have a standardized information pool about donations and at least enable some degree of trust and auditability in that, we created this repository.

## Methodology

You cannot merge on your own to this repository (even admins cannot), you need to submit a PR which will be reviewed by the CI and another member of the CMDP. In order to do this it is best for you to fork this repo to your personal github, add your files and then submit a PR.

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
