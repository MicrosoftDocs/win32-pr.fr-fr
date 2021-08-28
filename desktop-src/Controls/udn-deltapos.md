---
title: UDN_DELTAPOS le code de notification (commctrl. h)
description: Envoyé par le système d’exploitation à la fenêtre parente d’un contrôle up-up lorsque la position du contrôle est sur le point d’être modifiée.
ms.assetid: 66262566-d35a-4b2a-8157-d1e789a21016
keywords:
- UDN_DELTAPOS les contrôles de Windows de code de notification
topic_type:
- apiref
api_name:
- UDN_DELTAPOS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81285d2e0aa5c9a8b65eabf7c5b23d02da3acf02ac13e3274accce340530024f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120088409"
---
# <a name="udn_deltapos-notification-code"></a>\_Code de notification UDN DELTAPOS

Envoyé par le système d’exploitation à la fenêtre parente d’un contrôle up-up lorsque la position du contrôle est sur le point d’être modifiée. Cela se produit lorsque l’utilisateur demande une modification de la valeur en appuyant sur la flèche haut ou bas du contrôle. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .


```C++
UDN_DELTAPOS 

    lpnmud = (LPNMUPDOWN) lParam;
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**NMUPDOWN**](/windows/win32/api/commctrl/ns-commctrl-nmupdown) qui contient des informations sur la modification de la position. Le membre **IPOS** de cette structure contient la position actuelle du contrôle. Le membre **iDelta** de la structure est un entier signé qui contient la modification de position proposée. Si l’utilisateur a cliqué sur le bouton haut, il s’agit d’une valeur positive. Si l’utilisateur a cliqué sur le bouton enfoncé, il s’agit d’une valeur négative.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur différente de zéro pour empêcher la modification de la position du contrôle, ou zéro pour autoriser la modification.

## <a name="remarks"></a>Remarques

Le \_ Code de notification UDN DELTAPOS est envoyé avant le message [**WM \_ VSCROLL**](wm-vscroll.md) ou [**WM \_ HSCROLL**](wm-hscroll.md) , qui modifie en fait la position du contrôle. Cela vous permet d’examiner, d’autoriser, de modifier ou d’interdire la modification.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**WM, \_ commande**](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

