# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [1.0.141] - 2025-06-24

### Added

- Add more warnings to apply buffering on docs of affected functions by @JonathanBrouwer
- Add Map::into_values method by @tisonkun
- Add `'static` lifetime to `const`'s by @bheylin
- Add literal 'null', 'true' and 'false' consts to `RawValue` struct. by @bheylin
- Add a safety comment to unsafe block by @djmitche
- Add Number u128 conversions by @dtolnay
- Add i128 deserialization by @druide
- Add methods on Map and Value to destroy preserved ordering by @dtolnay
- Add support for 128 bit HashMap key serialization by @Mrreadiness
- Add `OccupiedEntry::shift_remove()` and `swap_remove()` by @GREsau
- Add `OccupiedEntry::remove_entry()` (and shift/swap versions) by @GREsau
- Add better tests by @purplesyringa
- Add Map::shift_insert() by @joshka
- Add swap_remove and shift_remove methods on Map by @dtolnay
- Add test of negative NaN and negative infinity by @dtolnay
- Support deserializing from &RawValue by @dtolnay
- Add cfg banner to documentation of Number::as_str by @dtolnay
- Adds missing cfg attr to as_str by @chanced
- Adds `as_str` to `Number` if `arbitrary_precision` is enabled by @chanced
- Adds `as_number` to `Value` by @chanced
- Support deserializing bool in map keys by @dtolnay
- Support serializing bool in map keys by @dtolnay
- Add test for boolean keys in map by @dtolnay
- Add test of leading and trailing whitespace in integer key in from_value by @dtolnay
- Add test of trailing whitespace in integer key by @dtolnay
- Add optional trailing commas in treemap macro by @dtolnay
- Add CI job using minimal-versions by @dtolnay
- Support a manual trigger on CI workflow by @dtolnay
- Add Error::io_error_kind by @dtolnay
- Add an example of producing a Null in a json! literal by @ndmitchell
- Add regression test for issue 1004 by @dtolnay
- Support 128-bit integers in to_value by @dtolnay
- Add test of integer128 to_value by @dtolnay
- Add regression test for issue 953 by @dtolnay
- Add `clone_from` to `Map`; `Map::append` now uses `IndexMap::extend` by @Lucretiel
- Add direct support for i128 and u128 via itoa by @Lucretiel
- Add a CI build for arbitrary precision without std by @dtolnay
- Add test of Display for Number containing float by @dtolnay
- Add categories to crates.io metadata by @dtolnay
- Add authors to Cargo.toml by @dtolnay
- Add actions job to notice outdated dependencies by @dtolnay
- Support deserializing map key as &RawValue by @dtolnay
- Add test of deserializing a &RawValue in map key position by @dtolnay
- Add discord invite links by @dtolnay
- Add regression test for issue 845 by @dtolnay
- Add a miri test job in CI by @dtolnay
- Add impl From<Box<RawValue>> for Box<str> by @jplatte
- Add `Map::get_key_value` method.
- Add retain to Map
- Add test parsing `-0` by @dtolnay
- Add regression test for issue 795 by @dtolnay
- Add doc(cfg(feature = "std")) attribute where appropriate by @jplatte
- Add CI job to ensure documentation can be built by @jplatte
- Add test of RawValue deserialization from invalid utf-8 by @dtolnay
- Add Entry::and_modify by @Krout0n
- Add impl From<Number> for Value by @imp
- Add test of as_f64 on large number by @dtolnay
- Add no-std preserve_order check in CI by @dtolnay
- Add CI builds on rust 1.40 and 1.45 by @dtolnay
- Add compiler version detection for BTreeMap api by @dtolnay
- Add skeleton for Map::remove_entry by @dtolnay
- Add Read implementation for &mut Read by @tinou98
- Add ui test of missing comma between object entries by @dtolnay
- Add float test case demonstrating exponent overflow by @dtolnay
- Add brief note to top of lexical sources by @dtolnay
- Add some more number failure tests by @dtolnay
- Add roundtrip test of f32 edge case by @dtolnay
- Add build script to set up limb width cfg by @dtolnay
- Add explanation to lexical lib by @dtolnay
- Add sample roundtrip test by @japaric
- Add no-std verification in CI by @dtolnay
- Support verifying no-std support through serde_json_test by @dtolnay
- Add CI build to cover fuzz target by @dtolnay
- Added from_slice fuzzer. by @DavidKorczynski
- Add test for {:#?} format of Value by @dtolnay
- Add Windows CI in GitHub Actions by @dtolnay
- Add value::to_raw_value by @jplatte
- Add user-friendly error when no alloc or std feature are enabled by @Xanewok
- Add facade around std/alloc/core like serde does by @Xanewok
- Add alloc/no_std support by @Freax13
- Add append to Map
- Add example for how to update value if one exists
- Add `impl From<()> for Value` by @Nilix007
- Added missing fake_main #522 by @andrisak
- Address needless_doctest_main lint by @dtolnay
- Add note about issue 160 to from_reader function by @est31
- Add a note about buffering in from_reader by @dtolnay
- Address into_iter_on_ref lint by @dtolnay
- Address needless_lifetimes lint in decode_hex_escape by @dtolnay
- Add Default for Box<RawValue> by @dtolnay
- Add a method to construct RawValue from String without allocation by @dtolnay
- Add a Travis step to test raw_value by @dtolnay
- Address needless_return lint by @dtolnay
- Add some rules to catch json macro syntax errors by @dtolnay
- Add tests for map with char keys by @dtolnay
- Add values_mut() iterator for serde_json::Map by @dtolnay
- Add `Value::take` method
- Support top-level primitives in StreamDeserializer by @bouk
- Add error banner when running test suite without nightly compiler by @dtolnay
- Add ErrorCode::TrailingComma by @fmoor
- Add license info to value files by @dtolnay
- Add test for borrowed map key by @dtolnay
- Add an example of to_value that fails by @dtolnay
- Add appveyor badge to crates.io by @dtolnay
- Add playground links to readme by @dtolnay
- Add a note about skipping over valid JSON by @dtolnay
- Support borrowing in from_slice by @dtolnay
- Support deserializing borrowed &str and &[u8] by @dtolnay
- Add 'de lifetime to Read trait by @dtolnay
- Add 'de lifetime to deserializer by @dtolnay
- Add test for {:#} representation of Value by @dtolnay
- Add char tests by @dtolnay
- Add entry API and expose map module by @dtolnay
- Fix #256: support deserializing strings with arbitrary bytes by @bennofs
- Add `impl FromIterator<T> for Value` by @killercup
- Add a short example to `<Value as Index>::index` by @killercup
- Add a short example to Value::pointer by @killercup
- Add crates.io category and travis badge by @dtolnay
- Add comment about sealed Index trait by @dtolnay
- Add test for comma within array element by @dtolnay
- Add a tt-muncher for constructing Value by @dtolnay
- Add recommended Cargo.toml line to readme by @dtolnay
- Add builds for supported old versions by @dtolnay
- Add comment about self.slice.get(self.index) being slow by @dtolnay
- Add preserve_order feature by @laktak
- Add newline by @s-panferov
- Add helper function to parse stream of json values by @little-arhat
- Add custom_derive by @vegai
- Add an example struct corresponding to example json by @vegai
- Add cargo metadata by @erickt
- Add coveralls badge by @erickt
- Add licenses by @erickt
- Add examples and json byte tests by @erickt
- Add a readme by @erickt

### Changed

- Create release automation workflows by @jost-s in [#1](https://github.com/holochain/serde-json/pull/1)
- Ignore mismatched_lifetime_syntaxes lint by @dtolnay
- Pin nightly toolchain used for miri job by @dtolnay
- Merge pull request #1248 from jimmycathy/master by @dtolnay
- Release 1.0.140 by @dtolnay
- Merge pull request #1245 from serde-rs/powerpc by @dtolnay
- Delete unused gcc installation by @dtolnay
- Ignore unbuffered_bytes clippy lint by @dtolnay
- Ignore elidable_lifetime_names pedantic clippy lint by @dtolnay
- Point standard library links to stable by @dtolnay
- Release 1.0.139 by @dtolnay
- Merge pull request #1242 from dtolnay/writefloat by @dtolnay
- Document behavior of write_f32/f64 on non-finite floats by @dtolnay
- Merge pull request #1241 from dtolnay/doclink by @dtolnay
- Convert html links to intra-doc links by @dtolnay
- Unset doc-scrape-examples for lib target by @dtolnay
- Resolve unnecessary_semicolon pedantic clippy lint by @dtolnay
- Release 1.0.138 by @dtolnay
- Move BufReader to caller by @dtolnay
- Sort imports from PR 1237 by @dtolnay
- Merge pull request #1237 from JonathanBrouwer/master by @dtolnay
- Fix example of from_reader not applying buffering when it should by @JonathanBrouwer
- More precise gitignore patterns by @dtolnay
- Release 1.0.137 by @dtolnay
- Merge pull request #1231 from dtolnay/playground by @dtolnay
- Enable "float_roundtrip" and "unbounded_depth" features in playground by @dtolnay
- Release 1.0.136 by @dtolnay
- Merge pull request #1230 from goffrie/patch-1 by @dtolnay
- Use Map::with_capacity in value::Serializer::serialize_map by @goffrie
- Release 1.0.135 by @dtolnay
- Merge pull request #1226 from tisonkun/map-into-values by @dtolnay
- Resolve precedence clippy lint by @dtolnay
- Release 1.0.134 by @dtolnay
- Tweak wording of NULL/TRUE/FALSE documentation by @dtolnay
- Merge pull request #1222 from dtolnay/rawvalueassoc by @dtolnay
- Move RawValue associated constants into same impl block as public functions by @dtolnay
- Merge pull request #1221 from bheylin/add-const-raw-values-for-null-and-bools by @dtolnay
- Release 1.0.133 by @dtolnay
- Merge pull request #1215 from dtolnay/fromarray by @dtolnay
- Implement From<[T; N]> for Value by @dtolnay
- Disable question_mark clippy lint in lexical test by @dtolnay
- Resolve unnecessary_map_or clippy lints by @dtolnay
- Wrap PR 1213 to 80 columns by @dtolnay
- Merge pull request #1213 from djmitche/safety-comment by @dtolnay
- Prevent upload-artifact step from causing CI failure by @dtolnay
- Raise minimum version for preserve_order feature to Rust 1.65 by @dtolnay
- Update ui test suite to nightly-2024-10-31 by @dtolnay
- Release 1.0.132 by @dtolnay
- Merge pull request #1206 from dtolnay/hasnext by @dtolnay
- Clearer order of comparisons by @dtolnay
- Handle early return sooner on eof in seq or map by @dtolnay
- Rearrange 'match peek' by @dtolnay
- Merge pull request #1205 from dtolnay/hasnext by @dtolnay
- Reduce duplicative instantiation of logic in SeqAccess and MapAccess by @dtolnay
- Release 1.0.131 by @dtolnay
- Touch up PR 1135 by @dtolnay
- Merge pull request #1135 from swlynch99/map-deserializer by @dtolnay
- Clean up deserialize_enum methods on Value and &Value by @swlynch99
- Clean up visit_object and visit_object_ref by @swlynch99
- Implement Deserializer for Map<String, Value> and &Map<String, Value> by @swlynch99
- Release 1.0.130 by @dtolnay
- Merge pull request #1204 from dtolnay/u128 by @dtolnay
- Merge pull request #1203 from dtolnay/i128err by @dtolnay
- Return error instead of Null if i128 deserialized to Value is out of range by @dtolnay
- Delete Number conversion example code by @dtolnay
- Delete Value::as_i128 by @dtolnay
- Update Number::from_i128 documentation regarding bounds by @dtolnay
- Merge pull request #1202 from dtolnay/useprimitive by @dtolnay
- Delete unneeded imports in doc code by @dtolnay
- Delete #[inline] from some Number methods by @dtolnay
- Merge pull request #1201 from dtolnay/from128 by @dtolnay
- Allow arbitrarily large i128 in arbitrary_precision mode by @dtolnay
- Flatten logic in Number::from_i128 by @dtolnay
- Merge pull request #1200 from dtolnay/from128 by @dtolnay
- Delete unreachable branch from Number::from_i128 by @dtolnay
- Format PR 1141 with rustfmt by @dtolnay
- Merge pull request #1141 from druide/master by @dtolnay
- Fix tests by @druide
- Improve rendering of sort_keys documentation by @dtolnay
- Release 1.0.129 by @dtolnay
- Merge pull request #1199 from dtolnay/sort by @dtolnay
- Ignore needless_lifetimes clippy lint by @dtolnay
- Resolve some needless_lifetimes clippy lints by @dtolnay
- Resolve empty_line_after_doc_comments clippy lint in lexical by @dtolnay
- Replace bool::to_string with if by @dtolnay
- Replace str::to_string with to_owned by @dtolnay
- Replace char::to_string with encode_utf8 by @dtolnay
- Replace integer to_string with itoa by @dtolnay
- Replace f64::to_string with ryu by @dtolnay
- Release 1.0.128 by @dtolnay
- Merge pull request #1188 from Mrreadiness/feat/add-hashmap-key-128-serializer by @dtolnay
- Upload CI Cargo.lock for reproducing failures by @dtolnay
- Release 1.0.127 by @dtolnay
- Merge pull request 1179 from GREsau/patch-1 by @dtolnay
- Release 1.0.126 by @dtolnay
- Merge pull request #1184 from serde-rs/fastarithmetic by @dtolnay
- Improve cfg names for fast arithmetic by @dtolnay
- Merge pull request #1183 from serde-rs/arithmetic by @dtolnay
- Unify chunk size choice between float and string parsing by @dtolnay
- Merge pull request #1182 from CryZe/chunk-64bit by @dtolnay
- Ensure the SWAR chunks are 64-bit in more cases by @CryZe
- Merge pull request #1178 from iex-rs/tiny-bit-faster-hex by @dtolnay
- Optimize Unicode decoding by 1% by @purplesyringa
- Release 1.0.125 by @dtolnay
- Touch up PR 1175 by @dtolnay
- Merge pull request 1175 from iex-rs/faster-backslash-u by @dtolnay
- Deserialize invalid UTF-8 into byte bufs as WTF-8 by @lucacasonato
- Correct WTF-8 parsing by @purplesyringa
- Simplify unicode escape handling by @purplesyringa
- Use the same UTF-8/WTF-8 impl for surrogates by @purplesyringa
- Format UTF-8 strings manually by @purplesyringa
- Mark \u parsing as cold by @purplesyringa
- Merge pull request #1172 from iex-rs/faster-hex by @dtolnay
- Parse \uXXXX escapes faster by @purplesyringa
- Merge pull request #1176 from dtolnay/miriname by @dtolnay
- Improve job names for miri jobs by @dtolnay
- Merge pull request #1174 from iex-rs/miri-on-ci by @dtolnay
- Test on BE and 32-bit platforms on CI via Miri by @purplesyringa
- Release 1.0.124 by @dtolnay
- Merge pull request #1173 from iex-rs/fix-big-endian by @dtolnay
- Fix skip_to_escape on BE architectures by @purplesyringa
- Release 1.0.123 by @dtolnay
- Fix needless_borrow clippy lint in new control character test by @dtolnay
- Merge pull request #1161 from iex-rs/vectorized-string-parsing by @dtolnay
- Immediately bail-out on empty strings by @purplesyringa
- Don't run the slow algorithm from the beginning by @purplesyringa
- Allow clippy::items_after_statements by @purplesyringa
- Big endian support by @purplesyringa
- Inline memchr2 logic into Mycroft's algorithm by @purplesyringa
- Bring MSRV down by @purplesyringa
- Replace ESCAPE array with is_escape fn by @purplesyringa
- Vectorize string parsing by @purplesyringa
- Release 1.0.122 by @dtolnay
- Work around buggy rust-analyzer behavior by @dtolnay
- Merge pull request #1166 from dtolnay/allocvec by @dtolnay
- Fix json! invocations when std prelude is not in scope by @dtolnay
- Merge pull request #1165 from serde-rs/jsonmac by @dtolnay
- Eliminate local_inner_macros in favor of non-ident macro paths by @dtolnay
- Release 1.0.121 by @dtolnay
- Merge pull request #1160 from iex-rs/efficient-position by @dtolnay
- Optimize position search in error path by @purplesyringa
- Merge pull request #1159 from iex-rs/fix-recursion by @dtolnay
- Move call to tri! out of check_recursion! by @purplesyringa
- Ignore byte_char_slices clippy lint in test by @dtolnay
- Merge pull request #1153 from dpathakj/master by @dtolnay
- Correct documentation URL for Value's Index impl. by @dpathakj
- Release 1.0.120 by @dtolnay
- Merge pull request #1152 from cforycki/fix/index-map-minimal-version by @dtolnay
- Release 1.0.119 by @dtolnay
- Make shift_insert available for inlining like other Map methods by @dtolnay
- Document the cfg required for Map::shift_insert to exist by @dtolnay
- Merge pull request #1149 from joshka/master by @dtolnay
- Merge pull request #1146 from haouvw/master by @dtolnay
- Release 1.0.118 by @dtolnay
- Combine Map's Hash into one impl by @dtolnay
- Touch up PR 1127 by @dtolnay
- Resolve semicolon_if_nothing_returned pedantic clippy lint from PR 1127 by @dtolnay
- Merge pull request #1127 from edwardycl/hash by @dtolnay
- Impl `Hash` for `Value` by @edwardycl
- Another lexical const that is unused, though not in test by @dtolnay
- Delete unused associated constant from lexical by @dtolnay
- Fill in ignore reasons in all #[ignore] attributes by @dtolnay
- Run more of test suite in preserve_order mode by @dtolnay
- Ignore large_digit_groups pedantic clippy lint in test by @dtolnay
- Resolve needless_raw_string_hashes pedantic clippy lint in test by @dtolnay
- Merge pull request #1136 from dtolnay/docsrs by @dtolnay
- Rely on docs.rs to define --cfg=docsrs by default by @dtolnay
- Release 1.0.117 by @dtolnay
- PartialEq is not implemented between Value and 128-bit ints by @dtolnay
- Combine number PartialEq tests by @dtolnay
- Merge pull request #1130 from serde-rs/checkcfg by @dtolnay
- Resolve unexpected_cfgs warning by @dtolnay
- Release 1.0.116 by @dtolnay
- Hide "non-exhaustive patterns" errors when crate fails to compile by @dtolnay
- Merge pull request 1124 from mleonhard/master by @dtolnay
- Replace `features_check` mod with a call to `std::compile_error!`.  Fixes https://github.com/serde-rs/json/issues/1123 . by @mleonhard
- Revert "Temporarily disable miri on doctests" by @dtolnay
- Resolve legacy_numeric_constants clippy lints by @dtolnay
- Release 1.0.115 by @dtolnay
- Merge pull request #1119 from titaniumtraveler/pr by @dtolnay
- Fix missing backticks in doc comments by @titaniumtraveler
- Explicitly install a Rust toolchain for cargo-outdated job by @dtolnay
- Temporarily disable miri on doctests by @dtolnay
- Format regression tests with rustfmt by @dtolnay
- Ignore dead code lint in tests by @dtolnay
- Merge pull request #1118 from serde-rs/transparent by @dtolnay
- Ignore non_local_definitions false positive in test by @dtolnay
- Release 1.0.114 by @dtolnay
- Work around prelude redundant import warnings by @dtolnay
- Ignore incompatible_msrv clippy false positives in test by @dtolnay
- Release 1.0.113 by @dtolnay
- Merge pull request #1109 from serde-rs/remove by @dtolnay
- Release 1.0.112 by @dtolnay
- Merge pull request #1107 from serde-rs/unexpectedfloat by @dtolnay
- Format f64 in error messages using ryu by @dtolnay
- Merge pull request #1106 from serde-rs/invalidvalue by @dtolnay
- Handle Unexpected::Unit in Error::invalid_value by @dtolnay
- Factor out JSON-specific Display impl for serde::de::Unexpected by @dtolnay
- Merge pull request #1105 from keienWang/master by @dtolnay
- Ignore unconditional_recursion clippy lint due to false positive by @dtolnay
- Release 1.0.111 by @dtolnay
- Merge pull request #1100 from heiher/limb-64-la64 by @dtolnay
- Set limb width to 64 for loongarch64 by @heiher
- Release 1.0.110 by @dtolnay
- Pull in proc-macro2 sccache fix by @dtolnay
- Release 1.0.109 by @dtolnay
- Merge pull request #1097 from serde-rs/doccfg by @dtolnay
- Restore doc cfg on re-exports by @dtolnay
- Merge pull request #1095 from dtolnay/hashtest by @dtolnay
- Eliminate hash closure in favor of calling hash_one directly by @dtolnay
- Use BuildHasher::hash_one by @dtolnay
- Use random hasher state for number hashing test by @dtolnay
- Delete trace_macros! functionality from test by @dtolnay
- Update ui test suite to nightly-2023-11-19 by @dtolnay
- Release 1.0.108 by @dtolnay
- Merge pull request #1082 from dtolnay/fromdoc by @dtolnay
- Improve Value From and FromIterator docs by @dtolnay
- Merge pull request #1081 from fritzrehde/master by @dtolnay
- Merge pull request #1080 from serde-rs/negativenan by @dtolnay
- Fix unused imports by @dtolnay
- Merge pull request #1075 from dimo414/master by @dtolnay
- Test docs.rs documentation build in CI by @dtolnay
- Release 1.0.107 by @dtolnay
- Merge pull request #1073 from dtolnay/rawvalue by @dtolnay
- IntoDeserializer for &RawValue by @dtolnay
- Merge pull request #1072 from dtolnay/rawvalue by @dtolnay
- Merge pull request #1062 from osiewicz/remove_build_rs by @dtolnay
- Omit return keyword in `remove_entry` by @osiewicz
- Revert "Remove limb_width32 and limb_width64 features" by @osiewicz
- Remove no_btreemap_get_key_value and no_btreemap_remove_entry. by @osiewicz
- Remove no_btreemap_retain feature from build.rs by @osiewicz
- Release 1.0.106 by @dtolnay
- Elaborate on documentation of Number::as_str by @dtolnay
- Touch up PR 1067 by @dtolnay
- Merge pull request #1067 from chanced/add-as_str-to-number by @dtolnay
- Improves `Number::as_str` doc example by @chanced
- Fix unintended u8 link inferred by intra doc link by @dtolnay
- Resolve rustdoc::redundant_explicit_links lint by @dtolnay
- Fix documentation typo from PR 1069 by @dtolnay
- Reorder Value::as_number after is_number by @dtolnay
- Wrap as_number documentation to 80 columns by @dtolnay
- Delete trailing whitespace from PR 1069 by @dtolnay
- Merge pull request 1069 from chanced/add-as_number-to-value by @dtolnay
- Minor cleanup of documentation for `Value::as_number` by @chanced
- Update actions/checkout@v3 -> v4 by @dtolnay
- Release 1.0.105 by @dtolnay
- Merge pull request #1055 from dtolnay/boolkey by @dtolnay
- Delete test_serialize_rejects_bool_keys by @dtolnay
- Resolve ignored_unit_patterns pedantic clippy lint by @dtolnay
- Release 1.0.104 by @dtolnay
- Merge pull request #1045 from ZetaNumbers/value-ref-into-deserializer by @dtolnay
- Implement IntoDeserializer for &Value by @zetanumbers
- Delete inline attributes throughout test suite by @dtolnay
- Release 1.0.103 by @dtolnay
- Opt in to generate-link-to-definition when building on docs.rs by @dtolnay
- Fix rustdoc::bare_urls lint in lexical code by @dtolnay
- Release 1.0.102 by @dtolnay
- Merge pull request #1039 from dtolnay/writebytearray by @dtolnay
- Factor out byte array serialization to a new Formatter method by @dtolnay
- Inline Serializer::serialize_u8 into serialize_bytes by @dtolnay
- Inline u8::serialize into serialize_bytes by @dtolnay
- Simplify serialize_bytes by @dtolnay
- Inline SerializeSeq::end into serialize_bytes by @dtolnay
- Inline SerializeSeq::serialize_element into serialize_bytes by @dtolnay
- Inline Serializer::serialize_seq into serialize_bytes by @dtolnay
- Format PR 1037 with rustfmt by @dtolnay
- Release 1.0.101 by @dtolnay
- Merge pull request #1037 from dtolnay/numkey by @dtolnay
- Insert check for whitespace surrounding numeric map key by @dtolnay
- Directly use caller's Visitor to deserialize numeric key from Value by @dtolnay
- Delete str fallback for Value numeric key methods by @dtolnay
- Inline de::from_trait into deserialize_numeric_key by @dtolnay
- Make number deserialization usable on text that lives shorter than input data by @dtolnay
- Merge adjacent integer key tests by @dtolnay
- Rewrap PR 1027 comments to 80 columns and reword by @dtolnay
- Deduplicate a bunch of identical deserialize_numeric_key expansions by @dtolnay
- Straighten control flow of deserialize_numeric_key by @dtolnay
- Delete dedicated whitespace-in-key error message by @dtolnay
- Merge pull request #1036 from dtolnay/nll by @dtolnay
- Enforce no use of question-mark operator by @dtolnay
- Buggy iter_not_returning_iterator lint has been fixed in clippy by @dtolnay
- Buggy ptr_arg lint has been fixed in clippy by @dtolnay
- Resolve unnested_or_patterns pedantic clippy lint by @dtolnay
- Merge pull request #1035 from dtolnay/numkey by @dtolnay
- Improve error message on invalid numeric key by @dtolnay
- Merge pull request #1027 from overdrivenpotato/float-key by @dtolnay
- Return error if numeric key starts with whitespace by @overdrivenpotato
- Use Deserializer::* methods instead of `.parse()` for integer keys by @overdrivenpotato
- Parse `Value::Map` numeric keys using `crate::from_str` by @overdrivenpotato
- Use `ryu` directly when formatting float keys by @overdrivenpotato
- Fix builds without `std` feature by @overdrivenpotato
- Fix formatting by @overdrivenpotato
- Deserialize float keys using `deserialize_number` by @overdrivenpotato
- Print map float keys with `CompactFormatter` by @overdrivenpotato
- Return error on non-finite float keys by @overdrivenpotato
- Allow f32 and f64 keys by @overdrivenpotato
- Fix bare trait in to_value doc example code by @dtolnay
- Update to 2021 edition by @dtolnay
- Release 1.0.100 by @dtolnay
- No pre_ci in this repo by @dtolnay
- Eliminate syn 1 from minimal-versions by @dtolnay
- Sort Cargo.toml dependencies list by @dtolnay
- Resolve explicit_iter_loop pedantic clippy lint by @dtolnay
- Release 1.0.99 by @dtolnay
- Merge pull request 1030 from SecondHalfGames/map-key-serialize-some by @dtolnay
- Change MapKeySerializer::serialize_some to fall through instead of erroring by @LPGhatguy
- Release 1.0.98 by @dtolnay
- Merge pull request #1031 from serde-rs/indexmap by @dtolnay
- Do all CI builds with old rustc using shim crate by @dtolnay
- Move serde_json_test crate to own workspace by @dtolnay
- Update indexmap dependency used for preserve_order feature to version 2 by @dtolnay
- Delete unneeded conditional on preserve_order steps in CI by @dtolnay
- Release 1.0.97 by @dtolnay
- Merge pull request #1026 from dtolnay/errorkind by @dtolnay
- Merge pull request #1025 from dtolnay/io by @dtolnay
- Standardize on "I/O" instead of "IO" by @dtolnay
- Merge pull request 1021 from ndmitchell/patch-2 by @dtolnay
- Switch to using null by @ndmitchell
- Show error details during miri setup in CI by @dtolnay
- Release 1.0.96 by @dtolnay
- Merge pull request #1011 from stepancheg/utf-8 by @dtolnay
- Document to_writer only writes valid UTF-8 strings by @stepancheg
- Fix needless_borrow clippy lint in test by @dtolnay
- Release 1.0.95 by @dtolnay
- Merge pull request #1005 from dtolnay/f32cast by @dtolnay
- Fix PartialEq between Value and f32 by @dtolnay
- Eliminate f32-to-f64 casting in arbitrary_precision mode by @dtolnay
- Update fuzz crate gitignore to ignore coverage dir by @dtolnay
- No longer test so many old compiler versions by @dtolnay
- Release 1.0.94 by @dtolnay
- Merge pull request #992 from dtolnay/errorsource by @dtolnay
- Fix message duplication between error Display and source() by @dtolnay
- Ignore let_underscore_untyped pedantic clippy lint by @dtolnay
- Release 1.0.93 by @dtolnay
- Merge pull request #982 from serde-rs/integer128tovalue by @dtolnay
- Release 1.0.92 by @dtolnay
- Merge pull request #980 from serde-rs/docrepr by @dtolnay
- Hide repr attribute from documentation by @dtolnay
- RawValue -> repr(transparent) by @dtolnay
- Update indoc dev-dependency to version 2 by @dtolnay
- Speed up cargo fuzz CI job by @dtolnay
- Sync license text with rust-lang repos by @dtolnay
- Merge pull request #964 from dtolnay/docsrs by @dtolnay
- Replace docs.serde.rs links with intra-rustdoc links by @dtolnay
- Point documentation links to docs.rs instead of docs.serde.rs by @dtolnay
- Release 1.0.91 by @dtolnay
- Opt out -Zrustdoc-scrape-examples on docs.rs by @dtolnay
- Release 1.0.90 by @dtolnay
- Replace ancient CI service provider in readme by @dtolnay
- Update build status badge by @dtolnay
- Prevent build.rs rerunning unnecessarily on all source changes by @dtolnay
- Time out workflows after 45 minutes by @dtolnay
- Fix renamed let_underscore_drop lint by @dtolnay
- Resolve needless_borrowed_reference clippy lints by @dtolnay
- Release 1.0.89 by @dtolnay
- Merge pull request #956 from dtolnay/decimal by @dtolnay
- Require at least one digit after decimal point by @dtolnay
- Resolve semicolon_if_nothing_returned pedantic clippy lint by @dtolnay
- Release 1.0.88 by @dtolnay
- Merge pull request #952 from Lucretiel/map-traits by @dtolnay
- Update ui test suite to nightly-2022-11-16 by @dtolnay
- Resolve needless_borrow pedantic clippy lint in test by @dtolnay
- Release 1.0.87 by @dtolnay
- Eliminate needless 'tri!' from Serializer impl by @dtolnay
- Merge pull request #942 from serde-rs/integer128 by @dtolnay
- Assume serde_if_integer128 is true by @dtolnay
- Use existing macros to implement 128-bit From impls by @dtolnay
- Merge pull request #941 from serde-rs/alloc by @dtolnay
- Delete 1.36+ caveat from descriptions of alloc feature by @dtolnay
- Merge pull request 940 from Lucretiel/int128 by @dtolnay
- Release 1.0.86 by @dtolnay
- Reorganize number.rs imports by @dtolnay
- Merge pull request #928 from kvinwang/nostd-arbp by @dtolnay
- Arbitrary_precision without std by @kvinwang
- GitHub Workflows security hardening by @dtolnay
- Resolve manual_string_new pedantic clippy lint in test by @dtolnay
- Resolve needless_borrow clippy lints by @dtolnay
- Ignore using destructuring assignment to wildcard pattern by @dtolnay
- Release 1.0.85 by @dtolnay
- Merge pull request #919 from serde-rs/displaynum by @dtolnay
- Make Display for Number produce the same representation as serializing by @dtolnay
- Preserve '.0' when Displaying Number by @dtolnay
- Release 1.0.84 by @dtolnay
- Revert "Avoid cargo 1.45–1.50 in GitHub Actions" by @dtolnay
- Merge pull request #918 from serde-rs/debug by @dtolnay
- Reduce unneeded parens and newlines in Debug for Value by @dtolnay
- Make Debug test compatible with preserve_order by @dtolnay
- Cover all the Value variants in indented Debug test by @dtolnay
- Move expected value for indented debug test into test by @dtolnay
- Avoid cargo 1.45–1.50 in GitHub Actions by @dtolnay
- Release 1.0.83 by @dtolnay
- Sort package entries in Cargo.toml by @dtolnay
- Ignore assertions_on_result_states clippy lint by @dtolnay
- Avoid cargo 1.43–1.45 in GitHub Actions by @dtolnay
- Convert i/u128 conversion to itoa instead of std::fmt by @dtolnay
- Directly install aarch64-unknown-none target support by @dtolnay
- Update ui test suite to nightly-2022-07-20 by @dtolnay
- Ignore explicit_auto_deref clippy lint by @dtolnay
- Speed up fuzz build in CI using precompiled cargo-fuzz by @dtolnay
- Release 1.0.82 by @dtolnay
- Merge pull request #900 from kvnvelasco/implement_from_option_for_value by @dtolnay
- Don't use experimental (in 1.36) Self:: access for enums by @kvnvelasco
- Make Value be From<Option<T>> by @kvnvelasco
- Bump oldest rustc for preserve_order feature to 1.56.1 by @dtolnay
- Merge pull request #895 from dtolnay/ref by @dtolnay
- Eliminate all use of ref keyword by @dtolnay
- Resolve borrow_deref_ref clippy lint by @dtolnay
- Resolve get_first clippy lint by @dtolnay
- Check for outdated deps in fuzz target by @dtolnay
- Ignore derive_partial_eq_without_eq clippy lint by @dtolnay
- Update fuzz manifest to match cargo fuzz's new template by @dtolnay
- Ignore unused_macro_rules warning in test macros by @dtolnay
- Run miri in stricter miri-strict-provenance mode by @dtolnay
- Merge pull request #889 from dzvon/patch-1 by @dtolnay
- Fix a typo by @dzvon
- Release 1.0.81 by @dtolnay
- Make it clearer that preserve_order implies a std dependency by @dtolnay
- Merge pull request #885 from cuviper/indexmap-std by @dtolnay
- Explicitly enable indexmap/std by @cuviper
- Ignore trait_duplication_in_bounds clippy false positives by @dtolnay
- Resolve type_repetition_in_bounds clippy lint by @dtolnay
- Release 1.0.80 by @dtolnay
- Pull miri from miri branch of dtolnay/rust-toolchain by @dtolnay
- Drop unneeded quoting from env variable in workflows yaml by @dtolnay
- Update workflows to actions/checkout@v3 by @dtolnay
- Fix dev dependencies on serde's derive feature by @dtolnay
- Rewrap readme to 80 columns by @dtolnay
- Apply readme changes from PR 864 to crate-level rustdoc by @dtolnay
- Merge pull request 864 from novedevo/patch-1 by @dtolnay
- Tweak grammar to improve readability by @novedevo
- Release 1.0.79 by @dtolnay
- Merge pull request #830 from lucacasonato/support_lone_surrogates_in_raw_value by @dtolnay
- Allow lone surrogates in raw values by @lucacasonato
- Ignore buggy ptr_arg clippy lint by @dtolnay
- Resolve needless_borrow clippy lint by @dtolnay
- Release 1.0.78 by @dtolnay
- Move raw_value test imports to block of imports by @dtolnay
- Merge pull request #851 from serde-rs/rawkey by @dtolnay
- Release 1.0.77 by @dtolnay
- Improve error on compiling with neither std nor alloc by @dtolnay
- Include integration tests in published package by @dtolnay
- Release 1.0.76 by @dtolnay
- Fix imports on features +alloc +raw_value -std by @dtolnay
- Release 1.0.75 by @dtolnay
- Merge pull request #848 from serde-rs/num by @dtolnay
- Deserialize small numbers as integers in arbitrary_precision by @dtolnay
- Disable buggy iter_not_returning_iterator lint by @dtolnay
- Raise toolchain version for preserve_order to rust 1.46 by @dtolnay
- Set miriflags once for whole miri job by @dtolnay
- Run miri also with some features enabled by @dtolnay
- Release 1.0.74 by @dtolnay
- Detect warnings in CI by @dtolnay
- Merge pull request 841 from EFanZh/unsized-value-to-raw-value by @dtolnay
- Allow creating `RawValue`s from references to unsized values by @EFanZh
- Avoid evaluating $c more than once in overflow macro by @dtolnay
- Eliminate lib module by @dtolnay
- Switch to $(,)? in tri macro by @dtolnay
- Unconditionally import from alloc by @dtolnay
- Ignore return_self_not_must_use clippy lint by @dtolnay
- Release 1.0.73 by @dtolnay
- Update to itoa 1.0 by @dtolnay
- Track raw pointers in miri CI run by @dtolnay
- Disable TcpStream test on miri by @dtolnay
- Raise required rustc from 1.31 to 1.36 by @dtolnay
- Collect imports to top of test suite by @dtolnay
- Skip ui test when running in miri by @dtolnay
- Ignore needless_late_init Clippy lint by @dtolnay
- Merge pull request #831 from serde-rs/from_u32 by @dtolnay
- Skip error codepath on hex escape outside the surrogate range by @dtolnay
- Release 1.0.72 by @dtolnay
- Merge pull request #829 from serde-rs/surrogate by @dtolnay
- Move discard of expected byte immediately after peek by @dtolnay
- Rearrange the early return on lone or encoded surrogate by @dtolnay
- Use binary mask to line up visually with the bits being |'d in by @dtolnay
- Extract common logic of surrogate encode by @dtolnay
- Document why the parse_escape recursion is not dangerous by @dtolnay
- Tail recurse on parse_escape by @dtolnay
- Collapse surrogate encode into extend_from_slice call by @dtolnay
- Touch up doc changes from PR 828 by @dtolnay
- Merge pull request #828 from lucacasonato/lone_surrogate by @dtolnay
- Deserialize lone surrogates into byte bufs by @lucacasonato
- Elaborate on StrRead::parse_str safety comment by @dtolnay
- Release 1.0.71 by @dtolnay
- Consolidate unsafe RawValue transmutes in one place by @dtolnay
- Merge pull request #824 from jplatte/box-raw-value-to-underlying by @dtolnay
- Merge pull request #821 from timothee-haudebourg/get_key_value by @dtolnay
- Disable `get_key_value` with older  Rust versions.
- Release 1.0.70 by @dtolnay
- Reorder Map::retain to keep keys() and values() adjacent by @dtolnay
- Merge pull request 822 from deankarn/master by @dtolnay
- Merge branch 'master' of github.com:deankarn/json
- Update build.rs
- Don't include indexmap retain without BTreeMap retain
- Only include retain for BTreeMap if Rust 1.53.0+
- Release 1.0.69 by @dtolnay
- Touch up PR 814 by @dtolnay
- Merge pull request #814 from timothee-haudebourg/hash-numbers-only by @dtolnay
- Use the same hash for +0 and -0.
- Fix `NaN` typo.
- Better justification for the use of `f64::to_bits`
- Avoid `Self::` for older Rust versions.
- Manual implementation of `Number`'s `PartialEq`.
- Use `core::hash` instead of `std::hash`.
- Discard `ordered_float`, use custom `Hash` impl.
- Do not import `ordered_float` default features.
- Do not import always `NotNan`.
- Do not show `NotNan` in `Number`'s `Debug` impl.
- Impl`Eq+Hash` for `Number` using `ordered_float`.
- Revert "Disable broken fuzz build in CI" by @dtolnay
- Update ui test suite to nightly-2021-10-17 by @dtolnay
- Ui test changes for trybuild 1.0.49 by @dtolnay
- Update ui test files by @dtolnay
- Declare minimum Rust version in Cargo metadata by @dtolnay
- Resolve semicolon_if_nothing_returned pedantic clippy lint by @dtolnay
- Resolve redundant_closure_for_method_calls pedantic clippy lint by @dtolnay
- Resolve needless_borrow clippy lint by @dtolnay
- Run clippy also with features enabled by @dtolnay
- Resolve manual_str_repeat clippy lint by @dtolnay
- Resolve semicolon_if_nothing_returned pedantic clippy lint by @dtolnay
- Resolve needless_borrow clippy lint by @dtolnay
- Run clippy on test suite too by @dtolnay
- Move clippy lint level to CI job by @dtolnay
- Skip clippy job on pull requests by @dtolnay
- Disable broken fuzz build in CI by @dtolnay
- Release 1.0.68 by @dtolnay
- Merge pull request #801 from dtolnay/negative0 by @dtolnay
- Parse -0 as float -0.0 instead of integer 0 by @dtolnay
- Test negative zero parsing to f32 by @dtolnay
- Suppress unused field in test_borrow_in_map_key by @dtolnay
- Fix dead code warning in issue 795 regression test by @dtolnay
- Ignore derivable_impls clippy false positive by @dtolnay
- Release 1.0.67 by @dtolnay
- Merge pull request #796 from dtolnay/visitobject by @dtolnay
- Detect unknown struct variant fields deserializing from Value by @dtolnay
- Merge pull request #794 from dtolnay/visitarray by @dtolnay
- Use existing helpers for running visit_seq over a Vec/slice by @dtolnay
- Merge pull request #793 from dtolnay/valuede by @dtolnay
- Delete Deserializer impl from value::de::MapRefDeserializer by @dtolnay
- Delete Deserializer impl from value::de::SeqRefDeserializer by @dtolnay
- Delete Deserializer impl from value::de::SeqDeserializer by @dtolnay
- Merge pull request #792 from dtolnay/valuemapde by @dtolnay
- Delete Deserializer impl from value::de::MapDeserializer by @dtolnay
- Release 1.0.66 by @dtolnay
- Merge pull request #789 from serde-rs/orpattern by @dtolnay
- Restore compatiblity with older rustc after PR 786 by @dtolnay
- Merge pull request #786 from ruifengx/master by @dtolnay
- Make arbitrary_precision preserve the exact string representation by @ruifengx
- Release 1.0.65 by @dtolnay
- Merge pull request 788 from jplatte/doc-cfg by @dtolnay
- Document unbounded_depth, raw_value feature-gated API via doc_cfg by @jplatte
- Update preserve_order required compiler to 1.38.0 for hashbrown by @dtolnay
- Resolve semicolon_if_nothing_returned clippy lints by @dtolnay
- Change readme run buttons to tab style by @dtolnay
- Merge pull request 778 from jayeshmann/patch-1 by @dtolnay
- Overlapping button fix by @jayeshmann
- Merge pull request #777 from striezel-stash/fix-typos by @dtolnay
- Update ui test suite to nightly-2021-05-14 by @dtolnay
- Update rustdoc link to serde-json-core by @dtolnay
- Merge pull request #773 from ratijas/patch-1 by @dtolnay
- Update link to serde-json-core by @ratijas
- Resolve branches_sharing_code clippy lint by @dtolnay
- Merge pull request 770 from DavidKorczynski/patch-1 by @dtolnay
- Fix breaking OSS-Fuzz coverage build by @DavidKorczynski
- Merge pull request 758 from Krout0n/use-try-fold by @dtolnay
- Use Iterator::try_fold instead of for loop in Value::pointer_functions by @Krout0n
- Release 1.0.64 by @dtolnay
- Fix IoRead's raw buffering on invalid utf-8 as well by @dtolnay
- Merge pull request #757 from serde-rs/panicraw by @dtolnay
- Fix panic deserializing RawValue from invalid utf-8 bytes by @dtolnay
- Fix unnecessary trailing semicolon lints in test suite by @dtolnay
- Release 1.0.63 by @dtolnay
- Merge pull request 754 from Krout0n/entry#and_modify by @dtolnay
- Merge pull request #752 from SamuelQZQ/patch-2 by @dtolnay
- Fix method document in de.rs by @SamuelQZQ
- Release 1.0.62 by @dtolnay
- Touch up PR 751 by @dtolnay
- Merge pull request #751 from icewind1991/value-display-utf8-unchecked by @dtolnay
- Use from_utf8_unchecked in the fmt::Display implementation of Value by @icewind1991
- Merge pull request #744 from Carreau/patch-1 by @dtolnay
- Update example to use Result<User, Box<dyn Error>> by @Carreau
- Intra-doc link for the crate::value link by @dtolnay
- Merge pull request #739 from rory/minor-doc-improvement by @dtolnay
- Make a html link in the doccomments
- Release 1.0.61 by @dtolnay
- Format with rustfmt 1.4.30-nightly by @dtolnay
- Merge pull request #737 from imp/value_from_number by @dtolnay
- Ignore redundant_else pedantic clippy lint by @dtolnay
- Release 1.0.60 by @dtolnay
- Merge pull request #733 from matklad/from-iter-of-pairs by @dtolnay
- Allow collecting an iterator of pairs into JSON object by @matklad
- Suppress clippy unnecessary_wraps lints by @dtolnay
- Resolve clippy comparison_to_empty lint by @dtolnay
- Suppress new manual_range_contains lint by @dtolnay
- Release 1.0.59 by @dtolnay
- Format with rustfmt 1.4.22-nightly by @dtolnay
- Filter floats that parse to infinity from as_f64 by @dtolnay
- Release 1.0.58 by @dtolnay
- Fix no-std preserve_order build by @dtolnay
- Merge pull request #712 from dtolnay/remove_entry by @dtolnay
- Fix no-std build on rust <1.40 by @dtolnay
- Format remove_entry cfg with rustfmt by @dtolnay
- Simplify remove_entry cfg expressions by @dtolnay
- Invert cfg polarity so builds without any cfg assume most recent compiler by @dtolnay
- Use BTreeMap::get_key_value on rust 1.40-1.44 by @dtolnay
- Use BTreeMap::remove_entry on rust 1.45+ by @dtolnay
- Implement remove_entry when feature="preserve_order" by @dtolnay
- Implement remove_entry for BTreeMap with support for rust 1.31 by @dtolnay
- Ignore map_err_ignore Clippy pedantic lint by @dtolnay
- Raise minimum preserve_order version to rust 1.36 by @dtolnay
- Update code of conduct link by @dtolnay
- Update to automod 1.0 by @dtolnay
- Simplify how regression tests are imported by @dtolnay
- Update to automod 0.2 by @dtolnay
- Release 1.0.57 by @dtolnay
- Clean up rustdoc representation of the &mut R Read impl by @dtolnay
- Move Read &mut impl after other Read impls by @dtolnay
- Merge pull request 684 from tinou98/read-mut by @dtolnay
- Raise preserve_order required Rust version to 1.32 by @dtolnay
- Suppress match_like_matches_macro clippy lint by @dtolnay
- Release 1.0.56 by @dtolnay
- Adjust wording of 'Using derive' link by @dtolnay
- Merge pull request #685 from rimutaka/master by @dtolnay
- Linked ReadMe to Using Derive page. by @rimutaka
- Merge pull request #688 from dtolnay/missingcomma by @dtolnay
- Trigger missing comma rustc suggestion by @dtolnay
- Prevent type ascription misdiagnosis by @dtolnay
- Ignore unnested_or_patterns suggesting unstable code by @dtolnay
- Release 1.0.55 by @dtolnay
- Publish with build.rs by @dtolnay
- No need to specify Cargo.toml in package.include by @dtolnay
- Release 1.0.54 by @dtolnay
- Exclude single_precision flag unless needed by @dtolnay
- Exclude lexical code when built without float_roundtrip by @dtolnay
- Extend CI with more feature combinations by @dtolnay
- Gate some tests behind float_roundtrip feature by @dtolnay
- Wire up non-float_roundtrip parsing in long number case by @dtolnay
- Restore best-effort float parse codepath by @dtolnay
- Contrast float_roundtrip and arbitrary_precision by @dtolnay
- Call out performance cost of float_roundtrip by @dtolnay
- Introduce float_roundtrip cargo cfg by @dtolnay
- Clarify explanation of preserve_order feature by @dtolnay
- Fix arithmetic overflow in parse_decimal_overflow by @dtolnay
- Take out some cold code from loop by @dtolnay
- Format with rustfmt 2020-05-19 by @dtolnay
- Merge pull request #680 from dtolnay/significand by @dtolnay
- Deduplicate significand computation by @dtolnay
- Cleanup in parse_integer by @dtolnay
- Reorder float parse methods to prepare for refactor by @dtolnay
- Print both values on failure in lexical parse test by @dtolnay
- Take nonzero fraction into account on exponent overflow by @dtolnay
- Clean up lexical comments by @dtolnay
- Move scratch clear down to first place scratch is needed by @dtolnay
- Suppress some clippy lints that trigger in all-features mode by @dtolnay
- Resolve explicit_into_iter_loop lint by @dtolnay
- Move trailing zero trim to lexical module by @dtolnay
- Skip unneeded scratch clear after parsing float by @dtolnay
- Don't need to push sole 0 in integer part by @dtolnay
- Clean up rustfmt trailing comma glitch by @dtolnay
- Permit trailing comma in tri macro by @dtolnay
- Attributes on fields are now in our oldest supported compiler by @dtolnay
- Fix f32 deserialization in arbitrary_precision mode by @dtolnay
- Rename f32 control field by @dtolnay
- Clean up float deserialization explanation by @dtolnay
- Replace use of AsPrimitive on concrete types by @dtolnay
- Ignore some clippy lints in lexical tests by @dtolnay
- Resolve redundant_field_names lint by @dtolnay
- Fix target arch detection for limb width by @dtolnay
- Tone down some unused num impls by @dtolnay
- Format macro_rules macro from lexical by @dtolnay
- Touch up new float roundtrip test from PR 671 by @dtolnay
- Move lexical unit tests to tests directory by @dtolnay
- Eliminate RSliceIndex trait by @dtolnay
- Replace some suspicious extend calls by @dtolnay
- Resolve clippy lints in lexical by @dtolnay
- Inline type of LimbVecType by @dtolnay
- Unify lexical and top level lib modules by @dtolnay
- Update de.rs use of minimal_lexical by @dtolnay
- Update imports in lexical module by @dtolnay
- Format lexical module with rustfmt by @dtolnay
- Reference lexical as a module by @dtolnay
- Import implementation of minimal-lexical by @dtolnay
- Merge pull request #671 from japaric/gh536 by @dtolnay
- If f32 was requested use 32-bit minimal-lexical by @japaric
- Make clippy happy by @japaric
- Integrate minimal-lexical by @japaric
- Format with rustfmt 2020-05-19 by @dtolnay
- Deal with clippy lints in tests by @dtolnay
- Merge pull request #679 from serde-rs/verify by @dtolnay
- Resolve match_wildcard_for_single_variants pedantic lint by @dtolnay
- Allow but ignore trailing comma in test macros by @dtolnay
- Be better at computer numbering by @dtolnay
- Use https in Cargo.toml documentation link (#675) by @atouchet
- Merge pull request #669 from dtolnay/fuzz by @dtolnay
- Touch up PR 668 by @dtolnay
- Merge pull request #668 from DavidKorczynski/master by @dtolnay
- Merge pull request #666 from dtolnay/help by @dtolnay
- Update 'Getting help' section by @dtolnay
- Release 1.0.53 by @dtolnay
- Downgrade some unnecessary runtime asserts to debug_assert by @dtolnay
- Update arbitrary_precision Debug impl of Number to match normal one by @dtolnay
- Omit a layer of unnecessary nesting from Debug impl by @dtolnay
- Update build status badge to GitHub Actions by @dtolnay
- Avoid repeating slow doctests and compiletests by @dtolnay
- Merge pull request #661 from serde-rs/actions by @dtolnay
- Enable GitHub Actions by @dtolnay
- Release 1.0.52 by @dtolnay
- Merge pull request #658 from jplatte/to_raw_value by @dtolnay
- Run clippy on latest nightly that has clippy by @dtolnay
- Mark StreamDeserializer's error codepaths as cold by @dtolnay
- Release 1.0.51 by @dtolnay
- Merge pull request #649 from serde-rs/fused by @dtolnay
- Implement FusedIterator for StreamDeserializer where possible by @dtolnay
- Implement FusedIterator for Map iterators by @dtolnay
- Merge pull request #648 from serde-rs/streamerror by @dtolnay
- Return None after stream deserializer has failed by @dtolnay
- Test stream behavior after error by @dtolnay
- Release 1.0.50 by @dtolnay
- Merge pull request #640 from smarnach/smarnach/eq-impls by @dtolnay
- Implement Eq for Map, Number and Value. by @smarnach
- Release 1.0.49 by @dtolnay
- Merge pull request #643 from serde-rs/nostd by @dtolnay
- Improve error message when neither std nor alloc is enabled by @dtolnay
- Provide optimized collect_str methods for Value serializer by @dtolnay
- Don't reallocate the string in serialize_char by @dtolnay
- Merge pull request #642 from serde-rs/sized by @dtolnay
- Move ?Sized bounds out of generic parameter lists by @dtolnay
- Merge pull request #641 from serde-rs/collect by @dtolnay
- Implement collect_str for map keys by @dtolnay
- Standardize on using Result type alias where possible by @dtolnay
- Format with rustfmt 2020-03-11 by @dtolnay
- Merge pull request #639 from serde-rs/map by @dtolnay
- Simplify Map's PartialEq impl by @dtolnay
- Select a single docs.rs build target by @dtolnay
- Update url for "Setting up derive" page by @dtolnay
- Suppress wildcard import pedantic lints by @dtolnay
- Suppress buggy excessive_precision lint by @dtolnay
- Release 1.0.48 by @dtolnay
- Show implementation of to_value in value::Serializer docs by @dtolnay
- Extend documentation of value::Serializer by @dtolnay
- Merge pull request #621 from sdleffler/master by @dtolnay
- Expose value serializer by @sdleffler
- Ignore match_single_binding clippy lint by @dtolnay
- Update ui tests to nightly-2020-02-08 by @dtolnay
- Release 1.0.47 by @dtolnay
- Merge pull request #617 from Xanewok/serde-no-std-error by @dtolnay
- Require serde >= 1.0.100 due to no_std-related Error re-export by @Xanewok
- Release 1.0.46 by @dtolnay
- Fixup serialize_entry PR by @dtolnay
- Merge pull request #614 from jmfiaschi/map-serialize-entry by @dtolnay
- Remplace serialize key,value functions by serialize_entry by @jmfiaschi
- Merge pull request #610 from adetaylor/edit-test-instructions by @dtolnay
- Removing obsolete test instructions. by @adetaylor
- Discard unimportant lines from ui tests by @dtolnay
- Release 1.0.45 by @dtolnay
- Copy no-std note to rustdoc by @dtolnay
- Tweak no-std wording to show Cargo.toml snippet by @dtolnay
- Switch rustfmt skip to tool attribute by @dtolnay
- Merge pull request #609 from Xanewok/patch-1 by @dtolnay
- Correct no-std support in README.md by @Xanewok
- Adopt dyn syntax for trait objects by @dtolnay
- Adopt inclusive range syntax by @dtolnay
- Switch to tool attrs by @dtolnay
- Adopt pub(crate) by @dtolnay
- Organize imports by @dtolnay
- Update tests to 2018 edition by @dtolnay
- Update serde_json_test to 2018 edition by @dtolnay
- Update to 2018 edition by @dtolnay
- Rename try! macro to avoid 2018 edition keyword by @dtolnay
- Raise minimum supported rustc to 1.31 by @dtolnay
- Really disable serde std feature in CI by @dtolnay
- Omit to_writer and Serializer in no_std mode by @dtolnay
- Omit from_reader in no_std mode by @dtolnay
- Preserve underlying Debug representation for io error by @dtolnay
- De Morgan the features check by @dtolnay
- Mirror serde_json features to serde_json_test crate by @dtolnay
- Tweak feature check message by @dtolnay
- Merge pull request #606 from Xanewok/no-std-patch by @dtolnay
- Move the core::io implementation to separate module by @Xanewok
- Make io a subset of `std::io` by @Xanewok
- Imply using alloc crate when `std` is not enabled by @Xanewok
- Inline the itoa::write calls by @Xanewok
- Test no_std/alloc on 1.36.0 by @Xanewok
- Mention availability of alloc feature by @Xanewok
- Reorganize std::io facade by @Xanewok
- Fix std feature dependency for itoa by @Freax13
- Ignore transmute_ptr_to_ptr lint by @dtolnay
- Resolve redundant_static_lifetimes lint by @dtolnay
- Merge pull request #600 from deankarn/master by @dtolnay
- Make compatible with older veersions of rust
- Merge pull request #605 from Xanewok/patch-1 by @dtolnay
- Update MSRV to 1.30 in README.md by @Xanewok
- Drop support for rustc <1.30 by @dtolnay
- Provide source method for Error, to allow downcasting cause by @dtolnay
- Drop support for rustc <1.27 by @dtolnay
- Opt in to experimental trybuild diffs by @dtolnay
- Merge pull request #595 from x3ro/doc/pointer_mut_map_example by @dtolnay
- Ignore missing_errors_doc pedantic lint by @dtolnay
- Release 1.0.44 by @dtolnay
- Merge pull request 591 from erickt/value-into-deserializer by @dtolnay
- Implement IntoDeserializer for Value by @erickt
- Release 1.0.43 by @dtolnay
- Merge pull request #590 from nlordell/bump_indexmap_version by @dtolnay
- Release 1.0.42 by @dtolnay
- Merge pull request #585 from Nilix007/add_from_unit_for_value by @dtolnay
- Merge pull request #580 from andrisak/docs_read_without_blocking_eof by @dtolnay
- Fix for Document how to deserialize from a prefix of an io::Read without blocking until EOF #522 by @andrisak
- Ignore must_use_candidate pedantic lint by @dtolnay
- Upgrade to rustversion 1.0 by @dtolnay
- Release 1.0.41 by @dtolnay
- Document that you can't deserialize &str from reader by @dtolnay
- Merge pull request #571 from yankuu/patch-1 by @dtolnay
- Minor typo in doc
- Ignore too_many_lines lint by @dtolnay
- Use swap_remove on IndexMap by @dtolnay
- Format with rustfmt 2019-08-19 by @dtolnay
- Include tests crate in workspace by @dtolnay
- Enable testing cargo build on old compilers by @dtolnay
- Work around rust-lang/cargo#4664 by @dtolnay
- Switch to rustversion by @dtolnay
- Merge pull request #544 from est31/master by @dtolnay
- Release 1.0.40 by @dtolnay
- Move raw_value feature note above the example code by @dtolnay
- Suppress integer_division pedantic lint by @dtolnay
- Update to ryu 1.0 by @dtolnay
- Ignore old inclusive range syntax to support old compilers by @dtolnay
- Suppress a new pedantic lint by @dtolnay
- Ignore bare_trait_objects lint to support old compilers by @dtolnay
- Smaller format for license section by @dtolnay
- Switch to SPDX 2.1 license expression by @dtolnay
- Run ui tests on nightly only by @dtolnay
- Switch ui tests to trybuild by @dtolnay
- Update serde_bytes dependency to 0.11 by @dtolnay
- Merge pull request #525 from 17dec/eof-numbers by @dtolnay
- Return EOF error on cut-off negative sign or exponent
- Return EOF error on cut-off decimal number
- Use non-preview name of Clippy rustup component by @dtolnay
- Release 1.0.39 by @dtolnay
- Merge pull request #521 from dtolnay/f by @dtolnay
- Fix adjacently tagged f32 roundtrip regression by @dtolnay
- Format with rustfmt 2019-02-14 by @dtolnay
- Simplify running update-references.sh by @dtolnay
- Release 1.0.38 by @dtolnay
- Merge pull request #509 from dtolnay/stacker by @dtolnay
- More sensitive test for recursion error by @dtolnay
- Restore support for old compilers by @dtolnay
- Unbounded depth by @dtolnay
- Release 1.0.37 by @dtolnay
- Work around erased-serde round-tripping through de::Error::custom by @dtolnay
- Release 1.0.36 by @dtolnay
- Merge pull request #512 from dtolnay/128key by @dtolnay
- Quotes around u128 in map key by @dtolnay
- Release 1.0.35 by @dtolnay
- Update examples to 2018 edition by @dtolnay
- Update ui tests to 2018 edition by @dtolnay
- Copyright/license headers by @dtolnay
- Simplify compiletest setup by @dtolnay
- Format lookup tables in a way that does not require rustfmt skip by @dtolnay
- Release 1.0.34 by @dtolnay
- Update name of deprecated str::trim_right by @dtolnay
- Conditionally provide impl From<i128> and From<u128> for Number by @dtolnay
- Merge pull request #506 from koushiro/fix_integer128_serialize by @dtolnay
- Modify test by @koushiro
- Fix serialization of i128 and u128 types by @koushiro
- Fix name of lint that was renamed in Clippy by @dtolnay
- Show how to use BufReader by @dtolnay
- Consistently apply Example and Errors headings by @dtolnay
- Update ui tests for rustc nightly-2018-11-29 by @dtolnay
- Set up Travis build names by @dtolnay
- Release 1.0.33 by @dtolnay
- Merge pull request #504 from serde-rs/key by @dtolnay
- Allow map key to be borrowed from &Value by @dtolnay
- Ignore lint about rustfmt::skip by @dtolnay
- Format with rustfmt 0.99.6-nightly by @dtolnay
- Drop nightly dependency of compiletest by @dtolnay
- Update ui tests at nightly 2018-10-26 by @dtolnay
- Release 1.0.32 by @dtolnay
- Merge pull request #493 from dtolnay/overflow by @dtolnay
- Fix overflow on i32::min_value() as exponent by @dtolnay
- Merge pull request #491 from yjh0502/error_location by @dtolnay
- Fix playground links in readme by @dtolnay
- Simplify by using json Result in Read methods by @dtolnay
- Release 1.0.31 by @dtolnay
- Merge pull request #489 from yjh0502/master by @dtolnay
- Specialize hexadecimal sequence decoding by @yjh0502
- Release 1.0.30 by @dtolnay
- Non-recursive ignore_value by @dtolnay
- Release 1.0.29 by @dtolnay
- Merge pull request #485 from dtolnay/raw by @dtolnay
- Fix malicious arbitrary precision number test by @dtolnay
- Fix raw value compilation on rustc older than 1.20 by @dtolnay
- Document RawValue ownership by @dtolnay
- Use Box<RawValue> as the owned raw value by @dtolnay
- Enable raw_value feature in docs.rs and playground by @dtolnay
- Document RawSlice by @dtolnay
- Split RawSlice and RawValue by @dtolnay
- Simplify naming of private tokens by @dtolnay
- Name the RawValue private field by @dtolnay
- Handwrite Debug for RawValue to minimize escaping by @dtolnay
- Fix up some unused import warnings by @dtolnay
- Cfg gate everything having to do with RawValue by @dtolnay
- Change mapping of RawValue to a struct with one key by @dtolnay
- Pass data to RawValue as a string by @dtolnay
- Simplify raw buffer toggle by @dtolnay
- Implement RawValue type by @srijs
- Release 1.0.28 by @dtolnay
- Avoid instantiating deserialize_any for KeyClassifier by @dtolnay
- Merge pull request #482 from dtolnay/mem by @dtolnay
- Tool attr syntax is not stable yet by @dtolnay
- Merge pull request #481 from dtolnay/ci by @dtolnay
- Move CI commands into travis.yml and appveyor.yml by @dtolnay
- Merge pull request #479 from srijs/refactor/reusable-special-types by @dtolnay
- Refactor to make "special" type machinery more reusable by @srijs
- Format with rustfmt 0.99.4 by @dtolnay
- Simplify itoa code in arbitrary_precision case by @dtolnay
- Release 1.0.27 by @dtolnay
- Merge pull request #476 from Enet4/docs/value_slice_u8 by @dtolnay
- Monospace format &[u8] in value module docs by @Enet4
- Release 1.0.26 by @dtolnay
- Merge pull request #472 from dtolnay/ryu by @dtolnay
- Switch from dtoa to ryu by @dtolnay
- Release 1.0.25 by @dtolnay
- Merge pull request #458 from dtolnay/local-inner-macros by @dtolnay
- Local inner macros by @dtolnay
- Release 1.0.24 by @dtolnay
- Merge pull request #462 from dtolnay/unused by @dtolnay
- Make json macro compatible with deny(unused_results) by @dtolnay
- Format with rustfmt 0.8.2 by @dtolnay
- Skip auto formatting test_stream macro by @dtolnay
- Revert "Local inner macros" by @dtolnay
- Release 1.0.23 by @dtolnay
- Local inner macros by @dtolnay
- Release 1.0.22 by @dtolnay
- Merge pull request #455 from dtolnay/eof by @dtolnay
- Produce eof error on truncated ident by @dtolnay
- Improve error message of unexpected colon or comma in json macro by @dtolnay
- Move Display impl for Value to value/mod.rs by @dtolnay
- Release 1.0.21 by @dtolnay
- Format with rustfmt 0.8.2 by @dtolnay
- Merge pull request #453 from fdionisi/feature/ser-char-map-key by @dtolnay
- Allow char to be a HashMap key
- Release 1.0.20 by @dtolnay
- Merge pull request #451 from lnicola/indexmap by @dtolnay
- Update Travis configuration to test preserve_order on 1.18 by @lnicola
- Use IndexMap instead of LinkedHashMap by @lnicola
- Release 1.0.19 by @dtolnay
- Release 1.0.18 by @dtolnay
- Merge pull request #449 from serde-rs/integer128 by @dtolnay
- Basic support for i128 and u128 by @dtolnay
- Format with rustfmt 0.7.0 by @dtolnay
- Update invalid length error messages for serde 1.0.52 by @dtolnay
- Follow clippy unseparated_literal_suffix pedantic lint by @dtolnay
- Release 1.0.17 by @dtolnay
- Merge pull request #439 from Diggsey/safe-eq by @dtolnay
- Use BTreeMap equality implementation when applicable by @Diggsey
- Implement order-independent equality by @Diggsey
- Format with rustfmt 0.6.0 by @dtolnay
- Release 1.0.16 by @dtolnay
- Mark error construction as cold code by @dtolnay
- Instantiate io::Result::<usize>::map just once by @dtolnay
- Map Into::into by @dtolnay
- Rename parser's Number to ParserNumber by @dtolnay
- Reduce visibility of parse_any_signed_number by @dtolnay
- Merge pull request #437 from serde-rs/mut by @dtolnay
- Merge pull request #436 from serde-rs/num by @dtolnay
- Drop num-traits dependency by @dtolnay
- Relase 1.0.15 by @dtolnay
- Fix non-reference pattern for old compilers by @dtolnay
- Format with rustfmt 0.4.2 by @dtolnay
- Struct deserialization from array Value by @dtolnay
- Implement all &Value deserializer hints by @dtolnay
- Implement all Value deserializer hints by @dtolnay
- Release 1.0.14 by @dtolnay
- Merge pull request #432 from serde-rs/curl by @dtolnay
- Get rustup-init with curl to avoid tls failures by @dtolnay
- Cleaner Debug representation of Error by @dtolnay
- Less eye-catching rustc version badge by @dtolnay
- Merge pull request #431 from serde-rs/pos by @dtolnay
- Spell out pos -> position by @dtolnay
- Spell out pos -> positive by @dtolnay
- Merge pull request #430 from serde-rs/rustc by @dtolnay
- Rustc version badge by @dtolnay
- Clarify guarantees of the arbitrary_precision feature by @dtolnay
- Update ui tests for nightly-2018-03-26 by @dtolnay
- Merge pull request #429 from serde-rs/rustfmt by @dtolnay
- Format with rustfmt 0.4.1 by @dtolnay
- Link to serde-json-core crate by @dtolnay
- Merge pull request #426 from mtn/exp_pos by @dtolnay
- Replace instances of "exp_pos" with "exp_positive" by @mtn
- Release 1.0.13 by @dtolnay
- Arbitrary-precision numerics support (#416) by @alexreg
- Merge pull request #425 from mtn/positive_patch by @oli-obk
- Replace relevant instance of "pos" with "positive" by @mtn
- Release 1.0.12 by @dtolnay
- Merge pull request #424 from Eijebong/itoa by @dtolnay
- Update itoa to 0.4 by @Eijebong
- Ignore unreadable_literal lint in tests by @dtolnay
- Update ui tests for nightly-2018-03-16 by @dtolnay
- Release 1.0.11 by @dtolnay
- Merge pull request #421 from dmizuk/value-take by @dtolnay
- Update ui tests for nightly-2018-03-03 by @dtolnay
- Release 1.0.10 by @dtolnay
- Merge pull request #414 from boxofrox/fix/issue-364 by @dtolnay
- Improve error when json strings contain control characters by @boxofrox
- Ignore redundant_field_names lint by @dtolnay
- Update ui tests for nightly-2018-02-26 by @dtolnay
- Merge pull request #415 from kraai/kraai-patch-1 by @dtolnay
- Simplify the implementation of str's index_or_insert by @kraai
- Note that eager_json depends on private API by @dtolnay
- Merge pull request #411 from cuviper/num-traits-0.2 by @dtolnay
- Update to num-traits 0.2 with no_std by @cuviper
- Ignore a new clippy lint by @dtolnay
- Merge pull request #406 from H2CO3/remove-copy-and-cleanup by @dtolnay
- Simplify impl FromIterator for Value::Array, and make it look consistent with the rest of the From<Collection> impls
- Follow clippy's replace_consts lint by @dtolnay
- Release 1.0.9 by @dtolnay
- Test fewer old versions by @dtolnay
- Hide Number implementation details from Debug representation by @dtolnay
- Test the debug representations of Number and Value by @dtolnay
- Upgrade to compiletest 0.3 by @dtolnay
- Merge pull request #399 from serde-rs/map-or by @dtolnay
- Fewer instantiations of Option::map_or by @dtolnay
- Release 1.0.8 by @dtolnay
- Merge pull request #392 from bouk/fix-truefalse by @dtolnay
- Fix falsey typo by @bouk
- Encountering an error is the cold path by @dtolnay
- Decrease size of ErrorCode from 32 bytes to 24 bytes by @dtolnay
- Make deserialize_bytes work more like deserialize_str by @dtolnay
- Merge pull request #390 from serde-rs/try by @dtolnay
- Override the try macro to eliminate From calls by @dtolnay
- Merge pull request #389 from serde-rs/hints by @dtolnay
- Implement all the deserializer hints by @dtolnay
- Merge pull request #388 from serde-rs/mapkey by @dtolnay
- Stop instantiating parse_value in MapKey::deserialize_any by @dtolnay
- Merge pull request #387 from serde-rs/fix-position by @dtolnay
- Stop instantiating fix_position so many times by @dtolnay
- Release 1.0.7 by @dtolnay
- Merge pull request #384 from bouk/stream-literals by @dtolnay
- Update ui tests to include nightly wording change by @dtolnay
- Update stderr files for -Z external-macro-backtrace by @dtolnay
- Merge pull request #383 from xfix/patch-1 by @dtolnay
- Warn about enum_variant_names violations in enum N by @LunaBorowska
- Release 1.0.6 by @dtolnay
- Merge pull request #382 from ignatenkobrain/patch-2 by @dtolnay
- Bump linked-hash-map to 0.5
- Whitelist needless_pass_by_value lint by @dtolnay
- Suppress lint about fallible From<Error> for io::Error by @dtolnay
- Release 1.0.5 by @dtolnay
- More detailed documentation of Index trait by @dtolnay
- Merge pull request #374 from sinkuu/takebyvalue by @dtolnay
- Adapt contributing.md from Serde by @dtolnay
- Clean up identity conversions by @dtolnay
- Release 1.0.4 by @dtolnay
- Explain square bracket indexing in more detail by @dtolnay
- Merge pull request #368 from twify93/patch-1 by @oli-obk
- README - add additional info about untyped Example by @elpiel
- Comma outside of array or object is not necessarily trailing by @dtolnay
- Update ui test failure message by @dtolnay
- Merge pull request #353 from fmoor/feature/trailing_comma by @dtolnay
- Change error type for trailing commas, fixes #352 by @fmoor
- Release 1.0.3 by @dtolnay
- Merge pull request #356 from serde-rs/ignore by @dtolnay
- Optimize deserialize_ignored_any by @dtolnay
- Ignore cast_lossless lint by @dtolnay
- Ignore clippy's use_self lint by @dtolnay
- Replace deprecated compiletest::default_config() by @dtolnay
- Update ui error message by @dtolnay
- Merge pull request #338 from foriequal0/master by @dtolnay
- Implement PartialEq<bool> for Value by @foriequal0
- Update ui error message by @dtolnay
- Test rust 1.15.0 by @dtolnay
- Refresh the ui tests by @dtolnay
- Merge pull request #332 from erickt/master by @dtolnay
- Switch to using char::encode_utf8 by @erickt
- Exclude macros file from being tested by itself by @dtolnay
- New error message in UI tests by @dtolnay
- Merge pull request #322 from GyrosOfWar/master by @dtolnay
- Fixed error in tests by @GyrosOfWar
- Better invalid type error message (addresses issue #319) by @GyrosOfWar
- Update ui/parse_expr for latest nightly by @dtolnay
- Link to benchmarks from readme by @dtolnay
- Release 1.0.2 by @dtolnay
- Take credit by @dtolnay
- Merge pull request #314 from Rufflewind/t313 by @dtolnay
- Fully factor out visitor dependence in number parser by @Rufflewind
- Reduce visitor-dependence in number parsers by @Rufflewind
- Release 1.0.1 by @dtolnay
- No need for pub use in private module by @dtolnay
- Index got lost in the grand value division by @dtolnay
- Merge pull request #311 from serde-rs/int by @dtolnay
- Treat non-integer key as a type error by @dtolnay
- Allow integers to be used as map keys again by @dtolnay
- Merge pull request #306 from serde-rs/entry by @dtolnay
- Use the new linked-hash-map entry API by @dtolnay
- Merge pull request #307 from killercup/feature/split-value-into-pieces by @dtolnay
- Grand value division: value::de by @killercup
- Grand value division: value::ser by @killercup
- Grand value division: value::from by @killercup
- Grand value division: value::partial_eq by @killercup
- Grand value division: value::index by @killercup
- Move Value into its own mod by @killercup
- New version number in readme by @dtolnay
- Release 1.0.0 by @dtolnay
- Update to serde 1.0 by @dtolnay
- Allow writing to writer by value by @dtolnay
- Use the conventional "Errors" heading by @dtolnay
- Less simplistic to_value example by @dtolnay
- Examples for the deserialization API by @dtolnay
- Fix copy-paste error in deserializer docs by @dtolnay
- Example of from_value by @dtolnay
- Clarify ambiguous imports by @dtolnay
- Allow borrowing from &Value by @dtolnay
- Cargo fmt the error conversions by @dtolnay
- Hide the conversion from io::Error to Error by @dtolnay
- Map type hyperlinks by @dtolnay
- Format in rfc style by @dtolnay
- The serde 1.0 branch merged by @dtolnay
- Merge branch 'origin/1.0' into 'origin/master' by @dtolnay
- Keep up with serde 1.0 branch by @dtolnay
- Organize top links by @dtolnay
- License boilerplate by @dtolnay
- Point html_root_url to docs.rs by @dtolnay
- Fix path to readme file by @dtolnay
- Merge branch 'origin/master' into 'origin/1.0' by @dtolnay
- Merge pull request #303 from serde-rs/offset by @dtolnay
- Test byte offsets of stream by @dtolnay
- Run the existing tests against every type of stream by @dtolnay
- Move stream tests to their own file by @dtolnay
- Expose number of bytes processed by StreamDeserializer by @dtolnay
- Rename ValueDeserializer trait to IntoDeserializer by @dtolnay
- Examples for all the conversion methods by @dtolnay
- Test and document preserve_order feature by @dtolnay
- Merge pull request #302 from serde-rs/combine by @dtolnay
- Combine serde_json and tests into one crate by @dtolnay
- Use the recommended default rustfmt style by @dtolnay
- Clean up some rustdoc example code by @dtolnay
- Merge branch 'origin/master' into 'origin/1.0' by @dtolnay
- Expand the readme examples into real code by @dtolnay
- Release 0.9.10 by @dtolnay
- Merge pull request #301 from serde-rs/stream by @dtolnay
- Require array or object in StreamDeserializer by @dtolnay
- More informative parse_whitespace method by @dtolnay
- Merge pull request #299 from serde-rs/ioerr by @dtolnay
- Return io::Error from formatter methods by @dtolnay
- Merge pull request #297 from serde-rs/fragment by @dtolnay
- Pass &str to write_string_fragment by @dtolnay
- Merge pull request #296 from serde-rs/appveyor by @dtolnay
- Set up AppVeyor by @dtolnay
- Merge pull request #295 from serde-rs/tojson by @dtolnay
- Ignore clippy false positive by @dtolnay
- Conversion to io::Error by @dtolnay
- Replace serde::bytes with serde_bytes by @dtolnay
- Keep up with serde 1.0 branch by @dtolnay
- Disable publishing by @dtolnay
- Catch up to serde's 1.0 branch by @dtolnay
- Merge pull request #288 from serde-rs/zerocopy by @dtolnay
- Use the Deserialize<'de> changes from serde's git by @dtolnay
- Merge pull request #278 from serde-rs/error by @dtolnay
- Extend the Error API with line, column, category by @dtolnay
- Merge pull request #280 from imp/value_pretty_print by @dtolnay
- Pretty print Value when alternate formatting requested by @imp
- Merge pull request #276 from serde-rs/ui by @oli-obk
- Compile-fail tests for the json macro by @dtolnay
- Two years outdated comment by @dtolnay
- Deny clippy lints in travis by @dtolnay
- Thanks for the test optimization clippy by @dtolnay
- Release 0.9.9 by @dtolnay
- Satisfy clippy with a panic message by @dtolnay
- Merge pull request #267 from nox/display by @dtolnay
- Update to serde 0.9.11 for collect_str by @nox
- Redefine Serializer::collect_str by @nox
- Avoid allocating a String to serialize a single char by @nox
- Merge pull request #273 from cspiegel/json-macro-panic by @dtolnay
- Document the fact that json! can panic. by @cspiegel-cypherpath
- Justify pass-by-value by @dtolnay
- Expose IoRead by @dtolnay
- Release 0.9.8 by @dtolnay
- Inline trivial method by @dtolnay
- Merge pull request #265 from bennofs/fix-256-followup by @dtolnay
- Fix performance regression caused by 8123ecc474ea599d4659f20c3cfbfb7011b77628 by @bennofs
- Merge pull request #263 from serde-rs/map by @oli-obk
- Merge pull request #261 from serde-rs/ref-value by @dtolnay
- Test deserializing from &Value by @dtolnay
- Deserializer for &Value by @dtolnay
- Merge pull request #260 from serde-rs/read by @oli-obk
- Expose the various Read implementations by @dtolnay
- Include readme and licenses in crates.io archive by @dtolnay
- Release 0.9.7 by @dtolnay
- Merge pull request #257 from bennofs/fix-256 by @dtolnay
- Merge pull request #255 from frewsxcv/patch-1 by @dtolnay
- Minor doc formatting improvements for `Number`. by @frewsxcv
- Typo in StreamDeserializer documentation by @dtolnay
- You shouldn't use Error::description() by @dtolnay
- Merge pull request #253 from killercup/feature/from-t-with-love by @dtolnay
- Implement a bunch of `From`s by @killercup
- Merge pull request #250 from serde-rs/stream by @dtolnay
- Expose serde_json::de::Read to use in where clauses by @dtolnay
- Release 0.9.6 by @dtolnay
- Merge pull request #249 from serde-rs/index by @oli-obk
- IndexMut for Map and Value by @dtolnay
- Merge pull request #243 from serde-rs/tojson by @oli-obk
- Generalize json! macro to ToJson by @dtolnay
- Release 0.9.5 by @dtolnay
- Merge pull request #240 from Kroisse/from-iterator-for-map by @dtolnay
- Implement Extend for value::Map by @Kroisse
- Implement FromIterator for value::Map by @Kroisse
- Release 0.9.4 by @dtolnay
- Simplify json macro error cases by @dtolnay
- Improve error message when json macro ends after colon by @dtolnay
- Resolve clippy lints in tests by @dtolnay
- Switch to cargo-clippy by @dtolnay
- Inline docs at the top level by @dtolnay
- Merge pull request #238 from serde-rs/pubtuple by @oli-obk
- No tuple structs with private fields in public API by @dtolnay
- Release 0.9.3 by @dtolnay
- Merge pull request #237 from serde-rs/nohelper by @dtolnay
- Refactor json_internal macro to need no helper macros by @dtolnay
- Upgrade to serde's impossible serializer by @dtolnay
- Merge pull request #235 from imp/value_partialeq by @oli-obk
- Update other tests to accomodate new PartialEq impl by @imp
- Impl PartialEq for Value by @imp
- Invalid type errors in unit variant visitor by @dtolnay
- Use json macro in index documentation by @dtolnay
- Use json macro in pointer documentation by @dtolnay
- Clean up value Default documentation by @dtolnay
- Fail to_value on float keys by @dtolnay
- Merge pull request #233 from frewsxcv/doc-example by @dtolnay
- Don't ignore Rust doc example. by @frewsxcv
- Merge pull request #232 from frewsxcv/bump by @dtolnay
- Bump 'itoa' and 'dtoa' dependencies. by @frewsxcv
- Merge pull request #231 from killercup/fix/221-integer-keys-in-to_value by @dtolnay
- Serialize Map with integer keys by @killercup
- Merge pull request #230 from killercup/fix/220-invalid-enum-parser by @dtolnay
- Prevent invalid enum deserialization by @killercup
- Rename KeyOnlyVariantVisitor to UnitVariantVisitor by @killercup
- Merge pull request #228 from killercup/docs/index-examples by @dtolnay
- Merge pull request #227 from killercup/docs/pointer-example by @dtolnay
- Merge pull request #226 from killercup/feature/impl-default-for-value by @dtolnay
- Impl Default for Value by @killercup
- Release 0.9.2 by @dtolnay
- Merge pull request #218 from serde-rs/indexmap by @oli-obk
- Index into Map by @dtolnay
- Clarify the type requirement for interpolating map keys by @dtolnay
- Release 0.9.1 by @dtolnay
- Non-nightly test on beta only by @dtolnay
- Clean up travis config by @dtolnay
- We don't look at coveralls anymore by @dtolnay
- Docs are built in a different repo by @dtolnay
- Clean up dependency declarations by @dtolnay
- Fix typo in rustdoc by @dtolnay
- Typo in readme by @dtolnay
- Readme cleanup by @dtolnay
- Revamp readme by @dtolnay
- Release 0.9.0 by @dtolnay
- Update to serde 0.9.0 by @dtolnay
- Release 0.9.0-rc3 by @dtolnay
- Update to serde 0.9.0-rc4 by @dtolnay
- Document some failure cases by @dtolnay
- Merge pull request #213 from serde-rs/rustdoc by @dtolnay
- Documentation by @dtolnay
- Merge pull request #211 from serde-rs/value by @dtolnay
- Ticks around `None` by @dtolnay
- Justify Index behavior by @dtolnay
- Merge branch master into origin/value by @dtolnay
- Merge pull request #210 from serde-rs/ref by @dtolnay
- Merge branch master into origin/ref by @dtolnay
- Release 0.9.0-rc2 by @dtolnay
- Update to serde 0.9.0-rc3 by @dtolnay
- Take T by ref by @dtolnay
- Implement indexing into Value by @dtolnay
- Drop pointer methods down to the bottom by @dtolnay
- Pin to rc2 by @dtolnay
- Merge pull request #209 from serde-rs/muncher by @dtolnay
- Improve tt object parsing error messages by @dtolnay
- Handle commas within tt object values by @dtolnay
- Better tt handling of commas within array values by @dtolnay
- Use vec![...] in tt-muncher to optimize arrays by @dtolnay
- Put error behind box behind opaque newtype by @dtolnay
- To_value can get away with just a borrow by @dtolnay
- Rearrange json macro to make top-level structure clear by @dtolnay
- Merge pull request #205 from serde-rs/constructors by @oli-obk
- Merge branch master into origin/constructors by @dtolnay
- Release 0.9.0-rc1 by @dtolnay
- Merge branch origin/master into origin/constructor by @dtolnay
- Whitelist should_implement_trait by @dtolnay
- Use serde_json::Deserializer for all deserialization by @dtolnay
- Merge pull request #207 from serde-rs/muncher by @dtolnay
- Merge branch master into origin/muncher by @dtolnay
- Merge pull request #208 from serde-rs/builder by @oli-obk
- Update tests to use the tt-muncher by @dtolnay
- Merge pull request #206 from serde-rs/rc2 by @dtolnay
- Update to serde 0.9.0-rc2 by @dtolnay
- Merge pull request #204 from serde-rs/debug by @dtolnay
- Derive Debug for Value by @dtolnay
- Merge pull request #197 from serde-rs/formatter by @dtolnay
- Require newline to be written successfully by @dtolnay
- Hide itoa/dtoa from the public API by @dtolnay
- Resolve conflicts by @dtolnay
- Merge branch v0.9.0 into master by @dtolnay
- Merge tag v0.8.4 into v0.9.0 by @dtolnay
- Merge tag v0.8.3 into v0.9.0 by @dtolnay
- Merge pull request #145 from dflemstr/string-formatter-forwarding by @dtolnay
- Forward the correct formatter instance to format_escaped_str by @dflemstr
- Merge pull request #143 from dflemstr/formatter by @dtolnay
- Replace accidental raw null write with Formatter call by @dflemstr
- Make Formatter have a sane default implementation by @dflemstr
- Extend Formatter with more callbacks by @dflemstr
- Merge tag v0.8.6 into master by @dtolnay
- Release 0.8.6 by @dtolnay
- Workaround to support rustc 1.8.0 by @dtolnay
- Merge tag v0.8.5 into master by @dtolnay
- Release 0.8.5 by @dtolnay
- Simplify eof logic by @dtolnay
- Propagate EOF found while checking trailing whitespace by @kchmck
- Merge pull request #188 from serde-rs/map by @oli-obk
- Update lint name to reflect private N by @dtolnay
- Simplify Value serializer's serialize_bytes by @dtolnay
- Private N by @dtolnay
- Resolve conflicts by @dtolnay
- Merge branch master into map by @dtolnay
- Merge pull request #187 from serde-rs/panic by @oli-obk
- Document the failure cases in to_value / to_json by @dtolnay
- Do not panic in to_value by @dtolnay
- Merge pull request #192 from serde-rs/lookup by @oli-obk
- Clippy lints by @dtolnay
- Inline all the wrapper things by @dtolnay
- Unify the number variants behind an opaque Number by @dtolnay
- Merge branch master into map by @dtolnay
- Stop testing on 1.11.0 by @dtolnay
- Fix ?Sized bounds for old compilers by @dtolnay
- Extract serde_json::Map into an opaque newtype by @dtolnay
- Simplify Value's VariantVisitor by @dtolnay
- Merge pull request #185 from serde-rs/up by @dtolnay
- Merge branch master into up by @dtolnay
- Workaround for Rust 1.12.0 by @dtolnay
- Do not depend on impls from linked-hash-map by @dtolnay
- Depend on serde 0.9.0-rc1 by @dtolnay
- Unabbreviated method naming by @dtolnay
- Implement Deserializer directly on Value by @dtolnay
- Use the Ok value of Serializer to do to_value by @dtolnay
- Enforce correct use of Serialize and Deserialize traits by @dtolnay
- Enforce correct use of Deserialize trait by @dtolnay
- Enforce correct use of Serialize trait by @dtolnay
- Update to Serde 0.9 by @dtolnay
- Merge pull request #182 from tshepang/patch-1 by @dtolnay
- Follow Rust idiom of trailing comma by @tshepang
- Allow integers to be used as map keys (#177) by @bjorn3
- Merge pull request #178 from serde-rs/newline by @oli-obk
- Require newline to be written successfully by @dtolnay
- Link to release notes from readme by @dtolnay
- Readme revamp by @dtolnay
- Release 0.8.4 by @dtolnay
- Merge pull request #171 from CryptArchy/pointer_mut by @oli-obk
- Implement issue #68 - add pointer_mut by @CryptArchy
- Merge pull request #172 from serde-rs/strkey by @oli-obk
- Round trip test for effectively string keys by @dtolnay
- Allow map keys that are effectively strings by @dtolnay
- Merge pull request #163 from serde-rs/limit by @dtolnay
- Limit recursion to 128 levels by @dtolnay
- Drop testing on rust 1.10 by @dtolnay
- Minimum support versions by @dtolnay
- Release 0.8.3 by @dtolnay
- Merge pull request #161 from mephinet/boolean-typo-fix by @dtolnay
- Typo fixed: it's called Bool, not Boolean - cf https://docs.serde.rs/serde_json/value/enum.Value.html by @mephinet
- Update to proc_macro by @dtolnay
- Merge pull request #159 from serde-rs/derive by @dtolnay
- Update to serde_derive by @dtolnay
- Fix serde_derive usage examples by @dtolnay
- Update README.md for deprecation of serde_macros for serde_derive by @Arzte
- Update docs for the deprecation of serde_macros. by @Arzte
- Merge pull request #156 from traviskaufman/fix/ser-nonfinite-f64-as-value by @dtolnay
- Ensure value::Serializer emits Value::Null for non-finite floats by @traviskaufman
- Release 0.8.2 by @dtolnay
- Merge pull request #150 from withoutboats/to_writer_trait_objects by @dtolnay
- Allow trait objects in the to_writer function. by @withoutboats
- Merge pull request #149 from rphmeier/to_value_by_value by @dtolnay
- Take argument to `Value::to_value` by value by @rphmeier
- Merge pull request #148 from serde-rs/forward by @oli-obk
- Use serde's forward_to_deserialize by @dtolnay
- Whitelist missing_docs_in_private_items by @dtolnay
- Merge pull request #141 from serde-rs/lints by @dtolnay
- Fix new lints in clippy 0.84 by @dtolnay
- Merge pull request #139 from dflemstr/patch-1 by @dtolnay
- Derive (Clone, Debug) for formatters by @dflemstr
- Skip preserve_order build on 1.8.0 by @dtolnay
- Update documentation links by @dtolnay
- Release 0.8.1 by @dtolnay
- Merge pull request #136 from laktak/order by @dtolnay
- Merge pull request #131 from serde-rs/clippy by @dtolnay
- Merge pull request #124 from killercup/patch-1 by @dtolnay
- Explicit version in Readme by @killercup
- Release 0.8.0 by @dtolnay
- Update for map serialization changes by @sfackler
- Fix test dependency by @dtolnay
- Release 0.8.0-rc1 by @dtolnay
- Merge pull request #122 from serde-rs/rc3 by @oli-obk
- Update to serde 0.8.0-rc3 by @dtolnay
- Bump dtoa depenency by @dtolnay
- Merge pull request #118 from serde-rs/serializer by @dtolnay
- Depend on serde 0.8.0-rc1 by @dtolnay
- New Serializer API by @dtolnay
- Merge pull request #117 from serde-rs/rustfmt by @dtolnay
- Run rustfmt by @dtolnay
- Merge pull request #114 from serde-rs/large by @dtolnay
- Parse_exponent_overflow is cold by @dtolnay
- Ignore if_same_then_else false positive by @dtolnay
- Error on large numbers instead of parsing infinity by @dtolnay
- Merge pull request #115 from serde-rs/brackets by @oli-obk
- Fix unexpected brackets in to_value of a newtype struct by @dtolnay
- Merge pull request #110 from serde-rs/float by @oli-obk
- Speed up float parsing by @dtolnay
- Merge pull request #111 from serde-rs/unstable by @dtolnay
- Rename feature "nightly-testing" to "unstable-testing" by @dtolnay
- Merge pull request #105 from serde-rs/str by @oli-obk
- Workaround to support rustc 1.8.0 by @dtolnay
- Specialize parse_string for Iter=&str by @dtolnay
- Merge pull request #106 from serde-rs/utf8err by @oli-obk
- Merge pull request #107 from serde-rs/version by @dtolnay
- Merge pull request #104 from serde-rs/type by @dtolnay
- Stop using {:?} to print de::Type by @dtolnay
- Merge pull request #102 from serde-rs/clippy by @oli-obk
- Fix clippy lints by @dtolnay
- Merge pull request #100 from serde-rs/str by @dtolnay
- Specialize parse_string for Iter=&[u8] by @dtolnay
- Merge branch origin/v0.8.0-rc into origin/master by @dtolnay
- Fix f64 tests by @dtolnay
- Speed up float printing by @dtolnay
- Merge pull request #92 from serde-rs/as by @dtolnay
- Rename Value::as_* functions by @dtolnay
- Merge pull request #93 from serde-rs/build by @dtolnay
- Rename Object/ArrayBuilder::unwrap() to build() by @dtolnay
- Merge pull request #94 from serde-rs/escape_bytes by @dtolnay
- Merge pull request #97 from dtolnay/sliceread by @dtolnay
- Specialize parser for Iter=&[u8] by @dtolnay
- Auto merge of #76 - dtolnay:unit, r=erickt by @homu
- Serialize unit variants as name only by @dtolnay
- Release 0.7.4 by @dtolnay
- Bump linked-hash-map dependency by @dtolnay
- Auto merge of #89 - dtolnay:str, r=oli-obk by @homu
- Speed up string printing by @dtolnay
- Merge pull request #87 from dtolnay/just-itoa by @dtolnay
- Speed up integer printing by @dtolnay
- Release 0.7.3 by @dtolnay
- Merge pull request #85 from npgm/fix-ctrl3 by @dtolnay
- Correctly escape ASCII control characters in strings by @raphlinus
- Auto merge of #83 - dtolnay:travis, r=oli-obk by @homu
- Trim down the Travis build by @dtolnay
- Release 0.7.2 by @dtolnay
- Rename the map visitor to MapVisitor by @dtolnay
- More consistent with imports between preserve_order and not by @dtolnay
- Mention LinkedHashMap in doc by @dtolnay
- Merge pull request #80 from laktak/preserve_order by @dtolnay
- Updated dependencies by @laktak
- Updated from code review by @laktak
- Use linked_hash_map::IntoIter by @laktak
- Merge pull request #78 from dtolnay/expand by @dtolnay
- Use serde_codegen::expand in json_tests/build.rs by @dtolnay
- Auto merge of #75 - erickt:fix-warning, r=erickt by @homu
- Fix a warning by @erickt
- Merge pull request #72 from dtolnay/release by @erickt
- Release 0.7.1 by @dtolnay
- Auto merge of #73 - Ms2ger:num, r=oli-obk by @homu
- Use num_traits. by @Ms2ger
- Auto merge of #61 - arcnmx:value-missing-field, r=oli-obk by @homu
- Auto merge of #63 - s-panferov:feature/traits, r=erickt by @homu
- Impl Display and FromStr traits by @s-panferov
- Auto merge of #41 - pyfisch:json-pointer, r=erickt by @homu
- Implement RFC6901 JSON Pointer by @pyfisch
- Auto merge of #64 - s-panferov:feature/to-json, r=oli-obk by @homu
- Create and impl ToJson trait by @s-panferov
- Merge pull request #49 from dtolnay/indoc by @erickt
- Use indoc for JSON document literals in test by @dtolnay
- Merge remote-tracking branch 'remotes/origin/master' by @erickt
- Merge pull request #38 from dtolnay/readme by @erickt
- Fix examples in readme by @dtolnay
- Add support for skeptic to test readme by @erickt
- Update to latest Error::custom signature by @erickt
- Merge branch 'master' into 0.7.x by @erickt
- Rename JSONStream to StreamDeserializer by @erickt
- Merge branch 'feature-parse-stream' by @erickt
- Fixed error handling by @little-arhat
- [add] test for empty input by @little-arhat
- [fix] Proper handling of trailing whitespaces by @little-arhat
- Apply review comments: by @little-arhat
- Add clippy support by @erickt
- Merge pull request #31 from cmbrandenburg/missing_field_fixes by @erickt
- Report correct error code for missing field by @cmbrandenburg
- Merge pull request #25 from tomjakubowski/unsize_to_value by @erickt
- Merge pull request #35 from nixpulvis/negative-zero by @erickt
- Fix negative zero by @nixpulvis
- Fix broken things with latest serde by @jwilm
- Update to latest serde master rev by @jwilm
- Feat(serde-up) Support serde 0.7 by @jwilm
- Merge pull request #27 from jnicholls/master by @erickt
- Make the constructor methods publicly visible for the PrettyFormatter.
- Merge pull request #23 from little-arhat/fix-minor-typo by @erickt
- Minor typo: Interator => Iterator by @little-arhat
- Merge remote-tracking branch 'remotes/discordtech/master' by @erickt
- Merge github.com:serde-rs/json by @vegai
- Add necessary whitespace, add renaming example by @vegai
- Pin to specific serde/num crates by @erickt
- Merge pull request #19 from zr40/patch-1 by @erickt
- Fix code example in docs by @zr40
- Merge pull request #15 from discordtech/master by @erickt
- Merge pull request #16 from jnicholls/master by @erickt
- Fix typo in documentation of Value::F64 by @jnicholls
- Merge pull request #12 from pwoolcoc/num-no-default-features by @erickt
- Merge pull request #4 from michaelsproul/readme by @erickt
- Fix typo in README plugin example by @michaelsproul
- Merge pull request #6 from kamalmarhubi/patch-1 by @erickt
- Fix typo in Value enum documentation by @kamalmarhubi
- Merge pull request #8 from droundy/master by @erickt
- Merge pull request #5 from 3Hren/patch-1 by @erickt
- Merge pull request #3 from erickt/doc by @erickt
- Document everything by @erickt
- Auto merge of #2 - erickt:bugs, r=erickt by @homu
- Move the examples since they don't compile on stable rust yet by @erickt
- Fixing two compile errors by @erickt
- Switch from .to_string() to String::from by @erickt
- Re-encrypt token by @erickt
- Fix doc url by @erickt
- Document serde_json::value by @erickt
- More travis work by @erickt
- Cleanup travis by @erickt
- Fix some links by @erickt
- Initial travis configuration by @erickt
- Initial import of serde_json by @erickt

### Fixed

- Fix typo by @jimmycathy
- Indexmap minimal version with Map::shift_insert() by @cforycki
- Correct spelling error by @keienWang
- Fixed typos by @fritzrehde
- Fixup! chore: Remove no_btreemap_get_key_value and no_btreemap_remove_entry. by @osiewicz
- Fixup! Remove limb_width32 and limb_width64 features
- Fix parsing escape sequences after lone surrogates by @lucacasonato
- Fix wording by @lucacasonato
- Fix function signature
- Fix no_btreemap_retain name
- Test order
- Fix typos by @striezel
- Fix required minimum indexmap version by @nlordell
- Fix bug on error position by @yjh0502
- Deserialize_bytes(): fix bug: clear scratch before parsing next by @bennofs
- Fix build for preserve_order by @laktak
- Missing field error when deserializing from Value by @arcnmx
- Fix the skeptic tests on stable rust by @erickt
- Update to latest error types by @erickt
- Fix missing variant/field, rename error variants by @erickt
- Fixup! Fix broken things with latest serde by @jwilm
- Fixup! feat(serde-up) Support serde 0.7 by @jwilm
- Fixup! feat(serde-up) Support serde 0.7 by @jwilm
- Fixup! feat(serde-up) Support serde 0.7 by @jwilm
- Fix some warnings by @erickt
- Ignore #[derive(...)] example by @erickt
- Opt-out of default features of `num`
- Fix bug in documentation by @droundy
- Fix. by @3Hren

### Removed

- Remove *.sw[po] from gitignore by @dtolnay
- Remove **/*.rs.bk from project-specific gitignore by @dtolnay
- Remove repeat words by @haouvw
- Remove conditional on repr(transparent) by @dtolnay
- Remove unused Float::is_sign_negative trait method by @dtolnay
- Remove 'remember to update' reminder from Cargo.toml by @dtolnay
- Remove a few unnecessary lifetimes by @dimo414
- Remove limb_width32 and limb_width64 features by @osiewicz
- Removes `println!` from example by @chanced
- Removes `unwrap` from assertions in `Value::as_number` by @chanced
- Remove pre-NLL borrow checker workarounds by @dtolnay
- Remove extra variable by @overdrivenpotato
- Remove default package.readme metadata from Cargo.toml by @dtolnay
- Remove duplicate function
- Remove redundant codepath from parse_float by @dtolnay
- Remove inapplicable comment about validation in parse_mantissa by @dtolnay
- Remove confusing 'prim' abbreviation by @dtolnay
- Remove i32 num impls by @dtolnay
- Remove unused associated items of Mantissa and Float by @dtolnay
- Remove unused supertraits in lexical num library by @dtolnay
- Remove test of removed num types by @dtolnay
- Remove gratuitous inline from lexical test by @dtolnay
- Remove dead lexical test code involving radix by @dtolnay
- Remove unneeded methods from Hi64 by @dtolnay
- Remove ReverseView and Slice abstractions by @dtolnay
- Remove dead RSliceIndex trait methods from lexical by @dtolnay
- Remove extremely sketchy and unnecessary code from lexical by @dtolnay
- Remove iterator overgeneralization from lexical by @dtolnay
- Remove arrayvec-oriented abstractions by @dtolnay
- Remove use of inline(always) by @dtolnay
- Remove no_alloc codepath and arrayvec by @dtolnay
- Remove reference to mozilla irc by @dtolnay
- Remove AppVeyor configuration by @dtolnay
- Remove Travis configuration by @dtolnay
- Remove CI badge from Cargo.toml by @dtolnay
- Remove error variants that are never constructed by @dtolnay
- Remove ```edition2018 from doc tests after edition update by @dtolnay
- Remove Read and Bytes by @dtolnay
- Remove more of core io error by @dtolnay
- Remove unneeded Debug impl on io error by @dtolnay
- Remove WriteZero error kind by @dtolnay
- Remove source method in no_std mode by @dtolnay
- Remove unneeded itoa std feature by @dtolnay
- Remove unnecessary box trait object from io error repr by @dtolnay
- Remove unnecessary From<Error> for io::Error in no_std mode by @dtolnay
- Remove unused ErrorKind from io error repr by @dtolnay
- Remove unused Simple io error variant by @dtolnay
- Remove reliance on serde StdError for io error repr by @dtolnay
- Remove a layer of reexports from io facade by @dtolnay
- Remove deprecated description() method from Error by @dtolnay
- Remove unneeded lifetimes from pointer signatures by @dtolnay
- Remove try! macro from tests by @dtolnay
- Remove old instructions intended for compiletest by @dtolnay
- Remove old compiletest step from appveyor build by @dtolnay
- Remove serde_derive from doc tests by @dtolnay
- Remove references to macro_use by @dtolnay
- Remove lints that are no longer triggering by @dtolnay
- Remove deprecated -Dclippy by @dtolnay
- Remove PartialEq from RawValue by @dtolnay
- Remove pre-allocation in Deserializer construction by @dtolnay
- Remove irrelevant detail from Map::insert documentation by @dtolnay
- Remove std::i64 imports by @dtolnay
- Remove old work-around for rustc 1.8 by @lnicola
- Remove allocation in parsing escape sequences by @dtolnay
- Remove unnecessary copy in Value::from(Cow::Owned)
- Remove unnecessary 'static in consts by @dtolnay
- Remove unnecessary allow(needless_pass_by_value) by @sinkuu
- Remove commented code from PR by @dtolnay
- Remove unused extern crate core by @dtolnay
- Remove an unreachable branch by @dtolnay
- Remove deserialization from Iterator<Item = io::Result<u8>> by @dtolnay
- Remove unused ErrorImpl conversion by @dtolnay
- Remove extremely old error conversion by @dtolnay
- Remove ToJson trait by @dtolnay
- Remove misleading comments about serializing to vec by @dtolnay
- Remove redundant EOF check by @dtolnay
- Remove stray comment line by @dtolnay
- Remove dependency on indoc by @dtolnay
- Remove syntex option from test suite by @dtolnay
- Remove escape_str by @dtolnay
- Remove crufty Value methods by @dtolnay
- Remove redundant nesting in debug representation of numbers by @dtolnay
- Remove builder API in favor of json! macro by @dtolnay
- Remove PrettyFormatter method bodies that are identical to the trait by @dflemstr
- Remove Formatter.begin_number and Formatter.end_number by @dflemstr
- Remove trailing whitespace and commented test by @dtolnay
- Remove Value::lookup by @dtolnay
- Remove benchmarks in favor of json-benchmark repo by @dtolnay
- Remove proc_macro feature from readme by @dtolnay
- Remove the proc_macro feature gate by @dtolnay
- Remove rust 1.8.0 workaround by @dtolnay
- Remove unused imports in de.rs by @dtolnay
- Remove unused serde_derive from example by @dtolnay
- Remove doc-upload by @dtolnay
- Remove whitelisted clippy lint fixed in 0.0.80 by @dtolnay
- Remove impossible FromUtf8 error by @dtolnay
- Remove escape_bytes by @dtolnay
- Remove runtime checks when deserializing key-only variant by @dtolnay
- Remove commented line in Cargo.toml by @dtolnay
- Remove unnecessary type path by @arcnmx
- Remove the Sized bound on to_value<T>() by @tomjakubowski
- Remove unused error codes by @erickt

## First-time Contributors

* @jost-s made their first contribution in [#1](https://github.com/holochain/serde-json/pull/1)

* @dtolnay made their first contribution

* @jimmycathy made their first contribution

* @JonathanBrouwer made their first contribution

* @goffrie made their first contribution

* @tisonkun made their first contribution

* @bheylin made their first contribution

* @djmitche made their first contribution

* @Mrreadiness made their first contribution

* @CryZe made their first contribution

* @GREsau made their first contribution

* @purplesyringa made their first contribution

* @dpathakj made their first contribution

* @cforycki made their first contribution

* @joshka made their first contribution

* @haouvw made their first contribution

* @druide made their first contribution

* @swlynch99 made their first contribution

* @edwardycl made their first contribution

* @mleonhard made their first contribution

* @titaniumtraveler made their first contribution

* @keienWang made their first contribution

* @heiher made their first contribution

* @fritzrehde made their first contribution

* @dimo414 made their first contribution

* @osiewicz made their first contribution

* @chanced made their first contribution

* @ made their first contribution

* @zetanumbers made their first contribution

* @overdrivenpotato made their first contribution

* @LPGhatguy made their first contribution

* @ndmitchell made their first contribution

* @stepancheg made their first contribution

* @Lucretiel made their first contribution

* @kvinwang made their first contribution

* @kvnvelasco made their first contribution

* @lucacasonato made their first contribution

* @dzvon made their first contribution

* @cuviper made their first contribution

* @novedevo made their first contribution

* @EFanZh made their first contribution

* @jplatte made their first contribution

* @ruifengx made their first contribution

* @jayeshmann made their first contribution

* @striezel made their first contribution

* @ratijas made their first contribution

* @DavidKorczynski made their first contribution

* @Krout0n made their first contribution

* @SamuelQZQ made their first contribution

* @icewind1991 made their first contribution

* @Carreau made their first contribution

* @imp made their first contribution

* @matklad made their first contribution

* @tinou98 made their first contribution

* @rimutaka made their first contribution

* @atouchet made their first contribution

* @japaric made their first contribution

* @smarnach made their first contribution

* @sdleffler made their first contribution

* @Xanewok made their first contribution

* @jmfiaschi made their first contribution

* @adetaylor made their first contribution

* @Freax13 made their first contribution

* @erickt made their first contribution

* @nlordell made their first contribution

* @Nilix007 made their first contribution

* @andrisak made their first contribution

* @est31 made their first contribution

* @koushiro made their first contribution

* @yjh0502 made their first contribution

* @srijs made their first contribution

* @Enet4 made their first contribution

* @lnicola made their first contribution

* @Diggsey made their first contribution

* @alexreg made their first contribution

* @mtn made their first contribution

* @oli-obk made their first contribution

* @Eijebong made their first contribution

* @boxofrox made their first contribution

* @kraai made their first contribution

* @bouk made their first contribution

* @LunaBorowska made their first contribution

* @sinkuu made their first contribution

* @elpiel made their first contribution

* @fmoor made their first contribution

* @foriequal0 made their first contribution

* @GyrosOfWar made their first contribution

* @Rufflewind made their first contribution

* @killercup made their first contribution

* @nox made their first contribution

* @cspiegel-cypherpath made their first contribution

* @bennofs made their first contribution

* @frewsxcv made their first contribution

* @Kroisse made their first contribution

* @kchmck made their first contribution

* @tshepang made their first contribution

* @bjorn3 made their first contribution

* @CryptArchy made their first contribution

* @mephinet made their first contribution

* @Arzte made their first contribution

* @traviskaufman made their first contribution

* @withoutboats made their first contribution

* @rphmeier made their first contribution

* @dflemstr made their first contribution

* @laktak made their first contribution

* @sfackler made their first contribution

* @homu made their first contribution

* @raphlinus made their first contribution

* @Ms2ger made their first contribution

* @arcnmx made their first contribution

* @s-panferov made their first contribution

* @pyfisch made their first contribution

* @jwilm made their first contribution

* @nixpulvis made their first contribution

* @little-arhat made their first contribution

* @cmbrandenburg made their first contribution

* @tomjakubowski made their first contribution

* @vegai made their first contribution

* @zr40 made their first contribution

* @jnicholls made their first contribution

* @droundy made their first contribution

* @kamalmarhubi made their first contribution

* @3Hren made their first contribution

* @michaelsproul made their first contribution


<!-- generated by git-cliff -->
