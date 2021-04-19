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
# <a name="creating-an-mciwnd-window"></a><span data-ttu-id="10a96-105">Création d’une fenêtre MCIWnd</span><span class="sxs-lookup"><span data-stu-id="10a96-105">Creating an MCIWnd Window</span></span>

<span data-ttu-id="10a96-106">La fonction [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) inscrit et crée une fenêtre MCIWnd.</span><span class="sxs-lookup"><span data-stu-id="10a96-106">The [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) function registers and creates an MCIWnd window.</span></span> <span data-ttu-id="10a96-107">La fenêtre peut être une fenêtre parente, enfant ou indépendante.</span><span class="sxs-lookup"><span data-stu-id="10a96-107">The window can be a parent, child, or pop-up window.</span></span> <span data-ttu-id="10a96-108">L’exemple suivant crée une fenêtre MCIWnd en tant que fenêtre enfant et permet à l’utilisateur de contrôler la lecture en fournissant un accès à la barre de suivi et aux boutons **lecture**, **arrêt** et **menu** .</span><span class="sxs-lookup"><span data-stu-id="10a96-108">The following example creates an MCIWnd window as a child window and lets the user control playback by providing access to the trackbar and the **Play**, **Stop**, and **Menu** buttons.</span></span> <span data-ttu-id="10a96-109">L’exemple spécifie un handle de fenêtre parente et spécifie la **valeur null** pour les styles de fenêtre. par conséquent, les styles de fenêtre par défaut de WS \_ Child, WS \_ Border et WS \_ visible sont utilisés pour créer la fenêtre MCIWnd.</span><span class="sxs-lookup"><span data-stu-id="10a96-109">The example specifies a handle of a parent window and specifies **NULL** for the window styles, so the default window styles of WS\_CHILD, WS\_BORDER, and WS\_VISIBLE are used to create the MCIWnd window.</span></span>


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
> <span data-ttu-id="10a96-110">Vous pouvez également spécifier **null** pour le handle de fenêtre parente et les styles de fenêtre, auquel cas les styles de fenêtre par défaut seraient WS \_ OVERLAPPED et WS \_ visible.</span><span class="sxs-lookup"><span data-stu-id="10a96-110">You could also specify **NULL** for both the parent window handle and the window styles, in which case the default window styles would be WS\_OVERLAPPED and WS\_VISIBLE.</span></span>

 

 

 




