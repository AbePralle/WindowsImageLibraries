# Windows Media Libraries
This repo contains Visual Studio 2019 projects (solutions) to build static JPEG, PNG, and ZLIB libraries.

# Current Versions
Library    | Version  | Folder
-----------|----------|-------------
JPEG       | 9d       | jpeg
PNG        | 1.6.37   | lpng
ZLIB       | 1.2.11   | lpng

# Notes

## General
1. The necessary headers for various projects have already been copied to `Products/`.
2. The binary `.lib` products are not part of this repository but are included in Releases.

## JPEG
1. Build `Release` for `Win32`
2. Copied `jconfig.vc` to `jconfig.h`.

## PNG
1. Build `Release Library` for `Win32`
2. For `libpng` and `zlib` projects, modified `Properties > C/C++ > Advanced > Disable Specific Warnings` to include `5045` to suppress Spectre exploit messages (Spectre fix mode is not enabled).

## ZLib
1. `zlib.lib` is part of the PNG/`lpng` product folder.
2. No headers for ZLib are included.

