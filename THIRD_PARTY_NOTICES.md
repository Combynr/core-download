# Third-Party Notices

combynr:core is proprietary freeware (see `LICENSE`). It includes and uses the
third-party software below, each under its own licence. The installed app carries the
full licence texts in its `licenses` folder.

## Included in the installed app

| Component | Licence | Source |
|---|---|---|
| llama.cpp (`llama-server` and its libraries) | MIT | https://github.com/ggml-org/llama.cpp |
| whisper.cpp (`whisper-cli`, Windows only) | MIT | https://github.com/ggml-org/whisper.cpp |
| CPython 3.12 (the interpreter that runs sandboxed scripts, and the app's own runtime), with the libraries it bundles (OpenSSL, SQLite, libffi, zlib, bzip2, xz and others) | PSF License 2.0 and the bundled libraries' own licences | https://www.python.org and https://github.com/astral-sh/python-build-standalone |
| Nuitka runtime (the compiler support code linked into the app) | Apache 2.0 | https://nuitka.net |
| The Python packages listed below | as listed | as listed |

## Downloaded on request

| Component | Licence | Source |
|---|---|---|
| ggml-base.en speech model | MIT (originally OpenAI Whisper) | whisper.cpp model repository on Hugging Face: https://huggingface.co/ggerganov/whisper.cpp |
| llama.cpp CUDA build and NVIDIA CUDA runtime (Windows, optional) | MIT; NVIDIA's licence terms for the CUDA runtime | https://github.com/ggml-org/llama.cpp |

## Code adapted into the app

The components in `web/components/ui/` (and the `cn` helper in `web/lib/utils.ts`) are
derived from shadcn/ui (https://github.com/shadcn-ui/ui), used under the MIT License:

```
MIT License

Copyright (c) 2023 shadcn

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```

## Python packages

Packages installed in the API virtual environment, excluding pip and the project itself.

| Package | Version | Licence |
|---|---|---|
| annotated-doc | 0.0.7 | MIT |
| annotated-types | 0.8.0 | MIT |
| anyio | 4.16.0 | MIT |
| attrs | 26.1.0 | MIT |
| certifi | 2026.11.20 | MPL-2.0 |
| cffi | 2.1.1 | MIT-0 |
| click | 8.5.1 | BSD-3-Clause |
| cryptography | 50.0.2 | Apache-2.0 OR BSD-3-Clause |
| fastapi | 0.165.0 | MIT |
| h11 | 0.16.0 | MIT |
| httpcore | 1.0.9 | BSD-3-Clause |
| httpcore2 | 2.16.2 | BSD-3-Clause |
| httpx | 0.28.1 | BSD-3-Clause |
| httpx2 | 2.16.2 | BSD-3-Clause |
| idna | 3.20 | BSD-3-Clause |
| iniconfig (development only) | 2.3.1 | MIT |
| jsonschema | 4.26.0 | MIT |
| jsonschema-specifications | 2025.9.1 | MIT |
| mcp | 2.3.0 | MIT |
| mcp-auditor | 1.0.2 | MIT |
| mcp-types | 2.3.0 | MIT |
| opentelemetry-api | 1.45.2 | Apache-2.0 |
| packaging (development only) | 26.4 | Apache-2.0 OR BSD-2-Clause |
| pluggy (development only) | 1.7.0 | MIT |
| pycparser | 3.12 | BSD-3-Clause |
| pydantic | 2.14.4 | MIT |
| pydantic_core | 2.50.5 | MIT |
| Pygments (development only) | 2.21.0 | BSD-2-Clause |
| PyJWT | 2.15.1 | MIT |
| pytest (development only) | 9.2.0 | MIT |
| python-multipart | 0.0.34 | Apache-2.0 |
| referencing | 0.37.0 | MIT |
| rpds-py | 2026.9.1 | MIT |
| sse-starlette | 3.7.1 | BSD-3-Clause |
| starlette | 1.10.0 | BSD-3-Clause |
| truststore | 0.10.5 | MIT |
| typing-inspection | 0.4.5 | MIT |
| typing_extensions | 4.16.0 | PSF-2.0 |
| uvicorn | 0.54.0 | BSD-3-Clause |

## JavaScript packages

Production dependency tree of `web/` (`npm ls --omit=dev --all`). Licences are read from each package's `package.json` in `web/node_modules`.
Entries marked "see package" were not installed in `web/node_modules` on the build machine (platform-specific or peer-only packages), so their licence was not read.

| Package | Version | Licence |
|---|---|---|
| @emnapi/runtime | 1.11.3 | MIT |
| @img/colour | 1.1.0 | MIT |
| @img/sharp-darwin-arm64 | not installed | see package |
| @img/sharp-darwin-x64 | not installed | see package |
| @img/sharp-freebsd-wasm32 | not installed | see package |
| @img/sharp-libvips-darwin-arm64 | not installed | see package |
| @img/sharp-libvips-darwin-x64 | not installed | see package |
| @img/sharp-libvips-linux-arm | not installed | see package |
| @img/sharp-libvips-linux-arm64 | not installed | see package |
| @img/sharp-libvips-linux-ppc64 | not installed | see package |
| @img/sharp-libvips-linux-riscv64 | not installed | see package |
| @img/sharp-libvips-linux-s390x | not installed | see package |
| @img/sharp-libvips-linux-x64 | 1.3.4 | LGPL-3.0-or-later |
| @img/sharp-libvips-linuxmusl-arm64 | not installed | see package |
| @img/sharp-libvips-linuxmusl-x64 | not installed | see package |
| @img/sharp-linux-arm | not installed | see package |
| @img/sharp-linux-arm64 | not installed | see package |
| @img/sharp-linux-ppc64 | not installed | see package |
| @img/sharp-linux-riscv64 | not installed | see package |
| @img/sharp-linux-s390x | not installed | see package |
| @img/sharp-linux-x64 | 0.35.5 | Apache-2.0 |
| @img/sharp-linuxmusl-arm64 | not installed | see package |
| @img/sharp-linuxmusl-x64 | not installed | see package |
| @img/sharp-wasm32 | 0.35.5 | Apache-2.0 AND LGPL-3.0-or-later AND MIT |
| @img/sharp-webcontainers-wasm32 | not installed | see package |
| @img/sharp-win32-arm64 | not installed | see package |
| @img/sharp-win32-ia32 | not installed | see package |
| @img/sharp-win32-x64 | not installed | see package |
| @next/env | 16.4.6 | MIT |
| @next/swc-darwin-arm64 | not installed | see package |
| @next/swc-darwin-x64 | not installed | see package |
| @next/swc-linux-arm64-gnu | not installed | see package |
| @next/swc-linux-arm64-musl | not installed | see package |
| @next/swc-linux-x64-gnu | 16.4.6 | MIT |
| @next/swc-linux-x64-musl | not installed | see package |
| @next/swc-win32-arm64-msvc | not installed | see package |
| @next/swc-win32-x64-msvc | not installed | see package |
| @opentelemetry/api | not installed | see package |
| @playwright/test | not installed | see package |
| @radix-ui/number | 1.1.3 | MIT |
| @radix-ui/primitive | 1.2.0 | MIT |
| @radix-ui/react-compose-refs | 1.1.5 | MIT |
| @radix-ui/react-context | 1.3.0 | MIT |
| @radix-ui/react-direction | 1.2.0 | MIT |
| @radix-ui/react-presence | 1.1.11 | MIT |
| @radix-ui/react-primitive | 2.2.0 | MIT |
| @radix-ui/react-scroll-area | 1.4.0 | MIT |
| @radix-ui/react-slot | 1.5.0 | MIT |
| @radix-ui/react-switch | 1.4.1 | MIT |
| @radix-ui/react-use-callback-ref | 1.1.5 | MIT |
| @radix-ui/react-use-controllable-state | 1.3.0 | MIT |
| @radix-ui/react-use-effect-event | 0.0.5 | MIT |
| @radix-ui/react-use-layout-effect | 1.1.4 | MIT |
| @radix-ui/react-use-size | 1.1.5 | MIT |
| @swc/helpers | 0.5.23 | Apache-2.0 |
| @types/react | 19.3.0 | MIT |
| @types/react-dom | 19.3.0 | MIT |
| @types/trusted-types | 2.0.7 | MIT |
| babel-plugin-react-compiler | not installed | see package |
| baseline-browser-mapping | 2.11.39 | Apache-2.0 |
| caniuse-lite | 1.0.30001827 | CC-BY-4.0 |
| class-variance-authority | 0.7.1 | Apache-2.0 |
| client-only | 0.0.1 | MIT |
| clsx | 2.1.1 | MIT |
| csstype | 3.2.4 | MIT |
| detect-libc | 2.1.2 | Apache-2.0 |
| dompurify | 3.5.0 | MPL-2.0 OR Apache-2.0 |
| lucide-react | 1.78.0 | ISC |
| nanoid | 3.3.20 | MIT |
| next | 16.4.6 | MIT |
| next-themes | 0.4.6 | MIT |
| picocolors | 1.1.1 | ISC |
| postcss | 8.5.33 | MIT |
| react | 19.3.1 | MIT |
| react-dom | 19.3.1 | MIT |
| sass | not installed | see package |
| scheduler | 0.28.0 | MIT |
| semver | 6.3.2 | ISC |
| sharp | 0.35.5 | Apache-2.0 |
| source-map-js | 1.2.4 | BSD-3-Clause |
| styled-jsx | 5.1.6 | MIT |
| tailwind-merge | 2.6.2 | MIT |
| tslib | 2.9.1 | 0BSD |

Direct development dependencies (`web/package.json`): @types/node, @types/react, @types/react-dom, autoprefixer, eslint, eslint-config-next, postcss, tailwindcss, tailwindcss-animate, typescript.
