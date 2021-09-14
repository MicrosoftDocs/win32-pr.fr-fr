---
title: DTN_USERSTRING le code de notification (commctrl. h)
description: Envoyé par un contrôle de sélecteur de date et heure (PAO) lorsqu’un utilisateur termine la modification d’une chaîne dans le contrôle.
ms.assetid: a5b13582-323b-4804-912c-a988d902547d
keywords:
- DTN_USERSTRING les contrôles de Windows de code de notification
topic_type:
- apiref
api_name:
- DTN_USERSTRING
- DTN_USERSTRINGA
- DTN_USERSTRINGW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4878875d23a0a5fce95aa4cc9ebfedfbdf24cb93
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127195716"
---
# <a name="dtn_userstring-notification-code"></a>\_Code de notification DTN USERSTRING

Envoyé par un contrôle de sélecteur de date et heure (PAO) lorsqu’un utilisateur termine la modification d’une chaîne dans le contrôle. Ce code de notification est uniquement envoyé par les contrôles de PAO définis sur le style [**DTS \_ APPCANPARSE**](date-and-time-picker-control-styles.md) . Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .


```C++
DTN_USERSTRING

    lpDTstring = (LPNMDATETIMESTRING) lParam;
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**NMDATETIMESTRING**](/windows/win32/api/commctrl/ns-commctrl-nmdatetimestringa) qui contient des informations sur l’instance du code de notification.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Le propriétaire du contrôle doit retourner zéro.

## <a name="remarks"></a>Notes

La gestion de ce code de notification permet au propriétaire de fournir des réponses personnalisées aux chaînes entrées dans le contrôle par l’utilisateur. Le propriétaire doit être prêt à analyser la chaîne d’entrée et à agir si nécessaire.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **DTN \_ USERSTRINGW** (Unicode) et **DTN \_ USERSTRINGA** (ANSI)<br/>             |



 

 





