---
title: Message TVM_GETINSERTMARKCOLOR (commctrl. h)
description: Récupère la couleur utilisée pour dessiner la marque d’insertion pour l’arborescence. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro GetInsertMarkColor TreeView.
ms.assetid: d1fba4bb-1bdb-44e0-8083-b564cdafc055
keywords:
- TVM_GETINSERTMARKCOLOR les contrôles de Windows de message
topic_type:
- apiref
api_name:
- TVM_GETINSERTMARKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61416a428fed88ece8f50ca640dd9a05ec131614
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127115697"
---
# <a name="tvm_getinsertmarkcolor-message"></a>TVM \_ GETINSERTMARKCOLOR message

Récupère la couleur utilisée pour dessiner la marque d’insertion pour l’arborescence. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**\_ GetInsertMarkColor TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getinsertmarkcolor) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>Doit être zéro.</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne une valeur [**COLORREF**](/windows/desktop/gdi/colorref) qui contient la couleur de la marque d’insertion actuelle.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**TVM \_ SETINSERTMARKCOLOR**](tvm-setinsertmarkcolor.md)
</dt> </dl>

 

