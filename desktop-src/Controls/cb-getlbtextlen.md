---
title: Message CB_GETLBTEXTLEN (winuser. h)
description: Obtient la longueur, en caractères, d’une chaîne dans la liste d’une zone de liste déroulante.
ms.assetid: f0fe0eef-f9db-4d9f-9a42-5bb2aeae30a0
keywords:
- CB_GETLBTEXTLEN les contrôles de message Windows
topic_type:
- apiref
api_name:
- CB_GETLBTEXTLEN
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e42dc19b13b22f577fcc21bb32cb8810bab29be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942113"
---
# <a name="cb_getlbtextlen-message"></a>\_Message GETLBTEXTLEN CB

Obtient la longueur, en caractères, d’une chaîne dans la liste d’une zone de liste déroulante.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Index de base zéro de la chaîne.

</dd> <dt>

*lParam* 
</dt> <dd>

Ce paramètre n'est pas utilisé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La valeur de retour est la longueur de la chaîne, dans **TCHAR** s, à l’exclusion du caractère null de fin. Si une chaîne ANSI correspond au nombre d’octets, et s’il s’agit d’une chaîne Unicode, il s’agit du nombre de caractères. Dans certaines conditions, cette valeur peut en fait être supérieure à la longueur du texte. Pour plus d'informations, consultez la section Notes.

Si le paramètre *wParam* ne spécifie pas d’index valide, la valeur de retour est CB \_ Err.

## <a name="remarks"></a>Notes

Dans certaines conditions, la valeur de retour est supérieure à la longueur réelle du texte. Cela se produit avec certains mélanges d’ANSI et Unicode, et est dû au système d’exploitation qui autorise l’existence possible de caractères DBCS (Double-Byte Character Set) dans le texte. Toutefois, la valeur de retour sera toujours au moins égale à la longueur réelle du texte. vous pouvez donc toujours l’utiliser pour guider l’allocation de mémoire tampon. Ce comportement peut se produire lorsqu’une application utilise à la fois des fonctions ANSI et des boîtes de dialogue courantes, qui utilisent Unicode.

Pour obtenir la longueur exacte du texte, utilisez les messages [**WM \_ gettext**](/windows/desktop/winmsg/wm-gettext), [**lb \_ gettext**](lb-gettext.md)ou [**CB \_ GETLBTEXT**](cb-getlbtext.md) , ou la fonction [**GetWindowText**](/windows/desktop/api/winuser/nf-winuser-getwindowtexta) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                                     |
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

 

