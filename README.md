# rust-aya-dev

## Prerequisites

1. Install bpf-linker: `cargo install bpf-linker`

## Build eBPF

```bash
cargo xtask build-ebpf
```

To perform a release build you can use the `--release` flag.
You may also change the target architecture with the `--target` flag.

## Build Userspace

```bash
cargo build
```

## Run

```bash
RUST_LOG=info cargo xtask run
```

<details>

<summary>log</summary>

```bash
user@rust:~/rust-aya-dev$ RUST_LOG=info cargo xtask run
warning: virtual workspace defaulting to `resolver = "1"` despite one or more workspace members being on edition 2021 which implies `resolver = "2"`
note: to keep the current resolver, specify `workspace.resolver = "1"` in the workspace root's manifest
note: to use the edition 2021 resolver, specify `workspace.resolver = "2"` in the workspace root's manifest
note: for more details see https://doc.rust-lang.org/cargo/reference/resolver.html#resolver-versions
    Finished dev [unoptimized + debuginfo] target(s) in 0.07s
     Running `target/debug/xtask run`
    Finished dev [optimized] target(s) in 0.58s
warning: virtual workspace defaulting to `resolver = "1"` despite one or more workspace members being on edition 2021 which implies `resolver = "2"`
note: to keep the current resolver, specify `workspace.resolver = "1"` in the workspace root's manifest
note: to use the edition 2021 resolver, specify `workspace.resolver = "2"` in the workspace root's manifest
note: for more details see https://doc.rust-lang.org/cargo/reference/resolver.html#resolver-versions
    Finished dev [unoptimized + debuginfo] target(s) in 0.12s
[2024-01-11T00:38:03Z INFO  rust_aya_dev] Waiting for Ctrl-C...
[2024-01-11T00:38:03Z INFO  rust_aya_dev] received a packet
[2024-01-11T00:38:03Z INFO  rust_aya_dev] received a packet
[2024-01-11T00:38:03Z INFO  rust_aya_dev] received a packet
[2024-01-11T00:38:03Z INFO  rust_aya_dev] received a packet
```

</details>
