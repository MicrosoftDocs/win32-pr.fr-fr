---
description: Avertit les applications que la puissance de la batterie est faible.
ms.assetid: ef24b8cf-d801-4452-a03c-3f2bdbdd7e5d
title: Événement PBT_APMBATTERYLOW (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1fc8f6d42d00ee1a4b92d7a977668b1161e1f91270e8d55c46d724f73ec105a3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119961769"
---
# <a name="pbt_apmbatterylow-event"></a>\_Événement PBT APMBATTERYLOW

\[PBT \_ APMBATTERYLOW peut être utilisé dans les systèmes d’exploitation spécifiés dans la section Configuration requise. la prise en charge de cet événement a été supprimée dans Windows Vista. Utilisez [PBT \_ APMPOWERSTATUSCHANGE](pbt-apmpowerstatuschange.md) à la place.\]

Avertit les applications que la puissance de la batterie est faible.

Une fenêtre reçoit cet événement par le biais du message [**WM \_ POWERBROADCAST**](wm-powerbroadcast.md) . Les paramètres *wParam* et *lParam* sont définis comme suit.


```C++
LRESULT 
CALLBACK 
WindowProc( HWND   hwnd,    // handle to window
            UINT   uMsg,    // WM_POWERBROADCAST
            WPARAM wParam,  // PBT_APMBATTERYLOW
            LPARAM lParam); // zero
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*HWND* 
</dt> <dd>

Handle de la fenêtre.

</dd> <dt>*uMsg*</dt> <dd> 

| Valeur                                                                                                                                                                                                                                                                   | Signification                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| <span id="WM_POWERBROADCAST"></span><span id="wm_powerbroadcast"></span><dl> <dt>**[**WM \_ POWERBROADCAST**](wm-powerbroadcast.md)**</dt> <dt>536 (0x218)</dt> </dl> | Identificateur du message.<br/> |



 

</dd> <dt>*wParam*</dt> <dd> 

| Valeur                                                                                                                                                                                                                                  | Signification                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------|
| <span id="PBT_APMBATTERYLOW"></span><span id="pbt_apmbatterylow"></span><dl> <dt>**PBT \_ APMBATTERYLOW**</dt> <dt>9 (0x9)</dt> </dl> | Identificateur d’événement.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Réservé, doit être égal à zéro.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Pas de valeur de retour.

## <a name="remarks"></a>Remarques

Cet événement est diffusé quand le BIOS APM d’un système signale une notification Low de batterie APM faible. Étant donné que certaines implémentations du BIOS APM ne fournissent pas de notifications lorsque les batteries sont faibles, cet événement peut ne jamais être diffusé sur certains ordinateurs.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>                                                              |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                                     |
| Fin de la prise en charge des clients<br/>    | Windows XP<br/>                                                                                    |
| Fin de la prise en charge des serveurs<br/>    | Windows Server 2003<br/>                                                                           |
| En-tête<br/>                   | <dl> <dt>WinUser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Événements de gestion de l’alimentation](power-management-events.md)
</dt> <dt>

[**\_POWERBROADCAST WM**](wm-powerbroadcast.md)
</dt> </dl>

 

 




