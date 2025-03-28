# Vue.js Development Rules with Composition API

## General Coding Standards
- Always use the Composition API for new Vue.js components
- Use `<script lang="ts" setup>` syntax for more concise component definitions
- Prefer `ref` and `reactive` for reactive state management
- Use TypeScript for type safety whenever possible
- Follow proper file naming convention: kebab-case for component files (e.g., `user-profile.vue`)

## Component Structure
- Organize components in the following order:
  1. `<script setup>` section
  2. `<template>` section
  3. `<style>` section (preferably scoped)
- Keep components focused on a single responsibility
- Extract reusable logic into composables (files using the pattern `use*.ts`)

## State Management
- Use `provide` and `inject` for passing data down multiple component levels
- For global state, prefer Pinia over Vuex
- Create stores with appropriate actions, getters, and state

## Styling
- Use scoped CSS or CSS modules to prevent style leakage
- Follow a consistent CSS naming convention (BEM recommended)
- Use CSS variables for theme colors and consistent spacing

## Performance Considerations
- Utilize `computed` properties for derived state
- Use `watchEffect` or `watch` carefully to avoid performance issues
- Implement lazy loading for routes and heavy components

## Testing
- Write unit tests for composables and components
- Use Vue Testing Library for component testing
- Follow the AAA pattern (Arrange, Act, Assert) in tests

## Vue.js Best Practices
- Properly handle component lifecycle with `onMounted`, `onUnmounted`, etc.
- Use `defineProps` and `defineEmits` for component communication
- Leverage Vue Router for navigation and route handling

## Git Workflow
- Write meaningful commit messages following conventional commits format (e.g., `feat: add user authentication`)
- Use semantic prefixes: `feat`, `fix`, `docs`, `style`, `refactor`, `test`, `chore`
- Create feature branches for new development work (`feature/user-authentication`)
- Rebase feature branches on main/develop before creating pull requests
- Squash commits when merging to keep a clean history
- Use `.gitignore` to exclude `node_modules`, build artifacts, and environment files
- Perform code reviews before merging pull requests
- Configure Git hooks with Husky to run linters and tests before commits

Remember that the Composition API allows for better code organization, type inference, and reusability compared to the Options API.