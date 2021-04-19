---
description: Obtient le handle d’une annotation en recherchant son nom.
ms.assetid: da4e2805-5f06-4a9b-836f-85a8c154c502
title: 'ID3DXBaseEffect :: GetAnnotationByName, méthode (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetAnnotationByName
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 00698030488b8f4ae788367f87b8d569476292ca
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106528578"
---
# <a name="id3dxbaseeffectgetannotationbyname-method"></a>ID3DXBaseEffect :: GetAnnotationByName, méthode

Obtient le handle d’une annotation en recherchant son nom.

## <a name="syntax"></a>Syntaxe


```C++
D3DXHANDLE GetAnnotationByName(
  [in] D3DXHANDLE hObject,
  [in] LPCSTR     pName
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hObject* \[ dans\]
</dt> <dd>

Type : **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Handle d’une technique, d’un passe ou d’un paramètre de niveau supérieur. Consultez [Handles (Direct3D 9)](handles.md).

</dd> <dt>

*pname* \[ dans\]
</dt> <dd>

Type : **[ **LPCSTR**](../winprog/windows-data-types.md)**

Chaîne contenant le nom de l’annotation.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Retourne le handle de l’annotation spécifiée, ou **null** si le nom est introuvable. Consultez [Handles (Direct3D 9)](handles.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXBaseEffect](id3dxbaseeffect.md)
</dt> </dl>

 

 
