---
description: Utilise une fonction fournie par l’utilisateur pour remplir chaque Texel de chaque niveau MIP d’une texture de volume donnée.
ms.assetid: cc9eb051-8a62-4e35-87df-c255f10e94d8
title: D3DXFillVolumeTexture, fonction (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFillVolumeTexture
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d817470f0f0617001fd83054e24e8881ac9a3a1f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322921"
---
# <a name="d3dxfillvolumetexture-function"></a>D3DXFillVolumeTexture fonction)

Utilise une fonction fournie par l’utilisateur pour remplir chaque Texel de chaque niveau MIP d’une texture de volume donnée.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT D3DXFillVolumeTexture(
  _Out_ LPDIRECT3DVOLUMETEXTURE9 pTexture,
  _In_  LPD3DXFILL3D             pFunction,
  _In_  LPVOID                   pData
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pTexture* \[ à\]
</dt> <dd>

Type : **[ **LPDIRECT3DVOLUMETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9)**

Pointeur vers une interface [**IDirect3DVolumeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9) représentant la texture remplie.

</dd> <dt>

*pFunction* \[ dans\]
</dt> <dd>

Type : **[LPD3DXFILL3D](lpd3dxfill3d.md)**

Pointeur vers une fonction évaluateur fournie par l’utilisateur, qui sera utilisée pour calculer la valeur de chaque Texel. La fonction suit le prototype de [LPD3DXFILL3D](lpd3dxfill3d.md).

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

Si le volume n’est pas dynamique (car l’utilisation est définie sur 0 lors de sa création) et située dans la mémoire vidéo (le pool de mémoire défini sur D3DPOOL \_ par défaut), **D3DXFillVolumeTexture** échoue car le volume ne peut pas être verrouillé.

Cet exemple crée une fonction appelée ColorVolumeFill, qui s’appuie sur D3DXFillVolumeTexture.


```
// Define a function that matches the prototype of LPD3DXFILL3D
VOID WINAPI ColorVolumeFill (D3DXVECTOR4* pOut, const D3DXVECTOR3* pTexCoord, 
const D3DXVECTOR3* pTexelSize, LPVOID pData)
{
   *pOut = D3DXVECTOR4(pTexCoord->x, pTexCoord->y, pTexCoord->z, 0.0f);
}
    
    
// Fill volume texture
if (FAILED (hr = D3DXFillVolumeTexture (m_pTexture, ColorVolumeFill, NULL)))
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

 

 
