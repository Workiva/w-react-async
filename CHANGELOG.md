## 3.0.0 (unreleased)

  - Rewrite React Async to consume observables instead of fetching state
    asynchronously.

## 2.1.0

  - Support for React 0.13

## 2.0.1

  - Bug fixes to make `isAsyncComponent()` not throw on DOM components.

## 2.0.0

  - React Async is now compatible with React >= 0.12.0 only.

  - `ReactAsync.renderComponentToStringWithAsyncState` is renamed to
    `ReactAsync.renderToStringAsync`. The old name still works but issues a
    deprecation warning.

## 1.0.2

  - Setting empty async state when getInitialStateAsync returns `false`

## 1.0.1

  - Avoid setting an empty state (set `{}` in that case).

## 1.0.0

  - Add support for returning promise from getInitialStateAsync.

## 0.10.1

  - fix React.renderComponentToString inside Fiber but.

## 0.10.0

  - support for React 0.11

## 0.9.4

  - expose `<Preloaded />` component directly on `ReactAsync`.

## 0.9.3

  - remove BaseMixin.componentWillReceiveProps so `asyncState` only takes effect
    during first render.

## 0.9.2

  - escape unicode character in JSON data transfered from server to browser

## 0.9.1

  - proper escaping for JSON data transfered from server to browser

## 0.9.0

  - Preloaded component to defer rendering of async components unless their
    state is available.

## 0.8.0

  - Hooks to serialize/deserialize async state — stateFromJSON/stateToJSON.

## 0.7.0

  - Bump react dep to 0.10.0.

## 0.6.1

  - Fix bug with updating injected state (via asyncState prop).

## 0.6.0

  - Fibers are now optional, they are only needed if you want to pre-render
    React components by fetching async state recursively, e.g. using
    `ReactAsync.renderComponentToStringWithAsyncState`

  - `ReactAsync.createClass` is removed, use `React.createClass` with
    `ReactAsync.Mixin` mixin instead.

  - `ReactAsync.renderComponent` is removed, use `React.renderComponent`
    instead.

  - `ReactAsync.renderComponentToString` is renamed to
    `ReactAsync.renderComponentToStringWithAsyncState`

  - Add `ReactAsync.isAsyncComponent` to test if a component is an async
    component.

  - Add `ReactAsync.prefetchAsyncState` to prefetch state of an async component.

## 0.5.1

  - Check if async component is still mounted before updating its state from and
    async call.

## 0.5.0

  - `ReactAsync.renderComponentToString` now can accept callback w/ 3rd argument
    `data`. In this case data will not be injected automatically into the
    markup.

  - `ReactAsync.injectIntoMarkup(markup, data, scripts)` to inject data into
    markup as JSON blob and a list of scripts (URLs) as <script> elements.

## 0.4.0

  - Upgrade for React 0.9.0.

  - React is now a peer dependency of react-async.
