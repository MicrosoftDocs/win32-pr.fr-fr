---
title: Message CB_FINDSTRINGEXACT (winuser. h)
description: Recherche la première chaîne de zone de liste dans une zone de liste déroulante qui correspond à la chaîne spécifiée dans le paramètre lParam.
ms.assetid: 9065af9f-b18e-4fd5-a8cc-f780f8d0fb05
keywords:
- CB_FINDSTRINGEXACT les contrôles de Windows de message
topic_type:
- apiref
api_name:
- CB_FINDSTRINGEXACT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f99d85c7dddb95bdfb168443d6f977c22273a87
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127123917"
---
# <a name="cb_findstringexact-message"></a>\_Message FINDEXACTSTRING CB

Recherche la première chaîne de zone de liste dans une zone de liste déroulante qui correspond à la chaîne spécifiée dans le paramètre *lParam* .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Index de base zéro de l’élément qui précède le premier élément dans lequel effectuer la recherche. Lorsque la recherche atteint le bas de la zone de liste, elle continue à partir du haut de la zone de liste jusqu’à l’élément spécifié par le paramètre *wParam* . Si *wParam* est-1, la zone de liste entière est recherchée à partir du début.

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers la chaîne terminée par le caractère null à rechercher. La recherche ne respecte pas la casse, par conséquent, cette chaîne peut contenir n’importe quelle combinaison de lettres majuscules et minuscules.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

La valeur de retour est l’index de base zéro de l’élément correspondant. Si la recherche échoue, il s’agit de l' \_ erreur CB.

## <a name="remarks"></a>Notes

Cette fonction est réussie uniquement si la chaîne spécifiée et un élément de zone de liste déroulante ont la même longueur (à l’exception du caractère null de fin) et les mêmes caractères.

Si vous créez la zone de liste déroulante avec un style owner-drawn mais sans le style [**CBS \_ HASSTRINGS**](combo-box-styles.md) , les fonctionnalités du message **CB \_ FindExactString** varient selon que votre application utilise ou non le style de [**\_ Tri CBS**](combo-box-styles.md) . Si vous utilisez le style de **\_ Tri CBS** , les messages [**WM \_ COMPAREITEM**](wm-compareitem.md) sont envoyés au propriétaire de la zone de liste déroulante pour déterminer quel élément correspond à la chaîne spécifiée. Si vous n’utilisez pas le style de **\_ Tri CBS** , le message **CB \_ FindExactString** recherche un élément de liste qui correspond à la valeur du paramètre *lParam* .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[**\_FindString CB**](cb-findstring.md)
</dt> <dt>

[**\_SELECTSTRING CB**](cb-selectstring.md)
</dt> <dt>

[**\_COMPAREITEM WM**](wm-compareitem.md)
</dt> </dl>

 

 





