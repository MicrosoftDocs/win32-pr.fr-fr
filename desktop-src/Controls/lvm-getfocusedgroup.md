---
title: Message LVM_GETFOCUSEDGROUP (commctrl. h)
description: Obtient le groupe qui a le focus. Envoyez ce message explicitement ou à l’aide de la \_ macro ListView GetFocusedGroup.
ms.assetid: c1902f35-84b7-4f46-89a6-e48148f06172
keywords:
- LVM_GETFOCUSEDGROUP les contrôles de message Windows
topic_type:
- apiref
api_name:
- LVM_GETFOCUSEDGROUP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e0d12eb637ec1a421a5eaff58636df7bef8f449
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464274"
---
# <a name="lvm_getfocusedgroup-message"></a>\_Message GETFOCUSEDGROUP LVM

Obtient le groupe qui a le focus. Envoyez ce message explicitement ou à l’aide de la macro [**ListView \_ GetFocusedGroup**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getfocusedgroup) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>Doit être zéro.</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne l’index du groupe avec l’État LVGS \_ Focused, ou-1 s’il n’existe aucun groupe avec l’État LVGS \_ focus.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





