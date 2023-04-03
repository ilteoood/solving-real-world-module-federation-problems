# TypeScript - solution 2 - diagram

<a href="https://github.com/ilteoood/solving-real-world-module-federation-problems" target="_blank" alt="GitHub" class="flex justify-center items-center text-xl slidev-icon-btn opacity-100 !border-none !hover:text-white">
    <carbon-logo-github /> ilteoood/native-federation-typescript
</a>

<div class="flex justify-center items-center">
```mermaid {scale: 0.75}
sequenceDiagram
    Note over Remote: Bundler starts
    Note over Remote: Builds TS types
    Note over Remote: Creates a zip file
    Note over Remote: Serves the zip file
    Note over Host: Bundler starts
    Host->>+Remote: I need the types' zip file
    Remote->>-Host: Here it is
    Note over Host: Unzip the content
```
</div>

<style>
    .slidev-layout h1 {
        margin-bottom: 0.5rem !important;
    }
</style>