﻿---
Description: 'Loads a surface from a resource.'
ms.assetid: '16d49f61-8c84-4e15-aacc-1d26099e65e0'
title: D3DXLoadSurfaceFromResource function
---

# D3DXLoadSurfaceFromResource function

Loads a surface from a resource.

## Syntax


```C++
HRESULT D3DXLoadSurfaceFromResource(
  _In_          LPDIRECT3DSURFACE9 pDestSurface,
  _In_    const PALETTEENTRY       *pDestPalette,
  _In_    const RECT               *pDestRect,
  _In_          HMODULE            hSrcModule,
  _In_          LPCTSTR            pSrcResource,
  _In_    const RECT               *pSrcRect,
  _In_          DWORD              Filter,
  _In_          D3DCOLOR           ColorKey,
  _Inout_       D3DXIMAGE_INFO     *pSrcInfo
);
```



## Parameters

<dl> <dt>

*pDestSurface* \[in\]
</dt> <dd>

Type: **[**LPDIRECT3DSURFACE9**](idirect3dsurface9.md)**

Pointer to an [**IDirect3DSurface9**](idirect3dsurface9.md) interface. Specifies the destination surface, which receives the image.

</dd> <dt>

*pDestPalette* \[in\]
</dt> <dd>

Type: **const [**PALETTEENTRY**](paletteentry.md)\***

Pointer to a [**PALETTEENTRY**](paletteentry.md) structure, the destination palette of 256 colors or **NULL**.

</dd> <dt>

*pDestRect* \[in\]
</dt> <dd>

Type: **const [**RECT**](gdi.rect)\***

Pointer to a [**RECT**](gdi.rect) structure. Specifies the destination rectangle. Set this parameter to **NULL** to specify the entire surface.

</dd> <dt>

*hSrcModule* \[in\]
</dt> <dd>

Type: **[**HMODULE**](winprog.windows_data_types)**

Handle to the module where the resource is located, or **NULL** for module associated with the image the operating system used to create the current process.

</dd> <dt>

*pSrcResource* \[in\]
</dt> <dd>

Type: **[**LPCTSTR**](winprog.windows_data_types)**

Pointer to a string that specifies the resource name. If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR. Otherwise, the string data type resolves to LPCSTR. See Remarks.

</dd> <dt>

*pSrcRect* \[in\]
</dt> <dd>

Type: **const [**RECT**](gdi.rect)\***

Pointer to a [**RECT**](gdi.rect) structure. Specifies the source rectangle. Set this parameter to **NULL** to specify the entire image.

</dd> <dt>

*Filter* \[in\]
</dt> <dd>

Type: **[**DWORD**](winprog.windows_data_types)**

Combination of one or more [D3DX\_FILTER](d3dx-filter.md) controlling how the image is filtered. Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER.

</dd> <dt>

*ColorKey* \[in\]
</dt> <dd>

Type: **[**D3DCOLOR**](d3dcolor.md)**

[**D3DCOLOR**](d3dcolor.md) value to replace with transparent black, or 0 to disable the colorkey. This is always a 32-bit ARGB color, independent of the source image format. Alpha is significant and should usually be set to FF for opaque color keys Thus, for opaque black, the value would be equal to 0xFF000000.

</dd> <dt>

*pSrcInfo* \[in, out\]
</dt> <dd>

Type: **[**D3DXIMAGE\_INFO**](d3dximage-info.md)\***

Pointer to a [**D3DXIMAGE\_INFO**](d3dximage-info.md) structure to be filled with a description of the data in the source image file, or **NULL**.

</dd> </dl>

## Return value

Type: **[**HRESULT**](455d07e9-52c3-4efb-a9dc-2955cbfd38cc)**

If the function succeeds, the return value is D3D\_OK. If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.

## Remarks

The compiler setting also determines the function version. If Unicode is defined, the function call resolves to D3DXLoadSurfaceFromResourceW. Otherwise, the function call resolves to D3DXLoadSurfaceFromResourceA because ANSI strings are being used.

The resource being loaded must be of type RT\_BITMAP or RT\_RCDATA. Resource type RT\_RCDATA is used to load formats other than bitmaps (such as .tga, .jpg, and .dds).

This function handles conversion to and from compressed texture formats.

Writing to a non-level-zero surface will not cause the dirty rectangle to be updated. If [**D3DXLoadSurfaceFromFile**](d3dxloadsurfacefromfile.md) is called and the surface was not already dirty (this is unlikely under normal usage scenarios), the application needs to explicitly call [**AddDirtyRect**](idirect3dtexture9--adddirtyrect.md) on the surface.

## Requirements



|                    |                                                                                       |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9tex.h</dt> </dl> |
| Library<br/> | <dl> <dt>D3dx9.lib</dt> </dl>  |



## See also

<dl> <dt>

[Texture Functions in D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 



