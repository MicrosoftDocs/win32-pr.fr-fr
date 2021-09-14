---
title: Message TVM_SORTCHILDREN (commctrl. h)
description: Trie les éléments enfants de l’élément parent spécifié dans un contrôle TreeView. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro SortChildren TreeView.
ms.assetid: c18bcd5f-c083-46ee-873b-d3100b0d7b04
keywords:
- TVM_SORTCHILDREN les contrôles de Windows de message
topic_type:
- apiref
api_name:
- TVM_SORTCHILDREN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 341591c31accb4aab0b49f611359a93ec99c0cab
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127115549"
---
# <a name="tvm_sortchildren-message"></a>TVM \_ SORTCHILDREN message

Trie les éléments enfants de l’élément parent spécifié dans un contrôle TreeView. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**\_ SortChildren TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_sortchildren) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Valeur qui spécifie si le tri est récursif. Affectez à *wParam* la **valeur true** pour trier tous les niveaux d’éléments enfants au-dessous de l’élément parent. Dans le cas contraire, seuls les enfants immédiats du parent sont triés.

</dd> <dt>

*lParam* 
</dt> <dd>

Handle vers l’élément parent dont les éléments enfants doivent être triés.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.

## <a name="remarks"></a>Notes

Ce message alphabetizes les éléments d’arborescence à l’aide de [**lstrcmpi**](/windows/desktop/api/winbase/nf-winbase-lstrcmpia) sur le nom de l’élément. Vous pouvez utiliser le message [**TVM \_ SORTCHILDRENCB**](tvm-sortchildrencb.md) pour personnaliser le comportement de classement.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

