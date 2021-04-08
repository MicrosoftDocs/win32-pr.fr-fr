---
description: Obtient le handle d’un paramètre de niveau supérieur ou d’un paramètre de membre de structure.
ms.assetid: 940f1bfd-ce62-4c86-88cc-787e62cf6a93
title: 'ID3DXBaseEffect :: GetParameter, méthode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetParameter
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: b7c96c371b36b8dcfc2e3e64a95798347ca3a6ea
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104043184"
---
# <a name="id3dxbaseeffectgetparameter-method"></a>ID3DXBaseEffect :: GetParameter, méthode

Obtient le handle d’un paramètre de niveau supérieur ou d’un paramètre de membre de structure.

## <a name="syntax"></a>Syntaxe


```C++
D3DXHANDLE GetParameter(
  [in] D3DXHANDLE hParameter,
  [in] UINT       Index
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hParameter* \[ dans\]
</dt> <dd>

Type : **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Handle du paramètre, ou **null** pour les paramètres de niveau supérieur. Consultez [Handles (Direct3D 9)](handles.md).

</dd> <dt>

*Index* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Index du paramètre.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Retourne le handle du paramètre spécifié, ou **null** si l’index n’est pas valide. Consultez [Handles (Direct3D 9)](handles.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXBaseEffect](id3dxbaseeffect.md)
</dt> </dl>

 

 
