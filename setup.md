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
pnpm add react react-dom
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
