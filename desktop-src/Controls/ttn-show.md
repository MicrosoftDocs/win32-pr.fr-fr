---
title: TTN_SHOW le code de notification (commctrl. h)
description: Notifie la fenêtre propriétaire qu’un contrôle ToolTip est sur le présent affiché. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: ddfd18cd-0681-4e4a-b258-873f98da7479
keywords:
- TTN_SHOW les contrôles de Windows de code de notification
topic_type:
- apiref
api_name:
- TTN_SHOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16acb41d1145c176799dd7997b56a850bb45ece7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127115750"
---
# <a name="ttn_show-notification-code"></a>TTN \_ afficher le code de notification

Notifie la fenêtre propriétaire qu’un contrôle ToolTip est sur le présent affiché. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .


```C++
TTN_SHOW

    pnmh = (LPNMHDR) lParam; 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) .

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

[Version 4,70](common-control-versions.md). Pour afficher l’info-bulle dans son emplacement par défaut, retournez zéro. Pour personnaliser la position de l’info-bulle, repositionnez la fenêtre d’info-bulle avec la fonction [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) et retournez la **valeur true**.

> [!Note]  
> Pour les versions antérieures à 4,70, il n’y a aucune valeur de retour.

 

## <a name="remarks"></a>Notes

Un rectangle de fenêtre d’info-bulle est un peu plus grand que son rectangle d’affichage de texte, et son origine est décalée vers le haut et vers la gauche. Si vous devez positionner avec précision le rectangle d’affichage du texte d’une info-bulle, le message [**atténuation \_ ADJUSTRECT**](ttm-adjustrect.md) convertit un rectangle d’affichage de texte dans le rectangle de fenêtre d’info-bulle correspondant et vice versa.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

