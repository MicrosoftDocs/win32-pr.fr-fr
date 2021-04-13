---
title: Code de notification NM_TOOLTIPSCREATED (barre d’outils) (commctrl. h)
description: Avertit la fenêtre parente d’une barre d’outils que la barre d’outils a créé un contrôle ToolTip. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 0e9517c1-aa3f-4b14-82b4-195a4ce99757
keywords:
- Contrôles Windows de code de notification NM_TOOLTIPSCREATED (barre d’outils)
topic_type:
- apiref
api_name:
- NM_TOOLTIPSCREATED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c13366348da075fab48e7a2f12381f51f7d87bf4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464871"
---
# <a name="nm_tooltipscreated-toolbar-notification-code"></a>\_Code de notification TOOLTIPSCREATED nm (barre d’outils)

Avertit la fenêtre parente d’une barre d’outils que la barre d’outils a créé un contrôle ToolTip. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .


```C++
NM_TOOLTIPSCREATED

    lpnmttc = (LPNMTOOLTIPSCREATED) lParam; 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**NMTOOLTIPSCREATED**](/windows/win32/api/commctrl/ns-commctrl-nmtooltipscreated) qui contient des informations supplémentaires sur cette notification.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Le contrôle ToolBar ignore la valeur de retour de ce code de notification.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





