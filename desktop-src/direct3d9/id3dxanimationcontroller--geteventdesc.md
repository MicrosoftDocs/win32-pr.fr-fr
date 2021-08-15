---
description: Obtient une description d’un événement d’animation spécifié.
ms.assetid: 7fb3def5-8df2-458d-b68e-5d540fd0a738
title: 'ID3DXAnimationController :: GetEventDesc, méthode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.GetEventDesc
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: bc113788a8eb6b64accfcba8c58dd3a3512e17601ec02ce5dd33349628c69212
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118987939"
---
# <a name="id3dxanimationcontrollergeteventdesc-method"></a>ID3DXAnimationController :: GetEventDesc, méthode

Obtient une description d’un événement d’animation spécifié.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetEventDesc(
  [in]  D3DXEVENTHANDLE  hEvent,
  [out] LPD3DXEVENT_DESC pDesc
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hEvent* \[ dans\]
</dt> <dd>

Type : **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**

Handle d’événement vers un événement d’animation à décrire.

</dd> <dt>

*pDesc* \[ à\]
</dt> <dd>

Type : **[ **LPD3DXEVENT \_ desc**](d3dxevent-desc.md)**

Pointeur vers une structure [**D3DXEVENT \_ desc**](d3dxevent-desc.md) qui contient une description de l’événement d’animation.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est S \_ OK. Si la méthode échoue, la valeur suivante est retournée : D3DERR \_ INVALIDCALL.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 




