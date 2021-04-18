---
title: Méthode OnPaint
description: Méthode OnPaint
ms.assetid: 4b335362-4430-4b05-8aea-7de8df9cc91f
keywords:
- Plug-ins du lecteur Windows Media, méthode OnPaint
- plug-ins, méthode OnPaint
- plug-ins d’interface utilisateur, méthode OnPaint
- Plug-ins d’interface utilisateur, méthode OnPaint
- OnPaint (méthode)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22641c34bb2edab30c1bf97011e893bc1d9d44a6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104462399"
---
# <a name="the-onpaint-method"></a><span data-ttu-id="36e41-108">Méthode OnPaint</span><span class="sxs-lookup"><span data-stu-id="36e41-108">The OnPaint Method</span></span>

<span data-ttu-id="36e41-109">La méthode OnPaint est appelée chaque fois que la fenêtre de plug-in doit se peindre elle-même.</span><span class="sxs-lookup"><span data-stu-id="36e41-109">The OnPaint method is called whenever the plug-in window should paint itself.</span></span> <span data-ttu-id="36e41-110">Cela se produit lorsque la fenêtre du plug-in reçoit un \_ message de peinture WM, qui est mappé à la méthode OnPaint dans la table des messages décrite précédemment.</span><span class="sxs-lookup"><span data-stu-id="36e41-110">This occurs when the plug-in window receives a WM\_PAINT message, which is mapped to the OnPaint method in the message map described earlier.</span></span> <span data-ttu-id="36e41-111">L’Assistant fournit une implémentation de cette méthode qui peint le noir d’arrière-plan et place le nom du plug-in dans la fenêtre du plug-in.</span><span class="sxs-lookup"><span data-stu-id="36e41-111">The wizard provides an implementation of this method that paints the background black and places the name of the plug-in in the plug-in window.</span></span> <span data-ttu-id="36e41-112">La seule modification nécessaire pour le plug-in de l’interface utilisateur de recherche est la suppression du code qui affiche le texte.</span><span class="sxs-lookup"><span data-stu-id="36e41-112">The only modification that is necessary for the Search UI plug-in is the removal of the code that displays the text.</span></span>

<span data-ttu-id="36e41-113">Le code suivant est utilisé pour implémenter cette méthode :</span><span class="sxs-lookup"><span data-stu-id="36e41-113">The following code is used to implement this method:</span></span>


```C++
LRESULT OnPaint(UINT nMsg, WPARAM wParam, 
                         LPARAM lParam, BOOL& bHandled)
{
    PAINTSTRUCT ps;

    HDC hDC = BeginPaint(&ps);

    RECT rc;
    GetClientRect(&rc);

    HBRUSH hNewBrush = ::CreateSolidBrush( RGB(0, 0, 0) );

    if (hNewBrush)
    {
        ::FillRect(hDC, &rc, hNewBrush );
        ::DeleteObject( hNewBrush );
    }

    EndPaint(&ps);
    return 0;
}

```



## <a name="related-topics"></a><span data-ttu-id="36e41-114">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="36e41-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="36e41-115">**Implémentation de CPluginWindow**</span><span class="sxs-lookup"><span data-stu-id="36e41-115">**Implementing CPluginWindow**</span></span>](implementing-cpluginwindow.md)
</dt> </dl>

 

 




