# play-with-clog
Simple repo to play around with clog

## Needed to make clog work

### Commit Message Format

Each commit message consists of a **header**, a **body** and a **footer**.  The header has a special
format that includes a **type**, a **scope** and a **subject**:

```
<type>(<scope>): <subject>
<BLANK LINE>
<body>
<BLANK LINE>
<footer>
```

Any line of the commit message cannot be longer 100 characters! This allows the message to be easier
to read on github as well as in various git tools.

### Type

Must be one of the following:

* **feat**: A new feature
* **fix**: A bug fix
* **docs**: Documentation only changes
* **style**: Changes that do not affect the meaning of the code (white-space, formatting, missing
  semi-colons, etc)
* **refactor**: A code change that neither fixes a bug or adds a feature
* **perf**: A code change that improves performance
* **test**: Adding missing tests
* **chore**: Changes to the build process or auxiliary tools and libraries such as documentation
  generation

### Scope

The scope could be anything specifying place of the commit change. For example `$location`,
`$browser`, `$compile`, `$rootScope`, `ngHref`, `ngClick`, `ngView`, etc...

### Subject

The subject contains succinct description of the change:

* use the imperative, present tense: "change" not "changed" nor "changes"
* don't capitalize first letter
* no dot (.) at the end

### Body

Just as in the **subject**, use the imperative, present tense: "change" not "changed" nor "changes"
The body should include the motivation for the change and contrast this with previous behavior.

### Footer

The footer should contain any information about **Breaking Changes** and is also the place to
reference GitHub issues that this commit **Closes**.

**Breaking Changes** are detected as such if the footer contains a line starting with BREAKING CHANGE:
(with optional newlines) The rest of the commit message is then used for this.


## Simple Commands

```
clog -f <commitid>
```

Generates Changelogs and prints them into the specified `outfile`:
```
clog -r https://github.com/jbellmann/play-with-clog --outfile only_new.md
```

Generate Changelogs starting from specific commit:
```
clog -f 346fbf7
```

Maybe we have to specify issues different than in github-markdown.
OR with double-quotes? No
OR with keywords like Closes|Fixes|Resolves ?
No again with only a number, no # in front of it.
So 'Closes' seems to work somehow
  Will try next with 'Closes' in subject, uppercase does not work, lowercase does not work
  Will try next with 'Closes' in body, 
    lowercase starting body does not work,
    starting uppercase 'Closes #3' works,
    in the body somewhere in the body also works
  Will try next with 'Closes' in footer,
    starting lowercase does not work
    starting uppercase and using 'Fixes #3' works
    uppercase in between the text in footer also works



