# @hydenliu/eslint-config
[![npm](https://img.shields.io/npm/v/@hydenliu/eslint-config?color=a1b858&label=)](https://npmjs.com/package/@hydenliu/eslint-config)

- Single quotes, no semi
- Auto fix for formatting (aimed to be used standalone without Prettier)
- TypeScript, Vue, React out-of-box
- Lint also for json, yaml, markdown
- Sorted imports, dangling commas for cleaner commit diff
- Reasonable defaults, best practices, only one-line of config

## WIP

- add stylelint

## Usage

### Install

```bash
# vue
pnpm add -D eslint @hydenliu/eslint-config-vue

# react
pnpm add -D eslint @hydenliu/eslint-config-react

# typescript
pnpm add -D eslint @hydenliu/eslint-config-ts
```

### Config `.eslintrc`

```bash
echo '{"extends": "@chansee97/eslint-config-xxx"}' > .eslintrc
```

> You don't need `.eslintignore` normally as it has been provided by the preset.

### Add script for package.json

For example:

```json
{
  "scripts": {
    "lint": "eslint .",
    "lint:fix": "eslint . --fix"
  }
}
```

### Config VS Code auto fix

Create `.vscode/settings.json`

```json
{
  "prettier.enable": false,
  "editor.codeActionsOnSave": {
    "source.fixAll.eslint": true
  }
}
```

## Reference
- [antfu/eslint-config](https://github.com/antfu/eslint-config)
- [chansee97/lint-config](https://github.com/chansee97/lint-config)

## License

[MIT](./LICENSE) License &copy; 2022-PRESENT [Hyden Liu](https://github.com/HydenLiu)
