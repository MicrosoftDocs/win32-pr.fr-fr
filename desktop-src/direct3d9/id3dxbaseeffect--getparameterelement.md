---
description: Obtient le handle d’un paramètre d’élément de tableau.
ms.assetid: fe8edbc5-dc1d-4386-8149-489541d55bde
title: 'ID3DXBaseEffect :: GetParameterElement, méthode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetParameterElement
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 5130ccf57634f9b1a569a1dd70833fe2014e1a74
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127517473"
---
# <a name="id3dxbaseeffectgetparameterelement-method"></a>ID3DXBaseEffect :: GetParameterElement, méthode

Obtient le handle d’un paramètre d’élément de tableau.

## <a name="syntax"></a>Syntaxe


```C++
D3DXHANDLE GetParameterElement(
  [in] D3DXHANDLE hParameter,
  [in] UINT       ElementIndex
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hParameter* \[ dans\]
</dt> <dd>

Type : **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Handle du tableau. Consultez [Handles (Direct3D 9)](handles.md).

</dd> <dt>

*ElementIndex* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Index de l’élément de tableau.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Type : **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Retourne le handle du paramètre spécifié, ou **null** si HParameter ou ElementIndex n’est pas valide. Consultez [Handles (Direct3D 9)](handles.md).

## <a name="remarks"></a>Notes

Cette méthode est utilisée pour obtenir un élément d’un paramètre qui est un tableau.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXBaseEffect](id3dxbaseeffect.md)
</dt> </dl>

 

 
