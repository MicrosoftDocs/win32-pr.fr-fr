---
title: Message TVM_SETTEXTCOLOR (commctrl. h)
description: Définit la couleur du texte du contrôle. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro SetTextColor TreeView.
ms.assetid: eb57dfd5-3e7b-4cda-a659-be9e03470a44
keywords:
- TVM_SETTEXTCOLOR les contrôles de Windows de message
topic_type:
- apiref
api_name:
- TVM_SETTEXTCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da0049c2666faccce7879146c78ddecc70825e8b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127115566"
---
# <a name="tvm_settextcolor-message"></a>TVM \_ SETTEXTCOLOR message

Définit la couleur du texte du contrôle. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**\_ SetTextColor TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_settextcolor) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>

Valeur [**COLORREF**](/windows/desktop/gdi/colorref) qui contient la nouvelle couleur de texte. Si cet argument a la valeur-1, le contrôle revient à l’utilisation de la couleur système pour la couleur du texte.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne une valeur **COLORREF** qui représente la couleur de texte précédente. Si cette valeur est-1, le contrôle utilisait la couleur système pour la couleur du texte.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**TVM \_ GETTEXTCOLOR**](tvm-gettextcolor.md)
</dt> </dl>

 

