# headr
Command-Line Rust page 82<br />
error[E0631]: type mismatch in function arguments<br />
   --> src/lib.rs:47:14<br />
    |<br />
47  |         .map(parse_positive_int)<br />
    |          --- ^^^^^^^^^^^^^^^^^^ expected signature of `fn(clap::Values<'_>) -> _`<br />
    |          |<br />
    |          required by a bound introduced by this call<br />
...<br />
70  | fn parse_positive_int(val: &str) -> MyResult<usize> {<br />
    | --------------------------------------------------- found signature of `for<'r> fn(&'r str) -> _`<br />
    |<br />
note: required by a bound in `Option::<T>::map`<br />
   --> /home/kenfang/.rustup/toolchains/stable-x86_64-unknown-linux-gnu/lib/rustlib/src/rust/library/core/src/option.rs:879:12<br />
    |<br />
879 |         F: ~const FnOnce(T) -> U,<br />
    |            ^^^^^^^^^^^^^^^^^^^^^ required by this bound in `Option::<T>::map`<br />
