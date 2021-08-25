---
description: Définit une valeur à virgule flottante.
ms.assetid: f49fb4d2-6e3d-4452-8102-76200c55cf1f
title: 'ID3DXBaseEffect :: SetFloat, méthode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.SetFloat
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: f55ede140e324daa52b5bafc24cc7004a75163a96bdf2e75d4e4be5e7a4c4b39
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119893699"
---
# <a name="id3dxbaseeffectsetfloat-method"></a>ID3DXBaseEffect :: SetFloat, méthode

Définit une valeur à virgule flottante.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetFloat(
  [in] D3DXHANDLE hParameter,
  [in] FLOAT      f
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hParameter* \[ dans\]
</dt> <dd>

Type : **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Identificateur unique. Consultez [Handles (Direct3D 9)](handles.md).

</dd> <dt>

*f* \[ dans\]
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)**

Valeur à virgule flottante.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est D3D \_ OK. Si la méthode échoue, la valeur de retour peut être D3DERR \_ INVALIDCALL.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXBaseEffect](id3dxbaseeffect.md)
</dt> <dt>

[**GetFloat**](id3dxbaseeffect--getfloat.md)
</dt> </dl>

 

 
