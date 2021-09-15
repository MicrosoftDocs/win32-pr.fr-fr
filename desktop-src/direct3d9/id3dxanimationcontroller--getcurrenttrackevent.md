---
description: Retourne un handle d’événement pour l’événement en cours d’exécution sur la piste d’animation spécifiée.
ms.assetid: 2e3d4b85-42f0-463f-9eca-d9b1fa8932f6
title: 'ID3DXAnimationController :: GetCurrentTrackEvent, méthode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.GetCurrentTrackEvent
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b00b90f6fbb3f4bb6170c8987f3634fec4bd0bf5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127404063"
---
# <a name="id3dxanimationcontrollergetcurrenttrackevent-method"></a>ID3DXAnimationController :: GetCurrentTrackEvent, méthode

Retourne un handle d’événement pour l’événement en cours d’exécution sur la piste d’animation spécifiée.

## <a name="syntax"></a>Syntaxe


```C++
D3DXEVENTHANDLE GetCurrentTrackEvent(
  [in] UINT           Track,
  [in] D3DXEVENT_TYPE EventType
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Suivre* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Identificateur de suivi.

</dd> <dt>

*EventType* \[ dans\]
</dt> <dd>

Type : **[ **D3DXEVENT \_**](./d3dxevent-type.md)**

Type d’événement à interroger.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Type : **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**

Handle d’événement de l’événement en cours d’exécution sur la piste spécifiée. La **valeur null** est retournée si aucun événement n’est en cours d’exécution sur la piste spécifiée.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 
