---
description: Tessellates la maille donnée à l’aide du schéma de pavage N-patch.
ms.assetid: e804905d-ee0b-484f-a621-58b197bd370b
title: D3DXTessellateNPatches, fonction (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXTessellateNPatches
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c1df63068f3eef608f797f8048231e744412c32f9e01a31a089c50f8a46465a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119122721"
---
# <a name="d3dxtessellatenpatches-function"></a>D3DXTessellateNPatches fonction)

Tessellates la maille donnée à l’aide du schéma de pavage N-patch.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT D3DXTessellateNPatches(
  _In_        LPD3DXMESH   pMeshIn,
  _In_  const CONST DWORD  *pAdjacencyIn,
  _In_        FLOAT        NumSegs,
  _In_        BOOL         QuadraticInterpNormals,
  _Out_       LPD3DXMESH   *ppMeshOut,
  _Out_       LPD3DXBUFFER *ppAdjacencyOut
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pMeshIn* \[ dans\]
</dt> <dd>

Type : **[ **LPD3DXMESH**](id3dxmesh.md)**

Pointeur vers une interface [**ID3DXMesh**](id3dxmesh.md) , qui représente le maillage à paver.

</dd> <dt>

*pAdjacencyIn* \[ dans\]
</dt> <dd>

Type : **const const DWORD \***

Pointeur vers un tableau de trois DWORD par visage qui spécifient les trois voisins pour chaque visage dans le maillage source. Ce paramètre peut avoir la **valeur null**.

</dd> <dt>

*NumSegs* \[ dans\]
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)**

Nombre de segments par périphérie à paver.

</dd> <dt>

*QuadraticInterpNormals* \[ dans\]
</dt> <dd>

Type : **[ **bool**](../winprog/windows-data-types.md)**

Affectez la valeur **true** pour utiliser l’interpolation quadratique pour les normales ; Affectez la valeur **false** à l’interpolation linéaire.

</dd> <dt>

*ppMeshOut* \[ à\]
</dt> <dd>

Type : **[ **LPD3DXMESH**](id3dxmesh.md)\***

Adresse d’un pointeur vers une interface [**ID3DXMesh**](id3dxmesh.md) représentant le maillage fractionné retourné.

</dd> <dt>

*ppAdjacencyOut* \[ à\]
</dt> <dd>

Type : **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Adresse d’un pointeur vers une interface [**ID3DXBuffer**](id3dxbuffer.md) . Si la valeur de ce paramètre n’est pas définie sur **null**, cette mémoire tampon contient un tableau de trois DWORDS par visage qui spécifient les trois voisins pour chaque visage dans le maillage de sortie. Ce paramètre peut avoir la **valeur null**.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la fonction est réussie, la valeur de retour est D3D \_ OK. Si la fonction échoue, la valeur de retour peut être l’une des valeurs suivantes : D3DERR \_ INVALIDCALL, D3DXERR \_ sera déplacé, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Remarques

Cette fonction tessellates à l’aide de l’algorithme N-patch.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions de maillage](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
