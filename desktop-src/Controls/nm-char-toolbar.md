---
title: Code de notification NM_CHAR (barre d’outils) (commctrl. h)
description: Envoyé par une barre d’outils lorsqu’il reçoit un \_ message WM char. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 7bf0b046-da8e-448f-94e1-62ba0989f7ba
keywords:
- Contrôles Windows de code de notification NM_CHAR (barre d’outils)
topic_type:
- apiref
api_name:
- NM_CHAR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5a68cb85130f22c8cda63920ada974453a36991
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844469"
---
# <a name="nm_char-toolbar-notification-code"></a>\_Code de notification nm caractère (barre d’outils)

Envoyé par une barre d’outils lorsqu’il reçoit un message [**WM \_ char**](/windows/desktop/inputdev/wm-char) . Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .


```C++
NM_CHAR

    lpnmc = (LPNMCHAR) lParam;
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**NMCHAR**](/windows/win32/api/commctrl/ns-commctrl-nmchar) qui contient des informations supplémentaires sur le caractère qui a provoqué le code de notification. Le membre **dwItemPrev** de cette structure contient l’identificateur de commande de l’élément qui est actuellement chaud ou-1 si aucun élément n’est actuellement chaud. Le membre **dwItemNext** de cette structure contient l’identificateur de commande de l’élément qui devient actif ou-1 si la clé ne correspond pas à l’accélérateur d’un élément.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la **valeur true** pour indiquer que la barre d’outils ne doit pas traiter le caractère et **false** pour que la barre d’outils traite le caractère.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

