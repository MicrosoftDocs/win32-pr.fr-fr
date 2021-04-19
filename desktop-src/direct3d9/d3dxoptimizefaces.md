---
description: Génère un remappage de visage optimisé pour une liste de triangles.
ms.assetid: 428c2af8-43e7-4cf7-8b9b-04ba5cff82c8
title: D3DXOptimizeFaces, fonction (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXOptimizeFaces
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6c56dec04e01b542d2c760852a58826a8186c213
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106538967"
---
# <a name="d3dxoptimizefaces-function"></a>D3DXOptimizeFaces fonction)

Génère un remappage de visage optimisé pour une liste de triangles.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT D3DXOptimizeFaces(
  _In_    LPCVOID pIndices,
  _In_    UINT    NumFaces,
  _In_    UINT    NumVertices,
  _In_    BOOL    Indices32Bit,
  _Inout_ DWORD   *pFaceRemap
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

Nombre de visages dans la liste de triangles. Pour les maillages 16 bits, cette valeur est limitée à 2 ^ 16-1 (65535) ou moins de visages.

</dd> <dt>

*NumVertices* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Nombre de vertex référencés par la liste de triangles.

</dd> <dt>

*Indices32Bit* \[ dans\]
</dt> <dd>

Type : **[ **bool**](../winprog/windows-data-types.md)**

Indicateur qui spécifie le type d’index : **true** si les index sont 32 bits (plus de 65535 index), **false** si les index sont 16 bits (65535 ou moins d’index).

</dd> <dt>

*pFaceRemap* \[ in, out\]
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)\***

Pointeur vers la face de maille d’origine qui a été fractionnée pour générer la face actuelle.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la fonction est réussie, la valeur de retour est D3D \_ OK. Si la fonction échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Notes

La procédure d’optimisation de cette fonction est fonctionnellement équivalente à l’appel de [**ID3DXMesh :: Optimize**](id3dxmesh--optimize.md) avec l' \_ indicateur D3DXMESHOPT DEVICEINDEPENDENT, mais cette fonction permet une utilisation plus efficace des caches de vertex.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions de maillage](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
