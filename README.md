# The Thinking Hub

[![Built with Astro](https://astro.badg.es/v2/built-with-astro/tiny.svg)](https://astro.build)
[![Netlify Status](https://api.netlify.com/api/v1/badges/aa48c7aa-8c23-4de4-b1a8-e59b2c6140a8/deploy-status)](https://app.netlify.com/projects/the-thinking-hub/deploys)

A curated collection of short, highly-digestible blog posts and articles exploring the eight fundamental **Ways of Thinking in Computer Science**.

### 💡 About This Repository

The field of Informatics extends far beyond coding and computation. It is shaped by a multitude of perspectives, methods, and ethical considerations.

The Thinking Hub serves as your central resource for understanding these critical intellectual frameworks. Each contribution is designed to be insightful, engaging, and easy to read during a short break.

### 🧭 Thinking Modes Covered

This repository contains focused content on the following essential disciplines:

* **Critical Thinking**
* **Computational Thinking**
* **Creative Thinking**
* **Responsible Thinking**
* **Design Thinking**
* **Policy Thinking**
* **Criminal Thinking**
* **Scientific Thinking**

Whether you are a student, educator, or simply curious about the broader impact of digital technology, `The Thinking Hub` provides the foundational knowledge you need to develop a well-rounded digital mindset.

## Development

Requires Node.js 24 and pnpm. The site is built on the [Chiri](https://github.com/the3ash/astro-chiri) theme.

```shell
pnpm install
pnpm dev
```

| Command             | Description                                                         |
| ------------------- | ------------------------------------------------------------------- |
| `pnpm check`        | Type check with `astro check`                                       |
| `pnpm lint`         | Lint with oxlint                                                    |
| `pnpm format:check` | Check formatting with Prettier                                      |
| `pnpm knip`         | Find unused files and dependencies                                  |
| `pnpm test`         | Unit tests with Vitest                                              |
| `pnpm test:e2e`     | Build, then run the Playwright tests against the built `dist` folder |
| `pnpm new`          | Create a new post                                                   |

## License

Licensed under the MIT license, Copyright © trueberryless.

See [LICENSE](https://github.com/trueberryless/the-thinking-hub/blob/main/LICENSE) for more information.
