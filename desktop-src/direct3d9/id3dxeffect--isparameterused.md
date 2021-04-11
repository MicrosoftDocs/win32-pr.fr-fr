---
description: Détermine si un paramètre est utilisé par la technique.
ms.assetid: ac50c0d3-93d9-4477-a854-d0b53df28c90
title: 'ID3DXEffect :: IsParameterUsed, méthode (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.IsParameterUsed
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 6cbe4783a9ad5b618f05941eae08af4c15be0512
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104116186"
---
# <a name="id3dxeffectisparameterused-method"></a>ID3DXEffect :: IsParameterUsed, méthode

Détermine si un paramètre est utilisé par la technique.

## <a name="syntax"></a>Syntaxe


```C++
BOOL IsParameterUsed(
  [in] D3DXHANDLE hParameter,
  [in] D3DXHANDLE hTechnique
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hParameter* \[ dans\]
</dt> <dd>

Type : **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Identificateur unique du paramètre. Consultez [Handles (Direct3D 9)](handles.md).

</dd> <dt>

*hTechnique* \[ dans\]
</dt> <dd>

Type : **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Identificateur unique de la technique. Consultez [Handles (Direct3D 9)](handles.md).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **bool**](../winprog/windows-data-types.md)**

Retourne la **valeur true** si le paramètre est utilisé et retourne la **valeur false** si le paramètre n’est pas utilisé.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXEffect](id3dxeffect.md)
</dt> </dl>

 

 
