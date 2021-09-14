---
title: Message TVM_SETINSERTMARK (commctrl. h)
description: Définit la marque d’insertion dans un contrôle TreeView. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro SetInsertMark TreeView.
ms.assetid: 35441807-406a-408c-ad89-6dd40c907e3c
keywords:
- TVM_SETINSERTMARK les contrôles de Windows de message
topic_type:
- apiref
api_name:
- TVM_SETINSERTMARK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff5a9cc9b05e9cd7dc3281d778734bee1048ffd2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127115589"
---
# <a name="tvm_setinsertmark-message"></a>TVM \_ SETINSERTMARK message

Définit la marque d’insertion dans un contrôle TreeView. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**\_ SetInsertMark TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setinsertmark) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Valeur **booléenne** qui spécifie si la marque d’insertion est placée avant ou après l’élément spécifié. Si cet argument est différent de zéro, la marque d’insertion sera placée après l’élément. Si cet argument est égal à zéro, la marque d’insertion sera placée avant l’élément.

</dd> <dt>

*lParam* 
</dt> <dd>

**HTREEITEM** qui spécifie à quel élément la marque d’insertion sera placée. Si cet argument a la **valeur null**, la marque d’insertion est supprimée.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne une valeur différente de zéro en cas de réussite, ou zéro dans le cas contraire.

## <a name="remarks"></a>Notes

Dans certains cas, la marque d’insertion peut apparaître à deux emplacements après le développement d’un nœud. Si vous utilisez des marques d’insertion, il est recommandé de forcer une actualisation du contrôle après le développement d’un nœud.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





