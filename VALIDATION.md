# Validation

Linux x86_64, Rust 1.95.0. The fork remains based on zbus 5.18.0.

The only production change is the Linux CMSG_CLOEXEC receive flag, with a
modification notice. Upstream crate APIs and non-Linux receive behavior remain
unchanged. Both the default and Tokio library configurations build.

```sh
cargo +1.95.0 check --locked -p zbus
cargo +1.95.0 check --locked -p zbus --no-default-features --features tokio,blocking-api
```

Upstream ancestry, license files, and both fork commit signatures are verified.
