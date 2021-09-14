---
title: Message TVM_GETTEXTCOLOR (commctrl. h)
description: Récupère la couleur de texte actuelle du contrôle. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro GetTextColor TreeView.
ms.assetid: fe1aa2e8-fdf2-48d1-936b-6d6bc8e589f4
keywords:
- TVM_GETTEXTCOLOR les contrôles de Windows de message
topic_type:
- apiref
api_name:
- TVM_GETTEXTCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 899fc68847fea937a6f62bff6367eeac5570a5a6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127115657"
---
# <a name="tvm_gettextcolor-message"></a>TVM \_ GETTEXTCOLOR message

Récupère la couleur de texte actuelle du contrôle. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**\_ GetTextColor TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_gettextcolor) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>Doit être zéro.</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne une valeur [**COLORREF**](/windows/desktop/gdi/colorref) qui représente la couleur du texte actuel. Si cette valeur est-1, le contrôle utilise la couleur système pour la couleur du texte.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**TVM \_ SETTEXTCOLOR**](tvm-settextcolor.md)
</dt> </dl>

 

