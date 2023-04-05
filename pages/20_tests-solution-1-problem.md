# Tests - solution 1

```bash
AssertionError: Snapshot `Component > can test federated components 1` mismatched
 ❯ src/component/Component.test.tsx:12:30
     10|         const { asFragment } = render(<Component />)
     11| 
     12|         expect(asFragment()).toMatchSnapshot()
       |                              ^
     13|     })
     14| })

  - Expected  - 6
  + Received  + 2

    <DocumentFragment>
      <div>
  -     <button>
  -       Federated button
  -     </button>
  -     <button>
  -       Another federated button
  -     </button>
  +     <button />
  +     <button />
      </div>
    </DocumentFragment>
```

<style>
    .slidev-layout h1 {
        margin-bottom: 0.5rem !important;
    }
</style>