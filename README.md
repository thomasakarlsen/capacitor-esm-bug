# Capacitor ESM bug

Reproduction repository for: https://github.com/ionic-team/capacitor/issues/7259

## Steps to reproduce
1. Install dependencies using yarn (`yarn install`)
2. Run `ionic capacitor run android`

## Alternative issue:
It seems like when running `yarn install` you get a similar error but for cypress instead.
For now it seems like the best way to reproduce the issue is to run `ionic start --type=vue` locally to create a new app.
