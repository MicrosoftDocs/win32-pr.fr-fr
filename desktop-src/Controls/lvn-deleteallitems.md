---
title: LVN_DELETEALLITEMS le code de notification (commctrl. h)
description: Avertit la fenêtre parente d’un contrôle List-View que tous les éléments du contrôle sont sur le côté d’être supprimés. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: e4a219cf-4af9-4d02-8810-f576ba658177
keywords:
- Contrôles Windows de code de notification LVN_DELETEALLITEMS
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942924"
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

## <a name="return-value"></a>Valeur retournée

Pour supprimer les codes de notification [LVN \_ DELETEITEM](lvn-deleteitem.md) suivants, retournez la **valeur true**.

Pour recevoir les codes de notification [LVN \_ DELETEITEM](lvn-deleteitem.md) suivants, retournez la **valeur false**.

## <a name="remarks"></a>Notes

Un contrôle List-View envoie le code de notification [**\_ DELETEALLITEMS LVM**](lvm-deleteallitems.md) lorsqu’il est détruit ou lorsqu’il reçoit le message **\_ DELETEALLITEMS LVM** . Si **LVM \_ DELETEALLITEMS** ne retourne pas la **valeur true**, le contrôle enverra également un code de notification [LVN \_ DELETEITEM](lvn-deleteitem.md) au fur et à mesure que chaque élément sera supprimé.

Si le gestionnaire de messages [**\_ DELETEALLITEMS LVM**](lvm-deleteallitems.md) se trouve dans une procédure de boîte de dialogue, retournez la valeur **true** à partir de la procédure de la boîte de dialogue et utilisez la fonction [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) avec le \_ MSGRESULT DWL pour définir la valeur de retour du message.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

