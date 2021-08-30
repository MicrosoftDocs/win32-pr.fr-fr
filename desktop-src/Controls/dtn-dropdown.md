---
title: DTN_DROPDOWN le code de notification (commctrl. h)
description: Envoyé par un contrôle de sélecteur de date et heure (PAO) lorsque l’utilisateur active le calendrier du mois de la liste déroulante. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 6f20fa87-2223-4876-b77d-2c684685bf10
keywords:
- DTN_DROPDOWN les contrôles de Windows de code de notification
topic_type:
- apiref
api_name:
- DTN_DROPDOWN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba6c583de68b8a92c8d93990bce84787fa061ec5422ea2c6b32a6a3942b766ef
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119877679"
---
# <a name="dtn_dropdown-notification-code"></a>\_Code de notification de liste déroulante DTN

Envoyé par un contrôle de sélecteur de date et heure (PAO) lorsque l’utilisateur active le calendrier du mois de la liste déroulante. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .


```C++
DTN_DROPDOWN

    lpNmhdr = (LPNMHDR)lParam;
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) qui contient des informations sur la notification.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La valeur de retour de cette notification n’est pas utilisée.

## <a name="remarks"></a>Remarques

L’une des tâches que votre gestionnaire de notification peut avoir à effectuer consiste à personnaliser le contrôle de mois-calendrier déroulant. Par exemple, si vous ne souhaitez pas « atteindre aujourd’hui », vous devez définir le style [**MCS \_ notoday**](month-calendar-control-styles.md)  du contrôle. Pour récupérer un handle pour le contrôle Month-Calendar, envoyez au contrôle de PAO un message [**DTM \_ GETMONTHCAL**](dtm-getmonthcal.md) . Vous pouvez ensuite utiliser ce handle et [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) pour définir le style Month-Calendar souhaité.

Les contrôles de PAO ne maintiennent pas un contrôle Month Calendar enfant statique. Le contrôle PAO crée un nouveau contrôle Month Calendar avant d’envoyer ce code de notification. En outre, le contrôle de PAO détruit le contrôle enfant lorsqu’il n’est pas actif (visible). Par conséquent, votre application ne doit pas s’appuyer sur un handle de fenêtre statique pour le calendrier de mois enfant du contrôle.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[DTN \_ gros plan](dtn-closeup.md)
</dt> <dt>

[**DTM \_ GETMONTHCAL**](dtm-getmonthcal.md)
</dt> </dl>

 

