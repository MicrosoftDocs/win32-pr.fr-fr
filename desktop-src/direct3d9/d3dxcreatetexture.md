---
description: Crée une texture vide, en ajustant les paramètres d’appel en fonction des besoins.
ms.assetid: ea028aa9-4f37-4625-9e07-9072ec1a61d0
title: D3DXCreateTexture, fonction (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateTexture
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ecbd5cbb94355af9c1e51e6c7e8fc31a862b03be
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104530916"
---
# <a name="d3dxcreatetexture-function"></a>D3DXCreateTexture fonction)

Crée une texture vide, en ajustant les paramètres d’appel en fonction des besoins.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT D3DXCreateTexture(
  _In_  LPDIRECT3DDEVICE9  pDevice,
  _In_  UINT               Width,
  _In_  UINT               Height,
  _In_  UINT               MipLevels,
  _In_  DWORD              Usage,
  _In_  D3DFORMAT          Format,
  _In_  D3DPOOL            Pool,
  _Out_ LPDIRECT3DTEXTURE9 *ppTexture
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pDevice* \[ dans\]
</dt> <dd>

Type : **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Pointeur vers une interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , représentant l’appareil à associer à la texture.

</dd> <dt>

*Largeur* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Largeur en pixels. Si cette valeur est égale à 0, la valeur 1 est utilisée. Consultez la section Notes.

</dd> <dt>

*Hauteur* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Hauteur en pixels. Si cette valeur est égale à 0, la valeur 1 est utilisée. Consultez la section Notes.

</dd> <dt>

*Miplevels a* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Nombre de niveaux MIP demandés. Si cette valeur est égale à zéro ou à D3DX \_ default, une chaîne mipmap complète est créée.

</dd> <dt>

*Utilisation* \[ dans\]
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

0, [**D3DUSAGE \_ RENDERTARGET**](d3dusage.md)ou **D3DUSAGE \_ dynamique**. L’affectation de la valeur **D3DUSAGE \_ RENDERTARGET** à cet indicateur indique que la surface doit être utilisée comme cible de rendu en appelant la méthode [**SetRenderTarget**](/windows/desktop/api) . Si **D3DUSAGE \_ RENDERTARGET** ou **D3DUSAGE \_ Dynamic** est spécifié, l’application doit vérifier que l’appareil prend en charge cette opération en appelant [**CheckDeviceFormat**](/windows/desktop/api). Pour plus d’informations sur l’utilisation des textures dynamiques, consultez [utilisation de textures dynamiques](performance-optimizations.md).

</dd> <dt>

*Format* \[ dans\]
</dt> <dd>

Type : **[D3DFORMAT](d3dformat.md)**

Membre du type énuméré [D3DFORMAT](d3dformat.md) , décrivant le format de pixel demandé pour la texture. La texture retournée peut être d’un format différent de celui spécifié, si l’appareil ne prend pas en charge le format demandé. Les applications doivent vérifier le format de la texture retournée pour voir si elle correspond au format demandé.

</dd> <dt>

*Pool* \[ dans\]
</dt> <dd>

Type : **[ **D3DPOOL**](./d3dpool.md)**

Membre du type énuméré [**D3DPOOL**](./d3dpool.md) , décrivant la classe de mémoire dans laquelle la texture doit être placée.

</dd> <dt>

*ppTexture* \[ à\]
</dt> <dd>

Type : **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)\***

Adresse d’un pointeur vers une interface [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) représentant l’objet de texture créé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la fonction est réussie, la valeur de retour est D3D \_ OK. Si la fonction échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, D3DERR \_ NOTAVAILABLE, D3DERR \_ OUTOFVIDEOMEMORY, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Notes

En interne, D3DXCreateTexture utilise [**D3DXCheckTextureRequirements**](d3dxchecktexturerequirements.md) pour ajuster les paramètres d’appel. Par conséquent, les appels à D3DXCreateTexture aboutissent souvent lorsque les appels à [**CreateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createtexture) échouent.

Si la hauteur et la largeur sont définies sur [D3DX \_ default](other-d3dx-constants.md), la valeur 256 est utilisée pour les deux paramètres. Si la hauteur ou la largeur est définie sur D3DX \_ Default et que l’autre paramètre est défini sur une valeur numérique, la texture sera carré avec la hauteur et la largeur égales à la valeur numérique.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx9tex. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions de texture dans D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
