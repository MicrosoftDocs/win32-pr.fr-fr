---
title: Message LB_GETTEXTLEN (winuser. h)
description: Obtient la longueur d’une chaîne dans une zone de liste.
ms.assetid: 866730bc-ffd4-42fd-9cea-5d326e129189
keywords:
- LB_GETTEXTLEN les contrôles de Windows de message
topic_type:
- apiref
api_name:
- LB_GETTEXTLEN
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f15d0d5ab89e9917e2062fe0e46505416d2eb3e7c8ca1e0cb0412952a10b8c0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120085469"
---
# <a name="lb_gettextlen-message"></a>\_Message GETTEXTLEN lb

Obtient la longueur d’une chaîne dans une zone de liste.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Index de base zéro de la chaîne.

Windows 95/Windows 98/Windows Millennium edition (Windows) : le paramètre *wParam* est limité aux valeurs 16 bits. Cela signifie que les zones de liste ne peuvent pas contenir plus de 32 767 éléments. Bien que le nombre d’éléments soit limité, la taille totale, en octets, des éléments d’une zone de liste n’est limitée que par la mémoire disponible.

</dd> <dt>

*lParam* 
</dt> <dd>

Ce paramètre n'est pas utilisé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La valeur de retour est la longueur de la chaîne, dans **TCHAR** s, à l’exclusion du caractère null de fin. Dans certaines conditions, cette valeur peut en fait être supérieure à la longueur du texte. Pour plus d'informations, consultez la section Notes qui suit.

Si le paramètre *wParam* ne spécifie pas d’index valide, la valeur de retour est lb \_ Err.

## <a name="remarks"></a>Remarques

Dans certaines conditions, la valeur de retour est supérieure à la longueur réelle du texte. Cela se produit avec certains mélanges d’ANSI et Unicode, et est dû au système d’exploitation qui autorise l’existence possible de caractères DBCS (Double-Byte Character Set) dans le texte. Toutefois, la valeur de retour sera toujours au moins égale à la longueur réelle du texte. vous pouvez donc toujours l’utiliser pour guider l’allocation de mémoire tampon. Ce comportement peut se produire lorsqu’une application utilise à la fois des fonctions ANSI et des boîtes de dialogue courantes, qui utilisent Unicode.

Pour obtenir la longueur exacte du texte, utilisez les messages [**WM \_ gettext**](/windows/desktop/winmsg/wm-gettext), [**lb \_ gettext**](lb-gettext.md)ou [**CB \_ GETLBTEXT**](cb-getlbtext.md) , ou la fonction [**GetWindowText**](/windows/desktop/api/winuser/nf-winuser-getwindowtexta) .

Si la zone de liste a un style owner-drawn, mais pas le style [**\_ HASSTRINGS kg**](list-box-styles.md) , la valeur de retour est toujours la taille, en octets, d’un **DWORD**.

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

[**\_GETLBTEXT CB**](cb-getlbtext.md)
</dt> <dt>

[**LB, \_ GETTEXT**](lb-gettext.md)
</dt> <dt>

**Autres ressources**
</dt> <dt>

[**GetWindowText**](/windows/desktop/api/winuser/nf-winuser-getwindowtexta)
</dt> <dt>

[**WM \_ GETTEXT**](/windows/desktop/winmsg/wm-gettext)
</dt> </dl>

 

