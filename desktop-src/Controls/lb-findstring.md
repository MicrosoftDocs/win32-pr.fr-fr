---
title: Message LB_FINDSTRING (winuser. h)
description: Recherche la première chaîne dans une zone de liste qui commence par la chaîne spécifiée.
ms.assetid: 1b7f25a7-0892-4d12-b3e3-21180d9ddfb1
keywords:
- LB_FINDSTRING les contrôles de Windows de message
topic_type:
- apiref
api_name:
- LB_FINDSTRING
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b528dbafbc386af05a091f24c8c28327739f5d40
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126999879"
---
# <a name="lb_findstring-message"></a>\_Message FindString lb

Recherche la première chaîne dans une zone de liste qui commence par la chaîne spécifiée.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Index de base zéro de l'élément précédant le premier élément sur lequel la recherche est effectuée. Lorsque la recherche atteint le bas de la zone de liste, elle continue à effectuer une recherche à partir du haut de la zone de liste jusqu’à l’élément spécifié par le paramètre *wParam* . Si *wParam* est-1, la zone de liste entière est recherchée à partir du début.

Windows 95/Windows 98/Windows Millennium edition (Windows) : le paramètre *wParam* est limité aux valeurs 16 bits. Cela signifie que les zones de liste ne peuvent pas contenir plus de 32 767 éléments. Bien que le nombre d’éléments soit limité, la taille totale, en octets, des éléments d’une zone de liste n’est limitée que par la mémoire disponible.

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers la chaîne terminée par le caractère null qui contient la chaîne à rechercher. La recherche étant indépendante de la casse, cette chaîne peut contenir n’importe quelle combinaison de lettres majuscules et minuscules.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

La valeur de retour est l’index de l’élément correspondant, ou LB \_ Err si la recherche a échoué.

## <a name="remarks"></a>Notes

Si la zone de liste a le style owner-drawn, mais pas le style [**\_ HASSTRINGS kg**](list-box-styles.md) , l’action entreprise par **lb \_ FindString** varie selon que le style de [**\_ Tri lbs**](list-box-styles.md) est utilisé ou non. Si **le \_ tri de lbs** est utilisé, le système envoie des messages [**WM \_ COMPAREITEM**](wm-compareitem.md) au propriétaire de la zone de liste pour déterminer l’élément qui correspond à la chaîne spécifiée. Dans le cas contraire, **lb \_ FindString** tente de trouver un élément ayant une valeur long (fourni comme paramètre *lParam* du message [**lb \_ ADDSTRING**](lb-addstring.md) ou [**lb \_ INSERTSTRING**](lb-insertstring.md) ) qui correspond au paramètre *lParam* .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_FINDEXACTSTRING lb**](lb-findstringexact.md)
</dt> </dl>

 

 





