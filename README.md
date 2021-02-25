# hygen-next

This is a [hygen](https://github.com/jondot/hygen) package for [Next.js](https://github.com/vercel/next.js) that makes it easier to scaffold out components, pages, and API routes in a Next.js project in a consistent manner. Feel free to adapt the templates to your specific use-case.

By default, the templates included use TypeScript and assume a basic setup of the following tools:

- Storybook using [Component Story Format](https://storybook.js.org/docs/react/api/csf)
- Jest with [React Testing Library](https://testing-library.com/docs/react-testing-library/intro/)

## Quick Start

Install `hygen-add` globally

```zsh
yarn global hygen-add
```

Then in your Next.js project directory run

```zsh
hygen-add next
```

If you prefer using `npx`, skip the global install and run

```zsh
npx hygen-add next
```

## Generators

Available generators are described in the following sections. Currently supported commands include:

- `hygen component new` for components in the `src/components` directory
- `hygen page [type]:new` for pages where `type` is one of `basic`, `ssg`, or `ssr`
- `hygen api new` for API routes in the `pages` directory

### Components

```zsh
hygen component new [name]
```

This generator creates a new React component with an accompanying Storybook file and a Jest test using React Testing Library.

If you don't pass any flags, an interactive CLI will prompt you for a name and location (default `src/components`) of the component you want to generate.

By default the component generators create a Storybook file, so you'll either need to have an instance in your project or create one by running

```zsh
npx sb init
```

### Pages

```zsh
hygen page [type]:new [name]
```

This generator creates a new page in your `pages` directory, where `type` is one of the following:

- `basic` for a generic page
- `ssg` for a page with `getStaticProps`
- `ssr` for a page with `getServerSideProps`

### API Routes

```zsh
hygen api new [name]
```

This generator creates a new API route in your `pages/api` directory. You can skip specifying a name to use the interactive CLI prompt instead.
