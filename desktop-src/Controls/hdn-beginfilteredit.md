---
title: HDN_BEGINFILTEREDIT le code de notification (commctrl. h)
description: Avertit la fenêtre parente d’un contrôle header qu’une modification de filtre a commencé. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 93964453-bb94-4127-8ed4-41acb226b8e2
keywords:
- HDN_BEGINFILTEREDIT les contrôles de Windows de code de notification
topic_type:
- apiref
api_name:
- HDN_BEGINFILTEREDIT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0527427752b5621e626add17d61e60a675958f42
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126999941"
---
# <a name="hdn_beginfilteredit-notification-code"></a>\_Code de notification HDN BEGINFILTEREDIT

Avertit la fenêtre parente d’un contrôle header qu’une modification de filtre a commencé. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .


```C++
HDN_BEGINFILTEREDIT

   pNMHeader = (LPNMHEADER) lParam;
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) qui contient des informations supplémentaires sur le filtre en cours de modification.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Pas de valeur de retour.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





