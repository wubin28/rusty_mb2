# Light it up

We will finish this chapter by making one of the many LEDs on the MB2 light up. In order to get this
task done we will use one of the traits provided by `embedded-hal`, specifically the [`OutputPin`]
trait which allows us to turn a pin on or off.

[`OutputPin`]: https://docs.rs/embedded-hal/0.2.6/embedded_hal/digital/v2/trait.OutputPin.html

## The micro:bit LEDs

On the back of the micro:bit you can see a 5x5 square of LEDs, usually called an LED matrix. This
matrix alignment is used so that instead of having to use 25 separate pins to drive every single one
of the LEDs, we can just use 10 (5+5) pins in order to control which column and which row of our
matrix lights up.

Right now we will use the `microbit-v2` crate to manipulate the LEDs. In the [next chapter] we will
go in detail through all of the options available.

[next chapter]: ../06-hello-world/index.html

## Actually lighting it up!

The code required to light up an LED in the matrix is actually quite simple but it requires a bit of
setup. First take a look at `examples/light-it-up.rs`; then we can go through it step by step.

```rust
{{#include examples/light-it-up.rs}}
```

The first few lines until the `main` function just do some basic imports and setup we mostly looked
at before.  However, the `main` function looks pretty different to what we have seen up to now.

The first line is related to how most HALs written in Rust work internally.
As discussed before they are built on top of PAC crates which own (in the Rust sense)
all the peripherals of a chip. When we say

    let mut board = Board::take().unwrap();
    
We take all of these peripherals from the PAC and bind them to a variable. In this specific case we
are not only working with a HAL but with an entire BSP, so this also takes ownership of the Rust
representation of the other chips on the board.

> **NOTE**: If you are wondering why we have to call `unwrap()` here, in theory it is possible for
> `take()` to be called more than once. This would lead to the peripherals being represented by two
> separate variables and thus lots of possible confusing behaviour because two variables modify the
> same resource. In order to avoid this, PACs are implemented in a way that it would panic if you
> tried to take the peripherals twice.

(Again, if you are confused by all of this, the [next chapter] will go through it all again in
greater detail.)

Now we can light the LED connected to `row1`, `col1` up by setting the `row1` pin to high
(i.e. switching it on).  The reason we can leave `col1` set to low is because of how the LED matrix
circuit works. Furthermore, `embedded-hal` is designed in a way that every operation on hardware can
possibly return an error, even just toggling a pin on or off. Since that is highly unlikely in our
case, we can just `unwrap()` the result.

## Testing it

Testing our little program is quite simple. First put it into `src/main.rs`. Afterwards we simply
have to run the `cargo embed` command from the last section again, and let it flash just like
before. Then open our GDB and connect to the GDB stub:

```
$ # Your GDB debug command from the last section
(gdb) target remote :1337
Remote debugging using :1337
cortex_m_rt::Reset () at /home/nix/.cargo/registry/src/github.com-1ecc6299db9ec823/cortex-m-rt-0.6.12/src/lib.rs:489
489     pub unsafe extern "C" fn Reset() -> ! {
(gdb)
```

We now let the program run via the GDB `continue` command: one of the LEDs on the front of the
micro:bit should light up.
