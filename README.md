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

Подробные инструкции по использованию Create React App и многие советы можно найти в [её документации](https://facebook.github.io/create-react-app/).

## Как обновить до новой версии?

Для получения дополнительной информации см. [Руководство пользователя](https://facebook.github.io/create-react-app/docs/update-to-new-releases).

## Философия

- **Одна зависимость:** Существует только одна зависимость сборки. Она использует Webpack, Babel, ESLint и другие удивительные проекты, но обеспечивает сплоченный кураторский опыт поверх них.

- **Не требуется настройка:** Вам не нужно ничего настраивать. Достаточно хорошая конфигурация как разработки, так и производственных сборок обрабатывается для вас, поэтому вы можете сосредоточиться на написании кода.

- **Нет блокировки:** Вы можете “извлечь” в пользовательскую установку в любое время. Выполните одну команду, и все зависимости конфигурации и сборки будут перенесены непосредственно в ваш проект, чтобы продолжить работу с того места, где остановились.

## Что включено?

В вашей среде будет все необходимое для создания современного одностраничного приложения React:

- Поддержка синтаксиса React, JSX, ES6, TypeScript и Flow.
- Язык экстры за пределами ES6, как оператор распространения объекта.
- Autoprefixed CSS, где не нужны `-webkit-` или другие префиксы.
- Быстрый интерактивный модульный тестовый бегун со встроенной поддержкой отчетов о покрытии.
- Живой сервер разработки, предупреждающий о распространенных ошибках.
- Сценарий сборки для связывания JS, CSS и изображений для производства с хэшами и исходными картами.
- Офлайн-первый [сервисный работник](https://developers.google.com/web/fundamentals/getting-started/primers/service-workers) и [web app manifest](https://developers.google.com/web/fundamentals/engage-and-retain/web-app-manifest/), собрание всех [Progressive Web App](https://facebook.github.io/create-react-app/docs/making-a-progressive-web-app) критерий. _(Примечание: использование работника службы является опционом с момента `react-scripts@2.0.0-и выше)_
- Беспроблемные обновления для вышеуказанных инструментов с одной зависимостью.

Проверьте [это руководство](https://github.com/nitishdayal/cra_closer_look) для обзора того, как эти инструменты сочетаются друг с другом.

Компромисс заключается в том, что **эти инструменты предварительно настроены для работы определенным образом**. Если ваш проект нуждается в дополнительной настройке, вы можете ["извлечь"](https://facebook.github.io/create-react-app/docs/available-scripts#npm-run-eject) и настроить его, но тогда вам нужно будет поддерживать эту конфигурацию.

## Популярная альтернатива

Create React App отлично подходит для:

- **Изучения React** в удобной и многофункциональной среде разработки.
- **Запуск новых одностраничных приложений React.**
- **Создание примеров** с помощью React для ваших библиотек и компонентов.

Вот несколько распространенных случаев, когда вы можете попробовать что-то еще:

- Если вы хотите **попробовать React** без сотен переходных зависимостей инструмента построения, попробуйте [использовать один HTML-файл или сетевую изолированную среду вместо](https://reactjs.org/docs/try-react.html).

- Если вам нужно **интегрировать React code с серверным фреймворком шаблонов**, таким как Rails, Django или Symfony, или если вы **не собираете одностраничное приложение**, подумайте об использовании [nwb](https://github.com/insin/nwb) или [Neutrino](https://neutrino.js.org/), которые являются более гибкими. Специально для Rails можно использовать [Rails Webpacker](https://github.com/rails/webpacker). Для Symfony попробуйте [Symfony's Webpack Encore](https://symfony.com/doc/current/frontend/encore/reactjs.html).

- Если вам нужно **публиковать React компонент**, используйте [nwb](https://github.com/insin/nwb), ещё можно [сделать это и здесь](https://github.com/insin/nwb#react-components-and-libraries), а также [предустановкой реактивных компонентов Нейтрино](https://neutrino.js.org/packages/react-components/).

- Если вы хотите сделать **серверный рендеринг** с помощью React и Node.js, посмотрите [Next.js](https://github.com/zeit/next.js/) или [Razzle](https://github.com/jaredpalmer/razzle). Create React App является агностичным по отношению к бэкэнду и производит только статические HTML/JS/CSS пакеты.

- Если ваш сайт **почти статичен** (например, портфолио или блог), подумайте об использовании [Gatsby](https://www.gatsbyjs.org/) вместо него. В отличие от Create React App, он предварительно возвращает сайт в HTML во время сборки.

- Наконец, если вам нужна **дополнительная настройка**, посмотрите [Neutrino](https://neutrino.js.org/) и его [React preset](https://neutrino.js.org/packages/react/).

Все вышеупомянутые инструменты могут работать практически без конфигурации.

Если вы предпочитаете настроить сборку самостоятельно, [следуйте этому руководству](https://reactjs.org/docs/add-react-to-an-existing-app.html).

## Содействие

Мы рады получить вашу помощь в `create-react-app`! См. [CONTRIBUTING.md](CONTRIBUTING.md) для получения дополнительной информации о том, что мы ищем и как начать работу.

## React Native

Ищете что-то похожее, но для React Native?<br>
Проверьте [Expo CLI](https://github.com/expo/expo-cli).

## Благодарности

Мы благодарны авторам существующих сопутствующих проектов за их идеи и сотрудничество:

- [@eanplatter](https://github.com/eanplatter)
- [@insin](https://github.com/insin)
- [@mxstbr](https://github.com/mxstbr)

## Лицензия

Create React App является открытым исходным кодом [licensed as MIT](https://github.com/facebook/create-react-app/blob/master/LICENSE).
