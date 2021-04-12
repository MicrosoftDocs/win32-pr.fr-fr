---
description: Obtient le handle d’une fonction en recherchant son nom.
ms.assetid: 1e2e2dae-5084-47f3-9812-3dbf609bd70b
title: 'ID3DXBaseEffect :: GetFunctionByName, méthode (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetFunctionByName
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: e1cd9ec56ff5df3bff293ade0669b4cd7c8dad5d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323341"
---
# <a name="id3dxbaseeffectgetfunctionbyname-method"></a>ID3DXBaseEffect :: GetFunctionByName, méthode

Obtient le handle d’une fonction en recherchant son nom.

## <a name="syntax"></a>Syntaxe


```C++
D3DXHANDLE GetFunctionByName(
  [in] LPCSTR pName
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pname* \[ dans\]
</dt> <dd>

Type : **[ **LPCSTR**](../winprog/windows-data-types.md)**

Chaîne contenant le nom de la fonction.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Retourne le handle de la fonction spécifiée, ou **null** si le nom est introuvable. Consultez [Handles (Direct3D 9)](handles.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXBaseEffect](id3dxbaseeffect.md)
</dt> </dl>

 

 
