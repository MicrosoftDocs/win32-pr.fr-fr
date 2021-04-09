---
title: Message LB_GETCARETINDEX (winuser. h)
description: Récupère l’index de l’élément qui a le focus dans une zone de liste à sélection multiple. L’élément peut être ou non sélectionné.
ms.assetid: vs|controls|~\controls\listboxes\listboxreference\listboxmessages\lb_getcaretindex.htm
keywords:
- LB_GETCARETINDEX les contrôles de message Windows
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
ms.openlocfilehash: 4b9e4b8b2c75d72cdec606942991e957d8109ac7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104033206"
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

## <a name="remarks"></a>Notes

Ce message peut également être utilisé pour obtenir l’index de l’élément qui est actuellement sélectionné dans une zone de liste à sélection unique.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_SETCARETINDEX lb**](lb-setcaretindex.md)
</dt> </dl>

 

 





