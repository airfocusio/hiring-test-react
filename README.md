# hiring-test-react

## Tasks overview

We want to be able to see your coding skills in action! For this please:

1. Create a private repository on your own (for example `my-account/airfocus-hiring-test-react`), clone this repo and push it to your private repo:
    ```bash
    mkdir airfocus-hiring-test-react
    cd airfocus-hiring-test-react
    git init
    git remote add origin git@github.com:my-account/airfocus-hiring-test-react.git
    git remote add airfocus https://github.com/airfocusio/hiring-test-react.git
    git fetch airfocus
    git reset --hard airfocus/master
    git push origin master -u
    ```
2. Work through the following tasks and push your solution to your private repository.
3. Once done, invite as collaborators:
    * [choffmeister](https://github.com/choffmeister)
    * [mscholz11](https://github.com/mscholz11)

A few general hints that apply to all tasks:

1. If feasible please write unit tests for your code.
2. Make sure that linting as well as tests that you might add run through smoothly
    * run `npm run lint` to run linting
    * run `npm run lint-fix` to apply automated fixes to many linting errors
    * run `npm test` to run tests

A few general hints that apply to [React](https://reactjs.org/) related tasks:

1. We prepared a storybook so that you can directly see what you have build. You can start it with
    * run `npm start`
2. We use css-in-js with [emotion](https://emotion.sh/) for styling (you can find an example in `src/task-look-and-feel/Dashboard.tsx`). Feel free to create some simple styling for your components.

## Task functional-programming (folder `src/task-functional-programming/`)

### Description

The goal of this task is to refactor the very badly written function `userListProcessor`. It is hard to understand, because it uses an imperative and mutating style of coding. Luckily there is already is a working unit test. This must of course still be green after you have refactored the function implementation.

### Todos

1. Inspect the existing implementation of the function `userListProcessor` in `userListProcessor.ts` (and the corresponding test in `userListProcessor.test.ts`) to understand, what the function does.
2. Refactor the implementation of the function and make it "better" (where the meaning of "better" is what you should come up with).

## Task look-and-feel (folder `src/task-look-and-feel/`)

### Description

The goal of this task is to create some nice styling for a dashboard component that shows a list of article cards. Currently there is basically no styling at all.

### Todos

1. Implement some nice styling for the `Dashboard` component (in `Dashboard.tsx`) and for the `ArticleCard` component (in `ArticleCard.tsx`)
    * The dashboard should show the article cards in a 4-column grid
    * Use modern css styles (for example css-grid might make sense here)
    * Make sure that the styling is responsive

## Task react-hooks (folder `src/task-react-hook/`)

### Description

The goal of this task is to build a react component that renders a list of users. Since the users are loaded asynchronously (like for example via a HTTP request) you have to somehow handle this. We use [react hooks](https://reactjs.org/docs/hooks-intro.html) all over the place, so the basic idea is to implement a custom hook called `usePromise` that manages all the state stuff.

### Todos

1. Implement the `usePromise` hook in `usePromise.ts`.
2. Implement the `UserTable` component in `UserTable.tsx`. Make sure to show some kind of "loading" indication while the data is not yet available.
