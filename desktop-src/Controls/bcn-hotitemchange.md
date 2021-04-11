---
title: BCN_HOTITEMCHANGE le code de notification (commctrl. h)
description: Notifie le propriétaire du contrôle de bouton que la souris entre dans la zone cliente du contrôle bouton. Le contrôle Button envoie ce code de notification sous la forme d’un \_ message WM Notify.
ms.assetid: 92882e21-b69d-4326-94e9-ae69a0d00a83
keywords:
- Contrôles Windows de code de notification BCN_HOTITEMCHANGE
topic_type:
- apiref
api_name:
- BCN_HOTITEMCHANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67ba6a7e64e95b45d0883b5adf34b384bccac8c0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032700"
---
# <a name="bcn_hotitemchange-notification-code"></a>\_Code de notification BCN HOTITEMCHANGE

Notifie le propriétaire du contrôle de bouton que la souris entre dans la zone cliente du contrôle bouton. Le contrôle Button envoie ce code de notification sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .


```C++
BCN_HOTITEMCHANGE

    pnmbchotitem = (NMBCHOTITEM*) lParam;
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**NMBCHOTITEM**](/windows/win32/api/commctrl/ns-commctrl-nmbchotitem) .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Ce message ne retourne pas de valeur.

## <a name="remarks"></a>Notes

> [!Note]  
> Pour utiliser ce code de notification, vous devez fournir un manifeste spécifiant Comclt32.dll version 6,0. Pour plus d’informations sur les manifestes, consultez [activation des styles visuels](cookbook-overview.md).

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





