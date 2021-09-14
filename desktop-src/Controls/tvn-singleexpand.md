---
title: TVN_SINGLEEXPAND le code de notification (commctrl. h)
description: Envoyé par un contrôle Tree-View avec le \_ style TV SINGLEEXPAND style lorsque l’utilisateur ouvre ou ferme un élément d’arborescence en un seul clic de souris. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: ae738237-172a-400b-b9fe-33832224e299
keywords:
- TVN_SINGLEEXPAND les contrôles de Windows de code de notification
topic_type:
- apiref
api_name:
- TVN_SINGLEEXPAND
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 976c0e8acfee1f024e4ee7f88d9f745e4029ec82
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127115478"
---
# <a name="tvn_singleexpand-notification-code"></a>\_Code de notification TVN SINGLEEXPAND

Envoyé par un contrôle Tree-View avec le style [**TV \_ SINGLEEXPAND**](tree-view-control-window-styles.md) style lorsque l’utilisateur ouvre ou ferme un élément d’arborescence en un seul clic de souris. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .


```C++
TVN_SINGLEEXPAND

    lpnmtv = (LPNMTREEVIEW)lParam;
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**NMTREEVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) qui contient des informations sur ce code de notification.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Return TVNRET \_ Default pour permettre au comportement par défaut de se produire. Pour modifier le comportement par défaut, retournez :



| Code de retour                                                                                    | Description                                                      |
|------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <dl> <dt>**TVNRET \_ SKIPOLD**</dt> </dl> | Ignore le traitement par défaut de l’élément non sélectionné.<br/> |
| <dl> <dt>**TVNRET \_ SKIPNEW**</dt> </dl> | Ignorer le traitement par défaut de l’élément sélectionné.<br/>   |



 

## <a name="remarks"></a>Notes

Pour ignorer le traitement par défaut des éléments sélectionnés et désélectionnés, retournez TVNRET \_ SKIPOLD et TVNRET \_ SKIPNEW en les associant à un or logique.

Ce code de notification est uniquement envoyé par les contrôles d’arborescence avec le style [**TV \_ SINGLEEXPAND**](tree-view-control-window-styles.md) style.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





