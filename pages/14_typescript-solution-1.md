# TypeScript - solution 1

#### moduleFederationTypescript.d.ts
```ts
interface AnotherButtonProps {
    onClick: () => void;
}

declare module "moduleFederationTypescript/anotherButton" {
    export const AnotherButton: ({ onClick }: AnotherButtonProps) => JSX.Element;
}

interface ButtonProps {
    onClick: () => void;
}

declare module "moduleFederationTypescript/button" {
    const Button: ({ onClick }: ButtonProps) => JSX.Element;
    export default Button;
}
```