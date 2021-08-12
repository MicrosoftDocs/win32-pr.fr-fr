---
description: 'ID3DX10Mesh :: GetAttributeTable, méthode-récupère soit une table d’attributs pour un maillage, soit le nombre d’entrées stockées dans une table d’attributs pour une maille.'
ms.assetid: cee49eba-c113-49f5-a702-c366401f1f2d
title: 'ID3DX10Mesh :: GetAttributeTable, méthode (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.GetAttributeTable
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: ce1f2464882bfdece8997aeea23f2bb42c276b3f6ce49b13cb242d517a522250
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118540289"
---
# <a name="id3dx10meshgetattributetable-method"></a>ID3DX10Mesh :: GetAttributeTable, méthode

Récupère une table d’attributs pour un maillage ou le nombre d’entrées stockées dans une table d’attributs pour une maille.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetAttributeTable(
  [in] D3DX10_ATTRIBUTE_RANGE *pAttribTable,
  [in] UINT                   *pAttribTableSize
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pAttribTable* \[ dans\]
</dt> <dd>

Type : **[ **\_ \_ plage d’attributs d3dx10**](d3dx10-attribute-range.md)\***

Pointeur vers un tableau de \_ structures de plage d’attributs d3dx10 \_ , représentant les entrées dans la table d’attributs du maillage. Spécifiez **null** pour récupérer la valeur de pAttribTableSize.

</dd> <dt>

*pAttribTableSize* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)\***

Pointeur vers le nombre d’entrées stockées dans pAttribTable ou une valeur à remplir avec le nombre d’entrées stockées dans la table d’attributs pour le maillage.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

La valeur de retour est l’une des valeurs indiquées dans les [codes de retour Direct3D 10](d3d10-graphics-reference-returnvalues.md).

## <a name="remarks"></a>Remarques

Une table d’attributs permet d’identifier les zones de la maille qui doivent être dessinées avec différentes textures, États de rendu, matériaux, etc. En outre, l’application peut utiliser la table d’attributs pour masquer des parties d’un maillage en ne dessinant pas d’identificateur d’attribut donné lors du dessin du frame.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Bibliothèque<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DX10Mesh](id3dx10mesh.md)
</dt> <dt>

[Interfaces D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
