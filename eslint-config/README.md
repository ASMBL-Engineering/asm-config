# ASMBL ESLint Configuration

This package contains ASMBL's ESLint configurations for JavaScript projects.

ESLint is used for enforcement of code quality across ASMBL projects.

All ESLint rules enforcing code style have been ~~disabled in favor of using prettier for code formatting~~ deprecated.

## Installation

From the root of your package, install the ASMBL configuration:

`yarn add --dev @assemble-inc/eslint-config-asm`

or

`pnpm add --dev @assemble-inc/eslint-config-asm`

or

`bun add --dev @assemble-inc/eslint-config-asm`

## Configuration

### Add Linting Scripts

Add the following scripts to your `package.json`.

```
"scripts": {
  "lint": "eslint \"src/**/*.{jsx,js}\"",
  "lint:fix": "eslint \"src/**/*.{jsx,js}\" --fix"
},
```

### Import the linting configuration

The ASMBL configuration needs to be imported into ESLint. Add the following to your `package.json`.

```
  "eslintConfig": {
    "extends": [
      "@assemble-inc/eslint-config-asm"
    ],
    "env": {
      "browser": true,
      "node": true
    }
  },
```

That's it! No eslint config file required.

## Usage

The `lint:fix` script will automatically attempt to fix reported errors and warnings. Running `lint` will report errors/warnings without attempting to fix them.
