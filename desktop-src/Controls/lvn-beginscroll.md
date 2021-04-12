---
title: LVN_BEGINSCROLL le code de notification (commctrl. h)
description: Avertit la fenêtre parente d’un contrôle List-View quand une opération de défilement démarre. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 67123db1-118c-43d7-8511-12a3c4413958
keywords:
- Contrôles Windows de code de notification LVN_BEGINSCROLL
topic_type:
- apiref
api_name:
- LVN_BEGINSCROLL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae09a05525ac6e9f08d8cc7a0b7de6ef51329baa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464406"
---
# <a name="lvn_beginscroll-notification-code"></a>\_Code de notification LVN BEGINSCROLL

Avertit la fenêtre parente d’un contrôle List-View quand une opération de défilement démarre. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .


```C++
LVN_BEGINSCROLL

    pnmLVScroll = (LPNMLVSCROLL) lParam;
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**NMLVSCROLL**](/windows/win32/api/commctrl/ns-commctrl-nmlvscroll) qui contient la position horizontale ou verticale de l’emplacement où l’opération de défilement démarre.

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



 

 





