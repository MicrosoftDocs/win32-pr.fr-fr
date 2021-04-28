---
description: 'Fonction D3DXFillCubeTextureTX : utilise une fonction de nuanceur de niveau supérieur (HLSL) compilée pour remplir chaque Texel de chaque niveau de mipmap d’une texture.'
ms.assetid: a0c36967-57e6-4771-8e9f-f32949c12001
title: D3DXFillCubeTextureTX, fonction (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFillCubeTextureTX
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 95c6d054900f3f4c4710e22c54759161800137c2
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107667"
---
# <a name="d3dxfillcubetexturetx-function"></a>D3DXFillCubeTextureTX fonction)

Utilise une fonction de nuanceur de niveau supérieur (HLSL, shader Language) compilée pour remplir chaque Texel de chaque niveau de mipmap d’une texture.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT D3DXFillCubeTextureTX(
  _In_ LPDIRECT3DCUBETEXTURE9 pTexture,
  _In_ LPD3DXTEXTURESHADER    pTextureShader
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pTexture* \[ dans\]
</dt> <dd>

Type : **[ **LPDIRECT3DCUBETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)**

Pointeur vers un objet [**IDirect3DCubeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9) représentant la texture à remplir.

</dd> <dt>

*pTextureShader* \[ dans\]
</dt> <dd>

Type : **[ **LPD3DXTEXTURESHADER**](id3dxtextureshader.md)**

Pointeur vers un objet de nuanceur de texture [**ID3DXTextureShader**](id3dxtextureshader.md) .

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

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

[**D3DXFillVolumeTextureTX**](d3dxfillvolumetexturetx.md)
</dt> </dl>

 

 
