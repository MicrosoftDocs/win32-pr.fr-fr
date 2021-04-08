---
title: Message LVN_ENDSCROLL (commctrl. h)
description: Avertit la fenêtre parente d’un contrôle List-View quand une opération de défilement se termine. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 2838dcd0-ac0f-48c7-94ba-dc36febedb94
keywords:
- LVN_ENDSCROLL les contrôles de message Windows
topic_type:
- apiref
api_name:
- LVN_ENDSCROLL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b9dcdcff2d0bcfc28e1818d5add6d37838e5f9b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844478"
---
# <a name="lvn_endscroll-message"></a>\_Message LVN ENDSCROLL

Avertit la fenêtre parente d’un contrôle List-View quand une opération de défilement se termine. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .


```C++
LVN_ENDSCROLL

    pnmLVScroll = (LPNMLVSCROLL) lParam;
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**NMLVSCROLL**](/windows/win32/api/commctrl/ns-commctrl-nmlvscroll) qui contient la position horizontale ou verticale de l’emplacement où l’opération de défilement se termine.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Valeur de retour non utilisée.

## <a name="remarks"></a>Notes

> [!Note]  
> Pour utiliser ce code de notification, vous devez fournir un manifeste spécifiant Comclt32.dll version 6,0. Pour plus d’informations sur les manifestes, consultez [activation des styles visuels](cookbook-overview.md).

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





