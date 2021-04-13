---
title: Automatisation de la lecture pour MCIWnd
description: Automatisation de la lecture pour MCIWnd
ms.assetid: 7e38e8b1-f56d-4008-83a7-4fba8333e328
keywords:
- MCIWndCreate macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b9224cfa4f5a93488f226d1aefa83201b8b0637
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311131"
---
# <a name="automating-playback-for-mciwnd"></a><span data-ttu-id="0b660-104">Automatisation de la lecture pour MCIWnd</span><span class="sxs-lookup"><span data-stu-id="0b660-104">Automating Playback for MCIWnd</span></span>

<span data-ttu-id="0b660-105">Vous pouvez automatiser la lecture pour MCIWnd en spécifiant certains styles de fenêtre dans la fonction [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) .</span><span class="sxs-lookup"><span data-stu-id="0b660-105">You can automate playback for MCIWnd by specifying certain window styles in the [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) function.</span></span> <span data-ttu-id="0b660-106">Pour lire l’appareil, la fenêtre a besoin d’une fenêtre parente pour traiter les messages de notification, d’une zone de lecture pour lire des fichiers AVI et de la notification des modifications du mode de l’appareil pour identifier le moment où la lecture s’arrête.</span><span class="sxs-lookup"><span data-stu-id="0b660-106">To play the device, the window needs a parent window to process notification messages, a playback area to play AVI files, and notification of device mode changes to identify when playback stops.</span></span> <span data-ttu-id="0b660-107">La fenêtre n’a pas besoin d’une barre d’outils.</span><span class="sxs-lookup"><span data-stu-id="0b660-107">The window does not need a toolbar.</span></span> <span data-ttu-id="0b660-108">Vous pouvez définir ces caractéristiques en spécifiant les styles appropriés dans **MCIWndCreate**.</span><span class="sxs-lookup"><span data-stu-id="0b660-108">You can set these characteristics by specifying the appropriate styles in **MCIWndCreate**.</span></span>

<span data-ttu-id="0b660-109">L’exemple suivant utilise des commandes de menu pour créer une fenêtre MCIWnd pour lire du contenu à partir de différents types d’appareils.</span><span class="sxs-lookup"><span data-stu-id="0b660-109">The following example uses menu commands to create an MCIWnd window to play content from several different types of devices.</span></span> <span data-ttu-id="0b660-110">La fonction **MCIWndCreate** crée la fenêtre MCIWnd, et les périphériques et les fichiers sont chargés à l’aide de la macro [**MCIWndOpen**](/windows/desktop/api/Vfw/nf-vfw-mciwndopen) dans les commandes spécifiques au périphérique.</span><span class="sxs-lookup"><span data-stu-id="0b660-110">The **MCIWndCreate** function creates the MCIWnd window, and devices and files are loaded by using the [**MCIWndOpen**](/windows/desktop/api/Vfw/nf-vfw-mciwndopen) macro in the device-specific commands.</span></span> <span data-ttu-id="0b660-111">Quand un appareil se termine, vous fermez l’appareil en interceptant le message [**MCIWNDM \_ NOTIFYMODE**](mciwndm-notifymode.md) et en émettant la macro [**MCIWndClose**](/windows/desktop/api/Vfw/nf-vfw-mciwndclose) .</span><span class="sxs-lookup"><span data-stu-id="0b660-111">When a device finishes playing, you close the device by trapping the [**MCIWNDM\_NOTIFYMODE**](mciwndm-notifymode.md) message and issuing the [**MCIWndClose**](/windows/desktop/api/Vfw/nf-vfw-mciwndclose) macro.</span></span>


```C++
case WM_COMMAND: 
    switch (wParam) 
    { 
        case IDM_CREATEMCIWND: 
            dwMCIWndStyle = WS_CHILD |     // child window
                WS_VISIBLE |               // visible
                MCIWNDF_NOTIFYMODE |       // notifies of mode changes
                MCIWNDF_NOPLAYBAR;            // hides toolbar 
            g_hwndMCIWnd = MCIWndCreate(hwnd, 
                g_hinst, dwMCIWndStyle, NULL); 
            break; 
        case IDM_PLAYCDA: 
            LoadNGoMCIWnd(hwnd, "CDAudio"); 
            break; 
        case IDM_PLAYWAVE: 
            LoadNGoMCIWnd(hwnd, "SoundWave.WAV"); 
            break; 
        case IDM_PLAYMIDI: 
            LoadNGoMCIWnd(hwnd, "MIDIFile.MID"); 
            break; 
        case IDM_PLAYAVI: 
            LoadNGoMCIWnd(hwnd, "AVIFile.AVI"); 
            break; 
        case IDM_EXIT: 
            MCIWndDestroy(g_hwndMCIWnd); 
            DestroyWindow(hwnd); 
            break; 
    } 
    break; 
 
case MCIWNDM_NOTIFYMODE: 
    if (lParam == MCI_MODE_STOP)  // device stopped
    { 
        MessageBox(hwnd,"","Closing Device",MB_OK); 
        MCIWndClose(g_hwndMCIWnd); 
    } 
    break; 

// Handle other messages here. 
 
// LoadNGoMCIWnd - automatically loads and plays a multimedia device 
// 
// hwnd -  handle to the parent window 
// lpstr - pointer to device or filename played by device 
// 
// Global variable 
// extern HINSTANCE g_hwndMCIWnd;  instance handle to MCIWnd window 
 
VOID LoadNGoMCIWnd(HWND hwnd, LPSTR lpstr) 
{ 
    MessageBox(hwnd, lpstr, "Loading Device", MB_OK); 
    MCIWndOpen(g_hwndMCIWnd, lpstr, NULL);   // new device in window 
    MCIWndPlay(g_hwndMCIWnd);                // plays device 
} 
```



 

 




