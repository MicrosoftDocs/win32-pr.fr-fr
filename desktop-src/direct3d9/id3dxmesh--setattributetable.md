---
description: 'ID3DXMesh :: SetAttributeTable, méthode-définit la table d’attributs pour un maillage et le nombre d’entrées stockées dans la table.'
ms.assetid: 22d46708-cffd-48da-bdad-8a43f9076356
title: 'ID3DXMesh :: SetAttributeTable, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMesh.SetAttributeTable
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e93bc3f077d239fb93ac23898635dfc2fe5157ed5d78c32719fca6980606658c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119606939"
---
# <a name="id3dxmeshsetattributetable-method"></a>ID3DXMesh :: SetAttributeTable, méthode

Définit la table d’attributs pour un maillage et le nombre d’entrées stockées dans la table.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetAttributeTable(
  [in] const D3DXATTRIBUTERANGE *pAttribTable,
  [in]       DWORD              cAttribTableSize
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pAttribTable* \[ dans\]
</dt> <dd>

Type : **const [**D3DXATTRIBUTERANGE**](d3dxattributerange.md) \***

Pointeur vers un tableau de structures [**D3DXATTRIBUTERANGE**](d3dxattributerange.md) représentant les entrées de la table d’attributs de maillage.

</dd> <dt>

*cAttribTableSize* \[ dans\]
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

Nombre d’attributs dans la table d’attributs du maillage.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est D3D \_ OK. Si la méthode échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Remarques

Si une application effectue le suivi des informations dans une table d’attributs et réorganise la table suite à des modifications apportées aux attributs ou aux visages, cette méthode permet à l’application de mettre à jour les tables d’attributs au lieu d’appeler [**ID3DXMesh :: Optimize**](id3dxmesh--optimize.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXMesh](id3dxmesh.md)
</dt> <dt>

[**ID3DXMesh::LockAttributeBuffer**](id3dxmesh--lockattributebuffer.md)
</dt> <dt>

**ID3DXMesh::LockAttributeBuffer**
</dt> </dl>

 

 
