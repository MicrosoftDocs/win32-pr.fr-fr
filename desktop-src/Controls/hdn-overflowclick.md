---
title: HDN_OVERFLOWCLICK le code de notification (commctrl. h)
description: Envoyé par un contrôle d’en-tête à son parent lorsque l’utilisateur clique sur le bouton de dépassement de capacité de l’en-tête. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 770ae00a-b87f-4de2-b869-2a233f2c493e
keywords:
- HDN_OVERFLOWCLICK les contrôles de Windows de code de notification
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
ms.openlocfilehash: 61cee31369bfa1574ba4690f952bc60fb0dde1e5a9bf2f41e98b659356a79625
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119576219"
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

## <a name="remarks"></a>Remarques

Le récepteur de notification convertit **lParam** pour récupérer la structure [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) . **WParam** contient l’ID du contrôle qui envoie la notification.

Ce message est envoyé uniquement lorsque le style de [**\_ dépassement de capacité HDS**](header-control-styles.md) est défini sur le contrôle header.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





