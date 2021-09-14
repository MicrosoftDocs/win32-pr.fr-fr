---
title: Message TVM_GETITEMHEIGHT (commctrl. h)
description: Récupère la hauteur actuelle de chaque élément d’affichage d’arborescence. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro GetItemHeight TreeView.
ms.assetid: 017476a3-1929-4a31-97a7-0f66175d47ea
keywords:
- TVM_GETITEMHEIGHT les contrôles de Windows de message
topic_type:
- apiref
api_name:
- TVM_GETITEMHEIGHT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 789347b7a50f9bb42a7aebb6fecddf24c42c559c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127115682"
---
# <a name="tvm_getitemheight-message"></a>TVM \_ GETITEMHEIGHT message

Récupère la hauteur actuelle de chaque élément d’affichage d’arborescence. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**\_ GetItemHeight TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getitemheight) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>Doit être zéro.</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne la hauteur de chaque élément, en pixels.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**TVM \_ SETITEMHEIGHT**](tvm-setitemheight.md)
</dt> </dl>

 

 





