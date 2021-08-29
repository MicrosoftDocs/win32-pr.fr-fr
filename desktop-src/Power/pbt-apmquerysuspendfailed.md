---
description: Notifie les applications que l’autorisation de suspendre l’ordinateur a été refusée.
ms.assetid: 0f68628f-9d38-45ca-9487-95bf62075e00
title: Événement PBT_APMQUERYSUSPENDFAILED (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4151829d2c00fc8d4577fb8a7231111df09eb1326985f274d4dcc9e8986b2b86
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119143362"
---
# <a name="pbt_apmquerysuspendfailed-event"></a>\_Événement PBT APMQUERYSUSPENDFAILED

\[PBT \_ APMQUERYSUSPENDFAILED peut être utilisé dans les systèmes d’exploitation spécifiés dans la section Configuration requise. la prise en charge de cet événement a été supprimée dans Windows Vista. Utilisez [**SetThreadExecutionState**](/windows/desktop/api/Winbase/nf-winbase-setthreadexecutionstate) à la place.\]

Notifie les applications que l’autorisation de suspendre l’ordinateur a été refusée. Cet événement est diffusé si une application ou un pilote retournait une **requête de diffusion \_ \_ Deny** à un événement [ \_ APMQUERYSUSPEND PBT](pbt-apmquerysuspend.md) précédent.

Une fenêtre reçoit cet événement par le biais du message [**WM \_ POWERBROADCAST**](wm-powerbroadcast.md) . Les paramètres *wParam* et *lParam* sont définis comme suit.


```C++
LRESULT 
CALLBACK 
WindowProc( HWND   hwnd,    // handle to window
            UINT   uMsg,    // WM_POWERBROADCAST
            WPARAM wParam,  // PBT_APMQUERYSUSPENDFAILED
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

| Valeur                                                                                                                                                                                                                                                          | Signification                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------|
| <span id="PBT_APMQUERYSUSPENDFAILED"></span><span id="pbt_apmquerysuspendfailed"></span><dl> <dt>**PBT \_ APMQUERYSUSPENDFAILED**</dt> <dt>2 (0X2)</dt> </dl> | Identificateur d’événement.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Réservé doit être égal à zéro.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Pas de valeur de retour.

## <a name="remarks"></a>Remarques

Les applications répondent généralement à cet événement en reprenant le fonctionnement normal.

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

[Gestion de l’alimentation](power-management-portal.md)
</dt> <dt>

[Événements de gestion de l’alimentation](power-management-events.md)
</dt> <dt>

[PBT \_ APMQUERYSUSPEND](pbt-apmquerysuspend.md)
</dt> <dt>

[**\_POWERBROADCAST WM**](wm-powerbroadcast.md)
</dt> </dl>

 

 




