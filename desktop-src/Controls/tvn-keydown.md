---
title: TVN_KEYDOWN le code de notification (commctrl. h)
description: Avertit la fenêtre parente d’un contrôle Tree-View que l’utilisateur a appuyé sur une touche et que le contrôle Tree-View a le focus d’entrée. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: da0d2b62-2295-4dce-9b37-a250f3be087f
keywords:
- TVN_KEYDOWN les contrôles de Windows de code de notification
topic_type:
- apiref
api_name:
- TVN_KEYDOWN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ccb18c3bf7dc03056abb55575850821e11eb9bf
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127115490"
---
# <a name="tvn_keydown-notification-code"></a>Code de notification KeyOut TVN \_

Avertit la fenêtre parente d’un contrôle Tree-View que l’utilisateur a appuyé sur une touche et que le contrôle Tree-View a le focus d’entrée. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .


```C++
TVN_KEYDOWN 

    ptvkd = (LPNMTVKEYDOWN) lParam 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**NMTVKEYDOWN**](/windows/win32/api/commctrl/ns-commctrl-nmtvkeydown) . Le membre **wVKey** spécifie le code de la touche virtuelle.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Si le membre **wVKey** de *lParam* est un code de touche de caractères, le caractère sera utilisé dans le cadre d’une recherche incrémentielle. Retourne une valeur différente de zéro pour exclure le caractère de la recherche incrémentielle, ou zéro pour inclure le caractère dans la recherche. Pour toutes les autres clés, la valeur de retour est ignorée.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





