---
description: Obtient le handle d’un paramètre de niveau supérieur ou d’un paramètre de membre de structure en recherchant son nom.
ms.assetid: fb03685e-e512-4293-80d7-6c2c0fc9ebfd
title: 'ID3DXBaseEffect :: GetParameterByName, méthode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetParameterByName
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 30a1e585cbbbaee4891e3e7dc2cd4e3d3c871fd33fe36daa51c9137c26bfdc7f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119848679"
---
# <a name="id3dxbaseeffectgetparameterbyname-method"></a>ID3DXBaseEffect :: GetParameterByName, méthode

Obtient le handle d’un paramètre de niveau supérieur ou d’un paramètre de membre de structure en recherchant son nom.

## <a name="syntax"></a>Syntaxe


```C++
D3DXHANDLE GetParameterByName(
  [in] D3DXHANDLE hParameter,
  [in] LPCSTR     pName
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hParameter* \[ dans\]
</dt> <dd>

Type : **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Handle du paramètre, ou **null** pour les paramètres de niveau supérieur. Consultez [Handles (Direct3D 9)](handles.md).

</dd> <dt>

*pname* \[ dans\]
</dt> <dd>

Type : **[ **LPCSTR**](../winprog/windows-data-types.md)**

Chaîne contenant le nom du paramètre.

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

 

 
