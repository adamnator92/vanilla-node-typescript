# The vanilla node + express + nodemon + typescript + tslint + prettier setup

### Step 1 Boiler plate setup

```
yarn add -D typescript
yarn add -D tslint
yarn add -D prettier --exact
yarn add -D nodemon
yarn add -D @types/express
yarn add express
```

### Step 2 Generate tsconfig.json

```
yarn tsc --init
```

### Step 3 Generate tsconfig.json

```
yarn tslint --init
```

### Step 4 Generate prettier

```
touch .prettierrc and copy options to that file
```

### Step 5 Configure nodemon

```
touch nodemon.json, add configuration rules
```

### Optional - Setup tsconfig-paths

enable use to load modules according to the `paths` section in tsconfig.json.
like so

in tsconfig.json

```
   "paths": {
      "@shared/*": ["src/shared/*"],
    },
```

in code

`import { HelperFunction } from '@shared'`

Setup

```
yarn add tsconfig-paths -D
```

in package.json `script`

`start: ts-node -r tsconfig-paths/register index.ts`
