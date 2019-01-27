---
title: Npm / Yarn
---

# Npm / Yarn
To install packages in package.json use
```js
npm install
yarn install
```

## Install
```js
npm i -g <pkg...>
yarn global add <pkg...>
```
install package-name globally

```js
npm i <pkg...> --save
yarn add <pkg...>
```
install in dependencies

```js
npm i <pkg...> --save-dev
yarn add <pkg...> -D
```
install in development dependencies

```js
npm i <pkg>@version
yarn add <pkg>@version
```
install at version

```js
npm uninstall <pkg>
yarn remove <pkg>
```
uninstall

## List
```js
npm ls (-g) (--depth=0)
yarn list (--depth=0)
```
list packages (globally) (by depth)

## Update
```js
npm outdated
yarn outdated
```
list all outdated packages

```js
npm update <pkg>
yarn upgrade <pkg>
```
update package

```js
npm install -g npm-check-updates
ncu -u
npm update
```
to update to a new major version for all the packages, instead install `npm-check-updates` then run it before updating all packages.

> warning: might break the code