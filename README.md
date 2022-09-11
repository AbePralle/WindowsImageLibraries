# Windows Media Libraries
This repo contains Visual Studio 2019 projects (solutions) to build static JPEG, PNG, and ZLIB libraries.

# Current Versions
Library    | Version  | Project Path                   | Product
-----------|----------|--------------------------------|-------------
JPEG       | 9d       | Projects/jpeg                  | Products/jpeg
PNG        | 1.6.37   | Projects/png/projects/vstudio  | Products/lpng
ZLIB       | 1.2.11   | (Build as part of PNG project) | Products/lpng

# Notes

## General
1. The necessary headers for various projects have already been copied to `Products/`.
2. The binary `.lib` products are not part of this repository but are included in Releases.

## JPEG
1. Build `Release` for `Win32`
2. Copy `jconfig.vc` to `jconfig.h`.

## PNG
Download latest release from [https://sourceforge.net/projects/libpng/files/](https://sourceforge.net/projects/libpng/files/).
Replace `Projects/png` with downloaded version.
Open `Projects/png/projects/vstudio/vstudio.sln` in Visual Studio 2022+.
Change the Solution Configuration to `Release`.
Select `Build > Build zlib` from the menu.
1. Build `Release Library` for `Win32`
2. For `libpng` and `zlib` projects, modified `Properties > C/C++ > Advanced > Disable Specific Warnings` to include `5045` to suppress Spectre exploit messages (Spectre fix mode is not enabled).
Build > Build zlib


## ZLib
Download latest release from https://www.zlib.net .
Delete old `Projects/zlib` and rename downloaded `zlib-<version>` to `Projects/zlib`.
1. `zlib.lib` is part of the PNG/`lpng` product folder.
2. No headers for ZLib are included.

