---
title: HDN_DIVIDERDBLCLICK le code de notification (commctrl. h)
description: Avertit la fenêtre parente d’un contrôle header que l’utilisateur a double-cliqué sur la zone de séparation du contrôle. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: b722196a-23ae-49c3-b0a2-8fe0d1e33b26
keywords:
- Contrôles Windows de code de notification HDN_DIVIDERDBLCLICK
topic_type:
- apiref
api_name:
- HDN_DIVIDERDBLCLICK
- HDN_DIVIDERDBLCLICKA
- HDN_DIVIDERDBLCLICKW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0129096139a4d698f25de543a2628b473bfd66e2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104033272"
---
# <a name="hdn_dividerdblclick-notification-code"></a>\_Code de notification HDN DIVIDERDBLCLICK

Avertit la fenêtre parente d’un contrôle header que l’utilisateur a double-cliqué sur la zone de séparation du contrôle. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .


```C++
HDN_DIVIDERDBLCLICK

    pNMHeader = (LPNMHEADER) lParam; 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) qui contient des informations sur le contrôle header et l’élément sur lequel l’utilisateur a double-cliqué sur le séparateur.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Pas de valeur de retour.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **HDN \_ DIVIDERDBLCLICKW** (Unicode) et **HDN \_ DIVIDERDBLCLICKA** (ANSI)<br/>   |



 

 





