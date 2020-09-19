# 📈GITDATA

## The main purpose of the App is to offer the posibility to the user to see Git Hub data in a visual way. The graphics will be displayed using data from Git Hub API.

---

## Team

- [Gerard Ramon](https://github.com/gerardramonp)
- [Daniel Alonso](https://github.com/Dani-Alonso)
- [Pablo Hortelano](https://github.com/phortela1n)

---

## Getting Started

### Clone the repository from github.com to your workspace folder:

`$ git clone https://github.com/phortela1n/GitData.git`

### Navigate to the repository folder:

`$ cd GitData`

### Install dependencies

`$ npm install`

### Run the server

`$ npm start`

---

## Feature's DEMO

### Login

![Gif](https://gyazo.com/1527094b903fe4ac45e6cfde74716094.gif)

### Repo details

![Gif](https://gyazo.com/5d8f4da7865710d68f1657a46583d261.gif)

### Create repo

![Gif](https://gyazo.com/db4c0424b694d28730e2e339b067dab7.gif)

### DarkMode

![Gif](https://gyazo.com/cb3c79615c43527655ff8191341450a6.gif)

---

## Initial Wireframe

### Mobile layout

![Imagen](https://i.gyazo.com/88152254c077829e32e9c04ba8ffd085.png)

### Desktop layout

![Imagen](https://i.gyazo.com/7f6d9013750fea3f216f1ffe5f75567e.png)

## Technologies

- Javascript (React mainly)
- Flux
- ES6
- API-Client
- Jasmine
- Jest
- React Bootstrap
- flexBox
- Css3
- SCSS
- Html5
- Firebase

### GitHub API

    - Documentation: https://developer.github.com/v3/

## Workflow

We are using this tools to develop the workflow

### - User Stories Map

**url** https://trello.com/b/nvS0fEFD/user-stories-map

### - Agile methodology with Trello

KANBAN board with Trello

**url:** https://trello.com/b/Qsj5UEvk/spa-gitdata

### GIT

- **In progress**

### Project structure

#### API STRUCTURE

- **In progress**

---

#### SRC TREE

```
├── actions
│   ├── actionTypes.js
│   ├── loginActions.js
│   ├── repoDetailActions.js
│   └── userDetailActions.js
├── components
│   ├── AuthComp
│   │   ├── AuthComp.js
│   │   └── AuthComp.css
│   ├── Footer
│   │   ├── __snapshots__
│   │   ├── Footer.css
│   │   ├── Footer.js
│   │   └── Footer.snapshot.test.js
│   ├── Landing
│   │   ├──Login
│   │   │  ├── Login.css
│   │   │  ├── Login.js
│   │   │  └── Login.snapshot.test.js
│   │   ├──PopUpBox
│   │   │  ├── __snapshots__
│   │   │  ├── PopUpBox.css
│   │   │  ├── PopUpBox.js
│   │   │  └── PopUpBox.snapshot.test.js
│   │   │── Landing.css
│   │   │── Landing.js
│   │   └── Landing.snapshot.test
│   ├── Navbar
│   │   │   ├──Switch
│   │   │   │  ├── __snapshots__
│   │   │   │  ├── Switch.css
│   │   │   │  ├── Switch.js
│   │   │   │  └── Switch.snapshot.test.js
│   │   ├── HeaderNavBar.css
│   │   ├── HeaderNavBar.js
│   │   └── HeaderNavBar.snapshot.test.js
│   ├── RepoCard
│   │   ├── RepoCard.css
│   │   ├── RepoCard.js
│   │   └── RepoCard.snapshot.test.js
│   ├── RepoDetail
│   │   ├── RepoDetail.css
│   │   ├── RepoDetail.js
│   │   └── RepoDetail.snapshot.test.js
│   └── UserDetail
│   │   ├──RepoCreation
│   │   │  ├── __snapshots__
│   │   │  ├── RepoDetail.css
│   │   │  ├── RepoDetail.js
│   │   │  └── RepoDetail.snapshot.test.js
│   │   ├──UserInfo
│   │   │  ├── __snapshots__
│   │   │  ├── UserInfo.css
│   │   │  ├── UserInfo.js
│   │   │  └── UserInfo.snapshot.test.js
│   │   │── UserDetail.css
│   │   │── UserDetail.js
│   │   └── UserDetail.snapshot.test
├── firebase
│   ├── firebaseAuthMethod.js
│   └── firebaseinit.js
├── shared
│   ├── colorMock.js
│   ├── generalStyles.css
│   └── githubApiConst.js
├── stores
│   ├── landingStore.js
│   ├── landingStore.spec.js
│   ├── navbarStore.js
│   ├── navbarStore.spec.js
│   ├── repoDetailStore.js
│   ├── repoDetailStore.spec.js
│   ├── userInfoStore.js
│   ├── userDetailStore.js
│   └── userDetailStore.spec.js
├── App.js
├── dispatcher.js
├── index.js
├── serviceWorker.js
└── registerServiceWorker.js
```

---

## USER STORIES

## **1. Login component**

As a user
I want to log in with Github / Google / Email
So that I can access the app

**Scenario #1**
Given an empty form, and a `checkForm` function
When user tries to log in
Then it should throw an Error

**Scenario #2**
Given a wrong user or password, and a `checkLogin` function
When user tries to log in
Then it should throw an Error

---

## **2. UserDetail component**

As a user
I want to see all my repos
So that I can see their statistics

**Scenario #1**
Given a `loadUserRepos` function
When I log in
Then it should load the repositories which I'm a contribuitor

**Scenario #2**
Given a `loadUserRepos` function
When user have no repositories
Then it should print a message (No repositories)

**Scenario #3**
Given a `loadUserRepos` function
When user isn't logged in with a GitHub account
Then it should print a message (No repositories)

---

As a user
I want to see create a GitHub repo
So that I can create a GitHub repo from this page.

**Scenario #1**
Given a GitHub user
When user log in
Then It should load a create repo button

**Scenario #2**
Given a NO GitHub user
When user log in
Then It should **NOT** load a create repo button

**Scenario #3**
Given a GitHub user and a `createGitHubRepo` function
When user clicks create repo Button
Then It should create a GitHub repository in his account

---

## **3. RepoDetail component**

As a user
I want to see the statistics of a repo
So that I can compare myself with the other collaborators

**Scenario #1**
Given a `loadRepo` function
When user is a contribuitor
Then it should show statistics from the user, all contribuitors and ranking

**Scenario #2**
Given a `loadRepo` function
When user is **NOT** a contribuitor
Then it should show statistics from all contribuitors and ranking

---

## **4. Header component**

As a user
I want to have a navbar
So that I can navigate & search specific projects or users.

**Scenario #1**
Given a `searchURL` function, and a GitHub user profile URL
When the search URL is a valid
Then it should Load UserDetail component with that user info.

**Scenario #2**
Given a `searchURL` function, and a GitHub user profile URL
When the search URL is **NOT** vàlid
Then it should show a not valid URL message

**Scenario #3**
Given a `searchURL` function, and a GitHub repo URL
When the search URL is vàlid
Then it should Load RepoDetail component with that repo info.

**Scenario #4**
Given a `searchURL` function, and a GitHub repo URL
When the search URL is **NOT** vàlid
Then it should show a not valid URL message

---

As a user
I want to have a theme swtich
So that I can switch between _Light_ & _Dark_ mode

**Scenario #1**
Given a `switchTheme` function
When user clicks in the switch
Then it should switch between theme modes.

---

## **5. Error404 component**

As a user
I want to have an Error page
So that I can navigate back to home page.

**Scenario #1**
Given a wrong site path
When user navigates to it
Then it should load Error404 component
