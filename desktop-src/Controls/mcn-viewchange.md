---
title: MCN_VIEWCHANGE le code de notification (commctrl. h)
description: Envoyé par un contrôle Month Calendar lorsque l’affichage actuel change. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: ee35ac1d-9aeb-4d75-9cef-016487f23602
keywords:
- Contrôles Windows de code de notification MCN_VIEWCHANGE
topic_type:
- apiref
api_name:
- MCN_VIEWCHANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: abbcad3fdda355ac2795dbe49a89fa4e7c2c5cad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464530"
---
# <a name="mcn_viewchange-notification-code"></a>\_Code de notification MCN VIEWCHANGE

Envoyé par un contrôle Month Calendar lorsque l’affichage actuel change. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .


```C++
MCN_VIEWCHANGE

    lpNMViewChange = (LPNMVIEWCHANGE) lParam;
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**NMVIEWCHANGE**](/windows/win32/api/commctrl/ns-commctrl-nmviewchange) qui contient des informations sur la vue actuelle.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Pas de valeur de retour.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





