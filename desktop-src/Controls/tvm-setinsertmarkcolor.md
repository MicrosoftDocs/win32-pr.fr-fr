---
title: Message TVM_SETINSERTMARKCOLOR (commctrl. h)
description: Définit la couleur utilisée pour dessiner la marque d’insertion pour l’arborescence. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro SetInsertMarkColor TreeView.
ms.assetid: c82304a8-3726-42c0-81e7-90d8f8205ead
keywords:
- TVM_SETINSERTMARKCOLOR les contrôles de Windows de message
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
ms.openlocfilehash: 05d5fd9984b77c99a13e1c7eab24c231e0ce7f601ecb79f8747cdf7ea3011327
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119636759"
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
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**TVM \_ GETINSERTMARKCOLOR**](tvm-getinsertmarkcolor.md)
</dt> </dl>

 

