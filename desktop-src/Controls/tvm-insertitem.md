---
title: Message TVM_INSERTITEM (commctrl. h)
description: Insère un nouvel élément dans un contrôle Tree-View. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro TreeView InsertItem.
ms.assetid: c5e5f88f-6ec8-4b95-89ea-97f6f1fd735e
keywords:
- TVM_INSERTITEM les contrôles de Windows de message
topic_type:
- apiref
api_name:
- TVM_INSERTITEM
- TVM_INSERTITEMA
- TVM_INSERTITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85f8a324613820b94e0bd2c49d8fa78136038471f820dd2b9ed8e38ace15f0cf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120060189"
---
# <a name="tvm_insertitem-message"></a>TVM- \_ message INSERTITEM

Insère un nouvel élément dans un contrôle Tree-View. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**TreeView \_ InsertItem**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_insertitem) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**TVINSERTSTRUCT**](/windows/win32/api/commctrl/ns-commctrl-tvinsertstructa) qui spécifie les attributs de l’élément d’arborescence.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne le handle **HTREEITEM** au nouvel élément en cas de réussite, ou **null** dans le cas contraire.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **TVM \_ INSERTITEMW** (Unicode) et **TVM \_ INSERTITEMA** (ANSI)<br/>             |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[TVN \_ ENDLABELEDIT](tvn-endlabeledit.md)
</dt> </dl>

 

 





