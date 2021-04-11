---
title: RBN_GETOBJECT le code de notification (commctrl. h)
description: Envoyé par un contrôle rebar créé avec le \_ style RBS REGISTERDROP lorsqu’un objet est glissé sur une bande dans le contrôle. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 057474c1-5f65-4290-973e-4366b760365a
keywords:
- Contrôles Windows de code de notification RBN_GETOBJECT
topic_type:
- apiref
api_name:
- RBN_GETOBJECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a390bc5c5f74a577805ca8ae1128fbb24e6b10b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104776"
---
# <a name="rbn_getobject-notification-code"></a>\_Code de notification RBN GETOBJECT

Envoyé par un contrôle rebar créé avec le style [**RBS \_ REGISTERDROP**](rebar-control-styles.md) lorsqu’un objet est glissé sur une bande dans le contrôle. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .


```C++
RBN_GETOBJECT

    lpnmon = (LPNMOBJECTNOTIFY) lParam;
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**NMOBJECTNOTIFY**](/windows/win32/api/commctrl/ns-commctrl-nmobjectnotify) qui contient des informations sur la bande sur laquelle l’objet est glissé et reçoit également les données fournies par l’application réceptrice en réponse à ce code de notification.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La valeur de retour pour ce code de notification doit être égale à zéro.

## <a name="remarks"></a>Notes

Pour recevoir le \_ Code de notification RBN GETOBJECT, initialisez OLE avec un appel à [**OleInitialize**](/windows/desktop/api/ole2/nf-ole2-oleinitialize) ou à [**CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

