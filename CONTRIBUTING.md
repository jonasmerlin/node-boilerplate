# Contributing to This Repo

## Commits

This repo uses [Conventional Commits](https://www.conventionalcommits.org) to make it easier to follow what changes between versions without having to dig deep into the code.

To make following the Conventional Commits guidelines easy, we use [husky](https://github.com/typicode/husky) to run a git hook that basically aliases `git commit` to use [commitizen](http://commitizen.github.io/cz-cli/), which makes this easy.

**PLEASE TAKE THIS SERIOUSLY!** Use `git commit` from the command line and then carefully think about the questions commitizen asks you. If you don't know the answers, talk to the maintainer. If you can't decide if your commit merits a longer description in addition to the basic commit message, it probably does.

### Comit Messages

For commit messages, we follow the suggestions outlined by [this article](https://chris.beams.io/posts/git-commit/).
Though it's strongly encouraged to read it, here are the most important parts from it that commitizen won't remember for you:

- Use present tense
- Use the imperative mood
- Begin your commit message with a capital letter
- Don't end on a period
- Describe _what_ the commit does in the subject line
- Describe _why_ the commit does this in the message body
- Don't describe _how_ this is done, the code should do this by itself

(Basically, the first two of these would be good examples of what we are aiming for here.)

The line from the article that made this click for me personally:

> A properly formed Git commit subject line should always be able to complete the following sentence:

> - If applied, this commit will <_your subject line here_>

_Again: All this may seem like a lot for something so basic, but makes it much easier to reason about what is happening with the code in this repo - for other contributors as well as users of the code._

Also, following these guidelines allows us to automatically generate a [changelog](https://keepachangelog.com/en/1.0.0/) for releases using [`standard-version`](https://github.com/conventional-changelog/standard-version). This makes keeping up with the progress of this repo even easier.

### Branching

For branching, we use the time-tested Gitflow model, first laid out [here](https://nvie.com/posts/a-successful-git-branching-model/). A Bitbucket specific overview can be found [here](https://www.atlassian.com/git/tutorials/comparing-workflows/gitflow-workflow). (But be aware that the `git-flow` tool the Getting Started section recommends doesn't seem to exist anymore, and we won't use it.)

### Coding Style

This repo follows the [StandardJS Style](https://standardjs.com/). To ensure this, a pre-commit hook is run that uses [lint-staged](https://github.com/okonet/lint-staged) to first reformat staged files using [Prettier](https://prettier.io/) (mainly for line-length) and then runs `standard --fix` on the reformatted code. This ensures that all code that gets committed reads in as similar a way as possible.

In addition, the usage of an editor extension like [vscode-standardjs](https://marketplace.visualstudio.com/items?itemName=chenxsan.vscode-standardjs) is recommended.
