# RustyGPT

A Fullstack Rust Chatbot built with Open Source LLMs using Rustformers LLM and Leptos.

## Installation

By default, `cargo-leptos` uses `nightly` Rust, `cargo-generate`, and `sass`. If you run into any trouble, you may need to install one or more of these tools.

1. `rustup toolchain install nightly --allow-downgrade` - make sure you have Rust nightly.
2. `rustup target add wasm32-unknown-unknown` - add the ability to compile Rust to WebAssembly.

### Rust Toolchain

You'll need to use the nightly Rust toolchain, and install the `wasm32-unknown-unknown` target as well as the Trunk and `cargo-leptos` tools:

```
rustup toolchain install nightly --allow-downgrade
rustup target add wasm32-unknown-unknown
cargo install trunk cargo-leptos
```

### Model

You'll also need to download a model (in GGML format) of your choice that is [supported by the Rustformers/llm Crate](https://huggingface.co/models?search=ggml).

In the root of the project directory, you'll find a `.env` file where an environment variable called `MODEL_PATH` is defined. Replace the value with the full path to the desired model file.

### TailwindCSS

Install TailwindCSS with `npm install -D tailwindcss`

## Running RustyGPT

To run the project locally, 
1. run `npx tailwindcss -i ./input.css -o ./style/output.css --watch` in a terminal - this will build `style/output.css` and automatically rebuild when a change is detected in `input.css`
2. `cargo leptos watch` in the project directory.
By default, you can access your local project at `http://localhost:3000`


## Tested Models

* [vicuna-7b-v1.5-16k.ggmlv3.q2_K.bin](https://huggingface.co/TheBloke/vicuna-7B-v1.5-16K-GGML)
* [Wizard-Vicuna-7B-Uncensored.ggmlv3.q8_0.bin](https://huggingface.co/TheBloke/Wizard-Vicuna-7B-Uncensored-GGML)

## By [Khalifa MBA](https://github.com/alfellati)
