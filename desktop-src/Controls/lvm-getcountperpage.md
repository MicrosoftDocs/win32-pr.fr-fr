---
title: Message LVM_GETCOUNTPERPAGE (commctrl. h)
description: Calcule le nombre d’éléments qui peuvent s’ajuster verticalement dans la zone visible d’un contrôle List View en mode liste ou rapport. Seuls les éléments entièrement visibles sont comptés. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro ListView GetCountPerPage.
ms.assetid: 2ffd2bb1-cddf-4a4a-a4a8-087c9dc3fec0
keywords:
- LVM_GETCOUNTPERPAGE les contrôles de message Windows
topic_type:
- apiref
api_name:
- LVM_GETCOUNTPERPAGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 734d460754f9ae8a11c3a42d8eacebf31d0b6fc0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032358"
---
# <a name="lvm_getcountperpage-message"></a>\_Message GETCOUNTPERPAGE LVM

Calcule le nombre d’éléments qui peuvent s’ajuster verticalement dans la zone visible d’un contrôle List View en mode liste ou rapport. Seuls les éléments entièrement visibles sont comptés. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**ListView \_ GetCountPerPage**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getcountperpage) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>Doit être zéro.</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne le nombre d’éléments entièrement visibles en cas de réussite. Si la vue actuelle est vue icône ou petite icône, la valeur de retour est le nombre total d’éléments dans le contrôle List-View.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





