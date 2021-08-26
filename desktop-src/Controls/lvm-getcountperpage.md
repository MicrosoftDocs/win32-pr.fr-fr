---
title: Message LVM_GETCOUNTPERPAGE (commctrl. h)
description: Calcule le nombre d’éléments qui peuvent s’ajuster verticalement dans la zone visible d’un contrôle List View en mode liste ou rapport. Seuls les éléments entièrement visibles sont comptés. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro ListView GetCountPerPage.
ms.assetid: 2ffd2bb1-cddf-4a4a-a4a8-087c9dc3fec0
keywords:
- LVM_GETCOUNTPERPAGE les contrôles de Windows de message
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
ms.openlocfilehash: deb5e7acf0c3db4add2d986a1821b9a76ae30fc1aec0af369e48e35e2a424f77
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119968339"
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
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





