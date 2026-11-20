# Aravis camera runtime

Singularity Vision uses the Aravis Project's camera control and acquisition library under the GNU Lesser General Public License version 2.1 or later. Copyright © Emmanuel Pacaud and the Aravis contributors. The library loads dynamically and an interface-compatible replacement may be used. [Upstream project](https://github.com/AravisProject/aravis) · [License text](Aravis-LGPL-2.1.txt)

On Windows, Setup downloads the pinned MSYS2 Aravis 0.8.33-4 build and verifies each downloaded package against a SHA-256 value embedded in the installer. It installs the runtime in the private Python's `Aravis` directory. Notices from the downloaded dependency archives accompany the DLLs under `Notices`. The MSYS2 source packages include the upstream sources and packaging changes. [Windows Aravis package and matching source archive](https://packages.msys2.org/packages/mingw-w64-ucrt-x86_64-aravis) · [MSYS2 source archives](https://repo.msys2.org/mingw/sources/)

On Linux, the distribution manages the Aravis 0.8 shared library, its dependencies, notices and corresponding source. The installed package version identifies the source revision.

For a redistributed offline binary bundle, supply the complete corresponding source of the exact packages in that bundle, including patches and build scripts, on the same media or alongside the binary download. Preserve the license texts and notices for each component.

Setup uses the upstream Zstandard 1.5.7 Windows command-line program temporarily to unpack the verified packages. Its release ZIP stays in the installer cache. [Zstandard release](https://github.com/meta/zstd/releases/tag/v1.5.7) and [BSD license](Zstandard-BSD.txt).
