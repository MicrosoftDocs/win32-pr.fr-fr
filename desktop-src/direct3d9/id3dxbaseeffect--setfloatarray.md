---
description: Définit un tableau de valeurs à virgule flottante.
ms.assetid: 4b9c27b4-0255-4bbf-9168-491936d64fb9
title: 'ID3DXBaseEffect :: SetFloatArray, méthode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.SetFloatArray
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 9927f3cd79d7950a94e62881089fb06c67395bac
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104211679"
---
# <a name="id3dxbaseeffectsetfloatarray-method"></a>ID3DXBaseEffect :: SetFloatArray, méthode

Définit un tableau de valeurs à virgule flottante.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetFloatArray(
  [in]       D3DXHANDLE hParameter,
  [in] const FLOAT      *pf,
  [in]       UINT       Count
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hParameter* \[ dans\]
</dt> <dd>

Type : **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Identificateur unique. Consultez [Handles (Direct3D 9)](handles.md).

</dd> <dt>

*PF* \[ dans\]
</dt> <dd>

Type : **const [**float**](../winprog/windows-data-types.md) \***

Tableau de valeurs à virgule flottante.

</dd> <dt>

*Nombre* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Nombre de valeurs à virgule flottante dans le tableau.

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

[**GetFloatArray**](id3dxbaseeffect--getfloatarray.md)
</dt> </dl>

 

 
