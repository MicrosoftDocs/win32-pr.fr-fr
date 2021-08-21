---
description: Avertit les applications que le système a repris l’opération.
ms.assetid: f2997905-26c9-4884-ae79-64df5ce6bc55
title: Événement PBT_APMRESUMECRITICAL (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f13214a97e99954d0649df0647bdf6ee3823b91926c0f2f2dc1212fa780a7b6c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119961706"
---
# <a name="pbt_apmresumecritical-event"></a>\_Événement PBT APMRESUMECRITICAL

\[PBT \_ APMRESUMECRITICAL peut être utilisé dans les systèmes d’exploitation spécifiés dans la section Configuration requise. la prise en charge de cet événement a été supprimée dans Windows Vista. Utilisez [PBT \_ APMRESUMEAUTOMATIC](pbt-apmresumeautomatic.md) à la place.\]

Avertit les applications que le système a repris l’opération. Cet événement peut indiquer que certaines ou toutes les applications n’ont pas reçu d’événement [PBT \_ APMSUSPEND](pbt-apmsuspend.md) . Par exemple, cet événement peut être diffusé après une suspension critique causée par une batterie défectueuse.

Une fenêtre reçoit cet événement par le biais du message [**WM \_ POWERBROADCAST**](wm-powerbroadcast.md) . Les paramètres *wParam* et *lParam* sont définis comme suit.


```C++
LRESULT 
CALLBACK 
WindowProc( HWND   hwnd,    // handle to window
            UINT   uMsg,    // WM_POWERBROADCAST
            WPARAM wParam,  // PBT_APMRESUMECRITICAL
            LPARAM lParam); // zero
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*HWND* 
</dt> <dd>

Handle de fenêtre.

</dd> <dt>*uMsg*</dt> <dd> 

| Valeur                                                                                                                                                                                                                                                                   | Signification                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| <span id="WM_POWERBROADCAST"></span><span id="wm_powerbroadcast"></span><dl> <dt>**[**WM \_ POWERBROADCAST**](wm-powerbroadcast.md)**</dt> <dt>536 (0x218)</dt> </dl> | Identificateur du message.<br/> |



 

</dd> <dt>*wParam*</dt> <dd> 

| Valeur                                                                                                                                                                                                                                              | Signification                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------|
| <span id="PBT_APMRESUMECRITICAL"></span><span id="pbt_apmresumecritical"></span><dl> <dt>**PBT \_ APMRESUMECRITICAL**</dt> <dt>6 (0x6)</dt> </dl> | Identificateur d’événement.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Réservé doit être égal à zéro.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Pas de valeur de retour.

## <a name="remarks"></a>Remarques

Étant donné qu’une suspension critique se produit sans notification préalable, les ressources et les données qui étaient disponibles peuvent ne pas être présentes lorsque l’application reçoit cet événement. L’application doit tenter de restaurer son état au meilleur de sa capacité. Lorsqu’il s’agit d’une suspension critique, le système conserve l’état de la DRAM et des disques durs locaux, mais il peut ne pas conserver les connexions réseau. Une application peut être amenée à agir en ce qui concerne les fichiers qui étaient ouverts sur le réseau avant la suspension critique.

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

[Événements de mise en éveil du système](system-wake-up-events.md)
</dt> <dt>

[Événements de gestion de l’alimentation](power-management-events.md)
</dt> <dt>

[**\_POWERBROADCAST WM**](wm-powerbroadcast.md)
</dt> </dl>

 

 




