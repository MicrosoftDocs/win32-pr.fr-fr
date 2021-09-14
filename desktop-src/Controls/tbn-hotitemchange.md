---
title: TBN_HOTITEMCHANGE le code de notification (commctrl. h)
description: Envoyé par un contrôle de barre d’outils lorsque l’élément réactif (en surbrillance) change. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 49e68e2a-d9c0-463d-954d-34c9adfad62b
keywords:
- TBN_HOTITEMCHANGE les contrôles de Windows de code de notification
topic_type:
- apiref
api_name:
- TBN_HOTITEMCHANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d314a7250128a0f3e6b3fed54e5765487619d8e2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127116289"
---
# <a name="tbn_hotitemchange-notification-code"></a>\_Code de notification TBN HOTITEMCHANGE

Envoyé par un contrôle de barre d’outils lorsque l’élément réactif (en surbrillance) change. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .


```C++
TBN_HOTITEMCHANGE

    lpnmhi = (LPNMTBHOTITEM) lParam;
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**NMTBHOTITEM**](/windows/win32/api/commctrl/ns-commctrl-nmtbhotitem) qui contient des informations sur ce code de notification.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne zéro pour permettre à l’élément d’être mis en surbrillance, ou différent de zéro pour empêcher la mise en surbrillance de l’élément.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





