# Желание внести свой вклад в Create React App

Вам нравится приложение Create React App, и вы хотите принять в нем участие? - Спасибо! Есть много способов помочь.

Пожалуйста, найдите время просмотреть весь документ, чтобы сделать процесс участия простым и эффективным для всех участников.

Следование этим рекомендациям поможет понять, что вы уважаете время разработчиков, управляющих этим проектом с открытым исходным кодом, и разрабатывающих его. В свою очередь, они должны ответить вам взаимностью при рассмотрении вашей проблемы или оценке ваших исправлений и функций.

## Основные идеи

Насколько это возможно, мы стараемся избегать добавления конфигурации и флагов. Цель этого инструмента - обеспечить лучшим опытом людей, начинающих работу с React, и это всегда будет нашим главным приоритетом. Это означает, что иногда мы [жертвуем дополнительной функциональностью](https://gettingreal.37signals.com/ch05_Half_Not_Half_Assed.php) (например, серверным рендерингом), поскольку это слишком сложно решить, не требуя никакой настройки.

Мы предпочитаем **условность, эвристику или интерактивность** - конфигурации.<br>
Вот несколько таких примеров в действии.

### Условность

<!--alex disable easy-->

Вместо того, чтобы позволить пользователю указать имя файла записи, мы всегда предполагаем, что это `src/index.js`. Вместо того, чтобы позволять пользователю указывать имя выходного пакета, мы его генерируем, но обязательно включаем в него хэш содержимого. Когда это возможно, мы хотим использовать соглашения, чтобы сделать правильный выбор для пользователя, особенно в тех случаях, когда что-то легко настроить неправильно.

### Эвристика

Обычно `npm start` работает на порте `3000`, и это не может быть явно настроено. Однако некоторые среды, такие как облачные IDE - хотят, чтобы программы запускались на определённом порту для обслуживания их вывода. Мы хотим хорошо работать с различными средами, поэтому приложение Create React App считывает переменную среды `PORT`, когда она указана и предпочитает именно её.
Зная, что облачные IDE задают этот порт автоматически, пользователю ничего делать уже не нужно. Хитрость в том, что Create React App, полагаясь на эвристику, сам выберет правильные действия в зависимости от среды.

<!--alex disable just-->

Другой пример - как обычно `npm test` запускает наблюдатель, но если переменная среды `CI` установлена, она запустит тесты один раз.
Мы знаем, что популярные среды CI устанавливают эту переменную, поэтому пользователю не нужно ничего делать. Просто работать.

### Интерактивность

Мы предпочитаем добавлять интерактивность в интерфейс командной строки, а не добавлять флаги конфигурации. Например, `npm start` будет пытаться работать с портом` 3000` по умолчанию, но в случае его занятости зависимые от этого инструменты запросят выдать другой порт и лишь Create React App отобразит запрос и предложит запустить приложение на следующем доступном порту.

Другой пример интерактивности - интерфейс наблюдателя `npm test`. Вместо того, чтобы просить людей передать флаги командной строки для переключения между режимами выполнения тестов или шаблонами поиска, мы печатаем подсказку с клавишами, нажимаемыми во время сеанса тестирования с указанием действий наблюдателю. Jest поддерживает как флаги, так и интерактивный интерфейс командной строки, но приложение Create React App предпочитает длительные сеансы, оставляя пользователя погруженным в поток в течение коротких сеансов с разными флагами.

### Нарушение правил

Нет идеальных правил. Иногда мы можем вводить флаги или конфигурацию считая их значение достаточно великим, чтобы оправдать сложность. Например, мы знаем, что у приложений могут быть размещены пути, отличные от корневого, и нам необходимо поддерживать этот вариант использования. Однако мы по прежнему стараемся прибегать к эвристике, когда это возможно. В этом примере мы просим вас указать `homepage` в` package.json` и вывести правильный путь на его основе. Мы также подталкиваем пользователя заполнить `homepage` после сборки, чтобы пользователь узнал, что функция существует.

## Отправка запроса на извлечение

Хорошие запросы на вытягивание, такие как исправления, улучшения и новые функции, являются фантастическим подспорьем. Они должны оставаться сфокусированными по своему охвату и избегать несвязанных коммитов.

Пожалуйста, **сначала спросите**, работает ли кто-то еще над этим или основные разработчики думают, что ваша функция входит в область действия приложения Create React App.   
Как правило, всегда есть связанная с этим проблема обсуждения того, что вы включаете.

Также предоставьте **план тестирования**, т.е. покажите надёжность работы вашего дополнения.

## Структура папок Create React App

`create-react-app` - это монорепозиторий, то есть он разделён на независимые подпакеты.<br>
Эти пакеты можно найти в каталоге [`packages/`](https://github.com/facebook/create-react-app/tree/master/packages).

### Обзор структуры каталогов

```
packages/
  babel-preset-react-app/
  create-react-app/
  eslint-config-react-app/
  react-dev-utils/
  react-scripts/
```

### Package Descriptions

#### [babel-preset-react-app](https://github.com/facebook/create-react-app/tree/master/packages/babel-preset-react-app)

This package is a babel preset intended to be used with `react-scripts`.<br>
It targets platforms that React is designed to support (IE 11+) and enables experimental features used heavily at Facebook.<br>
This package is enabled by default for all `create-react-app` scaffolded applications.

#### [create-react-app](https://github.com/facebook/create-react-app/tree/master/packages/create-react-app)

The global CLI command code can be found in this directory, and shouldn't often be changed. It should run on Node 0.10+.

#### [eslint-config-react-app](https://github.com/facebook/create-react-app/tree/master/packages/eslint-config-react-app)

This package contains a conservative set of rules focused on making errors apparent and enforces no style rules.<br>
This package is enabled by default for all `create-react-app` scaffolded applications.

#### [react-dev-utils](https://github.com/facebook/create-react-app/tree/master/packages/react-dev-utils)

This package contains utilities used for `react-scripts` and sibling packages.<br>
Its main purpose is to conceal code which the user shouldn't be burdened with upon ejecting.

#### [react-scripts](https://github.com/facebook/create-react-app/tree/master/packages/react-scripts)

This package is the heart of the project, which contains the scripts for setting up the development server, building production builds, configuring all software used, etc.<br>
All functionality must be retained (and configuration given to the user) if they choose to eject.

## Setting Up a Local Copy

1. Clone the repo with `git clone https://github.com/facebook/create-react-app`

2. Run `yarn` in the root `create-react-app` folder.

Once it is done, you can modify any file locally and run `yarn start`, `yarn test` or `yarn build` like you can in a generated project.

If you want to try out the end-to-end flow with the global CLI, you can do this too:

```sh
yarn create-react-app my-app
cd my-app
```

and then run `yarn start` or `yarn build`.

## Contributing to E2E (end to end) tests

**TL;DR** use the command `yarn e2e:docker` to run unit and e2e tests.

More detailed information are in the dedicated [README](/test/README.md).

### CI testing with private packages

**create-react-app** relies on main registry to fetch all dependencies, but, if you are in the need to usage of custom private packages that need to be fetch while running E2E test you might need a different configuration.

#### Customizing E2E registry configuration

We use [verdaccio](https://github.com/verdaccio/verdaccio) to emulate packages publishing in a registry using a default configuration. You might modify the current behaviour by editing the file `task/verdaccio.yaml`.

For more information about the configuration check out the [Verdaccio documentation](https://verdaccio.org/docs/en/configuration).

## Tips for contributors using Windows

The scripts in tasks folder and other scripts in `package.json` will not work in Windows out of the box. However, using [Bash on windows](https://msdn.microsoft.com/en-us/commandline/wsl/about) makes it easier to use those scripts without any workarounds. The steps to do so are detailed below:

### Install Bash on Ubuntu on Windows

A good step by step guide can be found [here](https://www.howtogeek.com/249966/how-to-install-and-use-the-linux-bash-shell-on-windows-10/)

### Install Node.js and yarn

Even if you have node and yarn installed on your windows, it would not be accessible from the bash shell. You would have to install it again. Installing via [`nvm`](https://github.com/creationix/nvm#install-script) is recommended.

### Line endings

By default git would use `CRLF` line endings which would cause the scripts to fail. You can change it for this repo only by setting `autocrlf` to false by running `git config core.autocrlf false`. You can also enable it for all your repos by using the `--global` flag if you wish to do so.

## Cutting a Release

1. Tag all merged pull requests that go into the release with the relevant milestone. Each merged PR should also be labeled with one of the [labels](https://github.com/facebook/create-react-app/labels) named `tag: ...` to indicate what kind of change it is. **Make sure all breaking changes are correctly labelled with `tag: breaking change`.**
2. Close the milestone and create a new one for the next release.
3. In most releases, only `react-scripts` needs to be released. If you don’t have any changes to the `packages/create-react-app` folder, you don’t need to bump its version or publish it (the publish script will publish only changed packages).
4. Note that files in `packages/create-react-app` should be modified with extreme caution. Since it’s a global CLI, any version of `create-react-app` (global CLI) including very old ones should work with the latest version of `react-scripts`.
5. Run `yarn compile:lockfile`. The command will generate an updated lockfile in `packages/create-react-app` that should be committed.
6. Create a change log entry for the release:

- You'll need an [access token for the GitHub API](https://help.github.com/articles/creating-an-access-token-for-command-line-use/). Save it to this environment variable: `export GITHUB_AUTH="..."`
- Run `yarn changelog`. The command will find all the labeled pull requests merged since the last release and group them by the label and affected packages, and create a change log entry with all the changes and links to PRs and their authors. Copy and paste it to `CHANGELOG.md`.
- Add a four-space indented paragraph after each non-trivial list item, explaining what changed and why. For each breaking change also write who it affects and instructions for migrating existing code.
- Maybe add some newlines here and there. Preview the result on GitHub to get a feel for it. Changelog generator output is a bit too terse for my taste, so try to make it visually pleasing and well grouped.

7. Make sure to include “Migrating from ...” instructions for the previous release. Often you can copy and paste them.
8. Run `npm run publish`. (It has to be `npm run publish` exactly, not `npm publish` or `yarn publish`.)
9. Wait for a long time, and it will get published. Don’t worry that it’s stuck. In the end the publish script will prompt for versions before publishing the packages.
10. After publishing, create a GitHub Release with the same text as the changelog entry. See previous Releases for inspiration.

Make sure to test the released version! If you want to be extra careful, you can publish a prerelease by running `npm run publish -- --canary --exact --preid next --dist-tag=next --force-publish=* minor` instead of `npm run publish`.

## Releasing the Docs

1. Go to the `docusaurus/website` directory
2. Run `yarn build`
3. You'll need an [access token for the GitHub API](https://help.github.com/articles/creating-an-access-token-for-command-line-use/). Save it to this environment variable: `export GITHUB_AUTH="..."`
4. Run `GIT_USER=<GITHUB_USERNAME> CURRENT_BRANCH=master USE_SSH=true yarn deploy`

---

_Many thanks to [h5bp](https://github.com/h5bp/html5-boilerplate/blob/master/.github/CONTRIBUTING.md) for the inspiration with this contributing guide_
