---
description: Obtient un État littéral d’un paramètre. Un paramètre littéral a une valeur qui ne change pas pendant la durée de vie d’un effet.
ms.assetid: 417abbee-5193-462e-b0d1-b4928ad0a041
title: 'ID3DXEffectCompiler :: GetLiteral, méthode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectCompiler.GetLiteral
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: d5c4fcb9b4eb3ee102d4e0676985945cfa227aa35cbd939c8dcd5b8d51da4826
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119493939"
---
# <a name="id3dxeffectcompilergetliteral-method"></a>ID3DXEffectCompiler :: GetLiteral, méthode

Obtient un État littéral d’un paramètre. Un paramètre littéral a une valeur qui ne change pas pendant la durée de vie d’un effet.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetLiteral(
  [in]  D3DXHANDLE hParameter,
  [out] BOOL       *pLiteral
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hParameter* \[ dans\]
</dt> <dd>

Type : **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Identificateur unique d’un paramètre. Consultez [Handles (Direct3D 9)](handles.md).

</dd> <dt>

*pLiteral* \[ à\]
</dt> <dd>

Type : **[ **bool**](../winprog/windows-data-types.md)\***

Retourne la valeur true si le paramètre est un littéral et la valeur false dans le cas contraire.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est D3D \_ OK. Si la méthode échoue, la valeur de retour peut être D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Remarques

Cette méthode change uniquement si le paramètre est un littéral ou non. Pour modifier la valeur d’un paramètre, utilisez une méthode comme [**ID3DXBaseEffect :: SetBool**](id3dxbaseeffect--setbool.md) ou [**ID3DXBaseEffect :: SetValue**](id3dxbaseeffect--setvalue.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXEffectCompiler](id3dxeffectcompiler.md)
</dt> <dt>

[Utilisations et littéraux (Direct3D 9)](usages-and-literals.md)
</dt> <dt>

[**ID3DXEffectCompiler::SetLiteral**](id3dxeffectcompiler--setliteral.md)
</dt> </dl>

 

 
