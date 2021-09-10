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
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124364379"
---
# <a name="customizing-the-recording-process"></a>Personnalisation du processus d’enregistrement

Vous pouvez personnaliser le processus d’enregistrement, en contrôlant entièrement le tout, de la création de la fenêtre MCIWnd à l’enregistrement des informations enregistrées dans un fichier. L’exemple suivant interroge l’appareil MCI pour les fonctionnalités d’enregistrement et d’enregistrement, et comprend des commandes de menu à enregistrer au début ou à la fin du contenu.

L’exemple suivant utilise la fonction [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) pour créer une nouvelle fenêtre et vous permet de spécifier un fichier existant pour stocker les données enregistrées et la macro [**MCIWndNew**](/windows/desktop/api/Vfw/nf-vfw-mciwndnew) pour associer un nouveau fichier à la fenêtre. Vous pouvez également utiliser la macro [**MCIWndOpen**](/windows/desktop/api/Vfw/nf-vfw-mciwndopen) ou [**MCIWndOpenDialog**](/windows/desktop/api/Vfw/nf-vfw-mciwndopendialog) pour spécifier un fichier.

L’exemple utilise la macro [**MCIWndCanRecord**](/windows/desktop/api/Vfw/nf-vfw-mciwndcanrecord) pour vérifier que l’appareil peut enregistrer et la macro [**MCIWndCanSave**](/windows/desktop/api/Vfw/nf-vfw-mciwndcansave) pour vérifier que l’appareil enregistre les informations. L’exemple définit la position de lecture actuelle à l’aide des macros [**MCIWndHome**](/windows/desktop/api/Vfw/nf-vfw-mciwndhome) et [**MCIWndEnd**](/windows/desktop/api/Vfw/nf-vfw-mciwndend) . L’exemple démarre l’enregistrement à l’aide de la macro [**MCIWndRecord**](/windows/desktop/api/Vfw/nf-vfw-mciwndrecord) . Une fois les informations enregistrées, l’exemple l’enregistre à l’aide de la macro [**MCIWndSaveDialog**](/windows/desktop/api/Vfw/nf-vfw-mciwndsavedialog) .


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



 

 




