---
title: Npm / Yarn
---

# Npm / Yarn
To install packages in package.json use
```bash
npm install
yarn install
```

## Install
```bash
npm i -g <pkg...>
yarn global add <pkg...>
```
install package-name globally

```bash
npm i <pkg...> --save
yarn add <pkg...>
```
install in dependencies

```bash
npm i <pkg...> --save-dev
yarn add <pkg...> -D
```
install in development dependencies

```bash
npm i <pkg>@version
yarn add <pkg>@version
```
install at version

```bash
npm uninstall <pkg>
yarn remove <pkg>
```
uninstall

## List
```bash
npm ls (-g) (--depth=0)
yarn list (--depth=0)
```
list packages (globally) (by depth)

## Update
```bash
npm outdated
yarn outdated
```
list all outdated packages

```bash
npm update <pkg>
yarn upgrade <pkg>
```
update package

```bash
npm install -g npm-check-updates
ncu -u
npm update
```
to update to a new major version for all the packages, instead install `npm-check-updates` then run it before updating all packages.

> warning: might break the code