---
description: Calcule les IMT par triangle à partir des données par texture. Cette fonction est similaire à D3DXComputeIMTFromTexture, mais elle utilise un tableau de valeurs float pour transmettre les données, et elle peut calculer des valeurs dimensionnelles supérieures à 4.
ms.assetid: 4a151184-e67e-41e9-83c6-63da72f262fa
title: D3DXComputeIMTFromPerTexelSignal, fonction (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXComputeIMTFromPerTexelSignal
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 48053a238806c223067742b62675f1c0b8bc5a53e8bdf05f78f3fc56520b8388
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118299888"
---
# <a name="d3dxcomputeimtfrompertexelsignal-function"></a>D3DXComputeIMTFromPerTexelSignal fonction)

Calcule les IMT par triangle à partir des données par texture. Cette fonction est similaire à [**D3DXComputeIMTFromTexture**](d3dxcomputeimtfromtexture.md), mais elle utilise un tableau de valeurs float pour transmettre les données, et elle peut calculer des valeurs dimensionnelles supérieures à 4.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT D3DXComputeIMTFromPerTexelSignal(
  _In_  LPD3DXMESH      pMesh,
  _In_  DWORD           dwTextureIndex,
  _In_  FLOAT           *pfTexelSignal,
  _In_  UINT            uWidth,
  _In_  UINT            uHeight,
  _In_  UINT            uSignalDimension,
  _In_  UINT            uComponents,
  _In_  DWORD           dwOptions,
        LPD3DXUVATLASCB pStatusCallback,
        LPVOID          pUserContext,
  _Out_ LPD3DXBUFFER    *ppIMTData
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pMesh* \[ dans\]
</dt> <dd>

Type : **[ **LPD3DXMESH**](id3dxmesh.md)**

Pointeur vers un maillage d’entrée (voir [**ID3DXMesh**](id3dxmesh.md)) qui contient la géométrie d’objet pour le calcul du IMT.

</dd> <dt>

*dwTextureIndex* \[ dans\]
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

Index de coordonnées de texture de base zéro qui identifie le jeu de coordonnées de texture à utiliser.

</dd> <dt>

*pfTexelSignal* \[ dans\]
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)\***

Pointeur vers un tableau de texels d’entrée à partir duquel IMT sera calculé. La taille du tableau est uWidth \* uHeight \* uComponents.

</dd> <dt>

*uWidth* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Largeur de la texture en pixels.

</dd> <dt>

*uHeight* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Hauteur de la texture en pixels.

</dd> <dt>

*uSignalDimension* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Nombre de valeurs float par composant dans chaque élément du tableau de signal.

</dd> <dt>

*uComponents* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Nombre de composants dans chaque Texel.

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

## <a name="return-value"></a>Valeur renvoyée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la fonction est réussie, la valeur de retour est D3D \_ OK ; sinon, la valeur est D3DERR \_ INVALIDCALL.

## <a name="requirements"></a>Configuration requise



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

 

 
