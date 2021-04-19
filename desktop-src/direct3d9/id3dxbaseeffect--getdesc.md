---
description: Obtient la description de l’effet.
ms.assetid: 96b53b8a-0c20-4bfd-af45-626f6e0305d2
title: 'ID3DXBaseEffect :: GetDesc, méthode (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetDesc
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 35fcb62e9461d419e6643c99c1879efa28fa78c1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106545314"
---
# <a name="id3dxbaseeffectgetdesc-method"></a>ID3DXBaseEffect :: GetDesc, méthode

Obtient la description de l’effet.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetDesc(
  [out] D3DXEFFECT_DESC *pDesc
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pDesc* \[ à\]
</dt> <dd>

Type : **[ **D3DXEFFECT \_ desc**](d3dxeffect-desc.md)\***

Retourne une description de l’effet. Consultez [**D3DXEFFECT \_ desc**](d3dxeffect-desc.md).

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

 

 




