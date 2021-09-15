---
description: Obtient le handle d’une technique en recherchant son nom.
ms.assetid: 34871229-ad63-4575-8c60-f27d7f7dddce
title: 'ID3DXBaseEffect :: GetTechniqueByName, méthode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetTechniqueByName
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 5827527bf5151b121958c3f5803ef8a7e74f8d60
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127531485"
---
# <a name="id3dxbaseeffectgettechniquebyname-method"></a>ID3DXBaseEffect :: GetTechniqueByName, méthode

Obtient le handle d’une technique en recherchant son nom.

## <a name="syntax"></a>Syntaxe


```C++
D3DXHANDLE GetTechniqueByName(
  [in] LPCSTR pName
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pname* \[ dans\]
</dt> <dd>

Type : **[ **LPCSTR**](../winprog/windows-data-types.md)**

Chaîne contenant le nom de la technique.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Type : **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Retourne le handle de la première technique qui porte le nom spécifié, ou **null** si le nom est introuvable. Consultez [Handles (Direct3D 9)](handles.md).

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXBaseEffect](id3dxbaseeffect.md)
</dt> </dl>

 

 
