---
title: Message LB_GETCARETINDEX (winuser. h)
description: Récupère l’index de l’élément qui a le focus dans une zone de liste à sélection multiple. L’élément peut être ou non sélectionné.
ms.assetid: vs|controls|~\controls\listboxes\listboxreference\listboxmessages\lb_getcaretindex.htm
keywords:
- LB_GETCARETINDEX les contrôles de Windows de message
topic_type:
- apiref
api_name:
- LB_GETCARETINDEX
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 74732bae571cdcba0cfe8096437bf681e7a339c5c0edb3f18d378ea610bdf8c2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120085539"
---
# <a name="lb_getcaretindex-message"></a>\_Message GETCARETINDEX lb

Récupère l’index de l’élément qui a le focus dans une zone de liste à sélection multiple. L’élément peut être ou non sélectionné.

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

La valeur de retour est l’index de base zéro de l’élément de zone de liste ayant le focus, ou 0 si aucun élément n’a le focus.

## <a name="remarks"></a>Remarques

Ce message peut également être utilisé pour obtenir l’index de l’élément qui est actuellement sélectionné dans une zone de liste à sélection unique.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_SETCARETINDEX lb**](lb-setcaretindex.md)
</dt> </dl>

 

 





