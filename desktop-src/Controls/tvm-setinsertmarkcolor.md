---
title: Message TVM_SETINSERTMARKCOLOR (commctrl. h)
description: Définit la couleur utilisée pour dessiner la marque d’insertion pour l’arborescence. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro SetInsertMarkColor TreeView.
ms.assetid: c82304a8-3726-42c0-81e7-90d8f8205ead
keywords:
- TVM_SETINSERTMARKCOLOR les contrôles de message Windows
topic_type:
- apiref
api_name:
- TVM_SETINSERTMARKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92668b1137b089f9a09cc9a34d63d472742bce4d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104176"
---
# <a name="tvm_setinsertmarkcolor-message"></a>TVM \_ SETINSERTMARKCOLOR message

Définit la couleur utilisée pour dessiner la marque d’insertion pour l’arborescence. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**\_ SetInsertMarkColor TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setinsertmarkcolor) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>

Valeur [**COLORREF**](/windows/desktop/gdi/colorref) qui contient la nouvelle couleur de la marque d’insertion.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur **COLORREF** qui contient la couleur de la marque d’insertion précédente.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**TVM \_ GETINSERTMARKCOLOR**](tvm-getinsertmarkcolor.md)
</dt> </dl>

 

