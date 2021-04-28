---
description: 'ID3DXBaseMesh :: GetAttributeTable, méthode-récupère soit une table d’attributs pour un maillage, soit le nombre d’entrées stockées dans une table d’attributs pour une maille.'
ms.assetid: 15b24137-0ff9-4299-971b-90fa4ef2686d
title: 'ID3DXBaseMesh :: GetAttributeTable, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.GetAttributeTable
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7f5d27de884f72b46db900487e26f1099bf30949
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115447"
---
# <a name="id3dxbasemeshgetattributetable-method"></a>ID3DXBaseMesh :: GetAttributeTable, méthode

Récupère une table d’attributs pour un maillage ou le nombre d’entrées stockées dans une table d’attributs pour une maille.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetAttributeTable(
  [in, out] D3DXATTRIBUTERANGE *pAttribTable,
  [in, out] DWORD              *pAttribTableSize
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pAttribTable* \[ in, out\]
</dt> <dd>

Type : **[ **D3DXATTRIBUTERANGE**](d3dxattributerange.md)\***

Pointeur vers un tableau de structures [**D3DXATTRIBUTERANGE**](d3dxattributerange.md) représentant les entrées dans la table d’attributs du maillage. Spécifiez **null** pour récupérer la valeur de pAttribTableSize.

</dd> <dt>

*pAttribTableSize* \[ in, out\]
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)\***

Pointeur vers le nombre d’entrées stockées dans pAttribTable ou une valeur à remplir avec le nombre d’entrées stockées dans la table d’attributs pour le maillage.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est D3D \_ OK. Si la méthode échoue, la valeur de retour peut être D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Notes 

Une table d’attributs est créée par [**ID3DXMesh :: Optimize**](id3dxmesh--optimize.md) et en passant D3DXMESHOPT \_ ATTRSORT pour le paramètre flags.

Une table d’attributs permet d’identifier les zones de la maille qui doivent être dessinées avec différentes textures, États de rendu, matériaux, etc. En outre, l’application peut utiliser la table d’attributs pour masquer des parties d’un maillage en ne dessinant pas d’identificateur d’attribut donné lors du dessin du frame.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXBaseMesh](id3dxbasemesh.md)
</dt> </dl>

 

 
