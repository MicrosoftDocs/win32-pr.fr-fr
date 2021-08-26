---
title: Méthode OnPaint
description: Méthode OnPaint
ms.assetid: 4b335362-4430-4b05-8aea-7de8df9cc91f
keywords:
- plug-ins Lecteur Windows Media, méthode OnPaint
- plug-ins, méthode OnPaint
- plug-ins d’interface utilisateur, méthode OnPaint
- Plug-ins d’interface utilisateur, méthode OnPaint
- OnPaint (méthode)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa5e121cdaeac1c7589e58b1613a8d25bdff4f44f6db2375bcbdc34da20929e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120001949"
---
# <a name="the-onpaint-method"></a>Méthode OnPaint

La méthode OnPaint est appelée chaque fois que la fenêtre de plug-in doit se peindre elle-même. Cela se produit lorsque la fenêtre du plug-in reçoit un \_ message de peinture WM, qui est mappé à la méthode OnPaint dans la table des messages décrite précédemment. L’Assistant fournit une implémentation de cette méthode qui peint le noir d’arrière-plan et place le nom du plug-in dans la fenêtre du plug-in. La seule modification nécessaire pour le plug-in de l’interface utilisateur de recherche est la suppression du code qui affiche le texte.

Le code suivant est utilisé pour implémenter cette méthode :


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



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Implémentation de CPluginWindow**](implementing-cpluginwindow.md)
</dt> </dl>

 

 




