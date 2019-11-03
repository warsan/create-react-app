# Create React App [![Build Status](https://dev.azure.com/facebook/create-react-app/_apis/build/status/facebook.create-react-app?branchName=master)](https://dev.azure.com/facebook/create-react-app/_build/latest?definitionId=1&branchName=master) [![PRs Welcome](https://img.shields.io/badge/PRs-welcome-green.svg)](https://github.com/facebook/create-react-app/pulls)

Создавайте приложения React без конфигурации сборки.

- [Creating an App](#создание-приложения) – Как создать новое приложение.
- [User Guide](https://facebook.github.io/create-react-app/) – Как разрабатывать приложения, загруженные с помощью Create React App.

**Create React App** работает на MacOS, Windows и Linux.<br>
Если что-то не работает, пожалуйста, [сообщите о проблеме](https://github.com/facebook/create-react-app/issues/new).<br>
Если вам нужна помощь или у вас есть вопросы - пожалуйста, задайте их в нашем [Spectrum](https://spectrum.chat/create-react-app) сообществе.

## Краткая информация

```sh
npx create-react-app my-app
cd my-app
npm start
```

_([npx](https://medium.com/@maybekatz/introducing-npx-an-npm-package-runner-55f7d4bd282b) поставляется с npm 5.2+ и выше, см. [инструкции для более старых версий npm](https://gist.github.com/gaearon/4064d3c23a77c74a3614c498a8bb1c5f))_

Затем откройте [http://localhost:3000/](http://localhost:3000/), чтобы увидеть ваше приложение.<br>
Когда будете готовы к развертыванию, создайте минимизированный пакет с `npm run build`.

<p align='center'>
<img src='https://cdn.jsdelivr.net/gh/facebook/create-react-app@27b42ac7efa018f2541153ab30d63180f5fa39e0/screencast.svg' width='600' alt='npm start'>
</p>

### Начните немедленно

Вам **не нужно** устанавливать или настраивать такие инструменты, как Webpack или Babel.<br>
Они предварительно настроены и скрыты, так что вы можете сосредоточиться на коде.

Создайте проект, и все готово.

## Создание приложения

**Для разработки вам понадобится Node 8.16.0 или Node 10.16.0 или более поздняя версия на вашем локальном компьютере** (но это не требуется на сервере). Вы можете использовать [nvm](https://github.com/creationix/nvm#installation) (macOS/Linux)  
или [nvm-windows](https://github.com/coreybutler/nvm-windows#node-version-manager-nvm-for-windows) для переключения версий Node между различными проектами.

Чтобы создать новое приложение, вы можете выбрать один из следующих методов:

### npx

```sh
npx create-react-app my-app
```

_([npx](https://medium.com/@maybekatz/introducing-npx-an-npm-package-runner-55f7d4bd282b) это инструмент для запуска пакетов, который поставляется с npm 5.2+ и выше, см. [instructions for older npm versions](https://gist.github.com/gaearon/4064d3c23a77c74a3614c498a8bb1c5f))_

### npm

```sh
npm init react-app my-app
```

_`npm init <initializer>` доступен в npm 6+_

### Yarn

```sh
yarn create react-app my-app
```

_`yarn create` доступен в Yarn 0.25+_

Он создаст каталог с именем `my-app` внутри текущей папки.<br>
Внутри этого каталога он сгенерирует исходную структуру проекта и установит переходные зависимости:

```
my-app
├── README.md
├── node_modules
├── package.json
├── .gitignore
├── public
│   ├── favicon.ico
│   ├── index.html
│   └── manifest.json
└── src
    ├── App.css
    ├── App.js
    ├── App.test.js
    ├── index.css
    ├── index.js
    ├── logo.svg
    └── serviceWorker.js
```

Нет конфигурации или сложной структуры папок, только файлы, необходимые для создания приложения.<br>
После завершения установки вы можете открыть папку вашего проекта:

```sh
cd my-app
```

Внутри недавно созданного проекта вы можете запустить несколько встроенных команд:

### `npm start` или `yarn start`

Запускает приложение в режиме разработки.<br>
Откройте [http://localhost:3000](http://localhost:3000), чтобы просмотреть его в браузере.

Страница автоматически перезагрузится, если вы внесете изменения в код.<br>
Вы увидите ошибки сборки и предупреждения lint в консоли.

<p align='center'>
<img src='https://cdn.jsdelivr.net/gh/marionebl/create-react-app@9f6282671c54f0874afd37a72f6689727b562498/screencast-error.svg' width='600' alt='Build errors'>
</p>

### `npm test` или `yarn test`

Запускает тестовый наблюдатель в интерактивном режиме.<br>
По умолчанию запускаются тесты, связанные с файлами, измененными с момента последней фиксации.

[Узнайте больше о тестировании.](https://facebook.github.io/create-react-app/docs/running-tests)

### `npm run build` или `yarn build`

Создает приложение для производства в папке `build`.<br>
Он корректно объединяет React в производственном режиме и оптимизирует сборку для лучшей производительности.

Сборка минимизирована, а имена файлов содержат хэши.<br>

Ваше приложение готово к развертыванию.

## Гид пользователя

You can find detailed instructions on using Create React App and many tips in [its documentation](https://facebook.github.io/create-react-app/).

## How to Update to New Versions?

Please refer to the [User Guide](https://facebook.github.io/create-react-app/docs/updating-to-new-releases) for this and other information.

## Philosophy

- **One Dependency:** There is only one build dependency. It uses Webpack, Babel, ESLint, and other amazing projects, but provides a cohesive curated experience on top of them.

- **No Configuration Required:** You don't need to configure anything. A reasonably good configuration of both development and production builds is handled for you so you can focus on writing code.

- **No Lock-In:** You can “eject” to a custom setup at any time. Run a single command, and all the configuration and build dependencies will be moved directly into your project, so you can pick up right where you left off.

## What’s Included?

Your environment will have everything you need to build a modern single-page React app:

- React, JSX, ES6, TypeScript and Flow syntax support.
- Language extras beyond ES6 like the object spread operator.
- Autoprefixed CSS, so you don’t need `-webkit-` or other prefixes.
- A fast interactive unit test runner with built-in support for coverage reporting.
- A live development server that warns about common mistakes.
- A build script to bundle JS, CSS, and images for production, with hashes and sourcemaps.
- An offline-first [service worker](https://developers.google.com/web/fundamentals/getting-started/primers/service-workers) and a [web app manifest](https://developers.google.com/web/fundamentals/engage-and-retain/web-app-manifest/), meeting all the [Progressive Web App](https://facebook.github.io/create-react-app/docs/making-a-progressive-web-app) criteria. (_Note: Using the service worker is opt-in as of `react-scripts@2.0.0` and higher_)
- Hassle-free updates for the above tools with a single dependency.

Check out [this guide](https://github.com/nitishdayal/cra_closer_look) for an overview of how these tools fit together.

The tradeoff is that **these tools are preconfigured to work in a specific way**. If your project needs more customization, you can ["eject"](https://facebook.github.io/create-react-app/docs/available-scripts#npm-run-eject) and customize it, but then you will need to maintain this configuration.

## Popular Alternatives

Create React App is a great fit for:

- **Learning React** in a comfortable and feature-rich development environment.
- **Starting new single-page React applications.**
- **Creating examples** with React for your libraries and components.

Here are a few common cases where you might want to try something else:

- If you want to **try React** without hundreds of transitive build tool dependencies, consider [using a single HTML file or an online sandbox instead](https://reactjs.org/docs/try-react.html).

- If you need to **integrate React code with a server-side template framework** like Rails, Django or Symfony, or if you’re **not building a single-page app**, consider using [nwb](https://github.com/insin/nwb), or [Neutrino](https://neutrino.js.org/) which are more flexible. For Rails specifically, you can use [Rails Webpacker](https://github.com/rails/webpacker). For Symfony, try [Symfony's Webpack Encore](https://symfony.com/doc/current/frontend/encore/reactjs.html).

- If you need to **publish a React component**, [nwb](https://github.com/insin/nwb) can [also do this](https://github.com/insin/nwb#react-components-and-libraries), as well as [Neutrino's react-components preset](https://neutrino.js.org/packages/react-components/).

- If you want to do **server rendering** with React and Node.js, check out [Next.js](https://github.com/zeit/next.js/) or [Razzle](https://github.com/jaredpalmer/razzle). Create React App is agnostic of the backend, and only produces static HTML/JS/CSS bundles.

- If your website is **mostly static** (for example, a portfolio or a blog), consider using [Gatsby](https://www.gatsbyjs.org/) instead. Unlike Create React App, it pre-renders the website into HTML at the build time.

- Finally, if you need **more customization**, check out [Neutrino](https://neutrino.js.org/) and its [React preset](https://neutrino.js.org/packages/react/).

All of the above tools can work with little to no configuration.

If you prefer configuring the build yourself, [follow this guide](https://reactjs.org/docs/add-react-to-an-existing-app.html).

## Contributing

We'd love to have your helping hand on `create-react-app`! See [CONTRIBUTING.md](CONTRIBUTING.md) for more information on what we're looking for and how to get started.

## React Native

Looking for something similar, but for React Native?<br>
Check out [Expo CLI](https://github.com/expo/expo-cli).

## Acknowledgements

We are grateful to the authors of existing related projects for their ideas and collaboration:

- [@eanplatter](https://github.com/eanplatter)
- [@insin](https://github.com/insin)
- [@mxstbr](https://github.com/mxstbr)

## License

Create React App is open source software [licensed as MIT](https://github.com/facebook/create-react-app/blob/master/LICENSE).
