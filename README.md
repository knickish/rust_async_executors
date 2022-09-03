Non-exhaustive list of async executors available for rust. PRs welcome to add missing ones, I had a hard time finding them on crates.io.

| ecosystem | executor name and version | crates.io downloads  | minimum deps   | async io  | no_std | lib size |
|---|---|---|---|---|---|---|
| [tokio](https://crates.io/crates/tokio) | tokio = "1.19.2" | 57.5M | 2 |  yes | no | 581kB |
| [async-std](https://crates.io/crates/async-std) | async-std = "1.12.0" | 7.8M | 1  |  yes | yes | 215kB |
| [smol](https://crates.io/crates/smol) | async-executor = "1.4.1"  | 1.5M | 14 | yes | yes | 15.5kB |
| [yaar](https://crates.io/crates/yaar) | yaar = "0.1.1"  | 941  | 1 | yes | yes | 10.1kB |
| [uasync](https://crates.io/crates/uasync) | uasync = "0.1.1"  | 175  | 1 | no | no | 12.4kB |
| [whorl](https://github.com/mgattozzi/whorl) | N/A | N/A  | 1 | no | no | N/A |
| [beul](https://crates.io/crates/beul) | beul = "0.1.0"  | 16  | 1 | no | no | 4.2kB |

used a bare cargo crate importing only each executor for the following: 
- out-of-tree deps command: `cargo tree -e normal --prefix none | sort | uniq | grep -v "rust_async_executors" | grep -v "(*)" | wc -l`