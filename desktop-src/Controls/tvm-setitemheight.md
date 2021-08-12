---
title: Message TVM_SETITEMHEIGHT (commctrl. h)
description: Définit la hauteur des éléments de l’arborescence. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro SetItemHeight TreeView.
ms.assetid: 23f6f2a4-cdd9-441d-af24-ed40513d2721
keywords:
- TVM_SETITEMHEIGHT les contrôles de Windows de message
topic_type:
- apiref
api_name:
- TVM_SETITEMHEIGHT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9afff57188a9683d18c6bff780b4a9f61479526d44ea77985742520a47e66cca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118669644"
---
# <a name="tvm_setitemheight-message"></a>TVM \_ SETITEMHEIGHT message

Définit la hauteur des éléments de l’arborescence. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**\_ SetItemHeight TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setitemheight) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Nouvelle hauteur de chaque élément dans l’arborescence, en pixels. Les hauteurs inférieures à 1 seront définis sur 1. Si cet argument n’est pas pair et que le contrôle Tree-View n’a pas le style [**TV \_ NONEVENHEIGHT**](tree-view-control-window-styles.md) , cette valeur est arrondie à la valeur paire la plus proche. Si cet argument a la valeur-1, le contrôle revient à l’utilisation de sa hauteur d’élément par défaut.

</dd> <dt>

*lParam* 
</dt> <dd>Doit être zéro.</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la hauteur précédente des éléments, en pixels.

## <a name="remarks"></a>Remarques

Le contrôle Tree-View utilise cette valeur pour la hauteur de tous les éléments. Pour modifier la hauteur des éléments individuels, consultez la description du membre **iIntegral** de la structure [**TVITEMEX**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**TVM \_ GETITEMHEIGHT**](tvm-getitemheight.md)
</dt> </dl>

 

 





