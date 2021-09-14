---
title: NM_RDBLCLK (onglet) Code de notification (commctrl. h)
description: Notifie la fenêtre parente d’un contrôle onglet sur lequel l’utilisateur a double-cliqué dans le contrôle avec le bouton droit de la souris. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: cdf0df70-e30b-4353-8c2a-26fffa0596c4
keywords:
- NM_RDBLCLK (onglet) code de notification Windows les contrôles
topic_type:
- apiref
api_name:
- NM_RDBLCLK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c4e159e64780f21576aa9e936379c881b32153d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127117873"
---
# <a name="nm_rdblclk-tab-notification-code"></a>\_Code de notification RDBLCLK nm (onglet)

Notifie la fenêtre parente d’un contrôle onglet sur lequel l’utilisateur a double-cliqué dans le contrôle avec le bouton droit de la souris. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .


```C++
NM_RDBLCLK 

    lpnmh = (LPNMHDR) lParam;
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) qui contient des informations supplémentaires sur cette notification.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne une valeur différente de zéro pour ne pas autoriser le traitement par défaut, ou zéro pour autoriser le traitement par défaut.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





