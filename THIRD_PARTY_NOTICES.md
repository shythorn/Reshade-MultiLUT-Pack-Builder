# Third-Party Notices

MultiLUT Pack Builder generates ReShade shader code that follows the classic MultiLUT workflow.

## OtisFX MultiLUT

**Project:** OtisFX  
**Author:** Frans Bouma (Otis / Infuse Project)  
**Source:** https://github.com/FransBouma/OtisFX  
**Relevant file:** https://github.com/FransBouma/OtisFX/blob/master/Shaders/MultiLUT.fx

`MultiLUT.fx` identifies itself as a Multi-LUT shader by Otis / Infuse Project and states that it is based on Marty McFly's LUT shader 1.0 for ReShade 3.0. The OtisFX repository's license applies the MIT License to its shaders except PandaFX.

The generated `.fx` files preserve attribution to:

- Frans Bouma / Otis — OtisFX MultiLUT
- Marty McFly / Pascal Gilcher — LUT shader lineage (2008–2016)

### MIT License notice for OtisFX

Copyright (c) 2018 Frans Bouma

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

## ReShade

**Project:** ReShade / ReShade shaders  
**Author / maintainer:** crosire and contributors  
**Sources:**
- https://github.com/crosire/reshade
- https://github.com/crosire/reshade-shaders

MultiLUT Pack Builder does not bundle ReShade or `ReShade.fxh`. Generated shaders reference `ReShade.fxh` as an external include expected to exist in the user's ReShade shader search path.

The current `ReShade.fxh` in `crosire/reshade-shaders` carries an SPDX `CC0-1.0` header. ReShade itself is distributed under the BSD 3-Clause License.

## Scope

These notices cover third-party lineage/dependencies known to be relevant to the current release. They are not legal advice. If the generated shader implementation changes substantially, re-check the applicable notices before publishing a new release.
