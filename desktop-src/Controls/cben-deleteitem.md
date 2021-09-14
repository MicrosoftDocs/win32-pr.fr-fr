---
title: CBEN_DELETEITEM le code de notification (commctrl. h)
description: Envoyé lorsqu’un élément a été supprimé. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 8b0d03ff-57fa-44dc-ab3e-05089b876e3c
keywords:
- CBEN_DELETEITEM les contrôles de Windows de code de notification
topic_type:
- apiref
api_name:
- CBEN_DELETEITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4c7ca7329898c9dd0c6bba76cba9d3524b017e3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127123874"
---
# <a name="cben_deleteitem-notification-code"></a>\_Code de notification CBEN DELETEITEM

Envoyé lorsqu’un élément a été supprimé. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .


```C++
CBEN_DELETEITEM

    pCBEx = (PNMCOMBOBOXEX) lParam;
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**NMCOMBOBOXEX**](/windows/desktop/api/Commctrl/ns-commctrl-nmcomboboxexa) qui contient des informations sur le code de notification et l’élément supprimé.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

L’application traitant ce code de notification doit retourner zéro.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





