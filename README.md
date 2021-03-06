# gd32f3

_Autogenerated with https://github.com/nviennot/gd32-rs_
Register definitions is complete, but HALs are not.

This crate provides an autogenerated API for access to GD32F3 peripherals.
The API is generated using [svd2rust] with patched svd files containing
extensive type-safe support. For more information please see the [main repo].

Refer to the [documentation] for full details.

[svd2rust]: https://github.com/japaric/svd2rust
[main repo]: https://github.com/qwandor/gd32-rs
[documentation]: https://docs.rs/gd32f3/latest/gd32f3/

## Usage
Each device supported by this crate is behind a feature gate so that you only
compile the device(s) you want. To use, in your Cargo.toml:

```toml
[dependencies.gd32f3]
version = "0.5.0"
features = ["gd32f305", "rt"]
```

The `rt` feature is optional and brings in support for `cortex-m-rt`.

In your code:

```rust
use gd32f3::gd32f305;

let mut peripherals = gd32f305::Peripherals::take().unwrap();
let gpioa = &peripherals.GPIOA;
gpioa.odr.modify(|_, w| w.odr0().set_bit());
```

For full details on the autogenerated API, please see:
https://docs.rs/svd2rust/0.19.0/svd2rust/#peripheral-api

## Supported Devices

| Module | Devices | Links |
|:------:|:-------:|:-----:|
| gd32f305 | GD32F305 | [GD32F305](https://www.gigadevice.com/manual/gd32f305xxxx-user-manual/), [gigadevice.com](https://www.gigadevice.com/products/microcontrollers/gd32/arm-cortex-m4/mainstream-line/gd32f305-series/) |
| gd32f307 | GD32F307 | [GD32F307](https://www.gigadevice.com/manual/gd32f307xxxx-user-manual/), [gigadevice.com](https://www.gigadevice.com/products/microcontrollers/gd32/arm-cortex-m4/mainstream-line/gd32f307-series/) |
