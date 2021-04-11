---
title: Personnalisation du processus d’enregistrement
description: Personnalisation du processus d’enregistrement
ms.assetid: 9453b9d3-ae9c-4f57-8dd6-f84b9a76618e
keywords:
- MCIWndCreate fonction)
- MCIWndNew macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec46f61ef4624ba613025f01b081ccc1ebda1cad
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103939938"
---
# <a name="customizing-the-recording-process"></a><span data-ttu-id="a9021-105">Personnalisation du processus d’enregistrement</span><span class="sxs-lookup"><span data-stu-id="a9021-105">Customizing the Recording Process</span></span>

<span data-ttu-id="a9021-106">Vous pouvez personnaliser le processus d’enregistrement, en contrôlant entièrement le tout, de la création de la fenêtre MCIWnd à l’enregistrement des informations enregistrées dans un fichier.</span><span class="sxs-lookup"><span data-stu-id="a9021-106">You can customize the recording process, taking complete control of most everything — from creating the MCIWnd window to saving the recorded information in a file.</span></span> <span data-ttu-id="a9021-107">L’exemple suivant interroge l’appareil MCI pour les fonctionnalités d’enregistrement et d’enregistrement, et comprend des commandes de menu à enregistrer au début ou à la fin du contenu.</span><span class="sxs-lookup"><span data-stu-id="a9021-107">The following example queries the MCI device for recording and saving capabilities, and includes menu commands to record at the beginning or end of the content.</span></span>

<span data-ttu-id="a9021-108">L’exemple suivant utilise la fonction [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) pour créer une nouvelle fenêtre et vous permet de spécifier un fichier existant pour stocker les données enregistrées et la macro [**MCIWndNew**](/windows/desktop/api/Vfw/nf-vfw-mciwndnew) pour associer un nouveau fichier à la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="a9021-108">The following example uses the [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) function to create a new window and allows you to specify an existing file to store the recorded data and the [**MCIWndNew**](/windows/desktop/api/Vfw/nf-vfw-mciwndnew) macro to associate a new file with the window.</span></span> <span data-ttu-id="a9021-109">Vous pouvez également utiliser la macro [**MCIWndOpen**](/windows/desktop/api/Vfw/nf-vfw-mciwndopen) ou [**MCIWndOpenDialog**](/windows/desktop/api/Vfw/nf-vfw-mciwndopendialog) pour spécifier un fichier.</span><span class="sxs-lookup"><span data-stu-id="a9021-109">Alternatively, you can use the [**MCIWndOpen**](/windows/desktop/api/Vfw/nf-vfw-mciwndopen) or [**MCIWndOpenDialog**](/windows/desktop/api/Vfw/nf-vfw-mciwndopendialog) macro to specify a file.</span></span>

<span data-ttu-id="a9021-110">L’exemple utilise la macro [**MCIWndCanRecord**](/windows/desktop/api/Vfw/nf-vfw-mciwndcanrecord) pour vérifier que l’appareil peut enregistrer et la macro [**MCIWndCanSave**](/windows/desktop/api/Vfw/nf-vfw-mciwndcansave) pour vérifier que l’appareil enregistre les informations.</span><span class="sxs-lookup"><span data-stu-id="a9021-110">The example uses the [**MCIWndCanRecord**](/windows/desktop/api/Vfw/nf-vfw-mciwndcanrecord) macro to verify that the device can record and the [**MCIWndCanSave**](/windows/desktop/api/Vfw/nf-vfw-mciwndcansave) macro to verify that the device save information.</span></span> <span data-ttu-id="a9021-111">L’exemple définit la position de lecture actuelle à l’aide des macros [**MCIWndHome**](/windows/desktop/api/Vfw/nf-vfw-mciwndhome) et [**MCIWndEnd**](/windows/desktop/api/Vfw/nf-vfw-mciwndend) .</span><span class="sxs-lookup"><span data-stu-id="a9021-111">The example sets the current playback position by using the [**MCIWndHome**](/windows/desktop/api/Vfw/nf-vfw-mciwndhome) and [**MCIWndEnd**](/windows/desktop/api/Vfw/nf-vfw-mciwndend) macros.</span></span> <span data-ttu-id="a9021-112">L’exemple démarre l’enregistrement à l’aide de la macro [**MCIWndRecord**](/windows/desktop/api/Vfw/nf-vfw-mciwndrecord) .</span><span class="sxs-lookup"><span data-stu-id="a9021-112">The example starts recording by using the [**MCIWndRecord**](/windows/desktop/api/Vfw/nf-vfw-mciwndrecord) macro.</span></span> <span data-ttu-id="a9021-113">Une fois les informations enregistrées, l’exemple l’enregistre à l’aide de la macro [**MCIWndSaveDialog**](/windows/desktop/api/Vfw/nf-vfw-mciwndsavedialog) .</span><span class="sxs-lookup"><span data-stu-id="a9021-113">After the information is recorded, the example saves it by using the [**MCIWndSaveDialog**](/windows/desktop/api/Vfw/nf-vfw-mciwndsavedialog) macro.</span></span>


```C++
case WM_COMMAND: 
    switch (wParam) 
    { 
        case IDM_CREATEMCIWND: 
            g_hwndMCIWnd = MCIWndCreate( hwnd, g_hinst, 
                WS_VISIBLE | WS_CHILD | 
                MCIWNDF_RECORD,                   // add Record button
                NULL ); 
 
            MCIWndNew(g_hwndMCIWnd, "waveaudio"); // new file 
 
            if( MCIWndCanRecord(g_hwndMCIWnd) ) 
            { 
                MessageBox( hwnd, 
                "Press the red button on the toolbar to record.", 
                "MCIWnd Record", 
                MB_OK ); 
            } 
            else 
            { 
                MessageBox( hwnd, 
                    "This device doesn't record.", 
                    "MCIWnd Record", 
                    MB_OK ); 
            } 
            break; 
        case IDM_RECORDATSTART: 
            if( MCIWndCanRecord(g_hwndMCIWnd) ) 
            { 
                MCIWndHome(g_hwndMCIWnd); 
                MCIWndRecord(g_hwndMCIWnd); 
            } 
            else 
            { 
                MessageBox( hwnd, 
                    "This device doesn't record.", 
                    "MCIWnd Record", 
                    MB_OK); 
            } 
            break; 
        case IDM_RECORDATEND: 
            if( MCIWndCanRecord(g_hwndMCIWnd) ) 
            { 
                MCIWndEnd(g_hwndMCIWnd); 
                MCIWndRecord(g_hwndMCIWnd); 
            } 
            else 
            { 
                MessageBox( hwnd, 
                    "This device doesn't record.", 
                    "MCIWnd Record", 
                    MB_OK); 
            } 
            break; 
        case IDM_SAVEMCIWND: 
            if( MCIWndCanSave(g_hwndMCIWnd) ) 
                MCIWndSaveDialog(g_hwndMCIWnd); 
    } 
    break; 
 
    // Handle other messages here. 
```



 

 




