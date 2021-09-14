---
description: Avertit les applications que le système, généralement un ordinateur personnel alimenté par batterie, est sur le même d’entrer en mode suspendu.
ms.assetid: ceaa5ca4-799e-4801-96cd-aeea3dfd7d52
title: Message WM_POWER (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc53fd165ee1cefe8970f85daea04b931a673b33
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127119070"
---
# <a name="wm_power-message"></a>\_Message d’alimentation WM

Avertit les applications que le système, généralement un ordinateur personnel alimenté par batterie, est sur le même d’entrer en mode suspendu.

> [!Note]  
> Le **message \_ d’alimentation WM** est obsolète. elle est fournie uniquement pour la compatibilité avec les applications à base de Windows 16 bits. Les applications doivent utiliser le message [**WM \_ POWERBROADCAST**](wm-powerbroadcast.md) .

 

Une fenêtre reçoit ce message par le biais de sa fonction **WindowProc** .


```C++
LRESULT CALLBACK WindowProc
  HWND   hwnd,    // handle to window
  UINT   uMsg,    // WM_POWER
  WPARAM wParam,  // power-event notification
  LPARAM lParam   // not used
); 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*HWND* 
</dt> <dd>

Handle de fenêtre.

</dd> <dt>

*uMsg* 
</dt> <dd>

Identificateur du message **\_ d’alimentation WM** .

</dd> <dt>

*wParam* 
</dt> <dd>

Notification d’événement d’alimentation. Ce paramètre peut prendre les valeurs suivantes.



| Valeur                                                                                                                                                                        | Signification                                                                                                                                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PWR_CRITICALRESUME"></span><span id="pwr_criticalresume"></span><dl> <dt>**\_CRITICALRESUME PWR**</dt> </dl> | Indique que le système reprend l’opération après avoir entré le mode suspendu sans avoir d’abord diffusé un message de notification **\_ SUSPENDREQUEST PWR** à l’application. Une application doit effectuer les actions de récupération nécessaires.<br/>                                                   |
| <span id="PWR_SUSPENDREQUEST"></span><span id="pwr_suspendrequest"></span><dl> <dt>**\_SUSPENDREQUEST PWR**</dt> </dl> | Indique que le système est sur le paragraphe d’entrer en mode suspendu.<br/>                                                                                                                                                                                                                                 |
| <span id="PWR_SUSPENDRESUME"></span><span id="pwr_suspendresume"></span><dl> <dt>**\_SUSPENDRESUME PWR**</dt> </dl>    | Indique que le système reprend l’opération après avoir entré le mode suspendu normalement, le système diffuse un message de notification **\_ SUSPENDREQUEST PWR** à l’application avant la suspension du système. Une application doit effectuer les actions de récupération nécessaires.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Ce paramètre n'est pas utilisé.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

La valeur retournée par une application dépend de la valeur du paramètre *wParam* . Si *wParam* est **un \_ SUSPENDREQUEST PWR**, la valeur de retour est la valeur **PWR \_ échoue** pour empêcher le système de passer à l’État Suspended ; sinon, il s’agit d’un **PWR \_ OK**. Si *wParam* est **PWR \_ SUSPENDRESUME** ou **PWR \_ CRITICALRESUME**, la valeur de retour est zéro.

## <a name="remarks"></a>Notes

Ce message est diffusé uniquement à une application qui s’exécute sur un système qui est conforme à la spécification BIOS (Advanced Power Management System) de base de la gestion avancée de l’alimentation (APM). Le message est diffusé par le pilote de gestion de l’alimentation à chaque fenêtre retournée par la fonction **EnumWindows** .

Le mode suspendu est l’État dans lequel la plus grande quantité d’économies d’énergie se produit, mais toutes les données et tous les paramètres opérationnels sont conservés. Le contenu de la mémoire vive (RAM) est conservé, mais de nombreux appareils sont susceptibles d’être désactivés.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>                                                              |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>WinUser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_POWERBROADCAST WM**](wm-powerbroadcast.md)
</dt> </dl>

 

 




