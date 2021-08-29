---
description: Avertit les applications que le système a repris l’opération après avoir été suspendue.
ms.assetid: 9058a2ff-9b8e-48e5-accb-4810c8598294
title: Événement PBT_APMRESUMESUSPEND (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c065d7997a152555cbd77153752cbaec77786aea5b95486ccf73985cc854ae0b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119961699"
---
# <a name="pbt_apmresumesuspend-event"></a>\_Événement PBT APMRESUMESUSPEND

Avertit les applications que le système a repris l’opération après avoir été suspendue.

Une fenêtre reçoit cet événement par le biais du message [**WM \_ POWERBROADCAST**](wm-powerbroadcast.md) . Les paramètres *wParam* et *lParam* sont définis comme suit.


```C++
LRESULT 
CALLBACK 
WindowProc( HWND hwnd,      // handle to window
            UINT uMsg,      // WM_POWERBROADCAST
            WPARAM wParam,  // PBT_APMRESUMESUSPEND
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

| Valeur                                                                                                                                                                                                                                           | Signification                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------|
| <span id="PBT_APMRESUMESUSPEND"></span><span id="pbt_apmresumesuspend"></span><dl> <dt>**PBT \_ APMRESUMESUSPEND**</dt> <dt>7 (0x7)</dt> </dl> | Identificateur d’événement.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Réservé doit être égal à zéro.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Pas de valeur de retour.

## <a name="remarks"></a>Remarques

Une application peut recevoir cet événement uniquement si elle a reçu l’événement [PBT \_ APMSUSPEND](pbt-apmsuspend.md) avant la suspension de l’ordinateur. Dans le cas contraire, l’application recevra un événement [PBT \_ APMRESUMECRITICAL](pbt-apmresumecritical.md) .

Si le système sort de veille en raison de l’activité de l’utilisateur (par exemple, en appuyant sur le bouton d’alimentation) ou si le système détecte l’interaction de l’utilisateur au niveau de la console physique (par exemple, la souris ou l’entrée au clavier) après l’éveil sans assistance, le système diffuse d’abord l’événement [ \_ APMRESUMEAUTOMATIC PBT](pbt-apmresumeautomatic.md) , puis diffuse l' \_ événement PBT APMRESUMESUSPEND En outre, le système active l’affichage. Votre application doit rouvrir les fichiers qu’elle a fermés lorsque le système est passé en mode veille et se prépare à l’entrée utilisateur.

Si le système sort de veille en raison d’un signal de réveil externe (éveil à distance), le système diffuse uniquement l’événement [PBT \_ APMRESUMEAUTOMATIC](pbt-apmresumeautomatic.md) . L' \_ événement PBT APMRESUMESUSPEND n’est pas envoyé.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>                                                              |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>WinUser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Événements de mise en éveil du système](system-wake-up-events.md)
</dt> <dt>

[Événements de gestion de l’alimentation](power-management-events.md)
</dt> <dt>

[PBT \_ APMSUSPEND](pbt-apmsuspend.md)
</dt> <dt>

[PBT \_ APMRESUMECRITICAL](pbt-apmresumecritical.md)
</dt> <dt>

[**\_POWERBROADCAST WM**](wm-powerbroadcast.md)
</dt> </dl>

 

 




