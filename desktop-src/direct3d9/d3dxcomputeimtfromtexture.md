---
description: Calcule les IMT par triangle à partir d’une texture mappée sur un maillage, à utiliser éventuellement comme entrée pour les fonctions D3DX UVAtlas.
ms.assetid: 6671edc4-e494-4847-ae99-b9e56651a875
title: D3DXComputeIMTFromTexture, fonction (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXComputeIMTFromTexture
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2fbed0411f3562e3a05ec2ec4df99dfad6d8c902
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127520172"
---
# <a name="d3dxcomputeimtfromtexture-function"></a>D3DXComputeIMTFromTexture fonction)

Calcule les IMT par triangle à partir d’une texture mappée sur un maillage, à utiliser éventuellement comme entrée pour les fonctions D3DX [UVAtlas](dx9-graphics-reference-d3dx-functions-uvatlas.md).

## <a name="syntax"></a>Syntaxe


```C++
HRESULT D3DXComputeIMTFromTexture(
  _In_  LPD3DXMESH         pMesh,
  _In_  LPDIRECT3DTEXTURE9 pTexture,
  _In_  DWORD              dwTextureIndex,
  _In_  DWORD              dwOptions,
        LPD3DXUVATLASCB    pStatusCallback,
        LPVOID             pUserContext,
  _Out_ LPD3DXBUFFER       *ppIMTData
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pMesh* \[ dans\]
</dt> <dd>

Type : **[ **LPD3DXMESH**](id3dxmesh.md)**

Pointeur vers un maillage d’entrée (voir [**ID3DXMesh**](id3dxmesh.md)) qui contient la géométrie d’objet pour le calcul du IMT.

</dd> <dt>

*pTexture* \[ dans\]
</dt> <dd>

Type : **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**

Pointeur vers la texture (voir [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)) qui est mappée à la maille.

</dd> <dt>

*dwTextureIndex* \[ dans\]
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

Index de coordonnées de texture de base zéro qui identifie le jeu de coordonnées de texture à utiliser.

</dd> <dt>

*dwOptions* \[ dans\]
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

Options de retour à la ligne. Il s’agit d’une combinaison d’un ou plusieurs [**indicateurs D3DXIMT**](./d3dximt-flags.md).

</dd> <dt>

*pStatusCallback* 
</dt> <dd>

Type : **[LPD3DXUVATLASCB](lpd3dxuvatlascb.md)**

Pointeur vers une fonction de rappel pour surveiller la progression du calcul IMT.

</dd> <dt>

*pUserContext* 
</dt> <dd>

Type : **[ **LPVOID**](../winprog/windows-data-types.md)**

Pointeur vers une variable définie par l’utilisateur qui est passée à la fonction de rappel d’État. Généralement utilisé par une application pour passer un pointeur vers une structure de données qui fournit des informations de contexte pour la fonction de rappel.

</dd> <dt>

*ppIMTData* \[ à\]
</dt> <dd>

Type : **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Pointeur vers la mémoire tampon (consultez [**ID3DXBuffer**](id3dxbuffer.md)) contenant le tableau IMT retourné. Ce tableau peut être fourni comme entrée aux fonctions D3DX [UVAtlas](dx9-graphics-reference-d3dx-functions-uvatlas.md) pour classer par ordre de priorité l’allocation d’espace de texture dans le paramétrage de la texture.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la fonction est réussie, la valeur de retour est D3D \_ OK ; sinon, la valeur est D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Notes

À partir d’une texture qui est mappée sur la surface de la maille, l’algorithme calcule le IMT pour chaque visage. Cela entraînera des triangles contenant des données de signal de faible fréquence pour occuper moins d’espace dans l’Atlas de texture final lorsqu’il est paramétré avec les fonctions UVAtlas. La texture est supposée être interpolée sur la maille de manière bilinéaire.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[UVAtlas, fonctions](dx9-graphics-reference-d3dx-functions-uvatlas.md)
</dt> <dt>

[Utilisation de UVAtlas (Direct3D 9)](using-uvatlas.md)
</dt> </dl>

 

 
