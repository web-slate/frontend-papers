## Contributing

Welcome to Frontend Paper Docs. Below are the guidelines. Happy Coding !

### Commit Message Format
Each commit message consists of a simple pattern.  Below is the
format that includes a **type**, a **scope**, a **story-id** and a **subject** and every Pull Request's commit should be squashed.

```
<type>(<scope>): <subject or your message>
```

## Commit Message Guidelines
Guidelines gives precise rules over how our git commit messages can be formatted.  This leads to **more
readable messages** that are easy to follow when looking through the **project history**.  But also,
we use the git commit messages to **generate the App change log**.

### Revert
If the commit reverts a previous commit, it should begin with `revert(<scope>): #Story-ID - Your Message `, followed by the header of the reverted commit. In the body it should say: `This reverts commit <hash>.`, where the hash is the SHA of the commit being reverted.

### Type
Must be one of the following:

* **build**: Changes that affect the build system or external dependencies (example scopes: gulp, broccoli, npm)
* **ci**: Changes to our CI configuration files and scripts (example scopes: Circle, BrowserStack, SauceLabs)
* **docs**: Documentation only changes

### Scope
The scope should be the name of the modules / directory affected (as perceived by the person reading the changelog generated from commit messages).

The following is the list of supported scopes:

* **client/html** - HTML docs
* **client/css3** - CSS3 docs
* **client/es6-10** - ES6 to 10 docs
* **server/node** - node docs
* **js-framework/react** - react docs
* **css-framework/material-ui** - react docs
* **bundlers/webpack** - Webpack docs
* **devops/docker** - Docker docs
* **js-test/jest** - JEST docs