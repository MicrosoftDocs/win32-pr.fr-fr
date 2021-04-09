---
description: Valide un maillage de correctifs, en retournant le nombre de Dégénérations de vertex et de correctifs.
ms.assetid: a95ff9d9-d476-42ac-8d7e-1dc42418f763
title: D3DXValidPatchMesh, fonction (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXValidPatchMesh
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 87d7fbe15c78a8b768d845e6a23cc084b69f3e02
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103953831"
---
# <a name="d3dxvalidpatchmesh-function"></a>D3DXValidPatchMesh fonction)

Valide un maillage de correctifs, en retournant le nombre de Dégénérations de vertex et de correctifs.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT D3DXValidPatchMesh(
  _In_  LPD3DXPATCHMESH pMeshIn,
  _Out_ DWORD           *pNumDegenerateVertices,
  _Out_ DWORD           *pNumDegeneratePatches,
  _Out_ LPD3DXBUFFER    *ppErrorsAndWarnings
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pMeshIn* \[ dans\]
</dt> <dd>

Type : **[ **LPD3DXPATCHMESH**](id3dxpatchmesh.md)**

Pointeur vers une interface [**ID3DXPatchMesh**](id3dxpatchmesh.md) représentant la maille de correctif à tester.

</dd> <dt>

*pNumDegenerateVertices* \[ à\]
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)\***

Retourne le nombre de vertex dégénérés dans la maille de correctifs.

</dd> <dt>

*pNumDegeneratePatches* \[ à\]
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)\***

Retourne le nombre de correctifs dégénérées dans le maillage des correctifs.

</dd> <dt>

*ppErrorsAndWarnings* \[ à\]
</dt> <dd>

Type : **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Retourne un pointeur vers une mémoire tampon contenant une chaîne d’erreurs et d’avertissements qui expliquent les problèmes détectés dans la maille de correctifs.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la fonction est réussie, la valeur de retour est D3D \_ OK. Si la fonction échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Notes

Cette méthode valide le maillage en vérifiant les index non valides. Les informations d’erreur sont disponibles à partir de la sortie du débogueur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions de maillage](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
