---
description: 'ID3DX10Mesh :: SetAttributeTable, méthode-définit la table d’attributs pour un maillage et le nombre d’entrées stockées dans la table.'
ms.assetid: 629fd31b-d88a-4650-82ed-ab7c40690986
title: 'ID3DX10Mesh :: SetAttributeTable, méthode (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.SetAttributeTable
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 4e06b181bb512e16e9caaa0d233ebbd3472bfcf8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126922707"
---
# <a name="id3dx10meshsetattributetable-method"></a>ID3DX10Mesh :: SetAttributeTable, méthode

Définit la table d’attributs pour un maillage et le nombre d’entrées stockées dans la table.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetAttributeTable(
  [in] const D3DX10_ATTRIBUTE_RANGE *pAttribTable,
  [in]       UINT                   cAttribTableSize
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pAttribTable* \[ dans\]
</dt> <dd>

Type : **const [**d3dx10 \_ attribut \_ Range**](d3dx10-attribute-range.md) \***

Pointeur vers un tableau de \_ structures de plage d’attributs d3dx10 \_ , représentant les entrées de la table d’attributs de maillage.

</dd> <dt>

*cAttribTableSize* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Nombre d’attributs dans la table d’attributs du maillage.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

La valeur de retour est l’une des valeurs indiquées dans les [codes de retour Direct3D 10](d3d10-graphics-reference-returnvalues.md).

## <a name="remarks"></a>Notes

Si une application effectue le suivi des informations dans une table d’attributs et réorganise la table suite à des modifications apportées aux attributs ou aux visages, cette méthode permet à l’application de mettre à jour les tables d’attributs au lieu d’appeler ID3DX10Mesh :: optimize.

## <a name="requirements"></a>Spécifications



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

 

 
