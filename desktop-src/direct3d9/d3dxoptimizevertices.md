---
description: Génère un remappage optimisé de vertex pour une liste de triangles. Cette fonction est couramment utilisée après l’application du remappage de visages généré par D3DXOptimizeFaces.
ms.assetid: a3b9cb68-204e-4e8f-a985-738d1cea1e29
title: D3DXOptimizeVertices, fonction (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXOptimizeVertices
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a60d7d47e78cd197a7bfcf6285509c9187e32e074347f63f8e76ef9ef866adfc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119044797"
---
# <a name="d3dxoptimizevertices-function"></a>D3DXOptimizeVertices fonction)

Génère un remappage optimisé de vertex pour une liste de triangles. Cette fonction est couramment utilisée après l’application du remappage de visages généré par [**D3DXOptimizeFaces**](d3dxoptimizefaces.md).

## <a name="syntax"></a>Syntaxe


```C++
HRESULT D3DXOptimizeVertices(
  _In_    LPCVOID pIndices,
  _In_    UINT    NumFaces,
  _In_    UINT    NumVertices,
  _In_    BOOL    Indices32Bit,
  _Inout_ DWORD   *pVertexRemap
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pIndices* \[ dans\]
</dt> <dd>

Type : **[ **LPCVOID**](../winprog/windows-data-types.md)**

Pointeur vers les index de liste de triangles à utiliser pour trier les vertex.

</dd> <dt>

*NumFaces* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Nombre de visages dans la liste de triangles.

</dd> <dt>

*NumVertices* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Nombre de vertex référencés par la liste de triangles.

</dd> <dt>

*Indices32Bit* \[ dans\]
</dt> <dd>

Type : **[ **bool**](../winprog/windows-data-types.md)**

Indicateur qui spécifie le type d’index : **true** si les index sont 32 bits (plus de 65535 sommets), **false** si les index sont 16 bits (65535 ou moins de sommets).

</dd> <dt>

*pVertexRemap* \[ in, out\]
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)\***

Pointeur vers une mémoire tampon de destination qui contiendra le nouvel index pour chaque vertex. La valeur stockée dans *pVertexRemap* pour un élément donné correspond à l’emplacement du vertex source dans le nouveau classement de vertex.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la fonction est réussie, la valeur de retour est D3D \_ OK. Si la fonction échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Remarques

Par défaut, un maillage utilise des index 16 bits lorsqu’il est créé, à moins que l’application spécifie dans le cas contraire. Pour vérifier si un maillage existant utilise des index 16 bits ou 32 bits, appelez [**ID3DXBaseMesh :: GetOptions**](id3dxbasemesh--getoptions.md) et recherchez l' \_ indicateur 32 bits D3DXMESH.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions de maillage](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
