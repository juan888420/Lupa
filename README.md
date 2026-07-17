# Lupa

**Find design system inconsistencies in React and Tailwind codebases.**

![npm](https://img.shields.io/badge/npm-lupa-CB3837?logo=npm&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?logo=typescript&logoColor=white)
![Node.js](https://img.shields.io/badge/Node.js-5FA04E?logo=nodedotjs&logoColor=white)

Lupa scans your codebase and reports where your UI drifts from your design system: rogue hex colors, arbitrary spacing values, off-scale font sizes and duplicated component patterns. Point it at a project and get a clear report of everything that should be a token but is not.

<!-- Add a screenshot of the CLI output here. Terminal output screenshots with your dark theme will look great. -->

---

## Features

- Detects hardcoded colors that bypass your Tailwind palette
- Flags arbitrary values (`mt-[13px]`, `text-[17px]`) that break the spacing and type scale
- Reports inconsistent usage across components
- Zero config to start, configurable when you need it
<!-- Adjust to the checks actually implemented. -->

## Installation

```bash
npm install -g lupa
# or run directly
npx lupa
```

<!-- Verify the final npm package name is available before publishing. -->

## Usage

```bash
# Scan the current project
lupa scan

# Scan a specific directory
lupa scan ./src/components

# Output as JSON for CI pipelines
lupa scan --format json
```

<!-- Replace with the real commands and flags. -->

## Example Output

```
src/components/Card.tsx
  12:8  color   #f97316 used directly, expected token "accent"
  24:3  spacing mt-[13px] is off-scale, nearest token: mt-3

2 issues found in 1 file
```

<!-- Replace with real output from the tool. -->

## License

MIT. See [LICENSE](./LICENSE).

<!-- Add the LICENSE file if it does not exist yet. -->
