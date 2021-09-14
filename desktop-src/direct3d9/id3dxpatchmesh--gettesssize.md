---
description: Obtient la taille du maillage fractionné, en fonction d’un niveau de pavage.
ms.assetid: 86d1d1a0-1934-40e9-bff9-6c435d1e5183
title: 'ID3DXPatchMesh :: GetTessSize, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.GetTessSize
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ef23f46baca7e05005cee83f6ca765b9a5214b8b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126998526"
---
# <a name="id3dxpatchmeshgettesssize-method"></a>ID3DXPatchMesh :: GetTessSize, méthode

Obtient la taille du maillage fractionné, en fonction d’un niveau de pavage.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetTessSize(
  [in]  FLOAT fTessLevel,
  [in]  DWORD Adaptive,
  [out] DWORD *NumTriangles,
  [out] DWORD *NumVertices
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*fTessLevel* \[ dans\]
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)**

Niveau de pavage.

</dd> <dt>

*Adaptative* \[ dans\]
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

Pavage adaptative. Pour le pavage adaptatif, définissez cette valeur sur **true** et définissez fTessLevel sur la valeur de pavage maximale. Cela entraîne la taille maximale de maillage nécessaire pour le pavage adaptatif.

</dd> <dt>

*NumTriangles* \[ à\]
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)\***

Pointeur vers le nombre de triangles générés par le maillage fractionné.

</dd> <dt>

*NumVertices* \[ à\]
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)\***

Pointeur vers le nombre de vertex générés par le maillage fractionné.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est D3D \_ OK. Si la méthode échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Notes

Cette méthode suppose une polygonalisation uniforme.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXPatchMesh](id3dxpatchmesh.md)
</dt> </dl>

 

 
