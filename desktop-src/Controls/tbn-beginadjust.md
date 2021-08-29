---
title: TBN_BEGINADJUST le code de notification (commctrl. h)
description: Avertit la fenêtre parente d’une barre d’outils que l’utilisateur a commencé à personnaliser une barre d’outils. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 689aeda3-5051-4422-9e66-64557b263943
keywords:
- TBN_BEGINADJUST les contrôles de Windows de code de notification
topic_type:
- apiref
api_name:
- TBN_BEGINADJUST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9b83d14d82b84e493d47e193542b1d2fdc83ba92ccc53bd4cb383f17436ad1d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119877009"
---
# <a name="tbn_beginadjust-notification-code"></a>\_Code de notification TBN BEGINADJUST

Avertit la fenêtre parente d’une barre d’outils que l’utilisateur a commencé à personnaliser une barre d’outils. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .


```C++
TBN_BEGINADJUST 

    lpnmhdr = (LPNMHDR) lParam; 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) qui contient des informations sur le code de notification.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Pas de valeur de retour.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





