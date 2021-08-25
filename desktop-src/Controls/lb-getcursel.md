---
title: Message LB_GETCURSEL (winuser. h)
description: Obtient l’index de l’élément actuellement sélectionné, le cas échéant, dans une zone de liste à sélection unique.
ms.assetid: 39ab7f77-6c8e-45a4-aad4-47eba0a11a11
keywords:
- LB_GETCURSEL les contrôles de Windows de message
topic_type:
- apiref
api_name:
- LB_GETCURSEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d67a060669d48a9ab020540c78ece395504c9f0b7e36807e3ac59daf216ea395
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120085519"
---
# <a name="lb_getcursel-message"></a>\_Message GETCURSEL lb

Obtient l’index de l’élément actuellement sélectionné, le cas échéant, dans une zone de liste à sélection unique.

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

Dans une zone de liste à sélection unique, la valeur de retour est l’index de base zéro de l’élément actuellement sélectionné. S’il n’y a aucune sélection, la valeur de retour est LB \_ Err.

## <a name="remarks"></a>Remarques

Pour récupérer les index des éléments sélectionnés dans une zone de liste à sélection multiple, utilisez le message [**lb \_ GETSELITEMS**](lb-getselitems.md) . Pour déterminer si l’élément qui a le rectangle de focus dans une zone de liste à sélection multiple est sélectionné, utilisez le message [**lb \_ GETSEL**](lb-getsel.md) .

En cas d’envoi à une zone de liste à sélection multiple, **lb \_ GETCURSEL** retourne l’index de l’élément qui a le rectangle de focus. Si aucun élément n’est sélectionné, la valeur retournée est zéro.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[**\_GETCARETINDEX lb**](lb-getcaretindex.md)
</dt> <dt>

[**\_GETSEL lb**](lb-getsel.md)
</dt> <dt>

[**\_GETSELITEMS lb**](lb-getselitems.md)
</dt> <dt>

[**\_SETCURSEL lb**](lb-setcursel.md)
</dt> </dl>

 

 





