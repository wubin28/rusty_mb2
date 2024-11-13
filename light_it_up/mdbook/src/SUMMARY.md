[Introduction](README.md)
- [Background](01-background/README.md)
- [Hardware/knowledge requirements](02-requirements/README.md)
- [Setting up a development environment](03-setup/README.md)
    - [Linux](03-setup/linux.md)
    - [Windows](03-setup/windows.md)
    - [macOS](03-setup/macos.md)
    - [Verify the installation](03-setup/verify.md)
    - [Setting up your IDE](03-setup/IDE.md)
- [Meet your hardware](04-meet-your-hardware/README.md)
    - [micro:bit v2](04-meet-your-hardware/microbit-v2.md)
    - [Rust Embedded terminology](04-meet-your-hardware/terminology.md)
- [Meet your software](05-meet-your-software/README.md)
    - [Build it](05-meet-your-software/build-it.md)
    - [Flash it](05-meet-your-software/flash-it.md)
    - [Debug it](05-meet-your-software/debug-it.md)
    - [Light it up](05-meet-your-software/light-it-up.md)
- [Hello World](06-hello-world/README.md)
    - [Toggle it](06-hello-world/toggle-it.md)
    - [Spin wait](06-hello-world/spin-wait.md)
    - [NOP](06-hello-world/nop.md)
    - [Timers](06-hello-world/timers.md)
    - [Portability](06-hello-world/portability.md)
    - [Board support crate](06-hello-world/board-support-crate.md)
- [Registers](07-registers/README.md)
    - [RTRM](07-registers/rtrm.md)
    - [(mis)Optimization](07-registers/misoptimization.md)
    - [`0xBAAAAAAD` address](07-registers/bad-address.md)
    - [Spooky action at a distance](07-registers/spooky-action-at-a-distance.md)
    - [Type safe manipulation](07-registers/type-safe-manipulation.md)
- [LED roulette](08-led-roulette/README.md)
    - [The challenge](08-led-roulette/the-challenge.md)
    - [My solution](08-led-roulette/my-solution.md)
- [Serial communication](09-serial-communication/README.md)
    - [\*nix tooling](09-serial-communication/nix-tooling.md)
    - [Windows tooling](09-serial-communication/windows-tooling.md)
- [UART](10-uart/README.md)
    - [Send a single byte](10-uart/send-a-single-byte.md)
    - [Send a string](10-uart/send-a-string.md)
    - [Naive approach and `write!`](10-uart/naive-approach-write.md)
    - [Receive a single byte](10-uart/receive-a-single-byte.md)
    - [Echo server](10-uart/echo-server.md)
    - [Reverse a string](10-uart/reverse-a-string.md)
    - [My solution](10-uart/my-solution.md)
- [I2C](11-i2c/README.md)
    - [The general protocol](11-i2c/the-general-protocol.md)
    - [LSM303AGR](11-i2c/lsm303agr.md)
    - [Read a single register](11-i2c/read-a-single-register.md)
    - [Using a driver](11-i2c/using-a-driver.md)
    - [The challenge](11-i2c/the-challenge.md)
    - [My solution](11-i2c/my-solution.md)
- [LED compass](12-led-compass/README.md)
    - [Magnitude](12-led-compass/magnitude.md)
    - [The challenge](12-led-compass/the-challenge.md)
    - [My solution](12-led-compass/my-solution.md)
- [Punch-o-meter](13-punch-o-meter/README.md)
    - [Gravity is up?](13-punch-o-meter/gravity-is-up.md)
    - [The challenge](13-punch-o-meter/the-challenge.md)
    - [My solution](13-punch-o-meter/my-solution.md)
- [Snake game](14-snake-game/README.md)
    - [Game logic](14-snake-game/game-logic.md)
    - [Controls](14-snake-game/controls.md)
    - [Non-blocking display](14-snake-game/nonblocking-display.md)
    - [Final assembly](14-snake-game/final-assembly.md)
- [What's left for you to explore](explore.md)

---

[General troubleshooting](appendix/1-general-troubleshooting/README.md)
[How to use GDB](appendix/2-how-to-use-gdb/README.md)
[Magnetometer Calibration](appendix/3-mag-calibration/README.md)

<!-- - [Async IO: The future](17-async-io-the-future/README.md) -->
<!--     - [Timer](17-async-io-the-future/timer.md) -->
<!--     - [Serial](17-async-io-the-future/serial.md) -->
<!--     - [The challenge](17-async-io-the-future/the-challenge.md) -->
<!--     - [My solution](17-async-io-the-future/my-solution.md) -->
<!--     - [Another challenge](17-async-io-the-future/another-challenge.md) -->
<!--     - [My other solution](17-async-io-the-future/my-other-solution.md) -->
<!--     - [More challenges](17-async-io-the-future/more-challenges.md) -->
---