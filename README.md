# 🏆 Trophy Case 🏆

A showcase of bugs found via fuzz testing Rust codebases. It serves multiple purposes:

- Help the community see what issues are common in Rust codebases (useful when e.g. designing APIs)
- Increase visibility of effective fuzz testing targets so people can reuse testing strategies
- Provide insight into common issues they can expect to find if they use a certain fuzzer

These bugs aren't nearly as serious as the [memory-safety issues afl has discovered](http://lcamtuf.coredump.cx/afl/#bugs) in C and C++ projects. That's because Rust is memory-safe by default! Have you fuzzed Rust code and found a bug? Please consider adding it to this table via a pull request!

Security issues are marked with a ❗️ in the "Security?" column. Denial of service, including panics and out-of-memory, are not considered security issues.

Crate | Information | Fuzzer | Category | Security?
----- | ----------- | ------ | ---------|----------
artichoke | [infinite loop in bison-generated C code](https://github.com/mruby/mruby/issues/5676) | libfuzzer | `loop`
asn1 | [#32](https://github.com/alex/rust-asn1/issues/32) | afl | `oom`
async-h1 | [non-ASCII input to method](https://github.com/http-rs/async-h1/issues/187) | libfuzzer | `panic`
bcrypt | [indexing on non-utf8 boundry](https://github.com/Keats/rust-bcrypt/issues/62) | libfuzzer | `utf-8`
bincode | [invalid system time panic](https://github.com/bincode-org/bincode/pull/469) | libfuzzer | `panic`
bincode | [invalid duration panic](https://github.com/bincode-org/bincode/pull/465) | libfuzzer | `panic`
bmfont | [panic on unwrapping](https://github.com/netgusto/rust-bmfont/issues/2) | libfuzzer | `panic`
boa | [invalid spans](https://github.com/boa-dev/boa/issues/771) | honggfuzz | `logic`
boa | [Could not convert to BigInt](https://github.com/boa-dev/boa/issues/772) | honggfuzz | `logic`
boa | [invalid utf16](https://github.com/boa-dev/boa/issues/778) | honggfuzz | `logic`
boa | [assignment to number](https://github.com/boa-dev/boa/issues/779) | honggfuzz | `logic`
boa | [division by zero](https://github.com/boa-dev/boa/issues/780) | honggfuzz | `arith`
boa | [assertion failure](https://github.com/boa-dev/boa/issues/1768) | libfuzzer | `panic`
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
bson | [arithmetic overflow leading to out of memory](https://github.com/mongodb/bson-rust/issues/243) | libfuzzer | `arith`, `oom`
capnproto-rust | [Multiple bugs, including a memory safety bug](https://dwrensha.github.io/capnproto-rust/2017/02/27/cargo-fuzz.html) | libfuzzer | | ❗️
capnproto-rust | [reddit](https://www.reddit.com/r/rust/comments/89y5eo/fuzzing_as_a_service_startup_looking_for_rust/dwueuww/), [`e72746c`](https://github.com/capnproto/capnproto-rust/commit/e72746cdd4c672a4b8881ed2ed0375b69d1afb3a) | libfuzzer | `logic`
chrono | [overflow in date arithmetic](https://github.com/chronotope/chrono/issues/645) | libfuzzer | `arith`
clap | [issue/2264](https://github.com/clap-rs/clap/issues/2264) | afl | `utf-8`
claxon | [0fd8815](https://github.com/ruuda/claxon/commit/0fd88158a4d29c27f8218a324505583906228289) | libfuzzer | `unwrap`
claxon | [21b1db4](https://github.com/ruuda/claxon/commit/21b1db4a7891afdd453ee60085afc92cf61913ca) | libfuzzer | `oor`
claxon | [875c3b2](https://github.com/ruuda/claxon/commit/875c3b2e76326a5672af9d9ac8f7f36def514834) | libfuzzer | `logic`
claxon | [c036944](https://github.com/ruuda/claxon/commit/c036944b93ed8f96701d39b3a76392d30fc12d19) | libfuzzer | `logic`
claxon | [Massive slowdown on malformed input](https://github.com/ruuda/claxon/commit/0ec74f400cf71b376be59b16d7411d951d5eaecc) | libfuzzer | `other`
claxon | [Memory disclosure on malformed input](https://github.com/ruuda/claxon/issues/10)  | afl + [libdiffuzz](https://github.com/Shnatsel/libdiffuzz) | `uninit` | ❗️
comrak | [#65](https://github.com/kivikakk/comrak/pull/65) | libfuzzer | `oor`
cookie | [indexing on non-utf8 boundry](https://github.com/SergioBenitez/cookie-rs/issues/178) | libfuzzer | `utf-8`
cpp_demangle | [Multiple panics](https://github.com/fitzgen/cpp_demangle/pull/41) | afl | `unwrap`, `arith`
cranelift | [#418](https://github.com/CraneStation/cranelift/issues/418) | libfuzzer | `logic`
csscolorparser | [indexing on non-utf8 boundry](https://github.com/mazznoer/csscolorparser-rs/pull/7) | libfuzzer | `utf-8`
cssparser | [floating-point parsing imprecision](https://github.com/servo/rust-cssparser/issues/167) | libfuzzer | `logic`
cursive | [grapheme boundary correctness](https://github.com/gyscos/cursive/issues/489) | libfuzzer | `utf-8`
deflate-rs | [#40](https://github.com/image-rs/deflate-rs/issues/40) | afl | `logic`
deflate-rs | [#42](https://github.com/image-rs/deflate-rs/issues/42) | afl | `logic`
der | [arithmetic overflow leading to index out of bounds](https://github.com/RustCrypto/formats/pull/447) | libfuzzer | `arith`
der-parser | [arithmetic overflow](https://github.com/rusticata/der-parser/issues/2) | libfuzzer | `arith`
dhcp4r | [#6](https://github.com/krolaw/dhcp4r/issues/6) | libfuzzer | `oor`
encoding_rs | [#44](https://github.com/hsivonen/encoding_rs/issues/44) | afl | `logic`
exmex | [#8](https://github.com/bertiqwerty/exmex/issues/8) | honggfuzz | `arith`, `logic`
exmex | [#13](https://github.com/bertiqwerty/exmex/issues/13) | libfuzzer | `utf-8`
fatfs | [arithmetic overflow](https://github.com/rafalh/rust-fatfs/issues/56) | libfuzzer | `arith`
flac | [#3](https://github.com/sourrust/flac/issues/3) | afl | `oom`
flac | [index out of bounds](https://github.com/sourrust/flac/issues/11) | libfuzzer | `oor`
flatgeobuf | [#85](https://github.com/bjornharrtell/flatgeobuf/issues/85) | libfuzzer | `oom`
flatgeobuf | [#86](https://github.com/bjornharrtell/flatgeobuf/issues/86) | libfuzzer | `oor`
flif | [#26](https://github.com/dgriffen/flif.rs/pull/26) | libfuzzer | `oom`
fontdue | [arithmetic overflow](https://github.com/mooman219/fontdue/issues/35) | libfuzzer | `arith`
fontdue | [slow parsing](https://github.com/mooman219/fontdue/issues/97) | libfuzzer | `other`
geo | [#531](https://github.com/georust/geo/issues/531) | libfuzzer | `logic`
geo | [#536](https://github.com/georust/geo/issues/536) | libfuzzer | `logic`
goblin | [memory exhaustion](https://github.com/m4b/goblin/issues/120) | afl | `oom`
goblin | [memory exhaustion](https://github.com/m4b/goblin/pull/298) | libfuzzer | `oom`
h2 | [#260](https://github.com/carllerche/h2/pull/260) | honggfuzz | `oor`
h2 | [#261](https://github.com/carllerche/h2/pull/261) | honggfuzz | `panic`
h2 | [#262](https://github.com/carllerche/h2/pull/262) | honggfuzz | `panic`
h2 | [assertion failure](https://github.com/hyperium/h2/issues/581) | libfuzzer | `panic`
handlebars | [index out of bounds](https://github.com/sunng87/handlebars-rust/pull/430) | libfuzzer | `oor`
handlebars | [unwrap panic](https://github.com/sunng87/handlebars-rust/issues/427) | libfuzzer | `unwrap`
hjson-rust | [invalid utf8](https://github.com/hjson/hjson-rust/issues/19) | libfuzzer | `utf-8`
hjson-rust | [subtract with overflow](https://github.com/hjson/hjson-rust/issues/20) | libfuzzer | `arith`
hjson-rust | [removal index (is 0) should be < len](https://github.com/hjson/hjson-rust/issues/21) | libfuzzer | `logic`
hjson-rust | [panics on ParseIntError](https://github.com/hjson/hjson-rust/issues/22) | libfuzzer | `arith`
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
image | [arithmetic overflow](https://github.com/image-rs/image/pull/1563) | libfuzzer | `arith`
image-gif | [infinite loop](https://github.com/image-rs/image-gif/issues/101) | libfuzzer | `loop`
inflate | [arithmetic overflow](https://github.com/PistonDevelopers/inflate/issues/14) | libfuzzer | `arith`
ipfix | [index out of bounds](https://github.com/DominoTree/rs-ipfix/issues/1) | libfuzzer | `oor`
jpeg-decoder | [#38](https://github.com/image-rs/jpeg-decoder/issues/38) | afl | `unwrap`
jpeg-decoder | [#50](https://github.com/image-rs/jpeg-decoder/issues/50) | afl | `oom`
jpeg-decoder | [arithmetic overflow](https://github.com/image-rs/jpeg-decoder/issues/69) | libfuzzer | `arith`
jpeg-decoder | [180](https://github.com/image-rs/jpeg-decoder/issues/180) | libfuzzer | `logic`
jpeg-decoder | [arithmetic overflow](https://github.com/image-rs/jpeg-decoder/pull/206) | libfuzzer | `arith`
json-rust | [arithmetic overflow](https://github.com/maciejhirsz/json-rust/issues/139) | afl | `arith`
json-rust | [issue/193](https://github.com/maciejhirsz/json-rust/issues/193) | afl | `panic`  
jsonschema | [issue/253](https://github.com/Stranger6667/jsonschema-rs/issues/253) | libfuzzer | `oor`  
juniper | [panic on "no character boundary"](https://github.com/graphql-rust/juniper/pull/645) | libfuzzer | `utf-8`
just | [#363](https://github.com/casey/just/issues/363) | libfuzzer | `logic`
kalker | [index out of bounds](https://github.com/PaddiM8/kalker/issues/57) | libfuzzer | `oor`
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
libflate | [internal assertion failure](https://github.com/sile/libflate/issues/64) | libfuzzer | `panic`
libpnet | [arithmetic overflow](https://github.com/libpnet/libpnet/pull/250) | libfuzzer | `arith`
libstd | [overflow in range bounds calculation on Vec::drain](https://github.com/rust-lang/rust/issues/74909) | [rutenspitz] | `arith`
lodepng-rust | [memory leak](https://github.com/kornelski/lodepng-rust/issues/28) | libfuzzer | `oom`
lopdf | [arithmetic overflow](https://github.com/J-F-Liu/lopdf/issues/153) | libfuzzer | `arith`
lz-fear | [index out of bounds](https://github.com/main--/rust-lz-fear/issues/7) | libfuzzer | `oor`
lz-fear | [index out of bounds](https://github.com/main--/rust-lz-fear/issues/8) | libfuzzer | `oor`
lz-fear | [memory exhaustion](https://github.com/main--/rust-lz-fear/issues/6) | libfuzzer | `oom`
lz4_flex | [memcpy-param-overlap](https://github.com/PSeitz/lz4_flex/commit/286ea4cf103078b5b814ef91b62fb2b4e038bceb#diff-2ccf95c39e3fe83bf326d3a07d4c388adb75795bc263b3622e0f804e033d5a0fR216) | libfuzzer | `other`
lz4_flex | [heap-buffer-overflow](ce92fbf28c94a0f1f6ebc711c86d854e2c9e5622) | libfuzzer | `oor` | ❗️ 
lzma-rs | [behavior mismatch with reference implementation](https://github.com/gendx/lzma-rs/issues/35) | libfuzzer | `logic`
matchit | [invalid utf-8](https://github.com/ibraheemdev/matchit/issues/3) | libfuzzer | `utf-8`
minidump | [#7](https://github.com/luser/rust-minidump/issues/7) | libfuzzer | `panic`
minidump | [unbounded allocation](https://github.com/luser/rust-minidump/issues/381) | libfuzzer | `oom`
minidump | [slicing out of bounds](https://github.com/luser/rust-minidump/pull/406) | libfuzzer | `oor`
minidump | [creating backwards ranges](https://github.com/luser/rust-minidump/issues/407) | libfuzzer | `panic`
minidump | [add with overflow #413](https://github.com/luser/rust-minidump/issues/413) | libfuzzer | `arith`
minidump | [add with overflow #422](https://github.com/luser/rust-minidump/issues/422) | libfuzzer | `arith`
minidump | [add with overflow #425](https://github.com/luser/rust-minidump/pull/425) | libfuzzer | `arith`
minidump | [infinitely extending vec OOM](https://github.com/luser/rust-minidump/issues/428) | libfuzzer | `oom`
minidump | [subtract with overflow #439](https://github.com/luser/rust-minidump/issues/439) | libfuzzer | `arith`
minidump | [index OOB](https://github.com/luser/rust-minidump/issues/440) | libfuzzer | `oor`
miniz_oxide | [Infinite loop exhausting memory](https://github.com/Frommi/miniz_oxide/commit/b53177a36853e265943fb01159da0fa99ebd430d) | libfuzzer | `loop`, `oom`
miniz_oxide | [Infinite loop](https://github.com/Frommi/miniz_oxide/commit/91c23bdbd54f60f91a34a299a08ef55ff68e6f15) | libfuzzer | `loop`
Molten | [#41](https://github.com/LeopoldArkham/Molten/issues/41) | libfuzzer | `utf-8`
Molten | [#42](https://github.com/LeopoldArkham/Molten/issues/42) | libfuzzer | `oor`
mongo_driver | [#55](https://github.com/thijsc/mongo-rust-driver/issues/55) | libfuzzer | `unwrap`
mp3-metadata | [Multiple panics](https://github.com/GuillaumeGomez/mp3-metadata/pull/9) | afl | `oor`
mp4ameta | [unbounded allocation](https://github.com/Saecki/rust-mp4ameta/issues/25) | libfuzzer | `oom`
mp4parse-rust | [#2](https://github.com/mozilla/mp4parse-rust/issues/2) | afl | `panic`
mp4parse-rust | [#4](https://github.com/mozilla/mp4parse-rust/issues/4) | afl | `panic`
mp4parse-rust | [#5](https://github.com/mozilla/mp4parse-rust/issues/5) | afl | `panic`
mp4parse-rust | [#6](https://github.com/mozilla/mp4parse-rust/issues/6) | afl | `panic`
msgpack-rust | [#151](https://github.com/3Hren/msgpack-rust/issues/151) | afl | `oom`
naga | [slicing not on a character boundary](https://github.com/gfx-rs/naga/issues/90) | libfuzzer | `utf-8`
ncurses-rs | [string with \0](https://github.com/jeaye/ncurses-rs/issues/196) | libfuzzer | `unwrap`
nifti | [out of bounds array slicing](https://github.com/Enet4/nifti-rs/pull/43) | libfuzzer | `oor`
nom | [arithmetic overflow](https://github.com/Geal/nom/pull/486) | libfuzzer | `arith`
npy-rs | [arithmetic overflow due to incorrect parameter declaration](https://github.com/potocpav/npy-rs/pull/2) | libfuzzer | `arith`, `logic`
ntfs | [multiply with overflow](https://github.com/ColinFinck/ntfs/issues/1) | libfuzzer | `arith`
ntfs | [index OOB](https://github.com/ColinFinck/ntfs/issues/2) | libfuzzer | `oor`
ntp | [panic caused by unwrap on invalid input](https://github.com/JeffBelgum/ntp/commit/f23ded23c26a5326dae249905d298e8c5f51d371) | libfuzzer | `unwrap`
num | [panic on `BigInt` parsing](https://github.com/rust-num/num/issues/268) | libfuzzer | `unwrap`
pancurses | [string with \0](https://github.com/ihalila/pancurses/issues/77) | libfuzzer | `unwrap`
parity | [panic on `BasicDecoder` unchecked addition](https://github.com/paritytech/parity/issues/6226) | libfuzzer | `arith`
pcapng | [arithmetic overflow](https://github.com/richo/pcapng-rs/issues/6) | libfuzzer | `arith`
pdf | [index out of bounds](https://github.com/pdf-rs/pdf/pull/105) | libfuzzer | `oor`
pdf | [infinite loop](https://github.com/pdf-rs/pdf/issues/103) | libfuzzer | `loop`
pdf | [stack overflow (unbounded recursion)](https://github.com/pdf-rs/pdf/issues/121) | libfuzzer | `so`
pdf | [stack overflow (unbounded recursion)](https://github.com/pdf-rs/pdf/issues/121#issuecomment-1003432668) | libfuzzer | `so`
pdf | [stack overflow (unbounded recursion)](https://github.com/pdf-rs/pdf/issues/121#issuecomment-1003575433) | libfuzzer | `so`
pdf | [stack overflow (unbounded recursion)](https://github.com/pdf-rs/pdf/issues/121#issuecomment-1003581020) | libfuzzer | `so`
pdf | [index out of bounds #122](https://github.com/pdf-rs/pdf/issues/122) | libfuzzer | `oor`
pdf | [index out of bounds #123](https://github.com/pdf-rs/pdf/issues/123) | libfuzzer | `oor`
pdf | [index out of bounds #124](https://github.com/pdf-rs/pdf/pull/124) | libfuzzer | `oor`
pdf | [index out of bounds #126](https://github.com/pdf-rs/pdf/issues/126) | libfuzzer | `oor`
pgp | [subtract with overflow](https://github.com/rpgp/rpgp/issues/146) | libfuzzer | `arith`
phonenumber | [internal unwrap](https://github.com/rustonaut/rust-phonenumber/issues/43) | libfuzzer | `unwrap`
picky | [#10](https://github.com/Devolutions/picky-rs/pull/10) | libfuzzer | `unwrap`
picky-asn1-der | [#10](https://github.com/Devolutions/picky-rs/pull/10) | libfuzzer | `arith`, `oom`, `oor`
plist | [arithmetic overflow](https://github.com/ebarnard/rust-plist/pull/71) | libfuzzer | `arith`
png | [crash on malformed input](https://github.com/PistonDevelopers/image-png/issues/103) | afl | `oom`
png | [incorrect buffer size due to integer overflow](https://github.com/PistonDevelopers/image-png/issues/80) | afl | `arith`, `oom`
png | [infinite loop on crafted input](https://github.com/PistonDevelopers/image-png/issues/217) | libfuzzer | `loop`
png | [panic on malformed input](https://github.com/PistonDevelopers/image-png/issues/222) | libfuzzer | `oor`
png | [panic on malformed input](https://github.com/PistonDevelopers/image-png/issues/79) | libfuzzer | `unwrap`
png | [panic on malformed input](https://github.com/PistonDevelopers/image-png/issues/79#issuecomment-400560072) | libfuzzer | `oor`
png | [panic on malformed input](https://github.com/PistonDevelopers/image-png/issues/79#issuecomment-400646862) | afl | `unwrap`, `logic`
prettytable-rs | [subtract with overflow](https://github.com/phsym/prettytable-rs/issues/130) | libfuzzer | `arith`
proc-macro2 | [#54](https://github.com/alexcrichton/proc-macro2/issues/54) | afl | `utf-8`
proc-macro2 | [#55](https://github.com/alexcrichton/proc-macro2/issues/55) | afl | `so`
prost | [Stack overflow](https://github.com/tokio-rs/prost/issues/267) | afl | `so`
pulldown-cmark | [arithmetic overflow](https://github.com/raphlinus/pulldown-cmark/issues/352) | libfuzzer | `arith`
pulldown-cmark | [Overflow ParseIntError](https://github.com/google/pulldown-cmark/issues/49) | libfuzzer | `unwrap`
pulldown-cmark | [Panics and infinite loop](https://github.com/google/pulldown-cmark/issues/81) | libfuzzer | `loop`, `utf-8`, `oor`
pulldown-cmark | [string slice out of bounds](https://github.com/raphlinus/pulldown-cmark/issues/521) | libfuzzer | `oor`
pulldown-cmark | [beginning more than end slice index](https://github.com/raphlinus/pulldown-cmark/issues/561) | libfuzzer | `oor`
pulldown-cmark | [option unwrap parsing heading attributes](https://github.com/raphlinus/pulldown-cmark/issues/571) | libfuzzer | `unwrap`
quick-xml | [arithmetic overflow](https://github.com/tafia/quick-xml/issues/53) | libfuzzer | `arith`
quick-xml | [arithmetic overflow](https://github.com/tafia/quick-xml/pull/55/commits/53a5c099df585dd65382ffd7f2912728eaa764d5) | libfuzzer | `arith`
quick-xml | [index out of bounds](https://github.com/tafia/quick-xml/issues/94) | libfuzzer | `oor`
quick-xml | [internal unreachable panic](https://github.com/tafia/quick-xml/issues/344) | libfuzzer | `panic`
rasn | [failed round trip](https://github.com/XAMPPRocky/rasn/issues/57) | libfuzzer | `logic`
rawloader | [abort on huge memory allocation](https://github.com/pedrocr/rawloader/commit/aaf584b4b10d859c9fb60c63d70c3d4437969c39) | afl | `oom`
rav1e | [Invalid assertion in rate control](https://github.com/xiph/rav1e/pull/1630) | libfuzzer | `panic`
rav1e | [LRF crash when encoding tiny frames](https://github.com/xiph/rav1e/pull/1797) | libfuzzer | `panic`
rav1e | [CDEF UV direction mismatch for 4:2:2](https://github.com/xiph/rav1e/pull/2224) | libfuzzer | `logic`
rav1e | [Safe wrappers for-sys dav1d](https://github.com/xiph/rav1e/pull/2225) | libfuzzer | `logic`
rav1e | [Crash with 4 tiles for 1080p 4:2:2](https://github.com/xiph/rav1e/pull/2302) | libfuzzer | `logic`
rav1e | [Buffer underflow in CDEF pad_into_tmp16](https://github.com/xiph/rav1e/pull/2536) | libfuzzer | `so`
rav1e | [Tiling mismatch for 4:2:2](https://github.com/xiph/rav1e/pull/2537) | libfuzzer | `logic`
rav1e | [Encode-decode mismatch ](https://github.com/xiph/rav1e/issues/1636) | libfuzzer | `logic`
rav1e | [Crash on width or height of 1](https://github.com/xiph/rav1e/pull/2644) | libfuzzer | `panic`
rav1e | [Encoder admits invalid color configuration](https://github.com/xiph/rav1e/issue/2586) | libfuzzer | `logic`
regex | [#417](https://github.com/rust-lang/regex/issues/417) | afl | `utf-8`
regex | [#84](https://github.com/rust-lang/regex/issues/84) | afl | `unwrap`
regex | [called Option::unwrap() on a None value](https://github.com/rust-lang/regex/issues/465) | honggfuzz | `unwrap`
regex | [index out of bounds](https://github.com/rust-lang/regex/issues/464) | honggfuzz | `oor`
regex | [regex parsing panics](https://github.com/rust-lang/regex/pull/349) with [blog post](https://www.nibor.org/blog/fuzzing-is-magic---or-how-i-found-a-panic-in-rusts-regex-library/) | libfuzzer | `unwrap`
regex | [Unexpected match branch](https://github.com/rust-lang/regex/issues/465) | honggfuzz | `logic`
regex | [issue/738](https://github.com/rust-lang/regex/issues/738) | afl | `arith`, `oor`, `utf-8`
rmpv | [Unchecked vector pre-allocation](https://github.com/3Hren/msgpack-rust/issues/151) | afl | `oom`
ron | [stack overflow (unbounded recursion)](https://github.com/ron-rs/ron/issues/307) | libfuzzer | `so`
ron | [Maps are wrapped in a sequence](https://github.com/ron-rs/ron/issues/338) | libfuzzer | `logic`
roughenough | [handle truncated message](https://github.com/int08h/roughenough/commit/f1f4af2cdfa6f46a58038ca0551c6353d819ac57) | afl | `oor`
roughenough | [incorrect range check fix](https://github.com/int08h/roughenough/commit/ed267f79b0bc070c5c63e5936db79e9d5aced30c) | libfuzzer | `logic`
roughenough | [reject messages with zero tags](https://github.com/int08h/roughenough/commit/1b21bbc074b8acd146abce50e520eef84bbbec2d) | afl | `logic`, `oor`
roughenough | [reject short single tag messages](https://github.com/int08h/roughenough/commit/e0d15dc1d9bfbd92518916dbfc306cda32c47ff3) | afl | `logic`, `oor`
roughenough | [return Error instead of panicking](https://github.com/int08h/roughenough/commit/1ce57a140bcdd1c0c6dfbef1403a1aa11e2240ae) | afl | `panic`
roughenough | [validate tag offset not past end of message](https://github.com/int08h/roughenough/commit/a029e5073603bf33f64c7550451d32d6ac62963c) | afl | `logic`
roughenough | [validate value offset not pass end of message](https://github.com/int08h/roughenough/commit/9656fdab0f702ccd784a2e50eabcf94809bc31b5) | afl | `logic`
rust-ini | [invalid codepoint](https://github.com/zonyitoo/rust-ini/issues/75) | libfuzzer | `utf-8`
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
semver | [issue/227](https://github.com/steveklabnik/semver/issues/227) | afl | `unwrap`
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
snap | [#12](https://github.com/BurntSushi/rust-snappy/issues/12) | libfuzzer | `oor`
snmp-parser | [panic on unwrapping](https://github.com/rusticata/snmp-parser/issues/2) | libfuzzer | `unwrap`
sqlformat | [panic on unwrapping error due to failure to parse int](https://github.com/shssoichiro/sqlformat-rs/issues/12) | libfuzzer | `unwrap`
sqlparser | [stack overflow (unbounded recursion)](https://github.com/sqlparser-rs/sqlparser-rs/issues/305) | libfuzzer | `so`
ssh-keys | [#3](https://github.com/tailhook/ssh-keys/issues/3) | afl | `oor`
ssh-keys | [panic on slice indexing](https://github.com/tailhook/ssh-keys/issues/1) | libfuzzer | `oor`
ssh-parser | [arithmetic overflow](https://github.com/rusticata/ssh-parser/issues/1) | libfuzzer | `arith`
svgparser | [arithmetic overflow, bound checking panic, incorrect result](https://github.com/RazrFalcon/libsvgparser/commit/4742f16e834445a682a0a4db62600d275a457390) | libfuzzer | `arith`, `oor`, `logic`
svgparser | [endless loop](https://github.com/RazrFalcon/libsvgparser/commit/c55d9a7d4d1e83f405be2e7bfddea89f579f6fc9) | libfuzzer | `loop`
swf-parser | [#23](https://github.com/open-flash/swf-parser/issues/23) | libfuzzer | `logic`
sxd-document | [use after free](https://github.com/shepmaster/sxd-document/issues/47) | libfuzzer | `uaf` | ❗️
symbolic-demangle | [extremely slow demangling, OOM](https://github.com/getsentry/symbolic/issues/477) | libfuzzer | `oom`
symbolic-minidump | [segfault in exposed C++ library](https://github.com/getsentry/symbolic/issues/478) | libfuzzer | `segfault` | ❗️
symbolic-unreal | [unbounded allocation](https://github.com/getsentry/symbolic/issues/476) | libfuzzer | `oom`
symphonia | [panic on unwrapping](https://github.com/pdeljanov/Symphonia/pull/58) | libfuzzer | `unwrap`
syn | [Unrecognized literal](https://github.com/dtolnay/syn/issues/897) | libfuzzer | `logic`
syn | [panic when parsing impl](https://github.com/dtolnay/syn/issues/1108) | libfuzzer | `logic`
tar-rs | [#23](https://github.com/alexcrichton/tar-rs/issues/23) | afl | `arith`
tera | [#396](https://github.com/Keats/tera/issues/396) | libfuzzer | `arith`, `logic`
tera | [unimplemented panic](https://github.com/Keats/tera/issues/657) | libfuzzer | `panic`
tf-demo-parser | [arithmetic overflow leading to out of memory](https://github.com/demostf/parser/issues/2) | libfuzzer | `arith`, `oom`
tiff | [index out of bounds](https://github.com/PistonDevelopers/image-tiff/issues/28) | afl | `oor`
tiff | [infinite loop on malformed input](https://github.com/PistonDevelopers/image-tiff/issues/31) | afl | `loop`
tiff | [memory exhaustion on malformed input](https://github.com/PistonDevelopers/image-tiff/issues/29) | afl | `oom`
tiff | [panic on attempt to divide by zero](https://github.com/PistonDevelopers/image-tiff/issues/33) | afl | `arith`
time | [issue/309](https://github.com/time-rs/time/issues/309) | afl | `panic`, `arith`
tinytemplate | [beginning more than end on string slicing](https://github.com/bheisler/TinyTemplate/issues/22) | libfuzzer | `oor`
tinyvec | [arithmetic underflow](https://github.com/Lokathor/tinyvec/pull/14) | [rutenspitz] | `arith`
tinyvec | [resize() could set incorrect size for inline storage](https://github.com/Lokathor/tinyvec/pull/16) | [rutenspitz] | `logic`
tinyvec | [swap_remove() for last element worked incorrectly](https://github.com/Lokathor/tinyvec/pull/15) | [rutenspitz] | `logic`
todotxt.rs | [index out of bounds](https://github.com/kstep/todotxt.rs/issues/1) | libfuzzer | `oor`
tokei | [panic](https://github.com/XAMPPRocky/tokei/issues/727) | libfuzzer | `oor`
tokei | consistency [#725](https://github.com/XAMPPRocky/tokei/issues/725) | libfuzzer | `logic`
toml | [#178](https://github.com/alexcrichton/toml-rs/issues/178) | libfuzzer | `logic`
toml | [#179](https://github.com/alexcrichton/toml-rs/issues/179) | libfuzzer | `logic`
toml | [#180](https://github.com/alexcrichton/toml-rs/issues/180) | libfuzzer | `logic`
toml | [#181](https://github.com/alexcrichton/toml-rs/issues/181) | libfuzzer | `logic`
toml | [#185](https://github.com/alexcrichton/toml-rs/issues/185) | libfuzzer | `logic`
toml | [#186](https://github.com/alexcrichton/toml-rs/issues/186) | libfuzzer | `logic`
toml | [stack overflow (unbounded recursion)](https://github.com/alexcrichton/toml-rs/issues/428) | libfuzzer | `so`
toml_edit | [stack overflow (unbounded recursion)](https://github.com/ordian/toml_edit/issues/206) | libfuzzer | `so`
trust-dns-proto | [Incorrect length check in Encoding](https://github.com/bluejekyll/trust-dns/issues/1570) | libfuzzer | `logic`
trust-dns-proto | [ZERO resouce records are mis-parsed](https://github.com/bluejekyll/trust-dns/issues/1571) | libfuzzer | `logic`
trust-dns-proto | [Incorrect handling of escapes](https://github.com/bluejekyll/trust-dns/issues/1575) | libfuzzer | `logic`
ttf-parser | [infinite loop](https://github.com/RazrFalcon/ttf-parser/issues/79) | libfuzzer | loop
ttf-parser | [assertion failure](https://github.com/RazrFalcon/ttf-parser/issues/80) | libfuzzer | `panic`
tui | [issue/446](https://github.com/fdehau/tui-rs/issues/446) | afl | `arith` 
ubyte | [multiply with overflow when parsing fractional number](https://github.com/SergioBenitez/ubyte/issues/5) | libfuzzer | `arith`
unicode-segmentation | [grapheme boundary correctness](https://github.com/unicode-rs/unicode-segmentation/issues/19) | libfuzzer | `logic`
unicode-segmentation | [word boundary correctness](https://github.com/unicode-rs/unicode-segmentation/issues/20) | libfuzzer | `logic`
unified-diff | [lines before 1, with no context](https://github.com/notriddle/rust-unified-diff/commit/e7e8a91d74b6d26d7fbcd50dcbe056e0d8e4c03f#diff-b1a35a68f14e696205874893c07fd24fdb88882b47c23cc0e0c80a30c7d53759R260) | libFuzzer | `logic`
url | [#108](https://github.com/servo/rust-url/pull/108) | afl | `oor`
url | [infinite loop](https://github.com/servo/rust-url/issues/692) | libfuzzer | `loop`
url | [slicing error](https://github.com/servo/rust-url/issues/654) | afl | `oor`  
url | [out of index](https://github.com/servo/rust-url/issues/656) | afl | `oor`  
url | [failed round trip parse](https://github.com/servo/rust-url/issues/729) | libfuzzer | `logic`
uuid | [index out of bounds](https://github.com/rust-lang-nursery/uuid/pull/81) | libfuzzer | `oor`
v_escape | [heap buffer overflow](https://gitlab.com/r-iendo/v_escape/issues/2) | libfuzzer | `oor` | ❗️ 
vial | [arithmetic overflow](https://github.com/sigaloid/vial/issues/5) | libfuzzer | `arith`
vosub | [arithmetic overflow](https://github.com/emk/subtitles-rs/commit/3afdb7e1c5e786e88653253243648dd9d49983f2) | libfuzzer | `arith`
vosub | [invalid slice](https://github.com/emk/subtitles-rs/commit/20e430105b1fc02aa135788ba150a0dd49a7d1ef) | libfuzzer | `oor`
vosub | [invalid slice](https://github.com/emk/subtitles-rs/commit/46df766dd22cb6a04a534611f08c23903e58746c) | libfuzzer | `oor`
vosub | [invalid slice](https://github.com/emk/subtitles-rs/commit/f2f5309aa8173dfec4bb5816950d718a1ac669c2) | libfuzzer | `panic`
vosub | [shift overflow](https://github.com/emk/subtitles-rs/commit/5d3364b96389d90deac0f024a57660951b7e1dd6) | libfuzzer | `arith`
wasmparser.rs | [arithmetic overflow](https://github.com/yurydelendik/wasmparser.rs/issues/21#issuecomment-310253956) | libfuzzer | `arith`
wayland-rs | [#187](https://github.com/Smithay/wayland-rs/pull/187) | libfuzzer | `oor` | 
ws-rs | [arithmetic overflow](https://github.com/housleyjk/ws-rs/pull/179) | libfuzzer | `arith`
xi-editor | [issue/1303](https://github.com/xi-editor/xi-editor/issues/1303) | afl | `arith`  
xml-rs | [#93](https://github.com/netvl/xml-rs/issues/93) | afl | `utf-8`
xml-rs | [arithmetic overflow](https://github.com/netvl/xml-rs/issues/204) | libfuzzer | `arith`
yaxpeax-x86 | [#12 arithmetic overflow](https://github.com/iximeow/yaxpeax-x86/issues/12) | libfuzzer | `arith`
yaxpeax-x86 | [#13 arithmetic overflow](https://github.com/iximeow/yaxpeax-x86/issues/13) | libfuzzer | `arith`
yaxpeax-x86 | [#15 arithmetic overflow](https://github.com/iximeow/yaxpeax-x86/issues/15) | libfuzzer | `arith`
zip-rs | [arithmetic overflow](https://github.com/mvdnes/zip-rs/issues/40) | libfuzzer | `arith`
zip-rs | [arithmetic overflow](https://github.com/zip-rs/zip/issues/234) | libfuzzer | `arith`

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
