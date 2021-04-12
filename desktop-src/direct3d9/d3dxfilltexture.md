---
description: Utilise une fonction fournie par l’utilisateur pour remplir chaque Texel de chaque niveau MIP d’une texture donnée.
ms.assetid: 9c822472-2bbf-4629-bdb3-6491573e8de2
title: D3DXFillTexture, fonction (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFillTexture
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 20790a9e4c1a9ce242a5e067dd617c7871a70b7c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322922"
---
# <a name="d3dxfilltexture-function"></a>D3DXFillTexture fonction)

Utilise une fonction fournie par l’utilisateur pour remplir chaque Texel de chaque niveau MIP d’une texture donnée.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT D3DXFillTexture(
  _Out_ LPDIRECT3DTEXTURE9 pTexture,
  _In_  LPD3DXFILL2D       pFunction,
  _In_  LPVOID             pData
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pTexture* \[ à\]
</dt> <dd>

Type : **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**

Pointeur vers une interface [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) représentant la texture remplie.

</dd> <dt>

*pFunction* \[ dans\]
</dt> <dd>

Type : **[LPD3DXFILL2D](lpd3dxfill2d.md)**

Pointeur vers une fonction évaluateur fournie par l’utilisateur, qui sera utilisée pour calculer la valeur de chaque Texel. La fonction suit le prototype de [LPD3DXFILL2D](lpd3dxfill2d.md).

</dd> <dt>

*pData* \[ dans\]
</dt> <dd>

Type : **[ **LPVOID**](../winprog/windows-data-types.md)**

Pointeur vers un bloc arbitraire de données définies par l’utilisateur. Ce pointeur sera passé à la fonction fournie dans *pFunction*.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la fonction est réussie, la valeur de retour est D3D \_ OK. Si la fonction échoue, la valeur de retour peut être l’une des valeurs suivantes : D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Notes

Voici un exemple qui crée une fonction appelée ColorFill, qui s’appuie sur D3DXFillTexture.


```
// Define a function that matches the prototype of LPD3DXFILL3D
VOID WINAPI ColorFill (D3DXVECTOR4* pOut, const D3DXVECTOR2* pTexCoord, 
const D3DXVECTOR2* pTexelSize, LPVOID pData)
{
    *pOut = D3DXVECTOR4(pTexCoord->x, pTexCoord->y, 0.0f, 0.0f);
}
    
    
// Fill the texture using D3DXFillTexture
if (FAILED (hr = D3DXFillTexture (m_pTexture, ColorFill, NULL)))
{
    return hr;
}
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx9tex. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions de texture dans D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
