---
title: DTN_WMKEYDOWN le code de notification (commctrl. h)
description: Envoyé par un contrôle de sélecteur de date et heure (PAO) lorsque l’utilisateur tape dans un champ de rappel. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: e67e222d-28a1-4d30-ae64-8ec9a62fa321
keywords:
- DTN_WMKEYDOWN les contrôles de Windows de code de notification
topic_type:
- apiref
api_name:
- DTN_WMKEYDOWN
- DTN_WMKEYDOWNA
- DTN_WMKEYDOWNW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce2e7d0761308805746278d2f542f5e9458b56d5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127195715"
---
# <a name="dtn_wmkeydown-notification-code"></a>\_Code de notification DTN WMKEYDOWN

Envoyé par un contrôle de sélecteur de date et heure (PAO) lorsque l’utilisateur tape dans un champ de rappel. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .


```C++
DTN_WMKEYDOWN

    lpDTKeystroke = (LPNMDATETIMEWMKEYDOWN)lParam;
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**NMDATETIMEWMKEYDOWN**](/windows/win32/api/commctrl/ns-commctrl-nmdatetimewmkeydowna) contenant des informations sur cette instance du code de notification. La structure comprend des informations sur la clé tapée par l’utilisateur, la sous-chaîne qui définit le champ de rappel et la date et l’heure système actuelles.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Le propriétaire du contrôle doit retourner zéro.

## <a name="remarks"></a>Notes

La gestion de ce code de notification permet au propriétaire du contrôle de fournir des réponses spécifiques aux séquences de touches dans les champs de rappel du contrôle.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **DTN \_ WMKEYDOWNW** (Unicode) et **DTN \_ WMKEYDOWNA** (ANSI)<br/>               |



 

 





