---
title: LVN_COLUMNOVERFLOWCLICK le code de notification (commctrl. h)
description: Envoyé par un contrôle List-View lorsque l’utilisateur clique sur le bouton de dépassement de capacité. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 3d3bb7be-b598-450a-b829-a5aa5b1a0c5d
keywords:
- Contrôles Windows de code de notification LVN_COLUMNOVERFLOWCLICK
topic_type:
- apiref
api_name:
- LVN_COLUMNOVERFLOWCLICK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7938d28be337f7255a9b84422fa090da5a494cc2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479445"
---
# <a name="lvn_columnoverflowclick-notification-code"></a>\_Code de notification LVN COLUMNOVERFLOWCLICK

Envoyé par un contrôle List-View lorsque l’utilisateur clique sur le bouton de dépassement de capacité. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .


```C++
LVN_COLUMNOVERFLOWCLICK
     
    pnmv = (LPNMLISTVIEW) lParam;
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lParam* \[ dans\]
</dt> <dd>

Pointeur vers une structure [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) qui décrit le code de notification. L’appelant est chargé d’allouer cette structure, y compris la structure [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) contenue. Définissez les membres de la structure **NMHDR** . Le membre de **code** doit être défini sur LVN \_ COLUMNOVERFLOWCLICK.

Affectez la valeur-1 au membre **iItem** de la structure [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) . Définissez le membre **iSubItem** sur l’index du sous-élément. Définissez les membres **uNewState**, **uOldState** et **lParam** sur zéro. Les membres restants de la structure **NMLISTVIEW** ne sont pas utilisés.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Pas de valeur de retour.

## <a name="remarks"></a>Notes

Le récepteur de notification convertit *lParam* pour récupérer la structure [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) . Le paramètre *wParam* contient l’ID du contrôle qui envoie le code de notification.

Si un contrôle header est un enfant de ListView, le contrôle header doit envoyer ce code de notification au contrôle ListView lorsque le contrôle header reçoit le code de notification [HDN \_ OVERFLOWCLICK](hdn-overflowclick.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





