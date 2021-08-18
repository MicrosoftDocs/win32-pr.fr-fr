---
description: 'ID3DXBaseMesh :: GenerateAdjacency, méthode-générer une liste de bords de maillage, ainsi qu’une liste des visages qui partagent chaque bord.'
ms.assetid: 9d52290f-1c9e-43a7-b239-35cd54e36466
title: 'ID3DXBaseMesh :: GenerateAdjacency, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.GenerateAdjacency
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d51070b5b67b50859338943a60e44cbb224e572ab9e5704e56940328a65479f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119848529"
---
# <a name="id3dxbasemeshgenerateadjacency-method"></a>ID3DXBaseMesh :: GenerateAdjacency, méthode

Générez une liste de contours de maillage, ainsi qu’une liste des visages qui partagent chaque arête.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GenerateAdjacency(
  [in] FLOAT Epsilon,
  [in] DWORD *pAdjacency
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Epsilon* \[ dans\]
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)**

Spécifie que les vertex qui diffèrent de la position par moins de Epsilon doivent être traités comme coïncidents.

</dd> <dt>

*pAdjacency* \[ dans\]
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)\***

Pointeur vers un tableau de trois DWORDs par visage à remplir avec les index des visages adjacents. Le nombre d’octets dans ce tableau doit être au moins égal à 3 \* [**ID3DXBaseMesh :: GetNumFaces**](id3dxbasemesh--getnumfaces.md) \* sizeof (DWORD).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est D3D \_ OK. Si la méthode échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Remarques

Une fois qu’une application a généré des informations d’adjacence pour une maille, les données de maillage peuvent être optimisées pour améliorer les performances de dessin.

L’ordre des entrées dans la mémoire tampon d’adjacence est déterminé par l’ordre des index de vertex dans le tampon d’index. Le triangle adjacent 0 correspond toujours au bord entre les index des angles 0 et 1. Le triangle 1 adjacent correspond toujours au bord entre les index des angles 1 et 2, tandis que le triangle 2 adjacent correspond au bord entre les index des angles 2 et 0.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXBaseMesh](id3dxbasemesh.md)
</dt> <dt>

[**ID3DXMesh :: Optimize**](id3dxmesh--optimize.md)
</dt> <dt>

[**ID3DXMesh::OptimizeInplace**](id3dxmesh--optimizeinplace.md)
</dt> </dl>

 

 
