---
title: Code de notification NM_RELEASEDCAPTURE (téléavertisseur) (commctrl. h)
description: Notifie la fenêtre parente d’un contrôle de pagineur que le contrôle a relâché la capture de la souris. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 5ce9c38a-5d37-4ac7-8510-30bc59d85cca
keywords:
- Contrôles Windows de code de notification NM_RELEASEDCAPTURE (téléavertisseur)
topic_type:
- apiref
api_name:
- NM_RELEASEDCAPTURE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0fb1d258d9baa0952e1707e36884a492ff65f99b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843702"
---
# <a name="nm_releasedcapture-pager-notification-code"></a>\_Code de notification RELEASEDCAPTURE nm (téléavertisseur)

Notifie la fenêtre parente d’un contrôle de pagineur que le contrôle a relâché la capture de la souris. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .


```C++
NM_RELEASEDCAPTURE

    lpnmh = (LPNMHDR) lParam; 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) qui contient des informations supplémentaires sur cette notification.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La valeur de retour est ignorée par le contrôle de pagineur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





