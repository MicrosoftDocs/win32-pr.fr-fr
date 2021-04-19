---
title: Création d’une fenêtre MCIWnd
description: Création d’une fenêtre MCIWnd
ms.assetid: bd45e813-5807-43cd-bef1-03285df9a018
keywords:
- Fenêtre MCIWnd, création
- MCIWndCreate fonction)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c205e87acf3e5f529d4b5cc9c9163b7fe887fe04
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106513453"
---
# <a name="creating-an-mciwnd-window"></a>Création d’une fenêtre MCIWnd

La fonction [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) inscrit et crée une fenêtre MCIWnd. La fenêtre peut être une fenêtre parente, enfant ou indépendante. L’exemple suivant crée une fenêtre MCIWnd en tant que fenêtre enfant et permet à l’utilisateur de contrôler la lecture en fournissant un accès à la barre de suivi et aux boutons **lecture**, **arrêt** et **menu** . L’exemple spécifie un handle de fenêtre parente et spécifie la **valeur null** pour les styles de fenêtre. par conséquent, les styles de fenêtre par défaut de WS \_ Child, WS \_ Border et WS \_ visible sont utilisés pour créer la fenêtre MCIWnd.


```C++
// Global variable and constants 
// extern HINSTANCE g_hinst;       instance handle 
// extern HWND g_hwndMCIWnd;       MCIWnd window handle 
 
case WM_COMMAND: 
    switch (wParam) { 
    case IDM_CREATEMCIWND: 
        g_hwndMCIWnd = MCIWndCreate(hwnd, g_hinst, NULL, 
            "sample.avi"); 
        break;    
    } 
    break; 
```



> [!Note]  
> Vous pouvez également spécifier **null** pour le handle de fenêtre parente et les styles de fenêtre, auquel cas les styles de fenêtre par défaut seraient WS \_ OVERLAPPED et WS \_ visible.

 

 

 




