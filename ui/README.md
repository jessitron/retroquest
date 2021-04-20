# RetroQuest UI

The RetroQuest UI is developed using the [Angular Framework](https://angular.io/)

## Running Package Scripts

For the purpose of this documentation, we will assume you are using [Yarn Package Manager](https://yarnpkg.com/), but
the commands are very similar using [Node Package manager](https://www.npmjs.com/).

### Starting the Development Server

```
yarn start
```

This command will start the server. Navigate to http://localhost:4200/ to begin interacting on your desktop with the
app. The app will automatically reload if you change any of the source files.

### Unit Testing

This code base uses [Jest](https://jestjs.io/) for its unit testing framework.

```
yarn unit
```

This command will execute the unit tests once and then terminate.

```
yarn unit-watch
```

This command will execute all the unit tests and then enter "watch mode" in which case it will execute any tests again where the code has changed.


```
yarn unit-coverage
```

This command will execute the unit tests once and then generate a code coverage report

### End to End Testing

This code base uses [Protractor](https://www.protractortest.org/) to execute end to end tests.

```
yarn e2e
```

This command will execute the end to end tests.

### Linting the Code base

```
yarn lint
```

This command will lint the typescript codebase and report violations

```
yarn lint-fix
```

This command will lint the typescript codebase and fix violations

## Angular Components

The UI makes use of Angular components to separate application UI logic. The image below shows a breakdown of the main components in the application.

![angular_components](./docs/retroquest-components.png)

## Angular Routing

Navigation through RetroQuest is managed by [Angular Router](https://angular.io/guide/router).

| Path                           | Component                          |
| ------------------------------ | ---------------------------------- |
| create                         | CreateComponent                    |
| login                          | LoginComponent                     |
| login/:teamId                  | LoginComponent                     |
| update-password/:teamId        | UpdatePasswordComponent            |
| create-user                    | CreateUserComponent                |
| login-user                     | LoginUserComponent                 |
| user/:user                     | UserViewComponent                  |
| styleguide                     | StyleGuidePageComponent            |
| team/:teamId                   | SubAppComponent, TeamPageComponent |
| team/:teamId/radiator          | ActionsRadiatorViewComponent       |
| team/:teamId/archives          | ArchivesPageComponent              |
| team/:teamId/archives/:boardId | ArchivedBoardPageComponent         |