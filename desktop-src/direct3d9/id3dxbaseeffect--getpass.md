---
description: Obtient le handle d’une passe.
ms.assetid: 71332f6a-18fe-4702-8620-6d16b835ba8f
title: 'ID3DXBaseEffect :: GetPass, méthode (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetPass
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 5db5c5da16a65b53b6e266886ee6ab8472dc3246
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127517472"
---
# <a name="id3dxbaseeffectgetpass-method"></a>ID3DXBaseEffect :: GetPass, méthode

Obtient le handle d’une passe.

## <a name="syntax"></a>Syntaxe


```C++
D3DXHANDLE GetPass(
  [in] D3DXHANDLE hTechnique,
  [in] UINT       Index
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hTechnique* \[ dans\]
</dt> <dd>

Type : **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Handle de la technique parente. Consultez [Handles (Direct3D 9)](handles.md).

</dd> <dt>

*Index* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Index pour la passe.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Type : **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Retourne le handle de la passe spécifiée à l’intérieur de la technique spécifiée, ou **null** si l’index n’est pas valide. Consultez [Handles (Direct3D 9)](handles.md).

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXBaseEffect](id3dxbaseeffect.md)
</dt> </dl>

 

 
