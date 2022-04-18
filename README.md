# headr
Command-Line Rust page 82
error[E0631]: type mismatch in function arguments
   --> src/lib.rs:47:14
    |
47  |         .map(parse_positive_int)
    |          --- ^^^^^^^^^^^^^^^^^^ expected signature of `fn(clap::Values<'_>) -> _`
    |          |
    |          required by a bound introduced by this call
...
70  | fn parse_positive_int(val: &str) -> MyResult<usize> {
    | --------------------------------------------------- found signature of `for<'r> fn(&'r str) -> _`
    |
note: required by a bound in `Option::<T>::map`
   --> /home/kenfang/.rustup/toolchains/stable-x86_64-unknown-linux-gnu/lib/rustlib/src/rust/library/core/src/option.rs:879:12
    |
879 |         F: ~const FnOnce(T) -> U,
    |            ^^^^^^^^^^^^^^^^^^^^^ required by this bound in `Option::<T>::map`
