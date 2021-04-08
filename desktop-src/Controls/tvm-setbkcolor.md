---
title: Message TVM_SETBKCOLOR (commctrl. h)
description: Définit la couleur d’arrière-plan du contrôle. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro SetBkColor TreeView.
ms.assetid: 087f5e0b-ac73-4db4-b82e-15c7641b681c
keywords:
- TVM_SETBKCOLOR les contrôles de message Windows
topic_type:
- apiref
api_name:
- TVM_SETBKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 151aef7aa61e7c66d436d0c90f2481fada017059
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843782"
---
# <a name="tvm_setbkcolor-message"></a>TVM \_ SETBKCOLOR message

Définit la couleur d’arrière-plan du contrôle. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**\_ SetBkColor TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setbkcolor) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>

Valeur [**COLORREF**](/windows/desktop/gdi/colorref) qui contient la nouvelle couleur d’arrière-plan. Si cette valeur est-1, le contrôle revient à l’utilisation de la couleur système pour la couleur d’arrière-plan.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur [**COLORREF**](/windows/desktop/gdi/colorref) qui représente la couleur d’arrière-plan précédente. Si cette valeur est-1, le contrôle utilisait la couleur système pour la couleur d’arrière-plan.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**TVM \_ GETBKCOLOR**](tvm-getbkcolor.md)
</dt> </dl>

 

