---
description: Effectue un pavage adaptatif basé sur le critère de pavage adaptative basé sur z.
ms.assetid: 9f8f5c18-e866-4893-ba07-2a3c0d26c028
title: 'ID3DXPatchMesh :: TessellateAdaptive, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.TessellateAdaptive
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e4cc6c6b7ff7b0cdb99e56386df49529f26c9166
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106539899"
---
# <a name="id3dxpatchmeshtessellateadaptive-method"></a>ID3DXPatchMesh :: TessellateAdaptive, méthode

Effectue un pavage adaptatif basé sur le critère de pavage adaptative basé sur z.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT TessellateAdaptive(
  [in] const D3DXVECTOR4 *pTrans,
  [in]       DWORD       dwMaxTessLevel,
  [in]       DWORD       dwMinTessLevel,
  [in]       LPD3DXMESH  pMesh
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pTrans* \[ dans\]
</dt> <dd>

Type : **const [**D3DXVECTOR4**](d3dxvector4.md) \***

Spécifie un vecteur 4D avec points avec les sommets pour obtenir la quantité de pavage adaptative par vertex. Chaque bord est fractionné sur la valeur moyenne des niveaux de pavage pour les deux vertex qu’il connecte.

</dd> <dt>

*dwMaxTessLevel* \[ dans\]
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

Limite maximale pour le pavage adaptatif. Il s’agit du nombre de vertex introduits entre les vertex existants. Cette valeur entière peut être comprise entre 1 et 32 inclus.

</dd> <dt>

*dwMinTessLevel* \[ dans\]
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

Limite minimale pour le pavage adaptatif. Il s’agit du nombre de vertex introduits entre les vertex existants. Cette valeur entière peut être comprise entre 1 et 32 inclus.

</dd> <dt>

*pMesh* \[ dans\]
</dt> <dd>

Type : **[ **LPD3DXMESH**](id3dxmesh.md)**

Maillage fractionné résultant. Consultez [**ID3DXMesh**](id3dxmesh.md).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est D3D \_ OK. Si la méthode échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Notes

Cette fonction s’exécute plus efficacement si la maille de correctifs a été optimisée à l’aide de [**ID3DXPatchMesh :: Optimize**](id3dxpatchmesh--optimize.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXPatchMesh](id3dxpatchmesh.md)
</dt> </dl>

 

 
