# PackageAutoPublish

## repo.yml

This file contains all repo urls. Pull from url then publish one by one.

It will skip to publish if Package already exist(or version).

Example:
```
repositories:
  - url: https://github.com/your/repo1.git
    directory: src1
  - url: https://github.com/your/repo2.git
    directory: src2
  - url: https://github.com/your/repo3.git
    directory: src3
```

`directory` refers to the directory path under the `package.json` file.

## Secrets
Before you run the action,go repo settings, add secrets below:
- NPMRC
- NPM_URL

### NPMRC
[.npmrc](https://docs.npmjs.com/cli/v10/configuring-npm/npmrc) file content.

Example like this:
```
//npm.pkg.github.com/:_authToken=TOKEN
@Github-User-Name:registry=https://npm.pkg.github.com/
```

### NPM_URL
Your target registry url, like this: 
`https://npm.pkg.github.com/@Github-User-Name`
