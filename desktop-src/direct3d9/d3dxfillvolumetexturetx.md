---
description: Utilise une fonction de nuanceur de niveau supérieur (HLSL, shader Language) compilée pour remplir chaque Texel de chaque niveau de mipmap d’une texture.
ms.assetid: f082e1d2-c433-482c-9288-58e5c558cdc5
title: D3DXFillVolumeTextureTX, fonction (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFillVolumeTextureTX
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: de310ee6171924a5d2b61071d47c421739f15833
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106520324"
---
# <a name="d3dxfillvolumetexturetx-function"></a>D3DXFillVolumeTextureTX fonction)

Utilise une fonction de nuanceur de niveau supérieur (HLSL, shader Language) compilée pour remplir chaque Texel de chaque niveau de mipmap d’une texture.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT D3DXFillVolumeTextureTX(
  _In_ LPDIRECT3DVOLUMETEXTURE9 pTexture,
  _In_ LPD3DXTEXTURESHADER      pTextureShader
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pTexture* \[ dans\]
</dt> <dd>

Type : **[ **LPDIRECT3DVOLUMETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9)**

Pointeur vers un objet [**IDirect3DVolumeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9) représentant la texture à remplir.

</dd> <dt>

*pTextureShader* \[ dans\]
</dt> <dd>

Type : **[ **LPD3DXTEXTURESHADER**](id3dxtextureshader.md)**

Pointeur vers un objet de nuanceur de texture [**ID3DXTextureShader**](id3dxtextureshader.md) .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la fonction est réussie, la valeur de retour est D3D \_ OK. Si la fonction échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ NOTAVAILABLE, D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Notes

La cible de la texture doit être une fonction HLSL qui prend la sémantique suivante :

-   Un paramètre d’entrée doit utiliser une sémantique de POSITION.
-   Un paramètre d’entrée doit utiliser une sémantique PSIZE.
-   La fonction doit retourner un paramètre qui utilise la sémantique de couleur.

Les paramètres d’entrée peuvent être dans n’importe quel ordre. Pour obtenir un exemple, consultez [ **D3DXFillTextureTX**](d3dxfilltexturetx.md)

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx9tex. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions de texture dans D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> <dt>

[**D3DXFillTextureTX**](d3dxfilltexturetx.md)
</dt> <dt>

[**D3DXFillCubeTextureTX**](d3dxfillcubetexturetx.md)
</dt> </dl>

 

 
