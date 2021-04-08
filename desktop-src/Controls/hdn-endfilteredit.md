---
title: HDN_ENDFILTEREDIT le code de notification (commctrl. h)
description: Avertit la fenêtre parente d’un contrôle header qu’une modification de filtre est terminée. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: d3832875-4cde-4d8a-b3a4-a8dae0742c56
keywords:
- Contrôles Windows de code de notification HDN_ENDFILTEREDIT
topic_type:
- apiref
api_name:
- HDN_ENDFILTEREDIT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f5a557278598600f1bd11ebfbe791691de954a9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103744012"
---
# <a name="hdn_endfilteredit-notification-code"></a>\_Code de notification HDN ENDFILTEREDIT

Avertit la fenêtre parente d’un contrôle header qu’une modification de filtre est terminée. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .


```C++
HDN_ENDFILTEREDIT

   pNMHeader = (LPNMHEADER) lParam;
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) qui contient des informations supplémentaires sur le filtre en cours de modification.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Pas de valeur de retour.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





