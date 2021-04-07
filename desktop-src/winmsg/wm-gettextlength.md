---
description: Détermine la longueur, en caractères, du texte associé à une fenêtre.
ms.assetid: 9e185435-a624-4380-adfd-be4f3645ee5d
title: Message WM_GETTEXTLENGTH (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0efc058033f9c4939137414d305d0717b54bef54
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952419"
---
# <a name="wm_gettextlength-message"></a>\_Message WM GETTEXTLENGTH

Détermine la longueur, en caractères, du texte associé à une fenêtre.


```C++
#define WM_GETTEXTLENGTH                0x000E
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Ce paramètre n’est pas utilisé et doit être égal à zéro.

</dd> <dt>

*lParam* 
</dt> <dd>

Ce paramètre n’est pas utilisé et doit être égal à zéro.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **LRESULT**

La valeur de retour correspond à la longueur du texte en caractères, à l’exclusion du caractère null de fin.

## <a name="remarks"></a>Notes

Pour un contrôle d’édition, le texte à copier correspond au contenu du contrôle d’édition. Pour une zone de liste modifiable, le texte est le contenu de la partie contrôle d’édition (ou texte statique) de la zone de liste déroulante. Pour un bouton, le texte est le nom du bouton. Pour les autres fenêtres, le texte est le titre de la fenêtre. Pour déterminer la longueur d’un élément dans une zone de liste, une application peut utiliser le message [**lb \_ GETTEXTLEN**](../controls/lb-gettextlen.md) .

Lorsque le message **WM \_ GETTEXTLENGTH** est envoyé, la fonction [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) retourne la longueur, en caractères, du texte. Dans certaines conditions, la fonction **DefWindowProc** retourne une valeur supérieure à la longueur réelle du texte. Cela se produit avec certains mélanges d’ANSI et Unicode, et est dû au système qui autorise l’existence possible de caractères DBCS (Double-Byte Character Set) dans le texte. Toutefois, la valeur de retour sera toujours au moins égale à la longueur réelle du texte. vous pouvez donc toujours l’utiliser pour guider l’allocation de mémoire tampon. Ce comportement peut se produire lorsqu’une application utilise à la fois des fonctions ANSI et des boîtes de dialogue courantes, qui utilisent Unicode.

Pour obtenir la longueur exacte du texte, utilisez les messages [**WM \_ gettext**](wm-gettext.md), [**lb \_ gettext**](../controls/lb-gettext.md)ou [**CB \_ GETLBTEXT**](../controls/cb-getlbtext.md) , ou la fonction [**GetWindowText**](/windows/win32/api/winuser/nf-winuser-getwindowtexta) .

L’envoi d’un message **WM \_ GETTEXTLENGTH** à un contrôle statique non textuel, tel qu’une image bitmap statique ou une icône statique controlc, ne retourne pas de valeur de chaîne. Au lieu de cela, elle retourne zéro.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                               |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**GetWindowText**](/windows/win32/api/winuser/nf-winuser-getwindowtexta)
</dt> <dt>

[**GetWindowTextLength**](/windows/win32/api/winuser/nf-winuser-getwindowtextlengtha)
</dt> <dt>

[**WM \_ GETTEXT**](wm-gettext.md)
</dt> <dt>

**Méthodologique**
</dt> <dt>

[Windows](windows.md)
</dt> <dt>

**Autres ressources**
</dt> <dt>

[**\_GETLBTEXT CB**](../controls/cb-getlbtext.md)
</dt> <dt>

[**LB, \_ GETTEXT**](../controls/lb-gettext.md)
</dt> <dt>

[**\_GETTEXTLEN lb**](../controls/lb-gettextlen.md)
</dt> </dl>

 

 
