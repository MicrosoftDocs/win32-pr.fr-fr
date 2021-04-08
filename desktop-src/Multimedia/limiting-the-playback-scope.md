---
title: Limitation de l’étendue de lecture
description: Limitation de l’étendue de lecture
ms.assetid: 080ab96f-1cb5-48d4-ac0a-8fd9ba68a31a
keywords:
- MCIWndPlayFrom macro)
- MCIWndPlayTo macro)
- MCIWndPlayFromTo macro)
- Commandes de lecture MCI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 465bcf7a7b6b5811de8413a1c89f7befcf81037f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839758"
---
# <a name="limiting-the-playback-scope"></a><span data-ttu-id="276e4-107">Limitation de l’étendue de lecture</span><span class="sxs-lookup"><span data-stu-id="276e4-107">Limiting the Playback Scope</span></span>

<span data-ttu-id="276e4-108">Le contrôle de la lecture commence par la macro [**MCIWndPlay**](/windows/desktop/api/Vfw/nf-vfw-mciwndplay) , qui lit le contenu ou le fichier associé à une fenêtre MCIWnd de la position de lecture actuelle jusqu’à la fin du contenu.</span><span class="sxs-lookup"><span data-stu-id="276e4-108">Controlling playback begins with the [**MCIWndPlay**](/windows/desktop/api/Vfw/nf-vfw-mciwndplay) macro, which plays the content or file associated with an MCIWnd window from the current playback position to the end of the content.</span></span> <span data-ttu-id="276e4-109">Si vous souhaitez limiter la lecture à une partie spécifique du contenu ou du fichier, vous pouvez choisir parmi les autres macros de lecture MCIWnd : [**MCIWndPlayFrom**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfrom), [**MCIWndPlayTo**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayto)et [**MCIWndPlayFromTo**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfromto).</span><span class="sxs-lookup"><span data-stu-id="276e4-109">If you want to limit playback to a specific portion of the content or file, you can choose from the other playback MCIWnd macros: [**MCIWndPlayFrom**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfrom), [**MCIWndPlayTo**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayto), and [**MCIWndPlayFromTo**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfromto).</span></span>

<span data-ttu-id="276e4-110">Vous devez également définir un format d’heure approprié.</span><span class="sxs-lookup"><span data-stu-id="276e4-110">You also need to set an appropriate time format.</span></span> <span data-ttu-id="276e4-111">Le format d’heure détermine si le contenu est mesuré en images, millisecondes, pistes ou d’autres unités.</span><span class="sxs-lookup"><span data-stu-id="276e4-111">The time format determines whether the content is measured in frames, milliseconds, tracks, or some other units.</span></span>

<span data-ttu-id="276e4-112">L’exemple suivant crée une fenêtre MCIWnd et fournit des commandes de menu pour lire le dernier tiers, le premier tiers ou le troisième milieu du contenu.</span><span class="sxs-lookup"><span data-stu-id="276e4-112">The following example creates an MCIWnd window and provides menu commands to play the last third, first third, or middle third of the content.</span></span> <span data-ttu-id="276e4-113">Ces commandes de menu utilisent **MCIWndPlayFrom**, **MCIWndPlayTo** et **MCIWndPlayFromTo** pour lire les segments de contenu.</span><span class="sxs-lookup"><span data-stu-id="276e4-113">These menu commands use **MCIWndPlayFrom**, **MCIWndPlayTo**, and **MCIWndPlayFromTo** to play the content segments.</span></span> <span data-ttu-id="276e4-114">L’exemple utilise également les macros [**MCIWndGetStart**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetstart) et [**MCIWndGetEnd**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetend) pour identifier le début et la fin du contenu, et il utilise la macro [**MCIWndHome**](/windows/desktop/api/Vfw/nf-vfw-mciwndhome) pour déplacer la position de lecture jusqu’au début du contenu.</span><span class="sxs-lookup"><span data-stu-id="276e4-114">The example also uses the [**MCIWndGetStart**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetstart) and [**MCIWndGetEnd**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetend) macros to identify the beginning and end of the content, and it uses the [**MCIWndHome**](/windows/desktop/api/Vfw/nf-vfw-mciwndhome) macro to move the playback position to the beginning of the content.</span></span>

<span data-ttu-id="276e4-115">La fonction [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) utilise les \_ styles WS Caption et MCIWNDF \_ ShowAll en plus des styles de fenêtre standard pour afficher le nom de fichier, le mode et la position de lecture actuelle dans la barre de titre de la fenêtre MCIWnd.</span><span class="sxs-lookup"><span data-stu-id="276e4-115">The [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) function uses the WS\_CAPTION and MCIWNDF\_SHOWALL styles in addition to the standard window styles to display the filename, mode, and current playback position in the title bar of the MCIWnd window.</span></span>


```C++
case WM_COMMAND: 
    switch (wParam) 
    { 
        case IDM_CREATEMCIWND: 
            g_hwndMCIWnd = MCIWndCreate(hwnd, 
                g_hinst, 
                WS_CHILD | WS_VISIBLE | WS_CAPTION | 
                MCIWNDF_SHOWALL, 
                "sample.avi"); 
            break;
        case IDM_PLAYFROM:                // plays last third of clip 
            MCIWndUseTime(g_hwndMCIWnd);  // millisecond format 
 
        // Get media start and end positions. 
            lStart = MCIWndGetStart(g_hwndMCIWnd); 
            lEnd = MCIWndGetEnd(g_hwndMCIWnd); 
 
        // Determine playback end position. 
            lPlayStart = 2 * (lEnd - lStart) / 3 + lStart; 
 
            MCIWndPlayFrom(g_hwndMCIWnd, lPlayStart); 
            break; 
        case IDM_PLAYTO:                  // plays first third of clip 
            MCIWndUseTime(g_hwndMCIWnd);  // millisecond format 
 
        // Get media start and end positions. 
            lStart = MCIWndGetStart(g_hwndMCIWnd); 
            lEnd = MCIWndGetEnd(g_hwndMCIWnd); 
 
        // Determine playback start position. 
            lPlayEnd = (lEnd - lStart) / 3 + lStart;
 
            MCIWndHome(g_hwndMCIWnd); 
            MCIWndPlayTo(g_hwndMCIWnd, lPlayEnd); 
            break; 
        case IDM_PLAYSOME:               // plays middle third of clip 
            MCIWndUseTime(g_hwndMCIWnd); // millisecond format 
 
        // Get media start and end positions. 
            lStart = MCIWndGetStart(g_hwndMCIWnd); 
            lEnd = MCIWndGetEnd(g_hwndMCIWnd); 
 
        // Determine playback start and end positions. 
            lPlayStart = (lEnd - lStart) / 3 + lStart;
            lPlayEnd = 2 * (lEnd - lStart) / 3 + lStart; 
 
            MCIWndPlayFromTo(g_hwndMCIWnd, lPlayStart, lPlayEnd); 
            break; 
    
    // Handle other commands here. 
    } 
```



 

 




