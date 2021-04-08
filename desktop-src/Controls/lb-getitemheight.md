---
title: Message LB_GETITEMHEIGHT (winuser. h)
description: Obtient la hauteur des éléments dans une zone de liste.
ms.assetid: ee96fce6-babd-4581-ac0e-2eb955fe543b
keywords:
- LB_GETITEMHEIGHT les contrôles de message Windows
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
ms.openlocfilehash: f44aa9e9b6d52c082a5f33a10280837a33372245
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843433"
---
# <a name="lb_getitemheight-message"></a>\_Message GETITEMHEIGHT lb

Obtient la hauteur des éléments dans une zone de liste.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Index de base zéro de l’élément de zone de liste. Cet index est utilisé uniquement si la zone de liste présente le style [**\_ OWNERDRAWVARIABLE**](list-box-styles.md) . sinon, elle doit être égale à zéro.

Windows 95/Windows 98/Windows Millennium Edition (Windows Me) : le paramètre *wParam* est limité aux valeurs 16 bits. Cela signifie que les zones de liste ne peuvent pas contenir plus de 32 767 éléments. Bien que le nombre d’éléments soit limité, la taille totale, en octets, des éléments d’une zone de liste n’est limitée que par la mémoire disponible.

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
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_SETITEMHEIGHT lb**](lb-setitemheight.md)
</dt> </dl>

 

 





