---
description: Valide une maille.
ms.assetid: e5bec2f3-e914-4677-8114-77c71b8a586e
title: D3DXValidMesh, fonction (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXValidMesh
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 299092700b015840376f3e4b297d7825366b6083e1458155f5963e1b5b1f4d73
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119749669"
---
# <a name="d3dxvalidmesh-function"></a>D3DXValidMesh fonction)

Valide une maille.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT D3DXValidMesh(
  _In_        LPD3DXMESH   pMeshIn,
  _In_  const DWORD        *pAdjacency,
  _Out_       LPD3DXBUFFER *ppErrorsAndWarnings
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pMeshIn* \[ dans\]
</dt> <dd>

Type : **[ **LPD3DXMESH**](id3dxmesh.md)**

Pointeur vers une interface [**ID3DXMesh**](id3dxmesh.md) représentant le maillage à tester.

</dd> <dt>

*pAdjacency* \[ dans\]
</dt> <dd>

Type : **const [**DWORD**](../winprog/windows-data-types.md) \***

Pointeur vers un tableau de trois DWORD par visage qui spécifient les trois voisins pour chaque face de la maille à tester.

</dd> <dt>

*ppErrorsAndWarnings* \[ à\]
</dt> <dd>

Type : **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Retourne une mémoire tampon contenant une chaîne d’erreurs et d’avertissements, qui expliquent les problèmes détectés dans la maille.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la fonction est réussie, la valeur de retour est D3D \_ OK. Si la fonction échoue, la valeur de retour peut être l’une des suivantes : D3DXERR \_ INVALIDMESH, D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Remarques

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

 

 
