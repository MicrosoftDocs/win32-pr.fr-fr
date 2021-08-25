---
title: Message LB_GETANCHORINDEX (winuser. h)
description: Obtient l’index de l’élément d’ancrage \ 8212 ; autrement dit, l’élément à partir duquel commence une sélection multiple. Une sélection multiple s’étend sur tous les éléments de l’élément d’ancrage à l’élément du signe insertion.
ms.assetid: vs|controls|~\controls\listboxes\listboxreference\listboxmessages\lb_getanchorindex.htm
keywords:
- LB_GETANCHORINDEX les contrôles de Windows de message
topic_type:
- apiref
api_name:
- LB_GETANCHORINDEX
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df33244a755ddd99a5af0c849e7753e478a91b94cd5cbd717505ca4ab37b0f9f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119799579"
---
# <a name="lb_getanchorindex-message"></a>\_Message GETANCHORINDEX lb

Obtient l’index de l’élément d’ancrage qui est, l’élément à partir duquel une sélection multiple démarre. Une sélection multiple s’étend sur tous les éléments de l’élément d’ancrage à l’élément du signe insertion.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Non utilisé ; doit être égal à zéro.

</dd> <dt>

*lParam* 
</dt> <dd>

Non utilisé ; doit être égal à zéro.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La valeur de retour est l’index de l’élément d’ancrage.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_SETANCHORINDEX lb**](lb-setanchorindex.md)
</dt> </dl>

 

 





