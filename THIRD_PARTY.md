# 第三方组件

腕读自己的代码是 MIT 许可。下面是用到的第三方组件。

## 插件（Rust）

| 组件 | 许可 | 用途 |
|---|---|---|
| [waki](https://github.com/wacker-dev/waki) 0.5.1 | Apache-2.0 | 联网（`wasi:http`）。**插件里用的是修改过的版本**：新增 `src/limits.rs`（用单调时钟和 poll 给等响应、读正文加硬性的时间和大小上限），并改了 `src/request.rs`、`src/body.rs`、`src/lib.rs` 里对应的几处（都有「腕读改的」注释）。其余未动 |
| [astrobox-ng-wit](https://crates.io/crates/astrobox-ng-wit) 0.3.1 | MIT，© 2026 AstralSight Studios | AstroBox 插件接口 |
| [image](https://crates.io/crates/image) 0.25 | MIT OR Apache-2.0 | 解码、缩小、编码图片（只开 jpeg、png、webp） |
| [encoding_rs](https://crates.io/crates/encoding_rs) 0.8 | (Apache-2.0 OR MIT) AND BSD-3-Clause | GBK、Big5 等编码转 UTF-8 |
| [serde_json](https://crates.io/crates/serde_json) 1 | MIT OR Apache-2.0 | JSON |
| [tracing](https://crates.io/crates/tracing) 0.1 | MIT | 日志 |

Apache-2.0 全文见 [licenses/Apache-2.0.txt](licenses/Apache-2.0.txt)，其余完整的许可文本见各自的仓库。

## 数据

| 数据 | 许可 | 用途 |
|---|---|---|
| [OpenCC](https://github.com/BYVoid/OpenCC) 的 `TSCharacters.txt` | Apache-2.0 | 繁体转简体的单字对照表。插件里的繁简对照表由它生成（一对多的、原字本身也是简体的字保持原样，其余取第一个）；只用了字表，没有用词组表 |

## 参考

插件连手环、打开手环应用的做法，以及日志的写法，参考了 [KlikBand](https://github.com/ashafizullah/klikband)（MIT）。没有复制它的源文件。

## 推荐订阅源

插件里「发现」页的 67 个订阅源只是公开的地址，内容版权归各自网站所有，腕读不存储、不转发，只在用户同步时从用户的设备上抓取。
