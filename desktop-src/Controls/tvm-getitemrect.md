---
title: Message TVM_GETITEMRECT (commctrl. h)
description: Récupère le rectangle englobant d’un élément d’arborescence et indique si l’élément est visible. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro GetItemRect TreeView.
ms.assetid: f2d7d7b1-cfe7-4361-bd90-e3e99dbcd99c
keywords:
- TVM_GETITEMRECT les contrôles de Windows de message
topic_type:
- apiref
api_name:
- TVM_GETITEMRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ebdf4d73fb83ddbd8e9e682f11ee1f5ecfbd5153
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127115677"
---
# <a name="tvm_getitemrect-message"></a>TVM \_ GETITEMRECT message

Récupère le rectangle englobant d’un élément d’arborescence et indique si l’élément est visible. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**\_ GetItemRect TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getitemrect) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Valeur spécifiant la partie de l’élément dont le rectangle englobant doit être récupéré. Si ce paramètre a la **valeur true**, le rectangle englobant comprend uniquement le texte de l’élément. Dans le cas contraire, il comprend la ligne entière occupée par l’élément dans le contrôle Tree-View.

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**Rect**](/previous-versions//dd162897(v=vs.85)) qui, lors de l’envoi du message, contient le handle de l’élément pour lequel récupérer le rectangle. Consultez l’exemple ci-dessous pour plus d’informations sur la façon de placer le descripteur d’élément dans ce paramètre. Après avoir retourné le message, ce paramètre contient le rectangle englobant. Les coordonnées sont relatives au coin supérieur gauche du contrôle Tree-View.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Si l’élément est visible et que le rectangle englobant a été récupéré avec succès, la valeur de retour est **true**. Dans le cas contraire, le message retourne la **valeur false** et ne récupère pas le rectangle englobant.

## <a name="remarks"></a>Notes

Lors de l’envoi de ce message, le paramètre *lParam* contient le handle de l’élément pour lequel le rectangle est récupéré. Le descripteur est placé dans *lParam* comme indiqué dans l’exemple suivant :


```
RECT rc;

*(HTREEITEM*)&rc = hTreeItem;

SendMessage(hwndTreeView, TVM_GETITEMRECT, FALSE, (LPARAM)&rc);
```



## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

