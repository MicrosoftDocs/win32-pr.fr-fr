---
description: Obtient un pointeur vers le pool de paramètres partagés.
ms.assetid: 1e999fd5-76ef-43fa-8a77-ae6f2821f46d
title: 'ID3DXEffect :: GetPool, méthode (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.GetPool
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 0220b2864d6c668c2d4fbb71925da6452f6cc8661d0d931a379969418dfe7e19
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118521225"
---
# <a name="id3dxeffectgetpool-method"></a>ID3DXEffect :: GetPool, méthode

Obtient un pointeur vers le pool de paramètres partagés.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetPool(
  [out] LPD3DXEFFECTPOOL *ppPool
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ppPool* \[ à\]
</dt> <dd>

Type : **[ **LPD3DXEFFECTPOOL**](id3dxeffectpool.md)\***

Pointeur vers un objet [**ID3DXEffectPool**](id3dxeffectpool.md) .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Cette méthode retourne toujours la valeur \_ OK.

## <a name="remarks"></a>Remarques

Les pools contiennent des paramètres partagés entre les effets. Consultez [clonage et partage (Direct3D 9)](cloning-and-sharing.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXEffect](id3dxeffect.md)
</dt> </dl>

 

 




