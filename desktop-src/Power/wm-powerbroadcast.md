---
description: Avertit les applications qu’un événement de gestion de l’alimentation s’est produit.
ms.assetid: 46452909-ac0e-4c06-8542-0b94d00e6556
title: Message WM_POWERBROADCAST (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82f1b273462d8de27c19d715836d168ab8bf8c90
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104529097"
---
# <a name="wm_powerbroadcast-message"></a>\_Message WM POWERBROADCAST

Avertit les applications qu’un événement de gestion de l’alimentation s’est produit.

Une fenêtre reçoit ce message par le biais de sa fonction **WindowProc** .


```C++
LRESULT CALLBACK WindowProc(
  HWND   hwnd,    // handle to window
  UINT   uMsg,    // WM_POWERBROADCAST
  WPARAM wParam,  // power-management event
  LPARAM lParam   // function-specific data
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*HWND* 
</dt> <dd>

Handle de fenêtre.

</dd> <dt>*uMsg*</dt> <dd> 

| Valeur                                                                                                                                                                                                                                          | Signification                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| <span id="WM_POWERBROADCAST"></span><span id="wm_powerbroadcast"></span><dl> * * * * <dt>WM \_ POWERBROADCAST * *</dt> * * <dt>536 (0x218)</dt> </dl> | Identificateur du message.<br/> |



 

</dd> <dt>

*wParam* 
</dt> <dd>

Événement de gestion de l’alimentation. Ce paramètre peut être l’un des identificateurs d’événements suivants.



| Événement                                                                                                                                                                                                                                                                                        | Signification                                                                                                                                                                                                     |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PBT_APMPOWERSTATUSCHANGE"></span><span id="pbt_apmpowerstatuschange"></span><dl> <dt>**[PBT \_ APMPOWERSTATUSCHANGE](pbt-apmpowerstatuschange.md)**</dt> <dt>10 (0xA)</dt> </dl> | L’état de l’alimentation a changé.<br/>                                                                                                                                                                        |
| <span id="PBT_APMRESUMEAUTOMATIC"></span><span id="pbt_apmresumeautomatic"></span><dl> <dt>**[PBT \_ APMRESUMEAUTOMATIC](pbt-apmresumeautomatic.md)**</dt> <dt>18 (0x12)</dt> </dl>        | L’opération reprend automatiquement à partir d’un état de faible consommation d’énergie. Ce message est envoyé à chaque reprise du système.<br/>                                                                                  |
| <span id="PBT_APMRESUMESUSPEND"></span><span id="pbt_apmresumesuspend"></span><dl> <dt>**[PBT \_ APMRESUMESUSPEND](pbt-apmresumesuspend.md)**</dt> <dt>7 (0x7)</dt> </dl>                  | L’opération reprend à partir d’un état de faible consommation d’énergie. Ce message est envoyé après [PBT \_ APMRESUMEAUTOMATIC](pbt-apmresumeautomatic.md) si la reprise est déclenchée par une entrée utilisateur, par exemple en appuyant sur une touche.<br/> |
| <span id="PBT_APMSUSPEND"></span><span id="pbt_apmsuspend"></span><dl> <dt>**[PBT \_ APMSUSPEND](pbt-apmsuspend.md)**</dt> <dt>4 (0x4)</dt> </dl>                                          | Le système interrompt l’opération.<br/>                                                                                                                                                                  |
| <span id="PBT_POWERSETTINGCHANGE"></span><span id="pbt_powersettingchange"></span><dl> <dt>**[PBT \_ POWERSETTINGCHANGE](pbt-powersettingchange.md)**</dt> <dt>32787 (0x8013)</dt> </dl>   | Un événement de modification du paramètre d’alimentation a été reçu. <br/>                                                                                                                                                 |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Données spécifiques à l’événement. Pour la plupart des événements, ce paramètre est réservé et n’est pas utilisé.

Si le paramètre *wParam* est [PBT \_ POWERSETTINGCHANGE](pbt-powersettingchange.md), le paramètre *lParam* est un pointeur vers une structure de [**\_ paramètre POWERBROADCAST**](/windows/desktop/api/WinUser/ns-winuser-powerbroadcast_setting) .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Une application doit retourner la **valeur true** si elle traite ce message.

## <a name="remarks"></a>Notes

Le système envoie toujours un message [PBT \_ APMRESUMEAUTOMATIC](pbt-apmresumeautomatic.md) à chaque reprise du système. Si le système reprend en réponse à une entrée utilisateur, par exemple en appuyant sur une touche, le système envoie également un message **PBT \_ APMRESUMESUSPEND** après l’envoi de \_ APMRESUMEAUTOMATIC PBT.

**WM \_** Les messages POWERBROADCAST ne font pas la distinction entre les différents États de faible consommation d’énergie. Une application peut déterminer uniquement que le système entre dans un état de faible consommation d’énergie. il ne peut pas déterminer l’état d’alimentation spécifique. Le système enregistre des détails sur les transitions d’état d’alimentation dans le journal des événements système de Windows.

Pour empêcher le système de passer à un état de faible consommation dans Windows Vista, une application doit appeler [**SetThreadExecutionState**](/windows/desktop/api/Winbase/nf-winbase-setthreadexecutionstate) pour informer le système qu’elle est en cours d’utilisation.

Les messages suivants ne sont pas pris en charge sur les systèmes d’exploitation spécifiés dans la section Configuration requise :

- PBT_APMQUERYSTANDBY  
- PBT_APMQUERYSTANDBYFAILED  
- PBT_APMSTANDBY  
- PBT_APMRESUMESTANDBY  

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows XP uniquement\]<br/>                                                              |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>WinUser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[\_Messages WM POWERBROADCAST](wm-powerbroadcast-messages.md)
</dt> <dt>

[Messages de gestion de l’alimentation](power-management-messages.md)
</dt> </dl>

 

 




