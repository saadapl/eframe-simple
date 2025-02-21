# Simple-eframe

## Usage

### Native App

Run command `cargo run --release` in root folder.

### Web Locally

1. Install the required target with `rustup target add wasm32-unknown-unknown`.
2. Install Trunk with `cargo install --locked trunk`.
3. Run `trunk serve` to build and serve on `http://127.0.0.1:8000`. Trunk will rebuild automatically if you edit the project.
4. Open `http://127.0.0.1:8000` in a browser. See the warning below.

> `assets/sw.js` script will try to cache our app, and loads the cached version when it cannot connect to server allowing your app to work offline (like PWA).
> appending `#dev` to `index.html` will skip this caching, allowing us to load the latest builds during development.