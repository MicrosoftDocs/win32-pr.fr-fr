---
title: MCN_GETDAYSTATE le code de notification (commctrl. h)
description: Envoyé par un contrôle Month Calendar pour demander des informations sur le mode d’affichage des jours individuels. Ce code de notification n’est envoyé que par les contrôles de calendrier mensuel qui utilisent le \_ style MCS DAYSTATE et il est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: dc2608e0-c598-4b26-9195-208f09cd84b7
keywords:
- MCN_GETDAYSTATE les contrôles de Windows de code de notification
topic_type:
- apiref
api_name:
- MCN_GETDAYSTATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64af64fde86ed91ae41cbd3fed53e9cb27a0be410140bc1d25e0548a64042668
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119697139"
---
# <a name="mcn_getdaystate-notification-code"></a>\_Code de notification MCN GETDAYSTATE

Envoyé par un contrôle Month Calendar pour demander des informations sur le mode d’affichage des jours individuels. Ce code de notification n’est envoyé que par les contrôles de calendrier mensuel qui utilisent le style [**MCS \_ DAYSTATE**](month-calendar-control-styles.md) et il est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .


```C++
MCN_GETDAYSTATE

    lpNMDayState = (LPNMDAYSTATE) lParam;
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**NMDAYSTATE**](/windows/win32/api/commctrl/ns-commctrl-nmdaystate) . La structure contient des informations sur le laps de temps pour lequel le contrôle a besoin d’informations et reçoit l’adresse d’un tableau qui fournit ces données.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Pas de valeur de retour.

## <a name="remarks"></a>Remarques

La gestion de ce code de notification permet à votre application de personnaliser son affichage en spécifiant que certains jours s’affichent en gras.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





