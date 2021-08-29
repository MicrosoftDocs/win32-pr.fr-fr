---
title: MCN_SELCHANGE le code de notification (commctrl. h)
description: Envoyé par un contrôle Month Calendar lorsque la date ou la plage de dates actuellement sélectionnée change. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 8923524f-d257-409d-bd3e-021684b88856
keywords:
- MCN_SELCHANGE les contrôles de Windows de code de notification
topic_type:
- apiref
api_name:
- MCN_SELCHANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3aa4c1d1f2d4c99ab9980deae4b64dc25fa7caf0818df31d1f160b2b1645d62f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119915019"
---
# <a name="mcn_selchange-notification-code"></a>\_Code de notification MCN selChange

Envoyé par un contrôle Month Calendar lorsque la date ou la plage de dates actuellement sélectionnée change. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .


```C++
MCN_SELCHANGE

    lpNMSelChange = (LPNMSELCHANGE) lParam;
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**NMSELCHANGE**](/windows/win32/api/commctrl/ns-commctrl-nmselchange) qui contient des informations sur la plage de dates actuellement sélectionnée.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Pas de valeur de retour.

## <a name="remarks"></a>Remarques

Par exemple, le contrôle envoie MCN \_ selChange lorsque l’utilisateur modifie explicitement la sélection dans le mois en cours ou lorsque la sélection est implicitement modifiée en réponse à la navigation vers le mois suivant/précédent. Ce code de notification est également envoyé par le système à intervalles réguliers afin que le contrôle puisse répondre aux modifications de date.

Ce code de notification est similaire à [MCN \_ Select](mcn-select.md), mais il est envoyé en réponse à toute modification de sélection. MCN \_ Select est envoyé uniquement pour une sélection de date explicite.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





