---
title: Message TVM_SORTCHILDRENCB (commctrl. h)
description: Trie les éléments d’arborescence à l’aide d’une fonction de rappel définie par l’application qui compare les éléments. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro SortChildrenCB TreeView.
ms.assetid: 1669e576-5e57-49f6-8097-7d6547306014
keywords:
- TVM_SORTCHILDRENCB les contrôles de Windows de message
topic_type:
- apiref
api_name:
- TVM_SORTCHILDRENCB
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b1dab4abbbc019a81d7a066c81dbb3537a0d80d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127115550"
---
# <a name="tvm_sortchildrencb-message"></a>TVM \_ SORTCHILDRENCB message

Trie les éléments d’arborescence à l’aide d’une fonction de rappel définie par l’application qui compare les éléments. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**\_ SortChildrenCB TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_sortchildrencb) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Réservé. Doit être zéro.

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**TVSORTCB**](/windows/win32/api/commctrl/ns-commctrl-tvsortcb) . Le membre **lpfnCompare** est l’adresse de la fonction de rappel définie par l’application, qui est appelée au cours de l’opération de tri chaque fois que l’ordre relatif de deux éléments de liste doit être comparé. Pour plus d’informations sur la fonction de rappel, consultez la description de **TVSORTCB**.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





