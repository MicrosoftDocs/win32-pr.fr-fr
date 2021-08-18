---
title: Code de notification NM_CHAR (barre d’outils) (commctrl. h)
description: Envoyé par une barre d’outils lorsqu’il reçoit un \_ message WM char. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 7bf0b046-da8e-448f-94e1-62ba0989f7ba
keywords:
- NM_CHAR (barre d’outils) code de notification Windows les contrôles
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
ms.openlocfilehash: a318c7385e9d7205ad0fa159e1f987c5d650d27414eefeed4d915c5544cb4564
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119018937"
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
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

