# Blink blinky LEDs with the nRF52840-MDK

Blinks alternating red and blue with a period of 500 milliseconds.

## Debug

I had to build openocd from source to get the DAPLink to function. The start
`openocd` using the provided configuration file.

```
$ openocd -f openocd.conf
```

Then run the program

```
$ cargo run --release
```

cargo will use the run definition found in `.cargo/config` to launch gdb with
the `openocd.gdb` script file.

Issue the gdb command `continue`/`c` to run the program in the debugger.

## License

Licensed under the MIT license. See LICENSE.