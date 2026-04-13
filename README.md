# Curly-broccoli

## ❓ Next.js + TypeScript CSS Import Issue

Hey, I’m a bit confused about this behavior:

I cloned a Next.js repo and ran:

```
npm install
npm run dev
```

I get a TypeScript error on:

`import './globals.css';`

### 🔍 What’s odd

 The error only goes away if I manually add:

`declare module "*.css";`

But in a fresh app (`npx create-next-app@latest`), this is already handled inside:

`node_modules/next/types/global.d.ts`

# 🤔 My questions
* Why isn’t that built-in declaration working in the cloned project?
* Is this normal, or is something misconfigured (like tsconfig.json)?
* In real projects, should I: \
   fix the root cause, or \
   just add a manual `global.d.ts`?

I want to keep things clean and production-ready, not patched with quick fixes.