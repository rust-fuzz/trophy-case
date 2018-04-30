# 🏆 Trophy Case 🏆

These bugs aren't nearly as serious as the [memory-safety issues afl has discovered](http://lcamtuf.coredump.cx/afl/#bugs) in C and C++ projects. That's because Rust is memory-safe by default, but also because not many people have tried fuzzing yet! Over time we will update this section with the most interesting bugs, whether they're logic errors or memory-safety problems arising from `unsafe` code. Pull requests are welcome!

Security issues are marked with a ❗️ in the "Security?" column. Denial of service, including panics and out-of-memory, are not considered security issues.

Crate | Information | Fuzzer | Category | Security?
----- | ----------- | ------ | ---------|----------
bmfont | [panic on unwrapping](https://github.com/netgusto/rust-bmfont/issues/2) | libfuzzer | `panic`
brotli-rs | [#10](https://github.com/ende76/brotli-rs/issues/10) | afl | `panic`
brotli-rs | [#11](https://github.com/ende76/brotli-rs/issues/11) | afl | `panic`
brotli-rs | [#12](https://github.com/ende76/brotli-rs/issues/12) | afl | `panic`
brotli-rs | [#2](https://github.com/ende76/brotli-rs/issues/2) | afl | `panic`
brotli-rs | [#3](https://github.com/ende76/brotli-rs/issues/3) | afl | `panic`
brotli-rs | [#4](https://github.com/ende76/brotli-rs/issues/4) | afl | `panic`
brotli-rs | [#5](https://github.com/ende76/brotli-rs/issues/5) | afl | `oor`
brotli-rs | [#6](https://github.com/ende76/brotli-rs/issues/6) | afl | `arith`
brotli-rs | [#7](https://github.com/ende76/brotli-rs/issues/7) | afl | `oor`
brotli-rs | [#8](https://github.com/ende76/brotli-rs/issues/8) | afl | `arith`
brotli-rs | [#9](https://github.com/ende76/brotli-rs/issues/9) | afl | `arith`
bson | [multiple bugs, including arithmetic overflow](https://github.com/zonyitoo/bson-rs/issues/64) | libfuzzer | `arith`, `other`, `unwrap`
capnproto-rust | [Multiple bugs, including a memory safety bug](https://dwrensha.github.io/capnproto-rust/2017/02/27/cargo-fuzz.html) | libfuzzer | | ❗️
cpp_demangle | [#41](https://github.com/fitzgen/cpp_demangle/pull/41) | afl |
cssparser | [floating-point parsing imprecision](https://github.com/servo/rust-cssparser/issues/167) | libfuzzer | `logic`
der-parser | [arithmetic overflow](https://github.com/rusticata/der-parser/issues/2) | libfuzzer | `arith`
flac | [#3](https://github.com/sourrust/flac/issues/3) | afl | `oom`
flac | [index out of bounds](https://github.com/sourrust/flac/issues/11) | libfuzzer | `oor`
h2 | [#260](https://github.com/carllerche/h2/pull/260) | honggfuzz | `oor`
h2 | [#261](https://github.com/carllerche/h2/pull/261) | honggfuzz | `panic`
h2 | [#262](https://github.com/carllerche/h2/pull/262) | honggfuzz | `panic`
httparse | [#9](https://github.com/seanmonstar/httparse/issues/9) | afl |
httpdate | [panics](https://pyfisch.org/blog/fuzzing-all-crates/): "no character boundary" and arithmetic overflow | libfuzzer |
hyper | [arithmetic overflow](https://github.com/hyperium/hyper/pull/1076) | libfuzzer |
image | [#414](https://github.com/PistonDevelopers/image/issues/414) | afl |
image | [#473](https://github.com/PistonDevelopers/image/issues/473) | afl |
image | [#474](https://github.com/PistonDevelopers/image/issues/474) | afl |
image | [#477](https://github.com/PistonDevelopers/image/issues/477) | afl |
image | [1](https://github.com/PistonDevelopers/image/issues/622) | libfuzzer |
image | [2](https://github.com/PistonDevelopers/image/issues/623) | libfuzzer |
image | [3](https://github.com/PistonDevelopers/image/issues/624) | libfuzzer |
image | [4](https://github.com/PistonDevelopers/image/issues/625) | libfuzzer |
inflate | [arithmetic overflow](https://github.com/PistonDevelopers/inflate/issues/14) | libfuzzer | `arith`
ipfix | [index out of bounds](https://github.com/DominoTree/rs-ipfix/issues/1) | libfuzzer | `oor`
jpeg-decoder | [#38](https://github.com/kaksmet/jpeg-decoder/issues/38) | afl |
jpeg-decoder | [#50](https://github.com/kaksmet/jpeg-decoder/issues/50) | afl |
jpeg-decoder | [arithmetic overflow](https://github.com/kaksmet/jpeg-decoder/issues/69) | libfuzzer |
json-rust | [arithmetic overflow](https://github.com/maciejhirsz/json-rust/issues/139) | afl | `arith`
libpnet | [arithmetic overflow](https://github.com/libpnet/libpnet/pull/250) | libfuzzer |
minidump | [#7](https://github.com/luser/rust-minidump/issues/7) | libfuzzer |
Molten | [#41](https://github.com/LeopoldArkham/Molten/issues/41) | libfuzzer | `utf-8`
Molten | [#42](https://github.com/LeopoldArkham/Molten/issues/42) | libfuzzer | `oor`
mp3-metadata | [#9](https://github.com/GuillaumeGomez/mp3-metadata/pull/9) | afl |
mp4parse-rust | [#2](https://github.com/mozilla/mp4parse-rust/issues/2) | afl |
mp4parse-rust | [#4](https://github.com/mozilla/mp4parse-rust/issues/4) | afl |
mp4parse-rust | [#5](https://github.com/mozilla/mp4parse-rust/issues/5) | afl |
mp4parse-rust | [#6](https://github.com/mozilla/mp4parse-rust/issues/6) | afl |
msgpack-rust | [#151](https://github.com/3Hren/msgpack-rust/issues/151) | afl | `oom`
nom | [arithmetic overflow](https://github.com/Geal/nom/pull/486) | libfuzzer | `arith`
npy-rs | [arithmetic overflow](https://github.com/potocpav/npy-rs/pull/2) | libfuzzer |
ntp | [panic caused by unwrap on invalid input](https://github.com/JeffBelgum/ntp/commit/f23ded23c26a5326dae249905d298e8c5f51d371) | libfuzzer |
num | [panic on `BigInt` parsing](https://github.com/rust-num/num/issues/268) | libfuzzer | `unwrap`
parity | [panic on `BasicDecoder` unchecked addition](https://github.com/paritytech/parity/issues/6226) | libfuzzer
pcapng | [arithmetic overflow](https://github.com/richo/pcapng-rs/issues/6) | libfuzzer |
proc-macro2 | [#54](https://github.com/alexcrichton/proc-macro2/issues/54) | afl | `utf-8`
proc-macro2 | [#55](https://github.com/alexcrichton/proc-macro2/issues/55) | afl | `so`
pulldown-cmark | [Overflow ParseIntError](https://github.com/google/pulldown-cmark/issues/49) | libfuzzer | `unwrap`
pulldown-cmark | [Panics and infinite loop](https://github.com/google/pulldown-cmark/issues/81) | libfuzzer | `loop`, `utf-8`, `oor`
quick-xml | [arithmetic overflow](https://github.com/tafia/quick-xml/issues/53) | libfuzzer | `arith`
quick-xml | [arithmetic overflow](https://github.com/tafia/quick-xml/pull/55/commits/53a5c099df585dd65382ffd7f2912728eaa764d5) | libfuzzer | `arith`
quick-xml | [index out of bounds](https://github.com/tafia/quick-xml/issues/94) | libfuzzer | `oor`
regex | [#84](https://github.com/rust-lang/regex/issues/84) | afl | `unwrap`
regex | [regex parsing panics](https://github.com/rust-lang/regex/pull/349) with [blog post](https://www.nibor.org/blog/fuzzing-is-magic---or-how-i-found-a-panic-in-rusts-regex-library/) | libfuzzer | `unwrap`
regex | [#417](https://github.com/rust-lang/regex/issues/417) | afl | `utf-8`
regex | [index out of bounds](https://github.com/rust-lang/regex/issues/464) | honggfuzz | `oor`
regex | [Unexpected match branch](https://github.com/rust-lang/regex/issues/465) | honggfuzz | `logic`
regex | [called Option::unwrap() on a None value](https://github.com/rust-lang/regex/issues/465) | honggfuzz | `unwrap`
rust-asn1 | [#32](https://github.com/alex/rust-asn1/issues/32) | afl |
rust-url | [#108](https://github.com/servo/rust-url/pull/108) | afl | `oor`
rustc | [#24275](https://github.com/rust-lang/rust/issues/24275) | afl | `other`
rustc | [#24276](https://github.com/rust-lang/rust/issues/24276) | afl | `segfault`
rustc-demangle | [multiply with overflow](https://github.com/alexcrichton/rustc-demangle/issues/9) | libfuzzer | `arith`
rustc-serialize | [#109](https://github.com/rust-lang/rustc-serialize/issues/109) | afl | `arith`
rustc-serialize | [#110](https://github.com/rust-lang/rustc-serialize/issues/110) | afl | `panic`
rust-snappy | [#12](https://github.com/BurntSushi/rust-snappy/issues/12) | libfuzzer | `oor`
semver | [logic error](https://github.com/steveklabnik/semver/issues/116#issuecomment-311215219) | libfuzzer | `logic`
serde | [#75](https://github.com/serde-rs/serde/issues/75) | afl | `arith`
serde | [#77](https://github.com/serde-rs/serde/issues/77) | afl | `arith`
serde | [#82](https://github.com/serde-rs/serde/issues/82) | afl | `so`
serde-yaml | [#49](https://github.com/dtolnay/serde-yaml/issues/49) | libfuzzer | `so`
serde-yaml | [#88](https://github.com/dtolnay/serde-yaml/pull/88) | libfuzzer | `logic`
sleep-parser | [#3](https://github.com/datrs/sleep-parser/issues/3) | honggfuzz | `oor`, `utf-8`
smoltcp | [index out of bounds](https://github.com/m-labs/smoltcp/commit/2582d1573de37f23d77ed2b1e491d095c920ccfc) | libfuzzer | `oor`
smoltcp | [index out of bounds](https://github.com/m-labs/smoltcp/commit/3f43be8d8450db19fd427f48e8c658561591da1f) | libfuzzer | `oor`
smoltcp | [index out of bounds](https://github.com/m-labs/smoltcp/commit/ed2c376628b6566b0e48af2ca5a942d9fa288b9a) | libfuzzer | `oor`
smoltcp | [arithmetic underflow](https://github.com/m-labs/smoltcp/commit/b33d867385e0f256f558d1268fa2c73470b7f34a) | libfuzzer | `arith`
smoltcp | [index out of bounds](https://github.com/m-labs/smoltcp/commit/2989fa334885916e9c8c76216a60b28c371a54cb) | libfuzzer | `oor`
smoltcp | [index out of bounds](https://github.com/m-labs/smoltcp/commit/31073835998016eb70982c69d0f2e5390dbc19b3) | libfuzzer | `oor`
smoltcp | [index out of bounds](https://github.com/m-labs/smoltcp/commit/c8ae7bdc219b82c62ee3410893fcc6d7455d64b0) | libfuzzer |  `oor`
smoltcp | [index out of bounds](https://github.com/m-labs/smoltcp/commit/181083f18c977b8a0463a67e360e4db20594fa21) | libfuzzer |  `oor`
snmp-parser | [panic on unwrapping](https://github.com/rusticata/snmp-parser/issues/2) | libfuzzer | `unwrap`
ssh-keys | [panic on slice indexing](https://github.com/tailhook/ssh-keys/issues/1) | libfuzzer | `oor`
ssh-parser | [arithmetic overflow](https://github.com/rusticata/ssh-parser/issues/1) | libfuzzer | `arith`
svgparser | [arithmetic overflow, bound checking panic, incorrect result](https://github.com/RazrFalcon/libsvgparser/commit/4742f16e834445a682a0a4db62600d275a457390) | libfuzzer | `arith`, `oor`, `logic`
svgparser | [endless loop](https://github.com/RazrFalcon/libsvgparser/commit/c55d9a7d4d1e83f405be2e7bfddea89f579f6fc9) | libfuzzer | `loop`
sxd-document | [use after free](https://github.com/shepmaster/sxd-document/issues/47) | libfuzzer | `uaf` | ❗️
tar-rs | [#23](https://github.com/alexcrichton/tar-rs/issues/23) | afl | `arith`
todotxt.rs | [index out of bounds](https://github.com/kstep/todotxt.rs/issues/1) | libfuzzer | `oor`
toml | [#178](https://github.com/alexcrichton/toml-rs/issues/178) | libfuzzer | `logic`
toml | [#179](https://github.com/alexcrichton/toml-rs/issues/179) | libfuzzer | `logic`
toml | [#180](https://github.com/alexcrichton/toml-rs/issues/180) | libfuzzer | `logic`
toml | [#181](https://github.com/alexcrichton/toml-rs/issues/181) | libfuzzer | `logic`
toml | [#185](https://github.com/alexcrichton/toml-rs/issues/185) | libfuzzer | `logic`
toml | [#186](https://github.com/alexcrichton/toml-rs/issues/186) | libfuzzer | `logic`
unicode-segmentation | [grapheme boundary correctness](https://github.com/unicode-rs/unicode-segmentation/issues/19) | libfuzzer |
unicode-segmentation | [word boundary correctness](https://github.com/unicode-rs/unicode-segmentation/issues/20) | libfuzzer |
uuid | [index out of bounds](https://github.com/rust-lang-nursery/uuid/pull/81) | libfuzzer | `oor`
vosub | [invalid slice](https://github.com/emk/subtitles-rs/commit/46df766dd22cb6a04a534611f08c23903e58746c) | libfuzzer | `oor`
vosub | [invalid slice](https://github.com/emk/subtitles-rs/commit/f2f5309aa8173dfec4bb5816950d718a1ac669c2) | libfuzzer | `panic`
vosub | [arithmetic overflow](https://github.com/emk/subtitles-rs/commit/3afdb7e1c5e786e88653253243648dd9d49983f2) | libfuzzer | `arith`
vosub | [invalid slice](https://github.com/emk/subtitles-rs/commit/20e430105b1fc02aa135788ba150a0dd49a7d1ef) | libfuzzer | `oor`
vosub | [shift overflow](https://github.com/emk/subtitles-rs/commit/5d3364b96389d90deac0f024a57660951b7e1dd6) | libfuzzer | `arith`
wasmparser.rs | [arithmetic overflow](https://github.com/yurydelendik/wasmparser.rs/issues/21#issuecomment-310253956) | libfuzzer | `arith`
ws-rs | [arithmetic overflow](https://github.com/housleyjk/ws-rs/pull/179) | libfuzzer | `arith`
xml-rs | [#93](https://github.com/netvl/xml-rs/issues/93) | afl | `utf-8`
zip-rs | [arithmetic overflow](https://github.com/mvdnes/zip-rs/issues/40) | libfuzzer | `arith`

## Description of categories:

* `arith`: Arithmetic error, eg. overflows
* `logic`: Logic bug
* `loop`: Infinite loop
* `oom`: Out of memory
* `oor`: Out of range access
* `segfault`: Program segfaulted
* `so`: Stack overflow
* `uaf`: Use after free
* `unwrap`: Call to `unwrap` on `None` or `Err(_)`
* `utf-8`: Problem with UTF-8 strings handling, eg. get a char not at a char boundary
* `panic`: A panic not covered by any of the above
* `other`: Anything that does not fit in another category, or unclear what the problem is
