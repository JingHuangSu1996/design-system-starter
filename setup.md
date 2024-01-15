## How I Built This

### Basic Setup

#### 1. Create a new folder

```bash
mkdir design-system-starter-kit
cd design-system-starter-kit
```

#### 2. Initialize a new npm project

```bash
pnpm init -y
```

**create a new folder `packages` and `cd packages`**

```bash
mkdir packages
```

#### 3. Git init

**git init**

```bash
git init
```

**.gitignore**

```bash
touch .gitignore
```

#### 4. Setup pnpm workspace

```bash
touch pnpm-workspace.yaml
```

```yaml
packages:
  - 'packages/*'
```

#### 5. Install turbo, changeset, react, react-dom in root folder

```bash
pnpm add -D @changesets/cli @changesets/cli turbo
```

```bash
pnpm install -D plop prettier husky eslint eslint-config-react eslint-config-prettier eslint-plugin-jsx-a11y eslint-plugin-react @commitlint/cli @commitlint/config-conventional @typescript-eslint/eslint-plugin @typescript-eslint/parser lint-staged -w
```

```bash
pnpm add react react-dom
```

##### Init changeset

```bash
pnpm changeset init
```

##### Setup turbo

**create turbo.json**

```js
{
  "$schema": "https://turbo.build/schema.json",
  "pipeline": {
    "build": {
      "outputs": ["dist/**"],
      "dependsOn": ["^build"]
    },
    "test": {},
    "dev": {
      "cache": false
    },
    "clean": {
      "cache": false
    }
  }
}
```

**turbo init**

```bash
npx turbo init
```

#### Create components and design-tokens package

```bash
mkdir packages/components
mkdir packages/design-tokens
mkdir packages/tsconfig
```

##### Create plop-templates folder

```bash

```
