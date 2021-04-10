---
title: Message LVM_GETEXTENDEDLISTVIEWSTYLE (commctrl. h)
description: Obtient les styles étendus en cours d’utilisation pour un contrôle List-View donné. Vous pouvez envoyer ce message explicitement ou utiliser la \_ macro ListView GetExtendedListViewStyle.
ms.assetid: 5cfccdb8-a81c-4fa9-a4fa-19cf49bd6ce0
keywords:
- LVM_GETEXTENDEDLISTVIEWSTYLE les contrôles de message Windows
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
ms.openlocfilehash: 273da9e7eac85475b90ad05dc5fdd7f70d524562
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032355"
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
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





