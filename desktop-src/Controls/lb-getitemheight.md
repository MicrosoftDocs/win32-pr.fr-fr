---
title: Message LB_GETITEMHEIGHT (winuser. h)
description: Obtient la hauteur des éléments dans une zone de liste.
ms.assetid: ee96fce6-babd-4581-ac0e-2eb955fe543b
keywords:
- LB_GETITEMHEIGHT les contrôles de Windows de message
topic_type:
- apiref
api_name:
- LB_GETITEMHEIGHT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29c232c172f14774db9dd7c783e18a10f0888190708432b9336208570f0d5031
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119434329"
---
# <a name="lb_getitemheight-message"></a>\_Message GETITEMHEIGHT lb

Obtient la hauteur des éléments dans une zone de liste.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Index de base zéro de l’élément de zone de liste. Cet index est utilisé uniquement si la zone de liste présente le style [**\_ OWNERDRAWVARIABLE**](list-box-styles.md) . sinon, elle doit être égale à zéro.

Windows 95/Windows 98/Windows Millennium edition (Windows) : le paramètre *wParam* est limité aux valeurs 16 bits. Cela signifie que les zones de liste ne peuvent pas contenir plus de 32 767 éléments. Bien que le nombre d’éléments soit limité, la taille totale, en octets, des éléments d’une zone de liste n’est limitée que par la mémoire disponible.

</dd> <dt>

*lParam* 
</dt> <dd>

Ce paramètre n'est pas utilisé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La valeur de retour correspond à la hauteur, en pixels, de chaque élément de la zone de liste. La valeur de retour correspond à la hauteur de l’élément spécifié par le paramètre *wParam* si la zone de liste présente le style [**\_ OWNERDRAWVARIABLE**](list-box-styles.md) . La valeur de retour est LB \_ Err si une erreur se produit.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_SETITEMHEIGHT lb**](lb-setitemheight.md)
</dt> </dl>

 

 





