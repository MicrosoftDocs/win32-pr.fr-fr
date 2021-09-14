---
title: Message TVM_ENSUREVISIBLE (commctrl. h)
description: Garantit qu’un élément d’arborescence est visible, en développant l’élément parent ou en faisant défiler le contrôle d’arborescence, si nécessaire. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro EnsureVisible TreeView.
ms.assetid: 7053438a-f9ca-4c4c-9da6-46b99fe1e4f8
keywords:
- TVM_ENSUREVISIBLE les contrôles de Windows de message
topic_type:
- apiref
api_name:
- TVM_ENSUREVISIBLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06100ee33106736076608aa216d2aebc03b76ebe
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127115733"
---
# <a name="tvm_ensurevisible-message"></a>TVM \_ ENSUREVISIBLE message

Garantit qu’un élément d’arborescence est visible, en développant l’élément parent ou en faisant défiler le contrôle d’arborescence, si nécessaire. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**\_ EnsureVisible TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_ensurevisible) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>

Handle de l’élément.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne une valeur différente de zéro si le système a fait défiler les éléments dans le contrôle Tree-View et qu’aucun élément n’a été développé. Dans le cas contraire, le message retourne la valeur zéro.

## <a name="remarks"></a>Notes

Si le \_ message TVM ENSUREVISIBLE développe l’élément parent, la fenêtre parente reçoit les codes de notification [TVN \_ ITEMEXPANDING](tvn-itemexpanding.md) et [TVN \_ ITEMEXPANDED](tvn-itemexpanded.md) .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





