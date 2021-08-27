---
title: Message LVM_GETITEMCOUNT (commctrl. h)
description: Récupère le nombre d’éléments dans un contrôle List-View. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro ListView GetItemCount.
ms.assetid: 7c639d69-e42c-41b5-9fdd-4943166752a2
keywords:
- LVM_GETITEMCOUNT les contrôles de Windows de message
topic_type:
- apiref
api_name:
- LVM_GETITEMCOUNT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1561e893930e4e3eca8de628c1df555e63794c3463edf81af798c53d873c8a4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120109619"
---
# <a name="lvm_getitemcount-message"></a>\_Message GETITEMCOUNT LVM

Récupère le nombre d’éléments dans un contrôle List-View. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**ListView \_ GetItemCount**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitemcount) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>Doit être zéro.</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne le nombre d’éléments.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





