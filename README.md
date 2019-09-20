
# svelte-netlify-faunadb-template

## Get Started

```
npx degit TheSacredLipton/svelte-netlify-faunadb-template
cd svelte-netlify-faunadb-template
npm install
```

## locale Setting

```
SET FAUNADB_SECRET=ADMIN_KEY
SET FAUNADB_SERVER_SECRET=DB_KEY
npm run bootstrap
npm run start
```

## build

```
npm run build
```

## Deploy & FaunaDB Auth

```
npx netlify login
npx netlify init
npx netlify link
npx netlify addons:create fauna
npx netlify addons:auth fauna
```

or

```
npx netlify init
npx netlify link
npx netlify addons:create fauna
npx netlify addons:auth fauna
```
