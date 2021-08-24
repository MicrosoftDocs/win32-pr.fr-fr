---
title: Message TVM_GETINDENT (commctrl. h)
description: Récupère la quantité, en pixels, que les éléments enfants sont mis en retrait par rapport à leurs éléments parents. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro GetIndent TreeView.
ms.assetid: 4109714e-94a3-4c88-96e7-b4b8ec67f4a1
keywords:
- TVM_GETINDENT les contrôles de Windows de message
topic_type:
- apiref
api_name:
- TVM_GETINDENT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bbee65da49efc19954209b2694d783761017d8c2ae53030e755b8bea61213276
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119834179"
---
# <a name="tvm_getindent-message"></a>TVM \_ GETINDENT message

Récupère la quantité, en pixels, que les éléments enfants sont mis en retrait par rapport à leurs éléments parents. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**\_ GetIndent TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getindent) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>Doit être zéro.</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la valeur de la mise en retrait.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





