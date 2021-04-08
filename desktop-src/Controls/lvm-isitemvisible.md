---
title: Message LVM_ISITEMVISIBLE (commctrl. h)
description: Indique si un élément du contrôle List-View est visible. Envoyez ce message explicitement ou à l’aide de la \_ macro ListView IsItemVisible.
ms.assetid: 355be527-e2b9-46be-96a0-951d72216d92
keywords:
- LVM_ISITEMVISIBLE les contrôles de message Windows
topic_type:
- apiref
api_name:
- LVM_ISITEMVISIBLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a95116d2d6da6e3554e63a8149c9b91d6c97f76
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844081"
---
# <a name="lvm_isitemvisible-message"></a>\_Message ISITEMVISIBLE LVM

Indique si un élément du contrôle List-View est visible. Envoyez ce message explicitement ou à l’aide de la macro [**ListView \_ IsItemVisible**](/windows/desktop/api/Commctrl/nf-commctrl-listview_isitemvisible) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* \[ dans\]
</dt> <dd>

Index de l’élément dans le contrôle List-View.

</dd> <dt>

*lParam* 
</dt> <dd>Doit être zéro.</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la **valeur true** si visible, ou **false** dans le cas contraire.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





