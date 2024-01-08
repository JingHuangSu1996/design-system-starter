## Design System Starter Kit

> **[Educational Purpose]** This is a design system starter kit for my blog series [Design System 101](https://www.jing-tech.me/series/design-system/index).

## Getting Started

### 1. Clone this repo

```bash
git clone https://github.com/jingsu96/design-system-starter-kit.git
```

### 2. Install dependencies

```bash
pnpm install
```

## Folder Structure

### Core of the design system

```
design-system-starter-kit
├── packages
│   ├── components      # React components library
│   ├── css             # CSS library for components
│   ├── design-tokens   # Design tokens
|   ├── tsconfig        # TypeScript config
│   └── core            # Core library for components
```

### DX tools

```
design-system-starter-kit
|── .changeset          # Changeset for versioning
|── .storybook          # Storybook config
├── plop-tmplates       # Plop templates
├── scripts             # Scripts (setupTest, ...)
```

## License

MIT
