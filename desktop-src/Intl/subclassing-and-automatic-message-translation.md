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
# <a name="subclassing-and-automatic-message-translation"></a><span data-ttu-id="ad83b-103">Sous-classe et traduction automatique des messages</span><span class="sxs-lookup"><span data-stu-id="ad83b-103">Subclassing and Automatic Message Translation</span></span>

<span data-ttu-id="ad83b-104">Le sous-classing est une technique qui permet à une application d’intercepter et de traiter les messages envoyés ou publiés dans une fenêtre particulière avant qu’une procédure de fenêtre n’ait la possibilité de les traiter.</span><span class="sxs-lookup"><span data-stu-id="ad83b-104">Subclassing is a technique that allows an application to intercept and process messages sent or posted to a particular window before a window procedure has a chance to process them.</span></span> <span data-ttu-id="ad83b-105">Le système d’exploitation convertit automatiquement les messages en page de codes ou formulaire [Unicode](unicode.md) [Windows (ANSI)](code-pages.md) , selon la forme de la fonction qui a sous-classé la procédure de fenêtre.</span><span class="sxs-lookup"><span data-stu-id="ad83b-105">The operating system automatically translates messages into [Windows (ANSI) code page](code-pages.md) or [Unicode](unicode.md) form, depending on the form of the function that has subclassed the window procedure.</span></span>

<span data-ttu-id="ad83b-106">L’appel suivant à la fonction [**SetWindowLongA**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) sous-classe la procédure de fenêtre active associée à la fenêtre identifiée par le paramètre *HWND* .</span><span class="sxs-lookup"><span data-stu-id="ad83b-106">The following call to the [**SetWindowLongA**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) function subclasses the current window procedure associated with the window identified by the *hWnd* parameter.</span></span> <span data-ttu-id="ad83b-107">Une application peut également utiliser [**SetWindowLongPtrA**](/windows/win32/api/winuser/nf-winuser-setwindowlongptra).</span><span class="sxs-lookup"><span data-stu-id="ad83b-107">Alternatively, an application can use [**SetWindowLongPtrA**](/windows/win32/api/winuser/nf-winuser-setwindowlongptra).</span></span> <span data-ttu-id="ad83b-108">La nouvelle procédure de fenêtre **NewWndProc** recevra des messages avec du texte dans le format de page de codes Windows.</span><span class="sxs-lookup"><span data-stu-id="ad83b-108">The new window procedure **NewWndProc**, will receive messages with text in Windows code page format.</span></span>


```C++
OldWndProc = (WNDPROC) SetWindowLongA(hWnd,
             GWL_WNDPROC, (LONG)NewWndProc); 
```



<span data-ttu-id="ad83b-109">Quand **NewWndProc** a terminé le traitement d’un message, il utilise la fonction [**CallWindowProc**](/windows/win32/api/winuser/nf-winuser-callwindowproca) comme suit pour transmettre le message à **OldWndProc**.</span><span class="sxs-lookup"><span data-stu-id="ad83b-109">When **NewWndProc** has finished processing a message, it uses the [**CallWindowProc**](/windows/win32/api/winuser/nf-winuser-callwindowproca) function as follows to pass the message to **OldWndProc**.</span></span>


```C++
CallWindowProc(OldWndProc, hWnd, uMessage, wParam, lParam);
```



<span data-ttu-id="ad83b-110">Si **OldWndProc** a été créé avec un style de classe Unicode, les messages sont traduits à partir du formulaire de page de codes Windows reçu par **NewWndProc** en Unicode.</span><span class="sxs-lookup"><span data-stu-id="ad83b-110">If **OldWndProc** was created with a class style of UNICODE, messages are translated from the Windows code page form received by **NewWndProc** into Unicode.</span></span>

<span data-ttu-id="ad83b-111">De même, un appel à la fonction [**SetWindowLongW**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) ou [**SetWindowLongPtrW**](/windows/win32/api/winuser/nf-winuser-setwindowlongptra) sous-classe la procédure de fenêtre active avec une procédure de fenêtre qui attend des messages texte Unicode.</span><span class="sxs-lookup"><span data-stu-id="ad83b-111">Similarly, a call to the [**SetWindowLongW**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) or [**SetWindowLongPtrW**](/windows/win32/api/winuser/nf-winuser-setwindowlongptra) function subclasses the current window procedure with a window procedure that expects Unicode text messages.</span></span> <span data-ttu-id="ad83b-112">La traduction du message, si nécessaire, est effectuée pendant le traitement de la fonction [**CallWindowProc**](/windows/win32/api/winuser/nf-winuser-callwindowproca) .</span><span class="sxs-lookup"><span data-stu-id="ad83b-112">Message translation, if necessary, is performed during the processing of the [**CallWindowProc**](/windows/win32/api/winuser/nf-winuser-callwindowproca) function.</span></span>

<span data-ttu-id="ad83b-113">Pour plus d’informations sur le sous-classement, consultez [procédures de fenêtre](../winmsg/window-procedures.md).</span><span class="sxs-lookup"><span data-stu-id="ad83b-113">For more information about subclassing, see [Window Procedures](../winmsg/window-procedures.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="ad83b-114">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ad83b-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ad83b-115">Utilisation d’Unicode et de jeux de caractères</span><span class="sxs-lookup"><span data-stu-id="ad83b-115">Using Unicode and Character Sets</span></span>](using-unicode-and-character-sets.md)
</dt> </dl>

 

 
