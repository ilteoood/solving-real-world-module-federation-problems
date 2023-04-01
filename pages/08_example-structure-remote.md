# Example - remote

<div class="flex gap-8">

<div class="flex flex-col items-center">

#### Exposed component

```ts
interface ButtonProps {
    onClick: () => void
}

const Button = ({ onClick }: ButtonProps) =>
    <button onClick={onClick}>Federated button</button>

export default Button
```

</div>

<div class="flex flex-col items-center w-full">

#### Exposed component
```ts
interface AnotherButtonProps {
    onClick: () => void
}

const AnotherButton = ({ onClick }: AnotherButtonProps) =>
    <button onClick={onClick}>Another federated button</button>

export default AnotherButton
```

</div>

</div>

<div class="flex items-center justify-center">

<h4 class="text-center">Module federation configuration</h4>

```ts
const moduleFederationConfig = {
  name: 'moduleFederationTypescript',
  filename: 'remoteEntry.js',
  exposes: {
    './button': './src/components/button',
    './anotherButton': './src/components/anotherButton'
  },
  shared: {
    ...deps,
    react: { singleton: true, eager: true, requiredVersion: deps.react },
    "react-dom": { singleton: true, eager: true, requiredVersion: deps["react-dom"] }
  },
}
```
</div>

<style>
    .slidev-layout h1 {
        margin-bottom: 0.5rem !important;
    }
</style>