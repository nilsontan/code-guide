---
title: Heroku
---

# Heroku
## Manage multiple accounts
### Install
```bash
$ heroku plugins:install heroku-accounts
```
### Usage
To add accounts:
```bash
$ heroku accounts:add personal
Enter your Heroku credentials.
Email: user@heroku.com
Password: ******
```
To add single sign-on (SSO) accounts:
```bash
$ heroku accounts:add work --sso
Enter your organization name: my-company-name
Opening browser for login... done
Enter your access token (typing will be hidden): **********************************
```
To switch to a different account:
```bash
$ heroku accounts:set personal
```
To list accounts:
```bash
$ heroku accounts
* personal
work
```
To find current account:
```bash
$ heroku accounts:current
personal
```
To remove an account:
```bash
$ heroku accounts:remove personal
Account removed: personal
```