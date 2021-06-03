# Rust Bare metal application for the nRF52833 dev-kit

This is a minimal application to demonstrate how to generate a bare metal application using Rust on the nRF52833 dev-kit

## How to build

`$ git clone https://github.com/sbourdelin/nrf52833-rust.git`

`$ cargo build`

## Convert the ELF to hex blob

`$ cargo objcopy -- -O ihex app.hex`

## How to flash

I'm using the nrfjprog

`$ nrfjprog -f nrf52 --program app.hex --chiperase --verify`

`$ nrfjprog -f nrf52 --reset`

## Use
Push the button 1 to trigger the led 1
