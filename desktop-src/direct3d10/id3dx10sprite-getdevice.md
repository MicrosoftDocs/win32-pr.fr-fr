---
description: Récupérez l’appareil associé à l’objet Sprite.
ms.assetid: 9119b232-22c8-4b05-b584-ce176370ca97
title: 'ID3DX10Sprite :: GetDevice, méthode (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Sprite.GetDevice
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 13513b6fcd2bdb952eda17f10cc81406ff484a20dce3f690d43dd3b5c28eb08f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119634249"
---
# <a name="id3dx10spritegetdevice-method"></a>ID3DX10Sprite :: GetDevice, méthode

Récupérez l’appareil associé à l’objet Sprite.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetDevice(
  [out] ID3D10Device **ppDevice
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ppDevice* \[ à\]
</dt> <dd>

Type : **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\*\***

Adresse d’un pointeur vers une interface ID3D10Device, représentant l’objet appareil Direct3D associé à l’objet Sprite.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est S \_ OK. Si la méthode échoue, la valeur suivante est retournée : D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Remarques

L’appel de cette méthode augmente le nombre de références internes sur l’interface ID3D10Device.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Bibliothèque<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DX10Sprite](id3dx10sprite.md)
</dt> <dt>

[Interfaces D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




