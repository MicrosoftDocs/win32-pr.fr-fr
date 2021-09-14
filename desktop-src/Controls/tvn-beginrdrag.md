---
title: TVN_BEGINRDRAG le code de notification (commctrl. h)
description: Avertit une fenêtre parente d’un contrôle Tree-View à propos de l’initiation d’une opération de glisser-déplacer impliquant le bouton droit de la souris. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 4a61d8b5-ceb9-46a3-95ef-27e843e8c986
keywords:
- TVN_BEGINRDRAG les contrôles de Windows de code de notification
topic_type:
- apiref
api_name:
- TVN_BEGINRDRAG
- TVN_BEGINRDRAGA
- TVN_BEGINRDRAGW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bec15b5f48d4ed5612778622bb3655ae153c1b9f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127115526"
---
# <a name="tvn_beginrdrag-notification-code"></a>\_Code de notification TVN BEGINRDRAG

Avertit une fenêtre parente d’un contrôle Tree-View à propos de l’initiation d’une opération de glisser-déplacer impliquant le bouton droit de la souris. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .


```C++
TVN_BEGINRDRAG 

    pnmtv = (LPNMTREEVIEW) lParam 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**NMTREEVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) . Le membre **itemNew** est une structure [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) qui contient des informations valides dans les membres **hitem**, **State** et **lParam** sur l’élément à faire glisser. Le membre **ptDrag** spécifie les coordonnées d’écran actuelles de la souris.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

La valeur de retour est ignorée.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **TVN \_ BEGINRDRAGW** (Unicode) et **TVN \_ BEGINRDRAGA** (ANSI)<br/>             |



 

 





