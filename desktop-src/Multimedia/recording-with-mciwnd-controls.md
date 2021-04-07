---
title: Enregistrement avec des contrôles MCIWnd
description: Enregistrement avec des contrôles MCIWnd
ms.assetid: 65a57400-aeea-4a27-8d51-37d3d9e9bd55
keywords:
- MCIWndCreate fonction)
- MCIWndNew macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 814bd9f92b895c03ccbb073f830dbf31dcd2e3c2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103939677"
---
# <a name="recording-with-mciwnd-controls"></a><span data-ttu-id="3a1fb-105">Enregistrement avec des contrôles MCIWnd</span><span class="sxs-lookup"><span data-stu-id="3a1fb-105">Recording with MCIWnd Controls</span></span>

<span data-ttu-id="3a1fb-106">L’exemple suivant enregistre l’audio de forme d’onde à l’aide des contrôles intégrés de la fenêtre MCIWnd.</span><span class="sxs-lookup"><span data-stu-id="3a1fb-106">The following example records waveform audio using the built-in controls of the MCIWnd window.</span></span> <span data-ttu-id="3a1fb-107">L’exemple crée une fenêtre MCIWnd en utilisant le \_ style de fenêtre d’enregistrement MCIWNDF avec la fonction [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) pour ajouter un bouton d' **enregistrement** à la barre d’outils.</span><span class="sxs-lookup"><span data-stu-id="3a1fb-107">The example creates an MCIWnd window by using the MCIWNDF\_RECORD window style with the [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) function to add a **Record** button to the toolbar.</span></span> <span data-ttu-id="3a1fb-108">La macro [**MCIWndNew**](/windows/desktop/api/Vfw/nf-vfw-mciwndnew) indique qu’un nouveau fichier est associé à la fenêtre MCIWnd et qu’un périphérique Wave-Audio fournit son contenu.</span><span class="sxs-lookup"><span data-stu-id="3a1fb-108">The [**MCIWndNew**](/windows/desktop/api/Vfw/nf-vfw-mciwndnew) macro indicates a new file is associated with the MCIWnd window and that a waveform-audio device will provide its content.</span></span> <span data-ttu-id="3a1fb-109">Une deuxième commande de menu, IDM \_ SAVEMCIWND, permet à l’utilisateur d’enregistrer l’enregistrement et de sélectionner un nom de fichier à l’aide de la macro [**MCIWndSaveDialog**](/windows/desktop/api/Vfw/nf-vfw-mciwndsavedialog) .</span><span class="sxs-lookup"><span data-stu-id="3a1fb-109">A second menu command, IDM\_SAVEMCIWND, lets the user save the recording and select a filename by using the [**MCIWndSaveDialog**](/windows/desktop/api/Vfw/nf-vfw-mciwndsavedialog) macro.</span></span>


```C++
case WM_COMMAND: 
    switch (wParam) { 
    case IDM_CREATEMCIWND: 
        g_hwndMCIWnd = MCIWndCreate(hwnd, g_hinst, 
            WS_VISIBLE | MCIWNDF_RECORD, NULL); 
        MCIWndNew(g_hwndMCIWnd, "waveaudio"); 
        break;    
    case IDM_SAVEMCIWND: 
        MCIWndSaveDialog(g_hwndMCIWnd); 
        break; 
    } 
```



 

 




