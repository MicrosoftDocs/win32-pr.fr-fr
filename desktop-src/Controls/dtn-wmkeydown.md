---
title: DTN_WMKEYDOWN le code de notification (commctrl. h)
description: Envoyé par un contrôle de sélecteur de date et heure (PAO) lorsque l’utilisateur tape dans un champ de rappel. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: e67e222d-28a1-4d30-ae64-8ec9a62fa321
keywords:
- Contrôles Windows de code de notification DTN_WMKEYDOWN
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103061"
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

## <a name="return-value"></a>Valeur retournée

Le propriétaire du contrôle doit retourner zéro.

## <a name="remarks"></a>Notes

La gestion de ce code de notification permet au propriétaire du contrôle de fournir des réponses spécifiques aux séquences de touches dans les champs de rappel du contrôle.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **DTN \_ WMKEYDOWNW** (Unicode) et **DTN \_ WMKEYDOWNA** (ANSI)<br/>               |



 

 





