# lox-models

Pinned copies of the on-device models the Lox app downloads. Each file is an
unmodified copy of an upstream release, published under a name that carries
its SHA-256, so its bytes never change under the app's pin. The app checks
that hash after every download.

## kokoro-multi-lang-v1_0

Release [`kokoro-multi-lang-v1_0`](https://github.com/lokitech/lox-models/releases/tag/kokoro-multi-lang-v1_0):

| File | Size | SHA-256 |
| --- | --- | --- |
| `kokoro-multi-lang-v1_0-c5f7e2d2.tar.bz2` | 349,906,910 bytes | `c5f7e2d2caf082bc1d20fb70334a61d99d20b484500aad32e7cf84c128ea3298` |

- **Source:** the sherpa-onnx `tts-models` release asset
  [`kokoro-multi-lang-v1_0.tar.bz2`](https://github.com/k2-fsa/sherpa-onnx/releases/download/tts-models/kokoro-multi-lang-v1_0.tar.bz2),
  as uploaded on 2026-09-08 (GitHub asset digest
  `sha256:c5f7e2d2…3298`). The bytes are identical.
- **What it is:** the [Kokoro-82M](https://huggingface.co/hexgrad/Kokoro-82M)
  v1.0 text-to-speech model, converted to ONNX by
  [sherpa-onnx](https://github.com/k2-fsa/sherpa-onnx), with its voices,
  tokens, lexicons, espeak-ng data and jieba dictionaries.

## Licenses

The archive bundles parts under different licenses:

| Part | License | Source |
| --- | --- | --- |
| Kokoro-82M weights and voices (`model.onnx`, `voices.bin`) | Apache-2.0 ([LICENSE-Apache-2.0](LICENSE-Apache-2.0), also inside the archive) | <https://huggingface.co/hexgrad/Kokoro-82M> |
| sherpa-onnx conversion and packaging (`tokens.txt`, lexicons, `.fst` files) | Apache-2.0 ([LICENSE-Apache-2.0](LICENSE-Apache-2.0)) | <https://github.com/k2-fsa/sherpa-onnx> |
| `espeak-ng-data/` | GPL-3.0-or-later ([LICENSE-GPL-3.0](LICENSE-GPL-3.0)) | <https://github.com/espeak-ng/espeak-ng> |
| `dict/` (jieba dictionaries) | MIT ([LICENSE-MIT-cppjieba](LICENSE-MIT-cppjieba)) | <https://github.com/yanyiwu/cppjieba> |

`espeak-ng-data/` is the compiled data of espeak-ng. Its corresponding source
is the espeak-ng repository linked above (`espeak-ng-data/` is built from its
`dictsource/` and `phsource/` directories).
