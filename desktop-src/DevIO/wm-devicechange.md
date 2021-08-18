---
description: Avertit une application d’une modification apportée à la configuration matérielle d’un appareil ou de l’ordinateur.
ms.assetid: b64a3983-ee75-4199-9778-1e5b7cec59e4
title: WM_DEVICECHANGE, message (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b32936d36e01a34acc9ace512703db7584768e8b51a9fe06a791b2a285ee2add
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119017797"
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

| Valeur | Signification |
|-------|---------|
| **[DBT \_ DEVNODES \_ modifié](dbt-devnodes-changed.md)**</br>0x0007 | Un appareil a été ajouté ou supprimé du système. |
| **[DBT \_ QUERYCHANGECONFIG](dbt-querychangeconfig.md)**</br>0x0017 | Une autorisation est requise pour modifier la configuration actuelle (ancrer ou détacher). |
| **[DBT \_ CONFIGCHANGED](dbt-configchanged.md)**</br>0x0018 | La configuration actuelle a changé, en raison d’une station d’accueil ou d’une déconnexion. |
| **[DBT \_ CONFIGCHANGECANCELED](dbt-configchangecanceled.md)**</br>0x0019 | Une demande de modification de la configuration actuelle (ancrer ou détacher) a été annulée. |
| **[DBT \_ DEVICEARRIVAL](dbt-devicearrival.md)**</br>0x8000 | Un appareil ou un élément multimédia a été inséré et est maintenant disponible. |
| **[DBT \_ DEVICEQUERYREMOVE](dbt-devicequeryremove.md)**</br>0x8001 | Une autorisation est requise pour supprimer un périphérique ou un élément multimédia. Toute application peut refuser cette demande et annuler la suppression. |
| **[DBT \_ DEVICEQUERYREMOVEFAILED](dbt-devicequeryremovefailed.md)**</br>0x8002 | Une demande de suppression d’un appareil ou d’un élément multimédia a été annulée. |
| **[DBT \_ DEVICEREMOVEPENDING](dbt-deviceremovepending.md)**</br>0x8003 | Un appareil ou un élément multimédia est sur le lieu d’être supprimé. Ne peut pas être refusé. |
| **[DBT \_ DEVICEREMOVECOMPLETE](dbt-deviceremovecomplete.md)**</br>0x8004 | Un appareil ou un élément multimédia a été supprimé. |
| **[DBT \_ DEVICETYPESPECIFIC](dbt-devicetypespecific.md)**</br>0x8005 | Un événement spécifique à l’appareil s’est produit. |
| **[DBT \_ CUSTOMEVENT](dbt-customevent.md)**</br>0x8006 | Un événement personnalisé s’est produit. |
| **[DBT \_ USERDEFINED](dbt-userdefined.md)**</br>0xFFFF | La signification de ce message est définie par l’utilisateur. |

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure qui contient des données spécifiques à l’événement. Son format dépend de la valeur du paramètre *wParam* . Pour plus d’informations, reportez-vous à la documentation de chaque événement.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la **valeur true** pour accorder la demande.

Retourne **la \_ requête \_ de diffusion Deny** pour refuser la demande.

## <a name="remarks"></a>Remarques

Pour les appareils qui offrent des fonctionnalités contrôlables par logiciel, telles que l’éjection et le verrouillage, le système envoie généralement un message [DBT \_ DEVICEREMOVEPENDING](dbt-deviceremovepending.md) pour permettre aux applications et pilotes de périphérique de mettre fin à leur utilisation de l’appareil. Si le système supprime de force un appareil, il ne peut pas envoyer un message [DBT \_ DEVICEQUERYREMOVE](dbt-devicequeryremove.md) .

## <a name="requirements"></a>Configuration requise

| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge | Windows XP |
| Serveur minimal pris en charge | Windows Server 2003|
| En-tête | <dl> <dt>Winuser. h (inclure Windows. h ou Dbt. h)</dt> </dl> |

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
