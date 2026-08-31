# Clean Reactive Architecture Documentation

- [Architecture](./docs/architecture.md) - the UML diagram, the units, and the
  reasoning behind them.
- [Development Methodology](./docs/methodology.md) - how features are built
  against the diagram.

## Samples

The samples implement the same architecture with different frameworks and
libraries. The units, the boundaries and the diagram do not change - only the
tools used to realize them. The samples also sit at different states of
decomposition.

- [One-file React App](https://github.com/clean-reactive/sample-react-one-file) -
  every unit inlined in a single component. The easiest place to start reading.
- [React App](https://github.com/clean-reactive/sample-react-rtk) - React and
  RTK Query, partially decomposed.
- [Angular App](https://github.com/clean-reactive/sample-angular-tanstack-query) -
  Angular and TanStack Query, partially decomposed.
- [Next.js App](https://github.com/clean-reactive/sample-react-nextjs) -
  full-stack, covering both the client and the server.

*Partially* decomposed is deliberate. Some units have their own files, others
remain inlined in the component that uses them, because [continuous
refactoring](./docs/methodology.md#continuous-refactoring) extracts a unit only
when it earns it.
