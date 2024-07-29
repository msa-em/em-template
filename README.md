# Elemental Microscopy

This repository contains the article template for an `Elemental Microscopy` article. It also contains several examples of interactive figures:

## Images
 <img src="/figures/demo_image_small.gif" alt="image widget example" width="360">

## Movies
 <img src="/figures/demo_movie_smaller.gif" alt="movie widget example" width="360">

## 3D Volumes
 <img src="/figures/demo_3d_small.gif" alt="3d volume widget example" width="360">


## People

This template was developed by [Colin Ophus](mailto:cophus@gmail.com) and [Georgios Varnavides](mailto:gvarnavides@berkeley.edu). 

## Installation Instructions

### Edit locally and push changes

> [!WARNING]
> First, ask one of the organization members to give you `write` access to the repo.

Steps to edit locally:
- git clone repo (`git clone git@github.com:msa-em/em-template.git`)
- switch to `dev` branch (`git checkout dev`)
- create virtual environment (`conda env create -f environment.yml`)
  - you might need to remove the environment if it already exists (`conda remove -n em-template --all`)
- activate virtual environment in two terminal windows (`conda activate em-template`)
- edit `myst.yml` file by:
  - commenting these lines out
  ```yml
    jupyter: true
  ```
  - uncommenting these lines
  ```yml
  #  jupyter:
    #    server:
    #      url: 'http://localhost:8888'
    #      token: '512ac78f14e1141db1fac17e8b4099c1e5bc7d589518b38c'
  ```
- start the jupyter server in one of the terminal windows (`jupyter lab --IdentityProvider.token=512ac78f14e1141db1fac17e8b4099c1e5bc7d589518b38c --ServerApp.allow_origin='http://localhost:3000' --port=8888`)
- start MyST in the other terminal window (`myst start`)
- edit, commit, and push to `dev` as per usual
  - make sure **NOT** to commit your `must.yml` changes!
- open a draft pull request into `main` (if one doesn't already exist) and keep pushing your changes to `dev`

> [!NOTE]
> If you don't plan on editing the notebooks, you can skip the `myst.yml` and `jupyter lab` steps above

## Preview draft deployed site
The repo has two github actions to automatically deploy computational sites, for the following two case:
- Commits to `main` directly
- Pull requests into `main`

If you followed the instructions above (i.e. working off of `dev` and have an open pull request into `main`), then you should see a `github-actions` bot at the top of your pull request which will keep getting edited.
Simply click on the `Inspect` link to see the curvenote staging site, and press `preview` to see the deployed site based on your latest commit.

