# How to run the code

On terminal 1:
```
cd light_it_up_from_new
cargo embed
```
On terminal 2:
```
cd light_it_up_from_new
gdb-multiarch target/thumbv7em-none-eabihf/debug/light_it_up_from_new
(gdb) target remote :1337
(gdb) break main
(gdb) continue
(gdb) quit
```