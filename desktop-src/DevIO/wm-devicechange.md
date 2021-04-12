---
description: Avertit une application d’une modification apportée à la configuration matérielle d’un appareil ou de l’ordinateur.
ms.assetid: b64a3983-ee75-4199-9778-1e5b7cec59e4
title: Message WM_DEVICECHANGE (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f631d75f89f306adc0594a3df6c63d63753e163
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393028"
---
# <a name="wm_devicechange-message"></a>\_Message WM DEVICECHANGE

Avertit une application d’une modification apportée à la configuration matérielle d’un appareil ou de l’ordinateur.

Une fenêtre reçoit ce message par le biais de sa fonction [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
LRESULT CALLBACK WindowProc(HWND   hwnd,     // handle to window
                            UINT   uMsg,     // WM_DEVICECHANGE
                            WPARAM wParam,   // device-change event
                            LPARAM lParam ); // event-specific data
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*HWND* 
</dt> <dd>

Handle de la fenêtre.

</dd> <dt>

*uMsg* 
</dt> <dd>

Identificateur **WM \_ DEVICECHANGE** .

</dd> <dt>

*wParam* 
</dt> <dd>

Événement qui s’est produit. Ce paramètre peut avoir l’une des valeurs suivantes du fichier d’en-tête DBT. h.



| Valeur                                                                                                                                                                                                                                                                                                  | Signification                                                                                                                                |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DBT_CONFIGCHANGECANCELED"></span><span id="dbt_configchangecanceled"></span><dl> <dt>**[DBT \_ CONFIGCHANGECANCELED](dbt-configchangecanceled.md)**</dt> <dt>0x0019</dt> </dl>             | Une demande de modification de la configuration actuelle (ancrer ou détacher) a été annulée.<br/>                                           |
| <span id="DBT_CONFIGCHANGED"></span><span id="dbt_configchanged"></span><dl> <dt>**[DBT \_ CONFIGCHANGED](dbt-configchanged.md)**</dt> <dt>0x0018</dt> </dl>                                         | La configuration actuelle a changé, en raison d’une station d’accueil ou d’une déconnexion.<br/>                                                             |
| <span id="DBT_CUSTOMEVENT"></span><span id="dbt_customevent"></span><dl> <dt>**[DBT \_ CUSTOMEVENT](dbt-customevent.md)**</dt> <dt>0x8006</dt> </dl>                                                 | Un événement personnalisé s’est produit.<br/>                                                                                                |
| <span id="DBT_DEVICEARRIVAL"></span><span id="dbt_devicearrival"></span><dl> <dt>**[DBT \_ DEVICEARRIVAL](dbt-devicearrival.md)**</dt> <dt>0x8000</dt> </dl>                                         | Un appareil ou un élément multimédia a été inséré et est maintenant disponible.<br/>                                                          |
| <span id="DBT_DEVICEQUERYREMOVE"></span><span id="dbt_devicequeryremove"></span><dl> <dt>**[DBT \_ DEVICEQUERYREMOVE](dbt-devicequeryremove.md)**</dt> <dt>0x8001</dt> </dl>                         | Une autorisation est requise pour supprimer un périphérique ou un élément multimédia. Toute application peut refuser cette demande et annuler la suppression.<br/> |
| <span id="DBT_DEVICEQUERYREMOVEFAILED"></span><span id="dbt_devicequeryremovefailed"></span><dl> <dt>**[DBT \_ DEVICEQUERYREMOVEFAILED](dbt-devicequeryremovefailed.md)**</dt> <dt>0x8002</dt> </dl> | Une demande de suppression d’un appareil ou d’un élément multimédia a été annulée.<br/>                                                           |
| <span id="DBT_DEVICEREMOVECOMPLETE"></span><span id="dbt_deviceremovecomplete"></span><dl> <dt>**[DBT \_ DEVICEREMOVECOMPLETE](dbt-deviceremovecomplete.md)**</dt> <dt>0x8004</dt> </dl>             | Un appareil ou un élément multimédia a été supprimé.<br/>                                                                                |
| <span id="DBT_DEVICEREMOVEPENDING"></span><span id="dbt_deviceremovepending"></span><dl> <dt>**[DBT \_ DEVICEREMOVEPENDING](dbt-deviceremovepending.md)**</dt> <dt>0x8003</dt> </dl>                 | Un appareil ou un élément multimédia est sur le lieu d’être supprimé. Ne peut pas être refusé.<br/>                                                        |
| <span id="DBT_DEVICETYPESPECIFIC"></span><span id="dbt_devicetypespecific"></span><dl> <dt>**[DBT \_ DEVICETYPESPECIFIC](dbt-devicetypespecific.md)**</dt> <dt>0x8005</dt> </dl>                     | Un événement spécifique à l’appareil s’est produit.<br/>                                                                                       |
| <span id="DBT_DEVNODES_CHANGED"></span><span id="dbt_devnodes_changed"></span><dl> <dt>**[DBT \_ DEVNODES \_ modifié](dbt-devnodes-changed.md)**</dt> <dt>0x0007</dt> </dl>                            | Un appareil a été ajouté ou supprimé du système.<br/>                                                                      |
| <span id="DBT_QUERYCHANGECONFIG"></span><span id="dbt_querychangeconfig"></span><dl> <dt>**[DBT \_ QUERYCHANGECONFIG](dbt-querychangeconfig.md)**</dt> <dt>0x0017</dt> </dl>                         | Une autorisation est requise pour modifier la configuration actuelle (ancrer ou détacher).<br/>                                               |
| <span id="DBT_USERDEFINED"></span><span id="dbt_userdefined"></span><dl> <dt>**[DBT \_ USERDEFINED](dbt-userdefined.md)**</dt> <dt>0xFFFF</dt> </dl>                                                 | La signification de ce message est définie par l’utilisateur.<br/>                                                                                |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure qui contient des données spécifiques à l’événement. Son format dépend de la valeur du paramètre *wParam* . Pour plus d’informations, reportez-vous à la documentation de chaque événement.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la **valeur true** pour accorder la demande.

Retourne **la \_ requête \_ de diffusion Deny** pour refuser la demande.

## <a name="remarks"></a>Notes

Pour les appareils qui offrent des fonctionnalités contrôlables par logiciel, telles que l’éjection et le verrouillage, le système envoie généralement un message [DBT \_ DEVICEREMOVEPENDING](dbt-deviceremovepending.md) pour permettre aux applications et pilotes de périphérique de mettre fin à leur utilisation de l’appareil. Si le système supprime de force un appareil, il ne peut pas envoyer un message [DBT \_ DEVICEQUERYREMOVE](dbt-devicequeryremove.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows XP<br/>                                                                                             |
| Serveur minimal pris en charge<br/> | Windows Server 2003<br/>                                                                                    |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h ou DBT. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[DBT \_ CONFIGCHANGECANCELED](dbt-configchangecanceled.md)
</dt> <dt>

[DBT \_ CONFIGCHANGED](dbt-configchanged.md)
</dt> <dt>

[DBT \_ CUSTOMEVENT](dbt-customevent.md)
</dt> <dt>

[DBT \_ DEVICEARRIVAL](dbt-devicearrival.md)
</dt> <dt>

[DBT \_ DEVICEQUERYREMOVE](dbt-devicequeryremove.md)
</dt> <dt>

[DBT \_ DEVICEQUERYREMOVEFAILED](dbt-devicequeryremovefailed.md)
</dt> <dt>

[DBT \_ DEVICEREMOVECOMPLETE](dbt-deviceremovecomplete.md)
</dt> <dt>

[DBT \_ DEVICEREMOVEPENDING](dbt-deviceremovepending.md)
</dt> <dt>

[DBT \_ DEVICETYPESPECIFIC](dbt-devicetypespecific.md)
</dt> <dt>

[DBT \_ DEVNODES \_ modifié](dbt-devnodes-changed.md)
</dt> <dt>

[DBT \_ QUERYCHANGECONFIG](dbt-querychangeconfig.md)
</dt> <dt>

[DBT \_ USERDEFINED](dbt-userdefined.md)
</dt> </dl>

 

