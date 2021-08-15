---
title: Message TVM_DELETEITEM (commctrl. h)
description: Supprime un élément et tous ses enfants d’un contrôle Tree-View. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro TreeView DeleteItem.
ms.assetid: 225420a5-6ded-4786-a080-2817aa5f66c9
keywords:
- TVM_DELETEITEM les contrôles de Windows de message
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
ms.openlocfilehash: 7ef0165ffaf1f0f04b32cda43e21c97fed012ad6d61b32f8919612f8924f7c66
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119018687"
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

## <a name="remarks"></a>Remarques

Il n’est pas possible de supprimer des éléments en réponse à une notification telle que [TVN \_ SELCHANGING](tvn-selchanging.md).

Une fois qu’un élément est supprimé, son handle n’est pas valide et ne peut pas être utilisé.

La fenêtre parente reçoit un code de notification [TVN \_ DELETEITEM](tvn-deleteitem.md) lorsque chaque élément est supprimé.

Si l’étiquette de l’élément est en cours de modification, l’opération de modification est annulée et la fenêtre parente reçoit le code de notification [TVN \_ ENDLABELEDIT](tvn-endlabeledit.md) .

Si vous supprimez tous les éléments d’un contrôle Tree-View qui a le style de [**\_ défilement TV**](tree-view-control-window-styles.md) , les éléments ajoutés ultérieurement peuvent ne pas s’afficher correctement. Pour plus d’informations, consultez [**TreeView \_ DeleteAllItems**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_deleteallitems).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





