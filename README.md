## NDS version NTRBOOTHAX flasher
Only tested with NDSL + AK2I & R4i Gold.

### Build
1. Copy these 5 binaries to the `binaries` directory.
  - `blowfish_ntr.bin`
  - `blowfish_dev.bin`
  - `blowfish_retail.bin`
  - `boot9strap_ntr_dev.firm`
  - `boot9strap_ntr.firm`
2. `python extract_binaries.py`
3. Then `make`

#### Notes for build
* Needs experimental libnds; after [9dcc1bd][expr_libnds] version.
* You can extract blowfish binaries using [ak2ifirm][ak2ifirm].
* Change mode requires `make clean` before rebuild.

[expr_libnds]: https://github.com/devkitPro/libnds/commit/9dcc1bd33
[ak2ifirm]: https://github.com/ntrteam/ak2ifirm

#### Special `make` options
* `DEBUG_DUMP=1`
  - print first 16bytes of loaded flash data
* `DEBUG_DUMP=2`
  - print all bytes of loaded flash data
* `DEBUG_PRINT=1`
  - enable flashcart_core's log message
* `NO_DEV=1`
  - build without devkit support, when this is used `blowfish_dev.bin` and `boot9strap_ntr_dev.firm` are not required

### Credits
* [Normmatt][normmatt] - Original implementation of the 3DS version ntrcardhax flasher.
* [SciresM][sciresm] - Parent of `boot9strap`
* [kitling][kitling] - Made `flashcart_core`
* [hedgeberg][hedgeberg] - RE Cartridge
* [HandsomeMatt][HandsomeMatt] - RE Cartridge
* And other talented hackers.

[normmatt]: https://github.com/Normmatt
[sciresm]: https://twitter.com/SciresM
[kitling]: https://github.com/kitling
[hedgeberg]: https://github.com/hedgeberg
[HandsomeMatt]: https://github.com/HandsomeMatt
