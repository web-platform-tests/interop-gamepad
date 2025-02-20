# Interop 2025: Gamepad API testing

Work on the [Gamepad API testing investigation effort](https://github.com/web-platform-tests/interop/blob/main/2025/README.md#gamepad-api-testing)
for [Interop 2025](https://github.com/web-platform-tests/interop/blob/main/2025/README.md).

## Why an investigation effort?

The goal of an interop focus area is to demonstrate improved interoperability by
increasing the pass rates of automated web platform tests on participating
browsers.
To qualify for an interop focus area, a feature needs good enough test coverage
to enable interoperability improvements to be scored using test results.

An [investigation effort](https://github.com/web-platform-tests/interop/blob/main/2025/README.md#investigation-efforts)
is a set of tasks that will bring the corresponding feature up to the bar that's
required for it to possibly become a focus area in the future.

For context, this investigation effort arose from a rejected
[focus area proposal](https://github.com/web-platform-tests/interop/issues/786).
This investigation effort is scoped to only the Gamepad API and is focused on
improving test coverage rather than fixing existing tests.

## Existing specifications

https://w3c.github.io/gamepad/

## Existing tests

https://github.com/web-platform-tests/wpt/tree/master/gamepad

## Known problems

Add a means to test the API [#175](https://github.com/w3c/gamepad/issues/175)

Most of Gamepad API cannot be tested by automated web platform tests.
The API does not expose any information about connected gamepads until a
[gamepad user gesture](https://w3c.github.io/gamepad/#dfn-gamepad-user-gesture)
is detected, and there is currently no way to simulate this gesture in tests.
Once the gesture is detected, tests also need a way to simulate other gamepad
interactions (connect, disconnect, buttons, axes, touch, vibration).

## Collaborators

| WebKit | Chromium | Gecko | NVidia |
|-|-|-|-|
| @marcoscaceres | @nondebug | | @xingri |
