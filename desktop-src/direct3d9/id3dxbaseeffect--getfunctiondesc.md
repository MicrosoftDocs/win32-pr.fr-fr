---
description: Obtient une description de fonction.
ms.assetid: a1a0ccf4-2428-4e60-9af0-07dc2132a367
title: 'ID3DXBaseEffect :: GetFunctionDesc, méthode (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetFunctionDesc
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: b8f74715b163b3d197f62274c6aa6bf52ae872254db9df8225e061dc54900964
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119893719"
---
# <a name="id3dxbaseeffectgetfunctiondesc-method"></a>ID3DXBaseEffect :: GetFunctionDesc, méthode

Obtient une description de fonction.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetFunctionDesc(
  [in]  D3DXHANDLE        hFunction,
  [out] D3DXFUNCTION_DESC *pDesc
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hFunction* \[ dans\]
</dt> <dd>

Type : **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Handle de fonction. Consultez [Handles (Direct3D 9)](handles.md).

</dd> <dt>

*pDesc* \[ à\]
</dt> <dd>

Type : **[ **D3DXFUNCTION \_ desc**](d3dxfunction-desc.md)\***

Retourne une description de la fonction. Consultez [**D3DXFUNCTION \_ desc**](d3dxfunction-desc.md).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est S \_ OK. Si la méthode échoue, la valeur de retour peut être D3DERR \_ INVALIDCALL.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXBaseEffect](id3dxbaseeffect.md)
</dt> </dl>

 

 




