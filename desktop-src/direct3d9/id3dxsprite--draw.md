﻿---
Description: 'Adds a sprite to the list of batched sprites.'
ms.assetid: '8f5c43a2-68dd-44a9-be2f-f76d9fa2d900'
title: 'ID3DXSprite::Draw method'
---

# ID3DXSprite::Draw method

Adds a sprite to the list of batched sprites.

## Syntax


```C++
HRESULT Draw(
  [in]       LPDIRECT3DTEXTURE9 pTexture,
  [in] const RECT               *pSrcRect,
  [in] const D3DXVECTOR3        *pCenter,
  [in] const D3DXVECTOR3        *pPosition,
  [in]       D3DCOLOR           Color
);
```



## Parameters

<dl> <dt>

*pTexture* \[in\]
</dt> <dd>

Type: **[**LPDIRECT3DTEXTURE9**](idirect3dtexture9.md)**

Pointer to an [**IDirect3DTexture9**](idirect3dtexture9.md) interface that represents the sprite texture.

</dd> <dt>

*pSrcRect* \[in\]
</dt> <dd>

Type: **const [**RECT**](gdi.rect)\***

Pointer to a [**RECT**](gdi.rect) structure that indicates the portion of the source texture to use for the sprite. If this parameter is **NULL**, then the entire source image is used for the sprite.

</dd> <dt>

*pCenter* \[in\]
</dt> <dd>

Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***

Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) vector that identifies the center of the sprite. If this argument is **NULL**, the point (0,0,0) is used, which is the upper-left corner.

</dd> <dt>

*pPosition* \[in\]
</dt> <dd>

Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***

Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) vector that identifies the position of the sprite. If this argument is **NULL**, the point (0,0,0) is used, which is the upper-left corner.

</dd> <dt>

*Color* \[in\]
</dt> <dd>

Type: **[**D3DCOLOR**](d3dcolor.md)**

[**D3DCOLOR**](d3dcolor.md) type. The color and alpha channels are modulated by this value. A value of 0xFFFFFFFF maintains the original source color and alpha data. Use the [**D3DCOLOR\_RGBA**](d3dcolor-rgba.md) macro to help generate this color.

</dd> </dl>

## Return value

Type: **[**HRESULT**](455d07e9-52c3-4efb-a9dc-2955cbfd38cc)**

If the method succeeds, the return value is S\_OK. If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.

## Remarks

To scale, rotate, or translate a sprite, call [**ID3DXSprite::SetTransform**](id3dxsprite--settransform.md) with a matrix that contains the scale, rotate, and translate (SRT) values, before calling ID3DXSprite::Draw. For information about setting SRT values in a matrix, see [Matrix Transforms](transforms.md).

## Requirements



|                    |                                                                                        |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9core.h</dt> </dl> |
| Library<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## See also

<dl> <dt>

[ID3DXSprite](id3dxsprite.md)
</dt> <dt>

[**ID3DXSprite::GetTransform**](id3dxsprite--gettransform.md)
</dt> </dl>

 

 



