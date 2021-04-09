---
title: Message LB_GETTOPINDEX (winuser. h)
description: Obtient l’index du premier élément visible dans une zone de liste.
ms.assetid: vs|controls|~\controls\listboxes\listboxreference\listboxmessages\lb_gettopindex.htm
keywords:
- LB_GETTOPINDEX les contrôles de message Windows
topic_type:
- apiref
api_name:
- LB_GETTOPINDEX
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bdeca8e3f40ab3105bb9703db9355d09a214f5fc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942165"
---
# <a name="lb_gettopindex-message"></a>\_Message GETTOPINDEX lb

Obtient l’index du premier élément visible dans une zone de liste. Initialement, l’élément avec l’index 0 est en haut de la zone de liste, mais si le contenu de la zone de liste a fait l’objet d’un défilement, un autre élément peut se trouver en haut. Le premier élément visible dans une zone de liste à plusieurs colonnes est l’élément en haut à gauche.

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

La valeur de retour est l’index du premier élément visible dans la zone de liste.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_SETTOPINDEX lb**](lb-settopindex.md)
</dt> </dl>

 

 





