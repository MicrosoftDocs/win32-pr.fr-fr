---
title: Message TVM_DELETEITEM (commctrl. h)
description: Supprime un élément et tous ses enfants d’un contrôle Tree-View. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro TreeView DeleteItem.
ms.assetid: 225420a5-6ded-4786-a080-2817aa5f66c9
keywords:
- TVM_DELETEITEM les contrôles de message Windows
topic_type:
- apiref
api_name:
- TVM_DELETEITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8783fd5acdf7319699cdc67cbb3ea075e4dbbc28
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465466"
---
# <a name="tvm_deleteitem-message"></a>TVM- \_ message DELETEITEM

Supprime un élément et tous ses enfants d’un contrôle Tree-View. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**TreeView \_ DeleteItem**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_deleteitem) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>

**HTREEITEM** handle de l’élément à supprimer. Si *lParam* a la valeur \_ root TVI ou la **valeur null**, tous les éléments sont supprimés. Vous pouvez également utiliser la [**macro \_ DeleteAllItems TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_deleteallitems) pour supprimer tous les éléments.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.

## <a name="remarks"></a>Notes

Il n’est pas possible de supprimer des éléments en réponse à une notification telle que [TVN \_ SELCHANGING](tvn-selchanging.md).

Une fois qu’un élément est supprimé, son handle n’est pas valide et ne peut pas être utilisé.

La fenêtre parente reçoit un code de notification [TVN \_ DELETEITEM](tvn-deleteitem.md) lorsque chaque élément est supprimé.

Si l’étiquette de l’élément est en cours de modification, l’opération de modification est annulée et la fenêtre parente reçoit le code de notification [TVN \_ ENDLABELEDIT](tvn-endlabeledit.md) .

Si vous supprimez tous les éléments d’un contrôle Tree-View qui a le style de [**\_ défilement TV**](tree-view-control-window-styles.md) , les éléments ajoutés ultérieurement peuvent ne pas s’afficher correctement. Pour plus d’informations, consultez [**TreeView \_ DeleteAllItems**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_deleteallitems).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





