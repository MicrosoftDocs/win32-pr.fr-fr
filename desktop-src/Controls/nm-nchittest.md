---
title: NM_NCHITTEST le code de notification (commctrl. h)
description: NM_NCHITTEST code de notification-envoyé par un contrôle rebar lorsque le contrôle reçoit un \_ message WM NCHITTEST. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 0e088b14-b912-4f60-9d25-cd0a0ba264c3
keywords:
- NM_NCHITTEST les contrôles de Windows de code de notification
topic_type:
- apiref
api_name:
- NM_NCHITTEST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab16a835e5e321b916f27b6c79141495f3c05cd4ca8e979e77fef50f84e2ca83
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118410690"
---
# <a name="nm_nchittest-notification-code"></a>\_Code de notification NCHITTEST nm

Envoyé par un contrôle rebar lorsque le contrôle reçoit un message [**WM \_ NCHITTEST**](/windows/desktop/inputdev/wm-nchittest) . Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .


```C++
NM_NCHITTEST
        
    lpnmmouse = (LPNMMOUSE) lParam;
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**NMMOUSE**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) qui contient des informations sur le code de notification. Le membre *PT* contient les coordonnées de la souris du message de test de positionnement.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Sauf indication contraire, retourne zéro pour permettre au contrôle d’effectuer le traitement par défaut du message de test de positionnement, ou de retourner l’une des \* valeurs HT documentées sous [**WM \_ NCHITTEST**](/windows/desktop/inputdev/wm-nchittest) pour remplacer le traitement par défaut du test de positionnement.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

