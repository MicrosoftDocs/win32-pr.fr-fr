---
title: UDN_DELTAPOS le code de notification (commctrl. h)
description: Envoyé par le système d’exploitation à la fenêtre parente d’un contrôle up-up lorsque la position du contrôle est sur le point d’être modifiée.
ms.assetid: 66262566-d35a-4b2a-8157-d1e789a21016
keywords:
- Contrôles Windows de code de notification UDN_DELTAPOS
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
ms.openlocfilehash: dec8f0ec2200d1f18e48c068b581b42868db197b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741684"
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

## <a name="remarks"></a>Notes

Le \_ Code de notification UDN DELTAPOS est envoyé avant le message [**WM \_ VSCROLL**](wm-vscroll.md) ou [**WM \_ HSCROLL**](wm-hscroll.md) , qui modifie en fait la position du contrôle. Cela vous permet d’examiner, d’autoriser, de modifier ou d’interdire la modification.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**WM, \_ commande**](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

