---
description: Obtient le handle d’un paramètre de niveau supérieur ou d’un paramètre de membre de structure en recherchant sa sémantique à l’aide d’une recherche qui ne respecte pas la casse.
ms.assetid: 3de3791a-fe09-4a39-bd6f-0e20a641dd32
title: 'ID3DXBaseEffect :: GetParameterBySemantic, méthode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetParameterBySemantic
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: fa00ef4585462f068e95fcefca8332acd46930efaf1bb1c108a471511ab63eb4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119791009"
---
# <a name="id3dxbaseeffectgetparameterbysemantic-method"></a>ID3DXBaseEffect :: GetParameterBySemantic, méthode

Obtient le handle d’un paramètre de niveau supérieur ou d’un paramètre de membre de structure en recherchant sa sémantique à l’aide d’une recherche qui ne respecte pas la casse.

## <a name="syntax"></a>Syntaxe


```C++
D3DXHANDLE GetParameterBySemantic(
  [in] D3DXHANDLE hParameter,
  [in] LPCSTR     pSemantic
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hParameter* \[ dans\]
</dt> <dd>

Type : **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Handle du paramètre, ou **null** pour les paramètres de niveau supérieur. Consultez [Handles (Direct3D 9)](handles.md).

</dd> <dt>

*pSemantic* \[ dans\]
</dt> <dd>

Type : **[ **LPCSTR**](../winprog/windows-data-types.md)**

Chaîne contenant le nom sémantique.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Retourne le handle du premier paramètre qui correspond à la sémantique spécifiée, ou **null** si la sémantique est introuvable. Consultez [Handles (Direct3D 9)](handles.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXBaseEffect](id3dxbaseeffect.md)
</dt> </dl>

 

 
