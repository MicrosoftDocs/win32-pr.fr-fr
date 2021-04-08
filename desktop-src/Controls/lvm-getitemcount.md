---
title: Message LVM_GETITEMCOUNT (commctrl. h)
description: Récupère le nombre d’éléments dans un contrôle List-View. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro ListView GetItemCount.
ms.assetid: 7c639d69-e42c-41b5-9fdd-4943166752a2
keywords:
- LVM_GETITEMCOUNT les contrôles de message Windows
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
ms.openlocfilehash: ff2791440c7285d054eca0d2945086d06e3c35a3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742989"
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
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





