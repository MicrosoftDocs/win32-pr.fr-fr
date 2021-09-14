---
title: DTN_CLOSEUP le code de notification (commctrl. h)
description: Envoyé par un contrôle de sélecteur de date et heure (PAO) lorsque l’utilisateur ferme le calendrier du mois déroulant.
ms.assetid: 94ace714-55cc-4c59-8b87-8d0348b15f34
keywords:
- DTN_CLOSEUP les contrôles de Windows de code de notification
topic_type:
- apiref
api_name:
- DTN_CLOSEUP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9cfcfb23215aeffe15bec576075fd4d930790e47
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127006821"
---
# <a name="dtn_closeup-notification-code"></a>\_Code de notification DTN gros plan

Envoyé par un contrôle de sélecteur de date et heure (PAO) lorsque l’utilisateur ferme le calendrier du mois déroulant. Le calendrier du mois est fermé lorsque l’utilisateur choisit une date dans le calendrier du mois ou clique sur la flèche déroulante pendant que le calendrier est ouvert. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .


```C++
DTN_CLOSEUP

    lpNmhdr = (LPMNHDR)lParam;
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) qui contient des informations sur la notification.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

La valeur de retour de cette notification n’est pas utilisée.

## <a name="remarks"></a>Notes

Les contrôles de PAO ne maintiennent pas un contrôle Month Calendar enfant statique. Le contrôle PAO détruit le contrôle Month Calendar enfant avant d’envoyer ce code de notification. Par conséquent, votre application ne doit pas s’appuyer sur un handle de fenêtre statique pour le calendrier de mois enfant du contrôle.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[\_liste déroulante DTN](dtn-dropdown.md)
</dt> <dt>

[**DTM \_ GETMONTHCAL**](dtm-getmonthcal.md)
</dt> </dl>

 

 





