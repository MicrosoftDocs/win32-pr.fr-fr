---
description: Obtient un tableau de valeurs à virgule flottante.
ms.assetid: ba839129-c332-4ce8-b7c1-ea0ef4697ade
title: 'ID3DXBaseEffect :: GetFloatArray, méthode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetFloatArray
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 2ea71daa3b207a8f7716bf0a0db3608554c0b9f8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126855069"
---
# <a name="id3dxbaseeffectgetfloatarray-method"></a>ID3DXBaseEffect :: GetFloatArray, méthode

Obtient un tableau de valeurs à virgule flottante.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetFloatArray(
  [in]  D3DXHANDLE hParameter,
  [out] FLOAT      *pf,
  [in]  UINT       Count
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hParameter* \[ dans\]
</dt> <dd>

Type : **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Identificateur unique. Consultez [Handles (Direct3D 9)](handles.md).

</dd> <dt>

*PF* \[ à\]
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)\***

Retourne un tableau de valeurs à virgule flottante.

</dd> <dt>

*Nombre* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Nombre de valeurs à virgule flottante dans le tableau.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est D3D \_ OK. Si la méthode échoue, la valeur de retour peut être D3DERR \_ INVALIDCALL.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXBaseEffect](id3dxbaseeffect.md)
</dt> <dt>

[**SetFloatArray**](id3dxbaseeffect--setfloatarray.md)
</dt> </dl>

 

 
