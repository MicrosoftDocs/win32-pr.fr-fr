---
title: Code de notification NM_KEYDOWN (barre d’outils) (commctrl. h)
description: 'Code de notification NM_KEYDOWN (barre d’outils) : envoyé par un contrôle lorsque le contrôle a le focus clavier et que l’utilisateur appuie sur une touche. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.'
ms.assetid: bdfcf9da-118b-4fe6-9a0a-6329eb9196ef
keywords:
- NM_KEYDOWN (barre d’outils) code de notification Windows les contrôles
topic_type:
- apiref
api_name:
- NM_KEYDOWN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73a937969b325de881caa97cd2a67d7c11056aa5542d0cd92c751d1ff42a569b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118958128"
---
# <a name="nm_keydown-toolbar-notification-code"></a>\_Code de notification (barre d’outils) de la touche nm

Envoyé par un contrôle lorsque le contrôle a le focus clavier et que l’utilisateur appuie sur une touche. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .


```C++
NM_KEYDOWN

    lpnmk = (LPNMKEY) lParam;
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**NMKEY**](/windows/win32/api/commctrl/ns-commctrl-nmkey) qui contient des informations supplémentaires sur la clé qui a provoqué le code de notification.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur différente de zéro pour empêcher le contrôle de traiter la clé, ou zéro dans le cas contraire.

## <a name="remarks"></a>Remarques

Actuellement, seul le contrôle ToolBar envoie ce code de notification.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





