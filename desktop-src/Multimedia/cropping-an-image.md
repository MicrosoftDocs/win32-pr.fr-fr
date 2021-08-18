---
title: Rognage d’une image
description: Rognage d’une image
ms.assetid: 6600751c-d4b6-481d-bf69-be2d34244c05
keywords:
- MCIWndGetSource macro)
- MCIWndPutSource macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0150962dc85e1e179e52a06c7af6c29193b40b50e9acc7a9feecd0570ab4214
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119144605"
---
# <a name="cropping-an-image"></a>Rognage d’une image

L’exemple suivant crée une fenêtre MCIWnd et charge un fichier AVI. La fenêtre comprend une commande Rogner dans le menu, qui rogne un quart de la hauteur ou de la largeur de chacun des quatre côtés du cadre. L’exemple récupère les dimensions actuelles (initiales) du rectangle source à l’aide de la macro [**MCIWndGetSource**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetsource) . Le rectangle source modifié est la moitié de la hauteur et de la largeur d’origine et est centré dans le frame d’origine. L’appel de la macro [**MCIWndPutSource**](/windows/desktop/api/Vfw/nf-vfw-mciwndputsource) redéfinit les coordonnées du rectangle source.


```C++
// extern RECT rSource, rDest; 
 
case WM_COMMAND: 
    switch (wParam) 
    { 
        case IDM_CREATEMCIWND: 
            g_hwndMCIWnd = MCIWndCreate( hwnd, 
                g_hinst, 
                WS_CHILD | WS_VISIBLE, 
                "sample.avi" ); 
            break; 
        case IDM_CROPIMAGE:                          // crops image 
            MCIWndGetSource(g_hwndMCIWnd, &rSource); // source rectangle
            rDest.left = rSource.left +              // new boundaries
                ((rSource.right - rSource.left) / 4); 
            rDest.right = rSource.right - 
                ((rSource.right - rSource.left) / 4); 
            rDest.top = rSource.top + 
                ((rSource.bottom - rSource.top) / 4); 
            rDest.bottom = rSource.bottom - 
                ((rSource.bottom - rSource.top) / 4); 
 
            MCIWndPutSource(g_hwndMCIWnd, &rDest);   // new source rectangle 
    } 
    break; 

    // Handle other messages here. 
```



 

 




