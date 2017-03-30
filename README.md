# trophy case

## afl

* brotli-rs: [#2](https://github.com/ende76/brotli-rs/issues/2), [#3](https://github.com/ende76/brotli-rs/issues/3), [#4](https://github.com/ende76/brotli-rs/issues/4), [#5](https://github.com/ende76/brotli-rs/issues/5), [#6](https://github.com/ende76/brotli-rs/issues/6), [#7](https://github.com/ende76/brotli-rs/issues/7), [#8](https://github.com/ende76/brotli-rs/issues/8), [#9](https://github.com/ende76/brotli-rs/issues/9), [#10](https://github.com/ende76/brotli-rs/issues/10), [#11](https://github.com/ende76/brotli-rs/issues/11), [#12](https://github.com/ende76/brotli-rs/issues/12)
* cpp_demangle: [#41](https://github.com/fitzgen/cpp_demangle/pull/41)
* flac: [#3](https://github.com/sourrust/flac/issues/3)
* httparse: [#9](https://github.com/seanmonstar/httparse/issues/9)
* image: [#414](https://github.com/PistonDevelopers/image/issues/414), [#473](https://github.com/PistonDevelopers/image/issues/473), [#474](https://github.com/PistonDevelopers/image/issues/474), [#477](https://github.com/PistonDevelopers/image/issues/477)
* jpeg-decoder: [#38](https://github.com/kaksmet/jpeg-decoder/issues/38), [#50](https://github.com/kaksmet/jpeg-decoder/issues/50)
* mp3-metadata: [#9](https://github.com/GuillaumeGomez/mp3-metadata/pull/9)
* mp4parse-rust: [#2](https://github.com/mozilla/mp4parse-rust/issues/2), [#4](https://github.com/mozilla/mp4parse-rust/issues/4), [#5](https://github.com/mozilla/mp4parse-rust/issues/5), [#6](https://github.com/mozilla/mp4parse-rust/issues/6)
* rustc: [#24275](https://github.com/rust-lang/rust/issues/24275), [#24276](https://github.com/rust-lang/rust/issues/24276)
* rust-url: [#108](https://github.com/servo/rust-url/pull/108)
* regex: [#84](https://github.com/rust-lang/regex/issues/84)
* rust-asn1: [#32](https://github.com/alex/rust-asn1/issues/32)
* rustc-serialize: [#109](https://github.com/rust-lang/rustc-serialize/issues/109), [#110](https://github.com/rust-lang/rustc-serialize/issues/110)
* serde: [#75](https://github.com/serde-rs/serde/issues/75), [#77](https://github.com/serde-rs/serde/issues/77), [#82](https://github.com/serde-rs/serde/issues/82)
* tar-rs: [#23](https://github.com/alexcrichton/tar-rs/issues/23)
* xml-rs: [#93](https://github.com/netvl/xml-rs/issues/93)
* Logic errors in [tendril](https://github.com/kmcallister/tendril) and its [html5ever](https://github.com/servo/html5ever) integration

## libfuzzer

* [regex parsing panics](https://github.com/rust-lang/regex/pull/349), with [blog post](https://www.nibor.org/blog/fuzzing-is-magic---or-how-i-found-a-panic-in-rusts-regex-library/)
* unicode-segmentation: [grapheme boundary correctness](https://github.com/unicode-rs/unicode-segmentation/issues/19), [word boundary correctness](https://github.com/unicode-rs/unicode-segmentation/issues/20)
* image: [1](https://github.com/PistonDevelopers/image/issues/622), [2](https://github.com/PistonDevelopers/image/issues/623), [3](https://github.com/PistonDevelopers/image/issues/624), [4](https://github.com/PistonDevelopers/image/issues/625)
* inflate: [arithmetic overflow](https://github.com/PistonDevelopers/inflate/issues/14)
* capnproto-rust: [Multiple bugs, including a memory safety bug](https://dwrensha.github.io/capnproto-rust/2017/02/27/cargo-fuzz.html)
* hyper: [arithmetic overflow](https://github.com/hyperium/hyper/pull/1076)
* libpnet: [arithmetic overflow](https://github.com/libpnet/libpnet/pull/250)
* quick-xml: [arithmetic overflow](https://github.com/tafia/quick-xml/issues/53), [arithmetic overflow](https://github.com/tafia/quick-xml/pull/55/commits/53a5c099df585dd65382ffd7f2912728eaa764d5)
* svgparser: [arithmetic overflow, bound checking panic, incorrect result](https://github.com/RazrFalcon/libsvgparser/commit/4742f16e834445a682a0a4db62600d275a457390), [endless loop](https://github.com/RazrFalcon/libsvgparser/commit/c55d9a7d4d1e83f405be2e7bfddea89f579f6fc9)
* num: [panic on `BigInt` parsing](https://github.com/rust-num/num/issues/268)
* [httpdate panics](https://pyfisch.org/blog/fuzzing-all-crates/): "no character boundary" and arithmetic overflow
* vobsub: [invalid slice 1](https://github.com/emk/subtitles-rs/commit/20e430105b1fc02aa135788ba150a0dd49a7d1ef), [2](https://github.com/emk/subtitles-rs/commit/46df766dd22cb6a04a534611f08c23903e58746c), [3](https://github.com/emk/subtitles-rs/commit/f2f5309aa8173dfec4bb5816950d718a1ac669c2), [shift overflow](https://github.com/emk/subtitles-rs/commit/5d3364b96389d90deac0f024a57660951b7e1dd6), [arithmetic overflow](https://github.com/emk/subtitles-rs/commit/3afdb7e1c5e786e88653253243648dd9d49983f2)
* uuid: [index out of bounds](https://github.com/rust-lang-nursery/uuid/pull/81)
* flac: [index out of bounds](https://github.com/sourrust/flac/issues/11)
* ntp: [panic caused by unwrap on invalid input](https://github.com/JeffBelgum/ntp/commit/f23ded23c26a5326dae249905d298e8c5f51d371)
* pulldown-cmark: [Overflow ParseIntError](https://github.com/google/pulldown-cmark/issues/49)
* bson: [multiple bugs, including arithmetic overflow](https://github.com/zonyitoo/bson-rs/issues/64)
* jpeg-decoder: [arithmetic overflow](https://github.com/kaksmet/jpeg-decoder/issues/69)
* npy-rs: [arithmetic overflow](https://github.com/potocpav/npy-rs/pull/2)
* snmp-parser: [panic on unwrapping](https://github.com/rusticata/snmp-parser/issues/2)
* der-parser: [arithmetic overflow](https://github.com/rusticata/der-parser/issues/2)
