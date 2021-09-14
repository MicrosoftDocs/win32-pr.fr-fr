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
ms.openlocfilehash: 33775341adc47d84ead9a633d7d31b16ffc4a723
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127115705"
---
# <a name="tvm_getindent-message"></a>TVM \_ GETINDENT message

Récupère la quantité, en pixels, que les éléments enfants sont mis en retrait par rapport à leurs éléments parents. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**\_ GetIndent TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getindent) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>Doit être zéro.</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne la valeur de la mise en retrait.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





