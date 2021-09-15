---
title: LVN_DELETEALLITEMS le code de notification (commctrl. h)
description: Avertit la fenêtre parente d’un contrôle List-View que tous les éléments du contrôle sont sur le côté d’être supprimés. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: e4a219cf-4af9-4d02-8810-f576ba658177
keywords:
- LVN_DELETEALLITEMS les contrôles de Windows de code de notification
topic_type:
- apiref
api_name:
- LVN_DELETEALLITEMS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 583ad6e2372649ab5f63bd208fb97b93b1591c12
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127312585"
---
# <a name="lvn_deleteallitems-notification-code"></a>\_Code de notification LVN DELETEALLITEMS

Avertit la fenêtre parente d’un contrôle List-View que tous les éléments du contrôle sont sur le côté d’être supprimés. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .


```C++
LVN_DELETEALLITEMS

    pnmv = (LPNMLISTVIEW) lParam; 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) . Le membre **iItem** a la valeur-1, et les autres membres sont nuls.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Pour supprimer les codes de notification [LVN \_ DELETEITEM](lvn-deleteitem.md) suivants, retournez la **valeur true**.

Pour recevoir les codes de notification [LVN \_ DELETEITEM](lvn-deleteitem.md) suivants, retournez la **valeur false**.

## <a name="remarks"></a>Remarques

Un contrôle List-View envoie le code de notification [**\_ DELETEALLITEMS LVM**](lvm-deleteallitems.md) lorsqu’il est détruit ou lorsqu’il reçoit le message **\_ DELETEALLITEMS LVM** . Si **LVM \_ DELETEALLITEMS** ne retourne pas la **valeur true**, le contrôle enverra également un code de notification [LVN \_ DELETEITEM](lvn-deleteitem.md) au fur et à mesure que chaque élément sera supprimé.

Si le gestionnaire de messages [**\_ DELETEALLITEMS LVM**](lvm-deleteallitems.md) se trouve dans une procédure de boîte de dialogue, retournez la valeur **true** à partir de la procédure de la boîte de dialogue et utilisez la fonction [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) avec le \_ MSGRESULT DWL pour définir la valeur de retour du message.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

