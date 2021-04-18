---
description: Crée un maillage d’apparence à partir d’un autre maillage.
ms.assetid: 4c69377e-61ef-42b8-8864-c116164d4b22
title: D3DXCreateSkinInfoFromBlendedMesh, fonction (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateSkinInfoFromBlendedMesh
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d81de43dde2b4f0df5913831ddfcefbab1a41855
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104530927"
---
# <a name="d3dxcreateskininfofromblendedmesh-function"></a>D3DXCreateSkinInfoFromBlendedMesh fonction)

Crée un maillage d’apparence à partir d’un autre maillage.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT D3DXCreateSkinInfoFromBlendedMesh(
  _In_        LPD3DXBASEMESH      pMesh,
  _In_        DWORD               NumBones,
  _In_  const D3DXBONECOMBINATION *pBoneCombinationTable,
  _Out_       LPD3DXSKININFO      *ppSkinInfo
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pMesh* \[ dans\]
</dt> <dd>

Type : **[ **LPD3DXBASEMESH**](id3dxbasemesh.md)**

Pointeur vers un objet [**ID3DXBaseMesh**](id3dxbasemesh.md) , le maillage à partir duquel créer le maillage d’apparence.

</dd> <dt>

*NumBones* \[ dans\]
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

Longueur du tableau attaché à BoneId. Consultez [**D3DXBONECOMBINATION**](d3dxbonecombination.md).

</dd> <dt>

*pBoneCombinationTable* \[ dans\]
</dt> <dd>

Type : **const [**D3DXBONECOMBINATION**](d3dxbonecombination.md) \***

Pointeur vers un tableau de combinaisons osseuses. Consultez [**D3DXBONECOMBINATION**](d3dxbonecombination.md).

</dd> <dt>

*ppSkinInfo* \[ à\]
</dt> <dd>

Type : **[ **LPD3DXSKININFO**](id3dxskininfo.md)\***

Adresse d’un pointeur vers une interface [**ID3DXSkinInfo**](id3dxskininfo.md) représentant l’objet de maillage d’apparence créé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la fonction est réussie, la valeur de retour est D3D \_ OK. Si la fonction échoue, la valeur de retour peut être la suivante : E \_ OUTOFMEMORY.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions de maillage](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
