---
description: Le sous-classing est une technique qui permet à une application d’intercepter et de traiter les messages envoyés ou publiés dans une fenêtre particulière avant qu’une procédure de fenêtre n’ait la possibilité de les traiter.
ms.assetid: 6f7ee9ff-479d-4cb0-8de1-1c3b671551f9
title: Sous-classe et traduction automatique des messages
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7f0aebabe4bde259a982152327ce61a14de915c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106522096"
---
# <a name="subclassing-and-automatic-message-translation"></a>Sous-classe et traduction automatique des messages

Le sous-classing est une technique qui permet à une application d’intercepter et de traiter les messages envoyés ou publiés dans une fenêtre particulière avant qu’une procédure de fenêtre n’ait la possibilité de les traiter. Le système d’exploitation convertit automatiquement les messages en page de codes ou formulaire [Unicode](unicode.md) [Windows (ANSI)](code-pages.md) , selon la forme de la fonction qui a sous-classé la procédure de fenêtre.

L’appel suivant à la fonction [**SetWindowLongA**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) sous-classe la procédure de fenêtre active associée à la fenêtre identifiée par le paramètre *HWND* . Une application peut également utiliser [**SetWindowLongPtrA**](/windows/win32/api/winuser/nf-winuser-setwindowlongptra). La nouvelle procédure de fenêtre **NewWndProc** recevra des messages avec du texte dans le format de page de codes Windows.


```C++
OldWndProc = (WNDPROC) SetWindowLongA(hWnd,
             GWL_WNDPROC, (LONG)NewWndProc); 
```



Quand **NewWndProc** a terminé le traitement d’un message, il utilise la fonction [**CallWindowProc**](/windows/win32/api/winuser/nf-winuser-callwindowproca) comme suit pour transmettre le message à **OldWndProc**.


```C++
CallWindowProc(OldWndProc, hWnd, uMessage, wParam, lParam);
```



Si **OldWndProc** a été créé avec un style de classe Unicode, les messages sont traduits à partir du formulaire de page de codes Windows reçu par **NewWndProc** en Unicode.

De même, un appel à la fonction [**SetWindowLongW**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) ou [**SetWindowLongPtrW**](/windows/win32/api/winuser/nf-winuser-setwindowlongptra) sous-classe la procédure de fenêtre active avec une procédure de fenêtre qui attend des messages texte Unicode. La traduction du message, si nécessaire, est effectuée pendant le traitement de la fonction [**CallWindowProc**](/windows/win32/api/winuser/nf-winuser-callwindowproca) .

Pour plus d’informations sur le sous-classement, consultez [procédures de fenêtre](../winmsg/window-procedures.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation d’Unicode et de jeux de caractères](using-unicode-and-character-sets.md)
</dt> </dl>

 

 
