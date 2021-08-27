---
title: Message TVM_GETBKCOLOR (commctrl. h)
description: Récupère la couleur d’arrière-plan actuelle du contrôle. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro GetBkColor TreeView.
ms.assetid: 1b9eea90-54cd-47b9-befa-ec0128a0230f
keywords:
- TVM_GETBKCOLOR les contrôles de Windows de message
topic_type:
- apiref
api_name:
- TVM_GETBKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a5a6530b1aada1fab06c0b353d7ead666e61f0f796b890d1f5c56fe0be094b5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120088449"
---
# <a name="tvm_getbkcolor-message"></a>TVM \_ GETBKCOLOR message

Récupère la couleur d’arrière-plan actuelle du contrôle. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**\_ GetBkColor TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getbkcolor) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>Doit être zéro.</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur [**COLORREF**](/windows/desktop/gdi/colorref) qui représente la couleur d’arrière-plan actuelle. Si cette valeur est-1, le contrôle utilise la couleur système pour la couleur d’arrière-plan.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**TVM \_ SETBKCOLOR**](tvm-setbkcolor.md)
</dt> </dl>

 

