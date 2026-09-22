# MultiLUT Pack Builder

A browser tool that converts `.cube` and common Autodesk/Lustre `.3dl` LUTs into ReShade-compatible MultiLUT packs.

**[Open MultiLUT Pack Builder](https://shythorn.github.io/Reshade-MultiLUT-Pack-Builder/)** or download .html from **[Releases Page](https://github.com/shythorn/Reshade-MultiLUT-Pack-Builder/releases)** and open in browser.

Add your LUTs, convert, and download a ready-to-install ZIP.

## Features

- Convert `.cube` and `.3dl` LUTs into ReShade MultiLUT packs
- Add individual LUTs or a whole folder
- Optional Pre-LUT / input transform
- Split large LUT collections into smaller shader groups
- Sort LUTs by filename or the order they were added
- Download everything as one ZIP

## How to use

1. Open the tool from the link above.
2. Add your LUT files or folder.
3. Set a pack name and adjust any optional settings you need.
4. Click **Convert & Download ZIP**.
5. Copy the generated `Shaders` and `Textures` files into the matching ReShade folders.

## Chunks

A chunk is one generated MultiLUT shader. Each shader can contain up to **256 LUTs**.

Large packs can be split into smaller chunks so they are easier to browse in ReShade. For example, 600 LUTs with a chunk size of 256 will create three shaders: 256 + 256 + 88 LUTs.

Leave it at 256 unless you prefer smaller groups.

## Pre-LUT / input transform

Leave this as **None** for normal use.

Use a Pre-LUT when all LUTs in the pack expect the same conversion first — for example, applying a **Rec.709 → Log** conversion LUT before LUTs designed for Log color inputs.

The transform is baked into the generated pack automatically so that no other LUT shader is required in the fx stack.

Currently, Pre-LUT can only be applied to the whole pack and is not customizable for each individual LUT.

### `.3dl` data order

Most Autodesk/Lustre `.3dl` files use **Blue fastest**, which is the default.

If a `.3dl` LUT produces incorrect or strangely shifted colors, try switching it to **Red fastest** instead. This setting only affects `.3dl` files; `.cube` files do not need it.

## Credits

The generated shader follows the classic MultiLUT work by **Frans Bouma / OtisFX**, based on earlier LUT shader work by **Marty McFly / Pascal Gilcher**.

See [`THIRD_PARTY_NOTICES.md`](THIRD_PARTY_NOTICES.md) for attribution and license details.

## License

MultiLUT Pack Builder is released under the [MIT License](LICENSE).

<details>
<summary>Development</summary>

The tool is contained in `index.html` and has no build step.

For a quick self-test, open the deployed page with `?selftest=1` appended to the URL.

</details>
