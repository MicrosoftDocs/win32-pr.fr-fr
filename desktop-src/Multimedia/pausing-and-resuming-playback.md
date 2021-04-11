---
title: Suspension et reprise de la lecture
description: Suspension et reprise de la lecture
ms.assetid: f5a7ef22-993c-4aab-bab0-2700289da7a7
keywords:
- MCIWndPause macro)
- MCIWndResume macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1876417b821a57f7ebbac0cd35bec184cc9d2da
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103939854"
---
# <a name="pausing-and-resuming-playback"></a><span data-ttu-id="88fe2-105">Suspension et reprise de la lecture</span><span class="sxs-lookup"><span data-stu-id="88fe2-105">Pausing and Resuming Playback</span></span>

<span data-ttu-id="88fe2-106">Vous pouvez interrompre la lecture d’un appareil ou d’un fichier associé à une fenêtre MCIWnd à l’aide de la macro [**MCIWndPause**](/windows/desktop/api/Vfw/nf-vfw-mciwndpause) .</span><span class="sxs-lookup"><span data-stu-id="88fe2-106">You can interrupt playback of a device or file associated with an MCIWnd window by using the [**MCIWndPause**](/windows/desktop/api/Vfw/nf-vfw-mciwndpause) macro.</span></span> <span data-ttu-id="88fe2-107">Vous pouvez ensuite redémarrer la lecture à l’aide de la macro [**MCIWndResume**](/windows/desktop/api/Vfw/nf-vfw-mciwndresume) .</span><span class="sxs-lookup"><span data-stu-id="88fe2-107">You can then restart playback by using the [**MCIWndResume**](/windows/desktop/api/Vfw/nf-vfw-mciwndresume) macro.</span></span> <span data-ttu-id="88fe2-108">Si l’appareil ne prend pas en charge la reprise ou si une erreur se produit, vous pouvez utiliser la macro [**MCIWndPlay**](/windows/desktop/api/Vfw/nf-vfw-mciwndplay) pour redémarrer la lecture.</span><span class="sxs-lookup"><span data-stu-id="88fe2-108">If the device does not support resume or if an error occurs, you can use the [**MCIWndPlay**](/windows/desktop/api/Vfw/nf-vfw-mciwndplay) macro to restart playback.</span></span>

<span data-ttu-id="88fe2-109">L’exemple suivant crée une fenêtre MCIWnd et exécute un fichier AVI.</span><span class="sxs-lookup"><span data-stu-id="88fe2-109">The following example creates an MCIWnd window and plays an AVI file.</span></span> <span data-ttu-id="88fe2-110">Les commandes du menu suspendre et reprendre sont accessibles à l’utilisateur pour interrompre et redémarrer la lecture.</span><span class="sxs-lookup"><span data-stu-id="88fe2-110">Pause and resume menu commands are available to the user to interrupt and restart playback.</span></span>

<span data-ttu-id="88fe2-111">Les styles de fenêtre MCIWnd sont modifiés temporairement en utilisant la macro [**MCIWndChangeStyles**](/windows/desktop/api/Vfw/nf-vfw-mciwndchangestyles) pour empêcher l’affichage d’une boîte de dialogue d’erreur MCI si [**MCIWndResume**](/windows/desktop/api/Vfw/nf-vfw-mciwndresume) échoue.</span><span class="sxs-lookup"><span data-stu-id="88fe2-111">MCIWnd window styles are changed temporarily by using the [**MCIWndChangeStyles**](/windows/desktop/api/Vfw/nf-vfw-mciwndchangestyles) macro to inhibit an MCI error dialog box from being displayed if [**MCIWndResume**](/windows/desktop/api/Vfw/nf-vfw-mciwndresume) fails.</span></span>


```C++
case WM_COMMAND: 
    switch (wParam) 
    { 
        case IDM_CREATEMCIWND:             // creates and plays clip 
            g_hwndMCIWnd = MCIWndCreate(hwnd,  
                g_hinst,                      
                WS_CHILD | WS_VISIBLE |    // standard styles
                MCIWNDF_NOPLAYBAR |        // hides toolbar 
                MCIWNDF_NOTIFYMODE,        // notifies of mode changes
                "sample.avi"); 
 
            MCIWndPlay(g_hwndMCIWnd); 
            break;    
        case IDM_PAUSEMCIWND:              // pauses playback 
            MCIWndPause(g_hwndMCIWnd); 
            MessageBox(hwnd, "MCIWnd", "Pausing Playback", MB_OK); 
            break; 
        case IDM_RESUMEMCIWND:          // resumes playback 
            MCIWndChangeStyles(      // hides error dialog messages
                g_hwndMCIWnd,        // MCIWnd window
                MCIWNDF_NOERRORDLG,  // mask of style to change
                MCIWNDF_NOERRORDLG); // suppresses MCI error dialogs 
 
            lResult = MCIWndResume(g_hwndMCIWnd); 
 
            if(lResult){                   // device doesn't resume 
                MessageBox(hwnd, "MCIWnd", 
                    "Resume with Stop and Play", MB_OK); 
                MCIWndStop(g_hwndMCIWnd); 
                MCIWndPlay(g_hwndMCIWnd); 
 
                MCIWndChangeStyles(        // resumes original styles
                    g_hwndMCIWnd, 
                    MCIWNDF_NOERRORDLG, 
                    NULL); 
        } 
        break; 
    } 
    break; 
 
// Handle other messages here. 
```



 

 




