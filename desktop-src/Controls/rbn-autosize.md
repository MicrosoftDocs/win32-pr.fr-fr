---
title: RBN_AUTOSIZE le code de notification (commctrl. h)
description: Envoyé par un contrôle rebar créé avec le \_ style RBS AutoSize quand le rebar se redimensionne automatiquement. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: d174fe99-13cc-404c-9dc5-d5a93e9807a2
keywords:
- Contrôles Windows de code de notification RBN_AUTOSIZE
topic_type:
- apiref
api_name:
- RBN_AUTOSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18ecfac5a4f84d69d444c25a24956cb911fd90a4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510366"
---
# <a name="rbn_autosize-notification-code"></a>\_Code de notification de REdimensionnement automatique RBN

Envoyé par un contrôle rebar créé avec le style [**RBS \_ AutoSize**](rebar-control-styles.md) quand le rebar se redimensionne automatiquement. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .


```C++
RBN_AUTOSIZE

    lpnmas = (LPNMRBAUTOSIZE) lParam;
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**NMRBAUTOSIZE**](/windows/win32/api/commctrl/ns-commctrl-nmrbautosize) qui contient des informations sur l’opération de redimensionnement.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La valeur de retour de cette notification n’est pas utilisée.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





