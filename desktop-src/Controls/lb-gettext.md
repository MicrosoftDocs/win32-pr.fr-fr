---
title: Message LB_GETTEXT (winuser. h)
description: Obtient une chaîne à partir d’une zone de liste.
ms.assetid: 6bf7ec3b-237b-4668-9493-40c098a32428
keywords:
- LB_GETTEXT les contrôles de message Windows
topic_type:
- apiref
api_name:
- LB_GETTEXT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c3dd5e2c7a9e6c1c1aa1b847592555a013766134
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466335"
---
# <a name="lb_gettext-message"></a>LB, \_ message GETTEXT

Obtient une chaîne à partir d’une zone de liste.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Index de base zéro de la chaîne à récupérer.

Windows 95/Windows 98/Windows Millennium Edition (Windows Me) : le paramètre *wParam* est limité aux valeurs 16 bits. Cela signifie que les zones de liste ne peuvent pas contenir plus de 32 767 éléments. Bien que le nombre d’éléments soit limité, la taille totale, en octets, des éléments d’une zone de liste n’est limitée que par la mémoire disponible.

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers la mémoire tampon qui recevra la chaîne ; Il s’agit du type **LPTStr** qui est ensuite casté en **lParam**. La mémoire tampon doit avoir suffisamment d’espace pour la chaîne et un caractère null de fin. Un [**message \_ GETTEXTLEN**](lb-gettextlen.md) peut être envoyé avant le message d’attente **\_ GETTEXT** pour récupérer la longueur, dans **TCHAR** s, de la chaîne.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La valeur de retour est la longueur de la chaîne, dans **TCHAR** s, à l’exclusion du caractère null de fin. Si *wParam* ne spécifie pas d’index valide, la valeur de retour est lb \_ Err.

## <a name="remarks"></a>Notes

Si la zone de liste a un style owner-drawn, mais pas le style [**\_ HASSTRINGS kg**](list-box-styles.md) , la mémoire tampon vers laquelle pointe le paramètre *lParam* reçoit la valeur associée à l’élément (les données de l’élément).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_GETTEXTLEN lb**](lb-gettextlen.md)
</dt> </dl>

 

 





