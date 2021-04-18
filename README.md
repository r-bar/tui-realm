# tui-realm

[![License: MIT](https://img.shields.io/badge/License-MIT-teal.svg)](https://opensource.org/licenses/MIT) [![Stars](https://img.shields.io/github/stars/veeso/tui-realm.svg)](https://github.com/veeso/tui-realm) [![Downloads](https://img.shields.io/crates/d/tui-realm.svg)](https://crates.io/crates/tui-realm) [![Crates.io](https://img.shields.io/badge/crates.io-v0.1.0-orange.svg)](https://crates.io/crates/tuirealm) [![Docs](https://docs.rs/tuirealm/badge.svg)](https://docs.rs/tuirealm)  

[![Build](https://github.com/veeso/tui-realm/workflows/Linux/badge.svg)](https://github.com/veeso/tui-realm/actions) [![Build](https://github.com/veeso/tui-realm/workflows/MacOS/badge.svg)](https://github.com/veeso/tui-realm/actions) [![Build](https://github.com/veeso/tui-realm/workflows/Windows/badge.svg)](https://github.com/veeso/tui-realm/actions) [![codecov](https://codecov.io/gh/veeso/tui-realm/branch/main/graph/badge.svg?token=au67l7nQah)](https://codecov.io/gh/veeso/tui-realm)

Developed by Christian Visintin  
Current version: 0.1.0 (19/04/2021)

---

- [tui-realm](#tui-realm)
  - [About tui-realm 👑](#about-tui-realm-)
    - [Why tui-realm 🤔](#why-tui-realm-)
  - [Get started 🏁](#get-started-)
    - [Add tui-realm to your Cargo.toml 🦀](#add-tui-realm-to-your-cargotoml-)
    - [Create a tui-realm application](#create-a-tui-realm-application)
    - [Run examples](#run-examples)
  - [Standard component library 🎨](#standard-component-library-)
  - [Guides 🎓](#guides-)
  - [Documentation 📚](#documentation-)
  - [About other backends](#about-other-backends)
  - [Contributing and issues 🤝🏻](#contributing-and-issues-)
  - [Changelog ⏳](#changelog-)
  - [Buy me a coffee ☕](#buy-me-a-coffee-)
  - [License 📃](#license-)

---

## About tui-realm 👑

tui-realm is a **framework** for [tui](https://github.com/fdehau/tui-rs) which provides a layer to simplify the implementation of terminal user interfaces adding the possibility to work with re-usable component with properties and state, as you'd do in React; but that's not all: the input events are handled through a system based on **Messages**, providing you with the possibility to implement `update` functions as happens in Elm.

And that's also explains the reason of the name: Realm stands for React and Elm.

Tui-realm also comes with a built-in standard library of components you may find very useful. Don't worry, they are optional if you don't want them 😉, just follow the guide in [get started](#get-started-).

### Why tui-realm 🤔

Personally I didn't start this project from scratch. I've just decided to make a library out of the already existing code in [termscp](https://github.com/veeso/termscp), which I had just finished at the time I started this project. I thought this library could have come handy for somebody.

You might be wondering now how much is this project influenced by the development of termscp. Well, a lot actually, I won't deny this, so don't expect this library to always try to fit the community needs, I'm just providing you with a tool I've made for myself, but that I wanted to share with the community.

---

## Get started 🏁

⚠ Warning: tui-realm works only with **crossterm** as backend ⚠

### Add tui-realm to your Cargo.toml 🦀

```toml
tuirealm = "0.1.0"
```

or if you want to include the [standard component library](#standard-component-library-)...

```toml
tuirealm = { "version" = "0.1.0", features = [ "with-components" ] }
```

Since this library requires `crossterm` too, you'll also need to add it to your Cargo.toml

```toml
crossterm = "0.19.0"
```

### Create a tui-realm application

View how to implement a tui-realm application in the [related guide](docs/get-started.md).

### Run examples

Still confused about how tui-realm works? Don't worry, try with the examples:

- [demo](examples/demo.rs): a simple application which shows how tui-realm works

    ```sh
    cargo run --features="with-components" --example demo
    ```

- [termscp](https://github.com/veeso/termscp): real production implemenetation of tui-realm; just browse the `src/ui/` folder.

---

## Standard component library 🎨

Tui-realm comes with an optional standard library of components I thought may be useful for most of the applications.
If you want to use it, just enabled the `with-components` feature in your `Cargo.toml`.

For each component, the standard library provides a `PropsBuilder` in the same module (e.g. `input::Input => input::InputPropsBuilder`), which provides methods to set only the properties actually used by the component.

To have an overview of the components just run the gallery example 🦄

```sh
cargo run --features="with-components" --example gallery
```

If you want a super-detailed guide about components check out the [components guide](docs/std-components.md).

---

## Guides 🎓

- [Get Started Guide](docs/get-started.md)
- [The UI lifecycle](docs/lifecycle.md)
- [Standard Library Components](docs/std-components.md)
- [Implement components](docs/new-components.md)

---

## Documentation 📚

The developer documentation can be found on Rust Docs at <https://docs.rs/tui-realm>

---

## About other backends

TODO: fill

---

## Contributing and issues 🤝🏻

Contributions, bug reports, new features and questions are welcome! 😉
If you have any question or concern, or you want to suggest a new feature, or you want just want to improve tui-realm, feel free to open an issue or a PR.

Please follow [our contributing guidelines](CONTRIBUTING.md) TODO: write contributing

---

## Changelog ⏳

View tui-realm's changelog [HERE](CHANGELOG.md)

---

## Buy me a coffee ☕

If you like tui-realm and you're grateful for the work I've done, please consider a little donation 🥳

[![Buy-me-a-coffee](https://img.buymeacoffee.com/button-api/?text=Buy%20me%20a%20coffee&emoji=&slug=veeso&button_colour=404040&font_colour=ffffff&font_family=Comic&outline_colour=ffffff&coffee_colour=FFDD00)](https://www.buymeacoffee.com/veeso)

---

## License 📃

tui-realm is licensed under the MIT license.

You can read the entire license [HERE](LICENSE)
