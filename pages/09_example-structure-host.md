# Example - host

<div class="flex items-center justify-center gap-8">

<h4 class="text-center">Components imported and used</h4>

```ts
import { AnotherButton } from 'moduleFederationTypescript/anotherButton'
import Button from 'moduleFederationTypescript/button'

const Component = () => <div>
    <Button onClick={console.log} />
    <AnotherButton onClick={console.error} />
</div>

export default Component
```

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