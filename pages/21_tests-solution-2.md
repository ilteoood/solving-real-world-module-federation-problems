# Tests - solution 2

<a href="https://github.com/module-federation/universe/tree/main/packages/native-federation-tests" target="_blank" alt="GitHub" class="flex justify-center items-center text-xl slidev-icon-btn opacity-100 !border-none !hover:text-white">
    <carbon-logo-github /> module-federation/native-federation-tests
</a>

<div class="flex justify-center items-center w-full">
<img class="pb-2" src="assets/tests-structure.png" />
</div>

#### anotherButton.mjs
```ts
import { jsx } from "react/jsx-runtime";
var AnotherButton = ({ onClick }) => /* @__PURE__ */ jsx("button", { onClick, children: "Another federated button" });
var AnotherButton_default = AnotherButton;
export {
  AnotherButton_default as AnotherButton
};
```

#### button.mjs
```ts
// src/components/button/Button.tsx
import { jsx } from "react/jsx-runtime";
var Button = ({ onClick }) => /* @__PURE__ */ jsx("button", { onClick, children: "Federated button" });
var Button_default = Button;
```

<style>
    .slidev-layout h1 {
        margin-bottom: 0.5rem !important;
    }
</style>