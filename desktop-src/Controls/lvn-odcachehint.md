---
title: LVN_ODCACHEHINT le code de notification (commctrl. h)
description: Envoyé par un contrôle List-View virtuel lorsque le contenu de sa zone d’affichage a changé.
ms.assetid: 2fac6a16-f65e-402f-9295-f2beb23db924
keywords:
- Contrôles Windows de code de notification LVN_ODCACHEHINT
topic_type:
- apiref
api_name:
- LVN_ODCACHEHINT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 827ad81b6ebb66a4fbe5c1a3b283175818b99e98
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942918"
---
# <a name="lvn_odcachehint-notification-code"></a>\_Code de notification LVN ODCACHEHINT

Envoyé par un contrôle List-View virtuel lorsque le contenu de sa zone d’affichage a changé. Par exemple, un contrôle List-View envoie ce code de notification lorsque l’utilisateur fait défiler l’affichage du contrôle. Le \_ Code de notification LVN ODCACHEHINT est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .


```C++
LVN_ODCACHEHINT

    pCachehint = (NMLVCACHEHINT *) lParam;
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**NMLVCACHEHINT**](/windows/win32/api/commctrl/ns-commctrl-nmlvcachehint) contenant des informations sur la plage d’éléments à mettre en cache.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

L’application recevant ce code de notification doit retourner zéro.

## <a name="remarks"></a>Notes

La gestion de ce message permet à l’application de mettre à jour les informations d’élément conservées dans le cache afin qu’elles soient facilement disponibles lorsqu’un code de notification [LVN \_ GETDISPINFO](lvn-getdispinfo.md) est envoyé.

Notez que ce code de notification n’est pas toujours une représentation exacte des éléments qui seront demandés par [LVN \_ GETDISPINFO](lvn-getdispinfo.md). Par conséquent, si l’élément demandé n’est pas mis en cache pendant la gestion de LVN \_ GETDISPINFO, l’application doit être préparée à fournir les informations demandées à partir d’une source située à l’extérieur du cache.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





