---
title: Message TVM_SORTCHILDREN (commctrl. h)
description: Trie les éléments enfants de l’élément parent spécifié dans un contrôle TreeView. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro SortChildren TreeView.
ms.assetid: c18bcd5f-c083-46ee-873b-d3100b0d7b04
keywords:
- TVM_SORTCHILDREN les contrôles de message Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104033193"
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

## <a name="return-value"></a>Valeur retournée

Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.

## <a name="remarks"></a>Notes

Ce message alphabetizes les éléments d’arborescence à l’aide de [**lstrcmpi**](/windows/desktop/api/winbase/nf-winbase-lstrcmpia) sur le nom de l’élément. Vous pouvez utiliser le message [**TVM \_ SORTCHILDRENCB**](tvm-sortchildrencb.md) pour personnaliser le comportement de classement.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

