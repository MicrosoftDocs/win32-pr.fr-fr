---
description: 'ID3DXConstantTable :: GetConstant, méthode-obtient une constante en recherchant son index.'
ms.assetid: 7db25171-9bda-4db8-b6a8-8a4d60a842f7
title: 'ID3DXConstantTable :: GetConstant, méthode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable.GetConstant
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 664a1b1a214b49eb731a3a0766a255e5f5acadd9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126921312"
---
# <a name="id3dxconstanttablegetconstant-method"></a>ID3DXConstantTable :: GetConstant, méthode

Obtient une constante en recherchant son index.

## <a name="syntax"></a>Syntaxe


```C++
D3DXHANDLE GetConstant(
  [in] D3DXHANDLE hConstant,
  [in] UINT       Index
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hConstant* \[ dans\]
</dt> <dd>

Type : **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Identificateur unique de la structure de données parent. Si la constante est un paramètre de niveau supérieur (il n’y a aucune structure de données parent), utilisez la **valeur null**.

</dd> <dt>

*Index* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Index de base zéro de la constante.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Type : **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Retourne un identificateur unique à la constante.

## <a name="remarks"></a>Notes

Pour obtenir une constante d’un tableau de constantes, utilisez [**ID3DXConstantTable :: GetConstantElement**](id3dxconstanttable--getconstantelement.md).

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXConstantTable](id3dxconstanttable.md)
</dt> </dl>

 

 
