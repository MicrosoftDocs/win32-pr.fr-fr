---
title: Message TVM_GETINSERTMARKCOLOR (commctrl. h)
description: Récupère la couleur utilisée pour dessiner la marque d’insertion pour l’arborescence. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro GetInsertMarkColor TreeView.
ms.assetid: d1fba4bb-1bdb-44e0-8083-b564cdafc055
keywords:
- TVM_GETINSERTMARKCOLOR les contrôles de message Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942755"
---
# <a name="tvm_getinsertmarkcolor-message"></a>TVM \_ GETINSERTMARKCOLOR message

Récupère la couleur utilisée pour dessiner la marque d’insertion pour l’arborescence. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**\_ GetInsertMarkColor TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getinsertmarkcolor) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>Doit être zéro.</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur [**COLORREF**](/windows/desktop/gdi/colorref) qui contient la couleur de la marque d’insertion actuelle.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**TVM \_ SETINSERTMARKCOLOR**](tvm-setinsertmarkcolor.md)
</dt> </dl>

 

