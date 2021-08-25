---
description: Retourne un handle d’événement pour l’événement de fusion Priority suivant planifié pour se produire après un événement spécifié.
ms.assetid: 64fa6fca-dc4a-4534-ab8e-b11b3c7ed23c
title: 'ID3DXAnimationController :: GetUpcomingPriorityBlend, méthode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.GetUpcomingPriorityBlend
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 4c58bf5e2a8736db98e0461988f984709e756d269d09c74dd673356676702ff9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119849079"
---
# <a name="id3dxanimationcontrollergetupcomingpriorityblend-method"></a>ID3DXAnimationController :: GetUpcomingPriorityBlend, méthode

Retourne un handle d’événement pour l’événement de fusion Priority suivant planifié pour se produire après un événement spécifié.

## <a name="syntax"></a>Syntaxe


```C++
D3DXEVENTHANDLE GetUpcomingPriorityBlend(
  [in] D3DXEVENTHANDLE hEvent
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hEvent* \[ dans\]
</dt> <dd>

Type : **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**

Handle d’événement vers un événement spécifié après lequel Rechercher un événement de fusion de priorité suivant. Si la valeur est **null**, la méthode retourne l’événement de fusion de la priorité planifiée suivante.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**

Handle d’événement vers l’événement suivant de fusion de priorité planifiée. La **valeur null** est retournée si aucun nouvel événement Priority Blend n’est planifié.

## <a name="remarks"></a>Remarques

Cette méthode peut être utilisée de façon itérative pour localiser un événement de fusion de priorité souhaité en passant à plusieurs reprises la **valeur null** pour hEvent.

> [!Note]  
> N’effectuez pas d’itération après que la méthode a retourné la **valeur null**.

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 




