# Tests - solution 1

```ts
vi.mock('moduleFederationTypescript/button', 
  () => ({default: () => <button />})
)

vi.mock('moduleFederationTypescript/anotherButton', 
  () => ({ AnotherButton: () => <button />})
)
```