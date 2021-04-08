---
description: Retourne un handle d’événement pour l’événement suivant planifié pour se produire après un événement spécifié sur une piste d’animation.
ms.assetid: 616b2de1-6107-4d18-ad2e-de2ef4560aee
title: 'ID3DXAnimationController :: GetUpcomingTrackEvent, méthode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.GetUpcomingTrackEvent
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f863ce918f25c6b0975010f71a63f067c01f7345
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103953806"
---
# <a name="id3dxanimationcontrollergetupcomingtrackevent-method"></a>ID3DXAnimationController :: GetUpcomingTrackEvent, méthode

Retourne un handle d’événement pour l’événement suivant planifié pour se produire après un événement spécifié sur une piste d’animation.

## <a name="syntax"></a>Syntaxe


```C++
D3DXEVENTHANDLE GetUpcomingTrackEvent(
  [in] UINT            Track,
  [in] D3DXEVENTHANDLE hEvent
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Suivre* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Identificateur de suivi.

</dd> <dt>

*hEvent* \[ dans\]
</dt> <dd>

Type : **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**

Handle d’événement vers un événement spécifié après lequel Rechercher un événement suivant. Si la valeur est **null**, la méthode retourne l’événement planifié suivant.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**

Handle d’événement vers l’événement suivant planifié pour s’exécuter sur la piste spécifiée. La **valeur null** est retournée si aucun nouvel événement n’est planifié.

## <a name="remarks"></a>Notes

Cette méthode peut être utilisée de façon itérative pour localiser un événement souhaité en passant à plusieurs reprises la **valeur null** pour hEvent.

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

 

 
