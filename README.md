# hygen-next

This is a [hygen](https://github.com/jondot/hygen) package for [Next.js](https://github.com/vercel/next.js) that makes it easier to scaffold out TypeScript components in a consistent manner. Feel free to adapt the templats to your specific use-case. The default templates included assume a basic TypeScript, Storybook, and Jest & React Testing Library setup.

## Quick Start

Install `hygen-add` globally

```sh
yarn global hygen-add
```

Then in your Next.js project directory run

```sh
hygen-add next
```

If you prefer using `npx`, skip the global install and run

```sh
npx hygen-add next
```

## Commands

```sh
hygen component new <name>
```

Generates a React component, a storybook story, and a test.

If you don't pass any flags, an interactive CLI will prompt you for a name and location (default "src/components') of the component you want to generate

By default the component generators use Storybook, so you'll either need to have an instance in your project or create one by running

```
npx sb init
```

Requires react-test-renderer to be installed:
\$ yarn add --dev react-test-renderer

```

```
