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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127110861"
---
# <a name="pausing-and-resuming-playback"></a>Suspension et reprise de la lecture

Vous pouvez interrompre la lecture d’un appareil ou d’un fichier associé à une fenêtre MCIWnd à l’aide de la macro [**MCIWndPause**](/windows/desktop/api/Vfw/nf-vfw-mciwndpause) . Vous pouvez ensuite redémarrer la lecture à l’aide de la macro [**MCIWndResume**](/windows/desktop/api/Vfw/nf-vfw-mciwndresume) . Si l’appareil ne prend pas en charge la reprise ou si une erreur se produit, vous pouvez utiliser la macro [**MCIWndPlay**](/windows/desktop/api/Vfw/nf-vfw-mciwndplay) pour redémarrer la lecture.

L’exemple suivant crée une fenêtre MCIWnd et exécute un fichier AVI. Les commandes du menu suspendre et reprendre sont accessibles à l’utilisateur pour interrompre et redémarrer la lecture.

Les styles de fenêtre MCIWnd sont modifiés temporairement en utilisant la macro [**MCIWndChangeStyles**](/windows/desktop/api/Vfw/nf-vfw-mciwndchangestyles) pour empêcher l’affichage d’une boîte de dialogue d’erreur MCI si [**MCIWndResume**](/windows/desktop/api/Vfw/nf-vfw-mciwndresume) échoue.


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



 

 




