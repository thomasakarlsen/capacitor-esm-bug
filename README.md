# Capacitor ESM bug

Reproduction repository for: https://github.com/ionic-team/capacitor/issues/7259

Somehow when starting a new project with `ionic start --type=vue` the resulting yarn.lock file and dependency graph is completely messed up making it so that the capacitor cli is unable to work.

## Versions used
npm: 10.2.3

node: 18.19.0 

yarn: 1.22.21

## Steps to reproduce the capacitor issue:
1. Create a new ionic app with `ionic start --type=vue`

During the creation of the app you should get the ESM error when ionic-cli is trying to init capacitor.

## Steps to reproduce the yarn issue:
1. Run `yarn install` in the root of this repository, or delete the `node_modules` folder and run `yarn install` in the root of the ionic app created with `ionic start --type=vue`

## Temporary solution to both issues
It seems like deleting the yarn.lock file and running `yarn install` again fixes the issue and the capacitor cli is able to work as expected.
