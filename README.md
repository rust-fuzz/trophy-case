# 🏆 Trophy Case 🏆

A showcase of bugs found via fuzz testing Rust codebases. It serves multiple purposes:

- Help the community see what issues are common in Rust codebases (useful when e.g. designing APIs)
- Increase visibility of effective fuzz testing targets so people can reuse testing strategies
- Provide insight into common issues they can expect to find if they use a certain fuzzer

These bugs aren't nearly as serious as the [memory-safety issues afl has discovered](http://lcamtuf.coredump.cx/afl/#bugs) in C and C++ projects. That's because Rust is memory-safe by default! Have you fuzzed Rust code and found a bug? Please consider adding it to this table via a pull request!

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
bson | [#116](https://github.com/zonyitoo/bson-rs/issues/116) | libfuzzer | `oom`
bson | [multiple bugs, including arithmetic overflow](https://github.com/zonyitoo/bson-rs/issues/64) | libfuzzer | `arith`, `other`, `unwrap`
capnproto-rust | [Multiple bugs, including a memory safety bug](https://dwrensha.github.io/capnproto-rust/2017/02/27/cargo-fuzz.html) | libfuzzer | | ❗️
capnproto-rust | [reddit](https://www.reddit.com/r/rust/comments/89y5eo/fuzzing_as_a_service_startup_looking_for_rust/dwueuww/), [`e72746c`](https://github.com/capnproto/capnproto-rust/commit/e72746cdd4c672a4b8881ed2ed0375b69d1afb3a) | libfuzzer | `logic`
claxon | [0fd8815](https://github.com/ruuda/claxon/commit/0fd88158a4d29c27f8218a324505583906228289) | libfuzzer | `unwrap`
claxon | [21b1db4](https://github.com/ruuda/claxon/commit/21b1db4a7891afdd453ee60085afc92cf61913ca) | libfuzzer | `oor`
claxon | [875c3b2](https://github.com/ruuda/claxon/commit/875c3b2e76326a5672af9d9ac8f7f36def514834) | libfuzzer | `logic`
claxon | [c036944](https://github.com/ruuda/claxon/commit/c036944b93ed8f96701d39b3a76392d30fc12d19) | libfuzzer | `logic`
claxon | [Massive slowdown on malformed input](https://github.com/ruuda/claxon/commit/0ec74f400cf71b376be59b16d7411d951d5eaecc) | libfuzzer | `other`
claxon | [Memory disclosure on malformed input](https://github.com/ruuda/claxon/issues/10)  | afl + [libdiffuzz](https://github.com/Shnatsel/libdiffuzz) | `uninit` | ❗️
comrak | [#65](https://github.com/kivikakk/comrak/pull/65) | libfuzzer | `oor`
cpp_demangle | [Multiple panics](https://github.com/fitzgen/cpp_demangle/pull/41) | afl | `unwrap`, `arith`
cranelift | [#418](https://github.com/CraneStation/cranelift/issues/418) | libfuzzer | `logic`
cssparser | [floating-point parsing imprecision](https://github.com/servo/rust-cssparser/issues/167) | libfuzzer | `logic`
cursive | [grapheme boundary correctness](https://github.com/gyscos/cursive/issues/489) | libfuzzer | `utf-8`
deflate-rs | [#40](https://github.com/image-rs/deflate-rs/issues/40) | afl | `logic`
deflate-rs | [#42](https://github.com/image-rs/deflate-rs/issues/42) | afl | `logic`
der-parser | [arithmetic overflow](https://github.com/rusticata/der-parser/issues/2) | libfuzzer | `arith`
dhcp4r | [#6](https://github.com/krolaw/dhcp4r/issues/6) | libfuzzer | `oor`
encoding_rs | [#44](https://github.com/hsivonen/encoding_rs/issues/44) | afl | `logic`
flac | [#3](https://github.com/sourrust/flac/issues/3) | afl | `oom`
flac | [index out of bounds](https://github.com/sourrust/flac/issues/11) | libfuzzer | `oor`
flif | [#26](https://github.com/dgriffen/flif.rs/pull/26) | libfuzzer | `oom`
fontdue | [arithmetic overflow](https://github.com/mooman219/fontdue/issues/35) | libfuzzer | `arith`
goblin | [memory exhaustion](https://github.com/m4b/goblin/issues/120) | afl | `oom`
h2 | [#260](https://github.com/carllerche/h2/pull/260) | honggfuzz | `oor`
h2 | [#261](https://github.com/carllerche/h2/pull/261) | honggfuzz | `panic`
h2 | [#262](https://github.com/carllerche/h2/pull/262) | honggfuzz | `panic`
httparse | [#9](https://github.com/seanmonstar/httparse/issues/9) | afl | `arith`
httpdate | [accepted dates like "May 35"](https://pyfisch.org/blog/fuzzing-all-crates/) | libfuzzer | `logic`, `arith`
httpdate | [panic on "no character boundary"](https://pyfisch.org/blog/fuzzing-all-crates/) | libfuzzer | `utf-8`
hyper | [arithmetic overflow](https://github.com/hyperium/hyper/pull/1076) | libfuzzer | `arith`
image | [#1238](https://github.com/image-rs/image/issues/1238) | afl | `oor`
image | [#414](https://github.com/PistonDevelopers/image/issues/414) | afl | `logic`
image | [#473](https://github.com/PistonDevelopers/image/issues/473) | afl | `arith`
image | [#474](https://github.com/PistonDevelopers/image/issues/474) | afl | `unwrap`
image | [#477](https://github.com/PistonDevelopers/image/issues/477) | afl | `oor`
image | [#622](https://github.com/PistonDevelopers/image/issues/622) | libfuzzer | `oom`
image | [#623](https://github.com/PistonDevelopers/image/issues/623) | libfuzzer | `oom`
image | [#624](https://github.com/PistonDevelopers/image/issues/624) | libfuzzer | `oom`
image | [#625](https://github.com/PistonDevelopers/image/issues/625) | libfuzzer | `oor`
image | [#876](https://github.com/PistonDevelopers/image/issues/876) | afl | `oor`
image | [#877](https://github.com/PistonDevelopers/image/issues/877) | afl | `arith`
image | [#878](https://github.com/PistonDevelopers/image/issues/878) | afl | `oor`
image | [Failed to break on an EOF](https://github.com/PistonDevelopers/image/issues/868) | afl | `oor`
inflate | [arithmetic overflow](https://github.com/PistonDevelopers/inflate/issues/14) | libfuzzer | `arith`
ipfix | [index out of bounds](https://github.com/DominoTree/rs-ipfix/issues/1) | libfuzzer | `oor`
jpeg-decoder | [#38](https://github.com/kaksmet/jpeg-decoder/issues/38) | afl | `unwrap`
jpeg-decoder | [#50](https://github.com/kaksmet/jpeg-decoder/issues/50) | afl | `oom`
jpeg-decoder | [arithmetic overflow](https://github.com/kaksmet/jpeg-decoder/issues/69) | libfuzzer | `arith`
json-rust | [arithmetic overflow](https://github.com/maciejhirsz/json-rust/issues/139) | afl | `arith`
juniper | [panic on "no character boundary"](https://github.com/graphql-rust/juniper/pull/645) | libfuzzer | `utf-8`
just | [#363](https://github.com/casey/just/issues/363) | libfuzzer | `logic`
lewton | [enormous CPU and memory consumption on crafted input](https://github.com/RustAudio/lewton/issues/35) | afl | `other`
lewton | [index out of bounds](https://github.com/RustAudio/lewton/issues/27) | honggfuzz | `oor`
lewton | [index out of bounds](https://github.com/RustAudio/lewton/issues/33) | afl | `oor`
lewton | [index out of bounds](https://github.com/RustAudio/lewton/issues/42) | afl | `oor`
lewton | [index out of bounds](https://github.com/RustAudio/lewton/issues/44) | afl | `oor`
lewton | [infinite loop](https://github.com/RustAudio/lewton/issues/46) | afl | `loop`
lewton | [large CPU and memory consumption on crafted input](https://github.com/RustAudio/lewton/issues/41) | afl | `other`
lewton | [memory exhaustion due to integer underflow](https://github.com/RustAudio/lewton/issues/32) | afl | `arith`, `oom`
lewton | [memory exhaustion](https://github.com/RustAudio/lewton/issues/43) | afl | `oom`
lexical | [arithmetic overflow](https://github.com/Alexhuszagh/rust-lexical/commit/466a63395e8d890cfa1fb650abb6e78fafe11771) | libfuzzer | `arith`
lexical | [arithmetic overflow](https://github.com/Alexhuszagh/rust-lexical/commit/cc8778384e6d77031b45aef2cb9cb831670573d6) | libfuzzer | `arith`
lexical | [Out-of-bounds read in unsafe code](https://github.com/Alexhuszagh/rust-lexical/commit/cc8778384e6d77031b45aef2cb9cb831670573d6) | libfuzzer | `oor`
libflate | [258cf44](https://github.com/sile/libflate/commit/258cf4430eb7e65bf904460b0334edcefb5d41a3) | honggfuzz | `oor`
libflate | [6157daa](https://github.com/sile/libflate/commit/6157daa468bc2d5c332c055570bfddefce3f5a3b) | honggfuzz | `panic`
libflate | [dc77163](https://github.com/sile/libflate/commit/dc77163c1cddf15a847f6217b4d838724dee5be0) | honggfuzz | `unwrap`
libflate | [Out-of-bounds read in unsafe code](https://github.com/sile/libflate/issues/16) | afl | `oor`
libpnet | [arithmetic overflow](https://github.com/libpnet/libpnet/pull/250) | libfuzzer | `arith`
libstd | [overflow in range bounds calculation on Vec::drain](https://github.com/rust-lang/rust/issues/74909) | [rutenspitz] | `arith`
lodepng-rust | [memory leak](https://github.com/kornelski/lodepng-rust/issues/28) | libfuzzer | `oom`
lz-fear | [index out of bounds](https://github.com/main--/rust-lz-fear/issues/7) | libfuzzer | `oor`
lz-fear | [index out of bounds](https://github.com/main--/rust-lz-fear/issues/8) | libfuzzer | `oor`
lz-fear | [memory exhaustion](https://github.com/main--/rust-lz-fear/issues/6) | libfuzzer | `oom`
lzma-rs | [behavior mismatch with reference implementation](https://github.com/gendx/lzma-rs/issues/35) | libfuzzer | `logic`
minidump | [#7](https://github.com/luser/rust-minidump/issues/7) | libfuzzer | `panic`
miniz_oxide | [Infinite loop exhausting memory](https://github.com/Frommi/miniz_oxide/commit/b53177a36853e265943fb01159da0fa99ebd430d) | libfuzzer | `loop`, `oom`
miniz_oxide | [Infinite loop](https://github.com/Frommi/miniz_oxide/commit/91c23bdbd54f60f91a34a299a08ef55ff68e6f15) | libfuzzer | `loop`
Molten | [#41](https://github.com/LeopoldArkham/Molten/issues/41) | libfuzzer | `utf-8`
Molten | [#42](https://github.com/LeopoldArkham/Molten/issues/42) | libfuzzer | `oor`
mongo_driver | [#55](https://github.com/thijsc/mongo-rust-driver/issues/55) | libfuzzer | `unwrap`
mp3-metadata | [Multiple panics](https://github.com/GuillaumeGomez/mp3-metadata/pull/9) | afl | `oor`
mp4parse-rust | [#2](https://github.com/mozilla/mp4parse-rust/issues/2) | afl | `panic`
mp4parse-rust | [#4](https://github.com/mozilla/mp4parse-rust/issues/4) | afl | `panic`
mp4parse-rust | [#5](https://github.com/mozilla/mp4parse-rust/issues/5) | afl | `panic`
mp4parse-rust | [#6](https://github.com/mozilla/mp4parse-rust/issues/6) | afl | `panic`
msgpack-rust | [#151](https://github.com/3Hren/msgpack-rust/issues/151) | afl | `oom`
ncurses-rs | [string with \0](https://github.com/jeaye/ncurses-rs/issues/196) | libfuzzer | `unwrap`
nifti | [out of bounds array slicing](https://github.com/Enet4/nifti-rs/pull/43) | libfuzzer | `oor`
nom | [arithmetic overflow](https://github.com/Geal/nom/pull/486) | libfuzzer | `arith`
npy-rs | [arithmetic overflow due to incorrect parameter declaration](https://github.com/potocpav/npy-rs/pull/2) | libfuzzer | `arith`, `logic`
ntp | [panic caused by unwrap on invalid input](https://github.com/JeffBelgum/ntp/commit/f23ded23c26a5326dae249905d298e8c5f51d371) | libfuzzer | `unwrap`
num | [panic on `BigInt` parsing](https://github.com/rust-num/num/issues/268) | libfuzzer | `unwrap`
pancurses | [string with \0](https://github.com/ihalila/pancurses/issues/77) | libfuzzer | `unwrap`
parity | [panic on `BasicDecoder` unchecked addition](https://github.com/paritytech/parity/issues/6226) | libfuzzer | `arith`
pcapng | [arithmetic overflow](https://github.com/richo/pcapng-rs/issues/6) | libfuzzer | `arith`
picky | [#10](https://github.com/Devolutions/picky-rs/pull/10) | libfuzzer | `unwrap`
picky-asn1-der | [#10](https://github.com/Devolutions/picky-rs/pull/10) | libfuzzer | `arith`, `oom`, `oor`
png | [crash on malformed input](https://github.com/PistonDevelopers/image-png/issues/103) | afl | `oom`
png | [incorrect buffer size due to integer overflow](https://github.com/PistonDevelopers/image-png/issues/80) | afl | `arith`, `oom`
png | [infinite loop on crafted input](https://github.com/PistonDevelopers/image-png/issues/217) | libfuzzer | `loop`
png | [panic on malformed input](https://github.com/PistonDevelopers/image-png/issues/222) | libfuzzer | `oor`
png | [panic on malformed input](https://github.com/PistonDevelopers/image-png/issues/79) | libfuzzer | `unwrap`
png | [panic on malformed input](https://github.com/PistonDevelopers/image-png/issues/79#issuecomment-400560072) | libfuzzer | `oor`
png | [panic on malformed input](https://github.com/PistonDevelopers/image-png/issues/79#issuecomment-400646862) | afl | `unwrap`, `logic`
proc-macro2 | [#54](https://github.com/alexcrichton/proc-macro2/issues/54) | afl | `utf-8`
proc-macro2 | [#55](https://github.com/alexcrichton/proc-macro2/issues/55) | afl | `so`
prost | [Stack overflow](https://github.com/danburkert/prost/issues/267) | afl | `so` | ❗️
pulldown-cmark | [arithmetic overflow](https://github.com/raphlinus/pulldown-cmark/issues/352) | libfuzzer | `arith`
pulldown-cmark | [Overflow ParseIntError](https://github.com/google/pulldown-cmark/issues/49) | libfuzzer | `unwrap`
pulldown-cmark | [Panics and infinite loop](https://github.com/google/pulldown-cmark/issues/81) | libfuzzer | `loop`, `utf-8`, `oor`
quick-xml | [arithmetic overflow](https://github.com/tafia/quick-xml/issues/53) | libfuzzer | `arith`
quick-xml | [arithmetic overflow](https://github.com/tafia/quick-xml/pull/55/commits/53a5c099df585dd65382ffd7f2912728eaa764d5) | libfuzzer | `arith`
quick-xml | [index out of bounds](https://github.com/tafia/quick-xml/issues/94) | libfuzzer | `oor`
rawloader | [abort on huge memory allocation](https://github.com/pedrocr/rawloader/commit/aaf584b4b10d859c9fb60c63d70c3d4437969c39) | afl | `oom`
regex | [#417](https://github.com/rust-lang/regex/issues/417) | afl | `utf-8`
regex | [#84](https://github.com/rust-lang/regex/issues/84) | afl | `unwrap`
regex | [called Option::unwrap() on a None value](https://github.com/rust-lang/regex/issues/465) | honggfuzz | `unwrap`
regex | [index out of bounds](https://github.com/rust-lang/regex/issues/464) | honggfuzz | `oor`
regex | [regex parsing panics](https://github.com/rust-lang/regex/pull/349) with [blog post](https://www.nibor.org/blog/fuzzing-is-magic---or-how-i-found-a-panic-in-rusts-regex-library/) | libfuzzer | `unwrap`
regex | [Unexpected match branch](https://github.com/rust-lang/regex/issues/465) | honggfuzz | `logic`
rmpv | [Unchecked vector pre-allocation](https://github.com/3Hren/msgpack-rust/issues/151) | afl | `oom`
roughenough | [handle truncated message](https://github.com/int08h/roughenough/commit/f1f4af2cdfa6f46a58038ca0551c6353d819ac57) | afl | `oor`
roughenough | [incorrect range check fix](https://github.com/int08h/roughenough/commit/ed267f79b0bc070c5c63e5936db79e9d5aced30c) | libfuzzer | `logic`
roughenough | [reject messages with zero tags](https://github.com/int08h/roughenough/commit/1b21bbc074b8acd146abce50e520eef84bbbec2d) | afl | `logic`, `oor`
roughenough | [reject short single tag messages](https://github.com/int08h/roughenough/commit/e0d15dc1d9bfbd92518916dbfc306cda32c47ff3) | afl | `logic`, `oor`
roughenough | [return Error instead of panicking](https://github.com/int08h/roughenough/commit/1ce57a140bcdd1c0c6dfbef1403a1aa11e2240ae) | afl | `panic`
roughenough | [validate tag offset not past end of message](https://github.com/int08h/roughenough/commit/a029e5073603bf33f64c7550451d32d6ac62963c) | afl | `logic`
roughenough | [validate value offset not pass end of message](https://github.com/int08h/roughenough/commit/9656fdab0f702ccd784a2e50eabcf94809bc31b5) | afl | `logic`
rust-asn1 | [#32](https://github.com/alex/rust-asn1/issues/32) | afl | `oom`
rust-snappy | [#12](https://github.com/BurntSushi/rust-snappy/issues/12) | libfuzzer | `oor`
rust-url | [#108](https://github.com/servo/rust-url/pull/108) | afl | `oor`
rustc | [#24275](https://github.com/rust-lang/rust/issues/24275) | afl | `other`
rustc | [#50577](https://github.com/rust-lang/rust/issues/50577) | [prog-fuzz] | `logic`
rustc | [#50582](https://github.com/rust-lang/rust/issues/50582) | [prog-fuzz] | `logic`
rustc | [#50585](https://github.com/rust-lang/rust/issues/50585) | [prog-fuzz] | `logic`
rustc | [#50600](https://github.com/rust-lang/rust/issues/50600) | [prog-fuzz] | `logic`
rustc | [#50637](https://github.com/rust-lang/rust/issues/50637) | [prog-fuzz] | `loop`
rustc | [#51070](https://github.com/rust-lang/rust/pull/51070) | [prog-fuzz] | `logic`
rustc-demangle | [multiply with overflow](https://github.com/alexcrichton/rustc-demangle/issues/9) | libfuzzer | `arith`
rustc-serialize | [#109](https://github.com/rust-lang/rustc-serialize/issues/109) | afl | `arith`
rustc-serialize | [#110](https://github.com/rust-lang/rustc-serialize/issues/110) | afl | `panic`
semver | [logic error](https://github.com/steveklabnik/semver/issues/116#issuecomment-311215219) | libfuzzer | `logic`
Sequoia-PGP | [#514](https://gitlab.com/sequoia-pgp/sequoia/-/issues/514) | libfuzzer | `arith`
Sequoia-PGP | [#515](https://gitlab.com/sequoia-pgp/sequoia/-/issues/515) | libfuzzer | `utf-8`
Sequoia-PGP | [#516](https://gitlab.com/sequoia-pgp/sequoia/-/issues/516) | libfuzzer | `oor`
Sequoia-PGP | [#516](https://gitlab.com/sequoia-pgp/sequoia/-/issues/517) | libfuzzer | `oor`
serde | [#75](https://github.com/serde-rs/serde/issues/75) | afl | `arith`
serde | [#77](https://github.com/serde-rs/serde/issues/77) | afl | `arith`
serde | [#82](https://github.com/serde-rs/serde/issues/82) | afl | `so`
serde-yaml | [#49](https://github.com/dtolnay/serde-yaml/issues/49) | libfuzzer | `so`
serde-yaml | [#88](https://github.com/dtolnay/serde-yaml/pull/88) | libfuzzer | `logic`
simple_asn1 | [#9](https://github.com/acw/simple_asn1/pull/9) | libfuzzer | `arith`, `oor`
sleep-parser | [#3](https://github.com/datrs/sleep-parser/issues/3) | honggfuzz | `oor`, `utf-8`
smoltcp | [arithmetic underflow](https://github.com/m-labs/smoltcp/commit/b33d867385e0f256f558d1268fa2c73470b7f34a) | libfuzzer | `arith`
smoltcp | [index out of bounds](https://github.com/m-labs/smoltcp/commit/181083f18c977b8a0463a67e360e4db20594fa21) | libfuzzer |  `oor`
smoltcp | [index out of bounds](https://github.com/m-labs/smoltcp/commit/2582d1573de37f23d77ed2b1e491d095c920ccfc) | libfuzzer | `oor`
smoltcp | [index out of bounds](https://github.com/m-labs/smoltcp/commit/2989fa334885916e9c8c76216a60b28c371a54cb) | libfuzzer | `oor`
smoltcp | [index out of bounds](https://github.com/m-labs/smoltcp/commit/31073835998016eb70982c69d0f2e5390dbc19b3) | libfuzzer | `oor`
smoltcp | [index out of bounds](https://github.com/m-labs/smoltcp/commit/3f43be8d8450db19fd427f48e8c658561591da1f) | libfuzzer | `oor`
smoltcp | [index out of bounds](https://github.com/m-labs/smoltcp/commit/c8ae7bdc219b82c62ee3410893fcc6d7455d64b0) | libfuzzer |  `oor`
smoltcp | [index out of bounds](https://github.com/m-labs/smoltcp/commit/ed2c376628b6566b0e48af2ca5a942d9fa288b9a) | libfuzzer | `oor`
snmp-parser | [panic on unwrapping](https://github.com/rusticata/snmp-parser/issues/2) | libfuzzer | `unwrap`
ssh-keys | [#3](https://github.com/tailhook/ssh-keys/issues/3) | afl | `oor`
ssh-keys | [panic on slice indexing](https://github.com/tailhook/ssh-keys/issues/1) | libfuzzer | `oor`
ssh-parser | [arithmetic overflow](https://github.com/rusticata/ssh-parser/issues/1) | libfuzzer | `arith`
svgparser | [arithmetic overflow, bound checking panic, incorrect result](https://github.com/RazrFalcon/libsvgparser/commit/4742f16e834445a682a0a4db62600d275a457390) | libfuzzer | `arith`, `oor`, `logic`
svgparser | [endless loop](https://github.com/RazrFalcon/libsvgparser/commit/c55d9a7d4d1e83f405be2e7bfddea89f579f6fc9) | libfuzzer | `loop`
swf-parser | [#23](https://github.com/open-flash/swf-parser/issues/23) | libfuzzer | `logic`
sxd-document | [use after free](https://github.com/shepmaster/sxd-document/issues/47) | libfuzzer | `uaf` | ❗️
tar-rs | [#23](https://github.com/alexcrichton/tar-rs/issues/23) | afl | `arith`
tera | [#396](https://github.com/Keats/tera/issues/396) | libfuzzer | `arith`, `logic`
tiff | [index out of bounds](https://github.com/PistonDevelopers/image-tiff/issues/28) | afl | `oor`
tiff | [infinite loop on malformed input](https://github.com/PistonDevelopers/image-tiff/issues/31) | afl | `loop`
tiff | [memory exhaustion on malformed input](https://github.com/PistonDevelopers/image-tiff/issues/29) | afl | `oom`
tiff | [panic on attempt to divide by zero](https://github.com/PistonDevelopers/image-tiff/issues/33) | afl | `arith`
tinyvec | [arithmetic underflow](https://github.com/Lokathor/tinyvec/pull/14) | [rutenspitz] | `arith`
tinyvec | [resize() could set incorrect size for inline storage](https://github.com/Lokathor/tinyvec/pull/16) | [rutenspitz] | `logic`
tinyvec | [swap_remove() for last element worked incorrectly](https://github.com/Lokathor/tinyvec/pull/15) | [rutenspitz] | `logic`
todotxt.rs | [index out of bounds](https://github.com/kstep/todotxt.rs/issues/1) | libfuzzer | `oor`
toml | [#178](https://github.com/alexcrichton/toml-rs/issues/178) | libfuzzer | `logic`
toml | [#179](https://github.com/alexcrichton/toml-rs/issues/179) | libfuzzer | `logic`
toml | [#180](https://github.com/alexcrichton/toml-rs/issues/180) | libfuzzer | `logic`
toml | [#181](https://github.com/alexcrichton/toml-rs/issues/181) | libfuzzer | `logic`
toml | [#185](https://github.com/alexcrichton/toml-rs/issues/185) | libfuzzer | `logic`
toml | [#186](https://github.com/alexcrichton/toml-rs/issues/186) | libfuzzer | `logic`
unicode-segmentation | [grapheme boundary correctness](https://github.com/unicode-rs/unicode-segmentation/issues/19) | libfuzzer | `logic`
unicode-segmentation | [word boundary correctness](https://github.com/unicode-rs/unicode-segmentation/issues/20) | libfuzzer | `logic`
uuid | [index out of bounds](https://github.com/rust-lang-nursery/uuid/pull/81) | libfuzzer | `oor`
v_escape | [heap buffer overflow](https://gitlab.com/r-iendo/v_escape/issues/2) | libfuzzer | `oor` | ❗️ 
vosub | [arithmetic overflow](https://github.com/emk/subtitles-rs/commit/3afdb7e1c5e786e88653253243648dd9d49983f2) | libfuzzer | `arith`
vosub | [invalid slice](https://github.com/emk/subtitles-rs/commit/20e430105b1fc02aa135788ba150a0dd49a7d1ef) | libfuzzer | `oor`
vosub | [invalid slice](https://github.com/emk/subtitles-rs/commit/46df766dd22cb6a04a534611f08c23903e58746c) | libfuzzer | `oor`
vosub | [invalid slice](https://github.com/emk/subtitles-rs/commit/f2f5309aa8173dfec4bb5816950d718a1ac669c2) | libfuzzer | `panic`
vosub | [shift overflow](https://github.com/emk/subtitles-rs/commit/5d3364b96389d90deac0f024a57660951b7e1dd6) | libfuzzer | `arith`
wasmparser.rs | [arithmetic overflow](https://github.com/yurydelendik/wasmparser.rs/issues/21#issuecomment-310253956) | libfuzzer | `arith`
wayland-rs | [#187](https://github.com/Smithay/wayland-rs/pull/187) | libfuzzer | `oor` | 
ws-rs | [arithmetic overflow](https://github.com/housleyjk/ws-rs/pull/179) | libfuzzer | `arith`
xml-rs | [#93](https://github.com/netvl/xml-rs/issues/93) | afl | `utf-8`
zip-rs | [arithmetic overflow](https://github.com/mvdnes/zip-rs/issues/40) | libfuzzer | `arith`

[prog-fuzz]: https://github.com/rust-fuzz/trophy-case/issues/36#issuecomment-388740655
[rutenspitz]: https://github.com/jakubadamw/rutenspitz

## Description of categories:

* `arith`: Arithmetic error, eg. overflows
* `logic`: Logic bug
* `loop`: Infinite loop
* `oom`: Out of memory
* `oor`: Out of range access
* `segfault`: Program segfaulted
* `so`: Stack overflow
* `uaf`: Use after free
* `uninit`: Program discloses contents of uninitialized memory
* `unwrap`: Call to `unwrap` on `None` or `Err(_)`
* `utf-8`: Problem with UTF-8 strings handling, eg. get a char not at a char boundary
* `panic`: A panic not covered by any of the above
* `other`: Anything that does not fit in another category, or unclear what the problem is
