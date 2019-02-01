---
title: Heroku
---

# Heroku
## Manage multiple accounts
### Install
```js
$ heroku plugins:install heroku-accounts
```
### Usage
To add accounts:
```js
$ heroku accounts:add personal
Enter your Heroku credentials.
Email: user@heroku.com
Password: ******
```
To add single sign-on (SSO) accounts:
```js
$ heroku accounts:add work --sso
Enter your organization name: my-company-name
Opening browser for login... done
Enter your access token (typing will be hidden): **********************************
```
To switch to a different account:
```js
$ heroku accounts:set personal
```
To list accounts:
```js
$ heroku accounts
* personal
work
```
To find current account:
```js
$ heroku accounts:current
personal
```
To remove an account:
```js
$ heroku accounts:remove personal
Account removed: personal
```