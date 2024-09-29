# socket2-plus

[![Build](https://github.com/keepsimple1/socket2-plus/actions/workflows/build.yml/badge.svg)](https://github.com/keepsimple1/socket2-plus/actions)
[![Cargo](https://img.shields.io/crates/v/socket2-plus.svg)](https://crates.io/crates/socket2-plus)

This library is a superset of [`socket2`](https://crates.io/crates/socket2) and it aims to provide some additional APIs currently missing from `socket2`. This library can be used as a drop-in replacement for `socket2`.

The following APIs are added:

- `recv_from_initialized` to support `recv_from` with a fully initialized buffer.
- `recvmsg_initialized` to support `recvmsg` and `MsgHdrInit` with initialized buffers.
- Support Windows for `recvmsg_initialized`.
- `set_pktinfo_v4` and `set_recv_pktinfo_v6` to support IP_PKTINFO and IPV6_PKTINFO socket options.

See [documentation](https://docs.rs/socket2-plus) for more details.

See test cases [`send_to_recv_from_init`](tests/socket.rs#L770) and [`sent_to_recvmsg_init_v4`](tests/socket.rs#L856).

## Target platforms

All new APIs are built and tested on `macOS`, `Linux` and `Windows`. For other platforms, the new APIs are only partially or not available.

## Forked from socket2

This version is forked from `socket2` v0.5.7. We plan to rebase to the latest `socket2` stable release regularly.

## Minimum Supported Rust Version (MSRV)

`socket2-plus` uses 1.63.0 as MSRV.

## License

This project is licensed under either of

 * Apache License, Version 2.0, ([LICENSE-APACHE](LICENSE-APACHE) or
   https://www.apache.org/licenses/LICENSE-2.0)
 * MIT license ([LICENSE-MIT](LICENSE-MIT) or
   https://opensource.org/licenses/MIT)

at your option.

## Contribution

Unless you explicitly state otherwise, any contribution intentionally submitted
for inclusion in this project by you, as defined in the Apache-2.0 license,
shall be dual licensed as above, without any additional terms or conditions.
