---
title: Message LVM_GETEXTENDEDLISTVIEWSTYLE (commctrl. h)
description: Obtient les styles étendus en cours d’utilisation pour un contrôle List-View donné. Vous pouvez envoyer ce message explicitement ou utiliser la \_ macro ListView GetExtendedListViewStyle.
ms.assetid: 5cfccdb8-a81c-4fa9-a4fa-19cf49bd6ce0
keywords:
- LVM_GETEXTENDEDLISTVIEWSTYLE les contrôles de Windows de message
topic_type:
- apiref
api_name:
- LVM_GETEXTENDEDLISTVIEWSTYLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d04b2f83f5a8bd55f01aa84e315512c5ccb1b28b17f196c0199fc417544a6737
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119968299"
---
# <a name="lvm_getextendedlistviewstyle-message"></a>\_Message GETEXTENDEDLISTVIEWSTYLE LVM

Obtient les styles étendus en cours d’utilisation pour un contrôle List-View donné. Vous pouvez envoyer ce message explicitement ou utiliser la macro [**ListView \_ GetExtendedListViewStyle**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getextendedlistviewstyle) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>Doit être zéro.</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une **valeur DWORD** qui représente les styles en cours d’utilisation pour un contrôle List View donné. Cette valeur peut être une combinaison de [styles de List-View étendus](extended-list-view-styles.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





