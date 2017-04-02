# 🏆 Trophy Case 🏆

These bugs aren't nearly as serious as the [memory-safety issues afl has discovered](http://lcamtuf.coredump.cx/afl/#bugs) in C and C++ projects. That's because Rust is memory-safe by default, but also because not many people have tried fuzzing yet! Over time we will update this section with the most interesting bugs, whether they're logic errors or memory-safety problems arising from `unsafe` code. Pull requests are welcome!

Crate | Information | Fuzzer
----- | ----------- | ------
brotli-rs | [#10](https://github.com/ende76/brotli-rs/issues/10) | afl
brotli-rs | [#11](https://github.com/ende76/brotli-rs/issues/11) | afl
brotli-rs | [#12](https://github.com/ende76/brotli-rs/issues/12) | afl
brotli-rs | [#2](https://github.com/ende76/brotli-rs/issues/2) | afl
brotli-rs | [#3](https://github.com/ende76/brotli-rs/issues/3) | afl
brotli-rs | [#4](https://github.com/ende76/brotli-rs/issues/4) | afl
brotli-rs | [#5](https://github.com/ende76/brotli-rs/issues/5) | afl
brotli-rs | [#6](https://github.com/ende76/brotli-rs/issues/6) | afl
brotli-rs | [#7](https://github.com/ende76/brotli-rs/issues/7) | afl
brotli-rs | [#8](https://github.com/ende76/brotli-rs/issues/8) | afl
brotli-rs | [#9](https://github.com/ende76/brotli-rs/issues/9) | afl
bson | [multiple bugs, including arithmetic overflow](https://github.com/zonyitoo/bson-rs/issues/64) | libfuzzer
capnproto-rust | [Multiple bugs, including a memory safety bug](https://dwrensha.github.io/capnproto-rust/2017/02/27/cargo-fuzz.html) | libfuzzer
cpp_demangle | [#41](https://github.com/fitzgen/cpp_demangle/pull/41) | afl
der-parser | [arithmetic overflow](https://github.com/rusticata/der-parser/issues/2) | libfuzzer
flac | [#3](https://github.com/sourrust/flac/issues/3) | afl
flac | [index out of bounds](https://github.com/sourrust/flac/issues/11) | libfuzzer
httparse | [#9](https://github.com/seanmonstar/httparse/issues/9) | afl
httpdate | [panics](https://pyfisch.org/blog/fuzzing-all-crates/): "no character boundary" and arithmetic overflow | libfuzzer
hyper | [arithmetic overflow](https://github.com/hyperium/hyper/pull/1076) | libfuzzer
image | [#414](https://github.com/PistonDevelopers/image/issues/414) | afl
image | [#473](https://github.com/PistonDevelopers/image/issues/473) | afl
image | [#474](https://github.com/PistonDevelopers/image/issues/474) | afl
image | [#477](https://github.com/PistonDevelopers/image/issues/477) | afl
image | [1](https://github.com/PistonDevelopers/image/issues/622) | libfuzzer
image | [2](https://github.com/PistonDevelopers/image/issues/623) | libfuzzer
image | [3](https://github.com/PistonDevelopers/image/issues/624) | libfuzzer
image | [4](https://github.com/PistonDevelopers/image/issues/625) | libfuzzer
inflate | [arithmetic overflow](https://github.com/PistonDevelopers/inflate/issues/14) | libfuzzer
jpeg-decoder | [#38](https://github.com/kaksmet/jpeg-decoder/issues/38) | afl
jpeg-decoder | [#50](https://github.com/kaksmet/jpeg-decoder/issues/50) | afl
jpeg-decoder | [arithmetic overflow](https://github.com/kaksmet/jpeg-decoder/issues/69) | libfuzzer
libpnet | [arithmetic overflow](https://github.com/libpnet/libpnet/pull/250) | libfuzzer
mp3-metadata | [#9](https://github.com/GuillaumeGomez/mp3-metadata/pull/9) | afl
mp4parse-rust | [#2](https://github.com/mozilla/mp4parse-rust/issues/2) | afl
mp4parse-rust | [#4](https://github.com/mozilla/mp4parse-rust/issues/4) | afl
mp4parse-rust | [#5](https://github.com/mozilla/mp4parse-rust/issues/5) | afl
mp4parse-rust | [#6](https://github.com/mozilla/mp4parse-rust/issues/6) | afl
npy-rs | [arithmetic overflow](https://github.com/potocpav/npy-rs/pull/2) | libfuzzer
ntp | [panic caused by unwrap on invalid input](https://github.com/JeffBelgum/ntp/commit/f23ded23c26a5326dae249905d298e8c5f51d371) | libfuzzer
num | [panic on `BigInt` parsing](https://github.com/rust-num/num/issues/268) | libfuzzer
pulldown-cmark | [Overflow ParseIntError](https://github.com/google/pulldown-cmark/issues/49) | libfuzzer
quick-xml | [arithmetic overflow](https://github.com/tafia/quick-xml/issues/53) | libfuzzer
quick-xml | [arithmetic overflow](https://github.com/tafia/quick-xml/pull/55/commits/53a5c099df585dd65382ffd7f2912728eaa764d5) | libfuzzer
regex | [#84](https://github.com/rust-lang/regex/issues/84) | afl
regex | [regex parsing panics](https://github.com/rust-lang/regex/pull/349) with [blog post](https://www.nibor.org/blog/fuzzing-is-magic---or-how-i-found-a-panic-in-rusts-regex-library/) | libfuzzer
rust-asn1 | [#32](https://github.com/alex/rust-asn1/issues/32) | afl
rust-url | [#108](https://github.com/servo/rust-url/pull/108) | afl
rustc | [#24275](https://github.com/rust-lang/rust/issues/24275) | afl
rustc | [#24276](https://github.com/rust-lang/rust/issues/24276) | afl
rustc-serialize | [#109](https://github.com/rust-lang/rustc-serialize/issues/109) | afl
rustc-serialize | [#110](https://github.com/rust-lang/rustc-serialize/issues/110) | afl
serde | [#75](https://github.com/serde-rs/serde/issues/75) | afl
serde | [#77](https://github.com/serde-rs/serde/issues/77) | afl
serde | [#82](https://github.com/serde-rs/serde/issues/82) | afl
snmp-parser | [panic on unwrapping](https://github.com/rusticata/snmp-parser/issues/2) | libfuzzer
ssh-keys | [panic on slice indexing](https://github.com/tailhook/ssh-keys/issues/1) | libfuzzer
svgparser | [arithmetic overflow, bound checking panic, incorrect result](https://github.com/RazrFalcon/libsvgparser/commit/4742f16e834445a682a0a4db62600d275a457390) | libfuzzer
svgparser | [endless loop](https://github.com/RazrFalcon/libsvgparser/commit/c55d9a7d4d1e83f405be2e7bfddea89f579f6fc9) | libfuzzer
tar-rs | [#23](https://github.com/alexcrichton/tar-rs/issues/23) | afl
unicode-segmentation | [grapheme boundary correctness](https://github.com/unicode-rs/unicode-segmentation/issues/19) | libfuzzer
unicode-segmentation | [word boundary correctness](https://github.com/unicode-rs/unicode-segmentation/issues/20) | libfuzzer
uuid | [index out of bounds](https://github.com/rust-lang-nursery/uuid/pull/81) | libfuzzer
vosub | [2](https://github.com/emk/subtitles-rs/commit/46df766dd22cb6a04a534611f08c23903e58746c) | libfuzzer
vosub | [3](https://github.com/emk/subtitles-rs/commit/f2f5309aa8173dfec4bb5816950d718a1ac669c2) | libfuzzer
vosub | [arithmetic overflow](https://github.com/emk/subtitles-rs/commit/3afdb7e1c5e786e88653253243648dd9d49983f2) | libfuzzer
vosub | [invalid slice 1](https://github.com/emk/subtitles-rs/commit/20e430105b1fc02aa135788ba150a0dd49a7d1ef) | libfuzzer
vosub | [shift overflow](https://github.com/emk/subtitles-rs/commit/5d3364b96389d90deac0f024a57660951b7e1dd6) | libfuzzer
xml-rs | [#93](https://github.com/netvl/xml-rs/issues/93) | afl
