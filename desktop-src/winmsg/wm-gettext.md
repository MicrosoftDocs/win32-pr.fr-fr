---
description: Copie le texte qui correspond à une fenêtre dans une mémoire tampon fournie par l’appelant.
ms.assetid: 117c3d6d-24cd-462f-bdb0-b65d8914273a
title: Message WM_GETTEXT (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3e1bc6a8a77c51b3ab5b84f5cce700e65b180b357c932b4044a2b65cb49fc8e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120089889"
---
# <a name="wm_gettext-message"></a>\_Message WM GETTEXT

Copie le texte qui correspond à une fenêtre dans une mémoire tampon fournie par l’appelant.


```C++
#define WM_GETTEXT                      0x000D
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Nombre maximal de caractères à copier, y compris le caractère null de fin.

La taille de la chaîne dans la mémoire tampon peut être réduite pour les applications ANSI (à un minimum de la moitié de la valeur *wParam* ) en raison de la conversion d’ANSI en Unicode.

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers la mémoire tampon qui doit recevoir le texte.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **LRESULT**

La valeur de retour est le nombre de caractères copiés, à l’exclusion du caractère null de fin.

## <a name="remarks"></a>Remarques

La fonction [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) copie le texte associé à la fenêtre dans la mémoire tampon spécifiée et retourne le nombre de caractères copiés. Notez que pour les contrôles statiques non textuels, vous obtenez le texte avec lequel le contrôle a été créé à l’origine, c’est-à-dire le numéro d’identification. Toutefois, il vous donne l’ID du contrôle statique non textuel tel qu’il a été créé à l’origine. Autrement dit, si vous utilisiez par la suite un **\_ SETIMAGE STM** pour le modifier, l’ID d’origine est toujours retourné.

Pour un contrôle d’édition, le texte à copier correspond au contenu du contrôle d’édition. Pour une zone de liste modifiable, le texte est le contenu de la partie contrôle d’édition (ou texte statique) de la zone de liste déroulante. Pour un bouton, le texte est le nom du bouton. Pour les autres fenêtres, le texte est le titre de la fenêtre. Pour copier le texte d’un élément dans une zone de liste, une application peut utiliser le message d’attente [**\_ GETTEXT**](../controls/lb-gettext.md) .

Lorsque le message **WM \_ GETTEXT** est envoyé à un contrôle statique avec le style d' **\_ icône SS** , un handle vers l’icône est retourné dans les quatre premiers octets de la mémoire tampon pointée par *lParam*. Cela est vrai uniquement si le message [**WM \_ SETTEXT**](wm-settext.md) a été utilisé pour définir l’icône.

**Modification riche :** Si le texte à copier dépasse 64 Ko, utilisez le message [**em \_ STREAMOUT**](../controls/em-streamout.md) ou [**em \_ GETSELTEXT**](../controls/em-getseltext.md) .

L’envoi d’un message **WM \_ GETTEXT** à un contrôle statique non textuel, tel qu’une image bitmap statique ou un contrôle d’icône statique, ne retourne pas de valeur de chaîne. Au lieu de cela, elle retourne zéro. en outre, dans les premières versions de Windows, les applications pouvaient envoyer un message **WM \_ GETTEXT** à un contrôle statique non textuel pour récupérer l’ID du contrôle. Pour récupérer l’ID d’un contrôle, les applications peuvent utiliser [**GetWindowLong**](/windows/win32/api/winuser/nf-winuser-getwindowlonga) en passant l' **\_ ID de GWL** en tant que valeur d’index ou [**GetWindowLongPtr**](/windows/win32/api/winuser/nf-winuser-getwindowlongptra) à l’aide de l' **\_ ID GWLP**.

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

[**GetWindowLong**](/windows/win32/api/winuser/nf-winuser-getwindowlonga)
</dt> <dt>

[**GetWindowLongPtr**](/windows/win32/api/winuser/nf-winuser-getwindowlongptra)
</dt> <dt>

[**GetWindowText**](/windows/win32/api/winuser/nf-winuser-getwindowtexta)
</dt> <dt>

[**GetWindowTextLength**](/windows/win32/api/winuser/nf-winuser-getwindowtextlengtha)
</dt> <dt>

[**\_GETTEXTLENGTH WM**](wm-gettextlength.md)
</dt> <dt>

[**WM, \_ SETTEXT**](wm-settext.md)
</dt> <dt>

**Méthodologique**
</dt> <dt>

[Windows](windows.md)
</dt> <dt>

**Autres ressources**
</dt> <dt>

[**\_GETSELTEXT em**](../controls/em-getseltext.md)
</dt> <dt>

[**\_STREAMOUT em**](../controls/em-streamout.md)
</dt> <dt>

[**LB, \_ GETTEXT**](../controls/lb-gettext.md)
</dt> </dl>

 

 
