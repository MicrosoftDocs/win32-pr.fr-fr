---
title: HDN_OVERFLOWCLICK le code de notification (commctrl. h)
description: Envoyé par un contrôle d’en-tête à son parent lorsque l’utilisateur clique sur le bouton de dépassement de capacité de l’en-tête. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 770ae00a-b87f-4de2-b869-2a233f2c493e
keywords:
- Contrôles Windows de code de notification HDN_OVERFLOWCLICK
topic_type:
- apiref
api_name:
- HDN_OVERFLOWCLICK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 911953fcbea785cb7024bc9d0670c8ed33239524
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843670"
---
# <a name="hdn_overflowclick-notification-code"></a>\_Code de notification HDN OVERFLOWCLICK

Envoyé par un contrôle d’en-tête à son parent lorsque l’utilisateur clique sur le bouton de dépassement de capacité de l’en-tête. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .


```C++
HDN_OVERFLOWCLICK

    pNMHeader = (LPNMHEADER) lParam;
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lParam* \[ dans\]
</dt> <dd>

Pointeur vers une structure [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) qui décrit le code de notification. Le processus appelant est chargé d’allouer cette structure, y compris la structure [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) contenue. Définissez les membres de la structure **NMHDR** , y compris le membre de *code* qui doit être défini sur HDN \_ OVERFLOWCLICK.

Définissez le membre **iItem** de la structure [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) sur l’index du premier élément d’en-tête qui n’est pas visible et doit donc être affiché sur un dépassement de capacité.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Pas de valeur de retour.

## <a name="remarks"></a>Notes

Le récepteur de notification convertit **lParam** pour récupérer la structure [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) . **WParam** contient l’ID du contrôle qui envoie la notification.

Ce message est envoyé uniquement lorsque le style de [**\_ dépassement de capacité HDS**](header-control-styles.md) est défini sur le contrôle header.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





