---
title: Message LB_GETITEMRECT (winuser. h)
description: Obtient les dimensions du rectangle qui délimite un élément de zone de liste tel qu’il est actuellement affiché dans la zone de liste.
ms.assetid: 84f94bc9-f7a4-4c2d-8c35-1bd291082af9
keywords:
- LB_GETITEMRECT les contrôles de Windows de message
topic_type:
- apiref
api_name:
- LB_GETITEMRECT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94e6fa6ed15f4d3a186800fd66e7c917e8620effa775c76f85b144e49207f12f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119799479"
---
# <a name="lb_getitemrect-message"></a>\_Message GETITEMRECT lb

Obtient les dimensions du rectangle qui délimite un élément de zone de liste tel qu’il est actuellement affiché dans la zone de liste.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Index de base zéro de l'élément.

Windows 95/Windows 98/Windows Millennium edition (Windows) : le paramètre *wParam* est limité aux valeurs 16 bits. Cela signifie que les zones de liste ne peuvent pas contenir plus de 32 767 éléments. Bien que le nombre d’éléments soit limité, la taille totale, en octets, des éléments d’une zone de liste n’est limitée que par la mémoire disponible.

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**Rect**](/previous-versions//dd162897(v=vs.85)) qui recevra les coordonnées clientes de l’élément dans la zone de liste.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si une erreur se produit, la valeur de retour est LB \_ Err.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**RECTANGULAIRE**](/previous-versions//dd162897(v=vs.85))
</dt> </dl>

 

