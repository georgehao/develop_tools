# Commitizen 使用介绍

## Commitizen是一个撰写合格 Commit message 的工具。


安装命令(全局):

    npm install -g commitizen

在home目录创建一个.czrc的配置文件,将commitizen进行一个全局的指向.

    echo '{ "path": "cz-conventional-changelog" }' > ~/.czrc


这样就配置好了! 现在你可以进入任何git repository, 并且使用`git cz` 替代 `git commit` 命令.

Protip: You can use all the git commit options with git cz, for example: `git cz -a`

![静态](https://raw.githubusercontent.com/commitizen/cz-cli/master/meta/screenshots/add-commit.png)
![动态](http://i.imgur.com/D6lFxHQ.gif)

## Commit Message Format

* A commit message consists of a header, body and footer.
* The header has a type and a subject:

```
    {{ type }}: {{ subject }}
    <BLANK LINE>
    {{ body }}
    <BLANK LINE>
    {{ breaking changes }}
    <BLANK LINE>
    {{ footer }}
```

The header is mandatory and the scope of the header is optional.

Any line of the commit message cannot be longer 100 characters! This allows the message to be easier to read on GitHub as well as in various git tools.


## Type
Must be one of the following:

* feat: A new feature.
* fix: A bug fix.
* docs: Documentation only changes.
* style: Changes that do not affect the meaning of the code (white-space, formatting, missing semi-colons, etc).
* refactor: A code change that neither fixes a bug or adds a feature.
* perf: A code change that improves performance.
* test: Adding missing tests.
* chore: Changes to the build process (grunt) or auxiliary tools and libraries such as documentation generation and linters (jshint, etc.)

## Subject
The subject contains succinct description of the change:

* Use the imperative, present tense: "change" not "changed" nor "changes"
* Don't capitalize first letter
* No dot (.) at the end.

## Body
Just as in the subject, use the imperative, present tense: "change" not "changed" nor "changes". The body should include the motivation for the change and contrast this with previous behavior.

## Breaking Changes
Breaking Changes should start with the word BREAKING CHANGE: with a space or two newlines.

## Footer
The footer is the place to reference any tasks that this commit Closes.



# 参考:


  [1] [Commitizen](https://github.com/commitizen/cz-cli)

  [2] [rb-conventional-changelog](https://www.npmjs.com/package/rb-conventional-changelog)

  [3] [Commit message 和 Change log 编写指南](http://www.ruanyifeng.com/blog/2016/01/commit_message_change_log.html)
