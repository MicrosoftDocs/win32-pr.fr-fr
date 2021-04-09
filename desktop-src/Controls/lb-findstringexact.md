---
title: Message LB_FINDSTRINGEXACT (winuser. h)
description: Recherche la première chaîne de zone de liste qui correspond exactement à la chaîne spécifiée, sauf que la recherche ne respecte pas la casse.
ms.assetid: 9bfe21af-626d-4416-aa20-65c425bd99af
keywords:
- LB_FINDSTRINGEXACT les contrôles de message Windows
topic_type:
- apiref
api_name:
- LB_FINDSTRINGEXACT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d85b4f817eabae95c6021647b0c47926b2163722
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104033208"
---
# <a name="lb_findstringexact-message"></a>\_Message FINDEXACTSTRING lb

Recherche la première chaîne de zone de liste qui correspond exactement à la chaîne spécifiée, sauf que la recherche ne respecte pas la casse.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Index de base zéro de l'élément précédant le premier élément sur lequel la recherche est effectuée. Lorsque la recherche atteint le bas de la zone de liste, elle continue à effectuer une recherche à partir du haut de la zone de liste jusqu’à l’élément spécifié par le paramètre *wParam* . Si *wParam* est-1, la zone de liste entière est recherchée à partir du début.

Windows 95/Windows 98/Windows Millennium Edition (Windows Me) : le paramètre *wParam* est limité aux valeurs 16 bits. Cela signifie que les zones de liste ne peuvent pas contenir plus de 32 767 éléments. Bien que le nombre d’éléments soit limité, la taille totale, en octets, des éléments d’une zone de liste n’est limitée que par la mémoire disponible.

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers la chaîne terminée par le caractère null à rechercher. La recherche ne respecte pas la casse, par conséquent, cette chaîne peut contenir n’importe quelle combinaison de lettres majuscules et minuscules.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La valeur de retour est l’index de base zéro de l’élément correspondant, ou LB \_ Err si la recherche a échoué.

## <a name="remarks"></a>Notes

Cette fonction est réussie uniquement si la chaîne spécifiée et un élément de zone de liste ont la même longueur (à l’exception de la valeur null à la fin de la chaîne spécifiée) et ont exactement les mêmes caractères.

Si la zone de liste a le style owner-drawn, mais pas le style [**\_ HASSTRINGS kg**](list-box-styles.md) , l’action entreprise par **lb \_ FindExactString** varie selon que le style de [**\_ Tri lbs**](list-box-styles.md) est utilisé ou non. Si **le \_ tri de lbs** est utilisé, le système envoie des messages [**WM \_ COMPAREITEM**](wm-compareitem.md) au propriétaire de la zone de liste pour déterminer l’élément qui correspond à la chaîne spécifiée. Dans le cas contraire, **lb \_ FindExactString** tente de trouver un élément ayant une valeur long (fourni comme paramètre *lParam* du message [**lb \_ ADDSTRING**](lb-addstring.md) ou [**lb \_ INSERTSTRING**](lb-insertstring.md) ) qui correspond au paramètre *lParam* .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_FindString lb**](lb-findstring.md)
</dt> </dl>

 

 





