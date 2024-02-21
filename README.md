# ⬆️ @xarunoba/clai

![Static Badge](https://img.shields.io/badge/Made_with-%E2%9D%A4%EF%B8%8F-red?style=for-the-badge) ![Static Badge](https://img.shields.io/badge/Under-100%20Lines-blue?style=for-the-badge) ![NPM License](https://img.shields.io/npm/l/%40xarunoba%2Fclai?style=for-the-badge)
![GitHub package.json version](https://img.shields.io/github/package-json/v/xarunoba/clai?style=for-the-badge&logo=npm)

**`clai`** — check lockfiles and install

Run package installation after checking for lockfile updates. Integrate with git hooks. Supports `npm`, `pnpm`, and `yarn`.

## Why

Using a bot to update dependencies is becoming widespread. Installing after pulling from your remote repository is now needed in order to synchronize your local modules. `clai` fixes this issue by checking for lockfile updates and running install.

## Installation

### With [`simple-git-hooks`](https://github.com/toplenboren/simple-git-hooks)

Integrating with [`simple-git-hooks`](https://github.com/toplenboren/simple-git-hooks) is easy as a toasted bread:

```json
// package.json
{
  ...
  "simple-git-hooks": {
    "post-merge": "npx @xarunoba/clai" // or use pnpm dlx, yarn dlx
  }
  ...
}
```
