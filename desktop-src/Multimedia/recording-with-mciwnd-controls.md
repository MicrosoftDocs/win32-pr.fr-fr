---
title: Enregistrement avec des contrôles MCIWnd
description: Enregistrement avec des contrôles MCIWnd
ms.assetid: 65a57400-aeea-4a27-8d51-37d3d9e9bd55
keywords:
- MCIWndCreate fonction)
- MCIWndNew macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a02dfd62985b0267c685e6893512f977340f47f95801e8821d46005d5371397
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119805559"
---
# <a name="recording-with-mciwnd-controls"></a>Enregistrement avec des contrôles MCIWnd

L’exemple suivant enregistre l’audio de forme d’onde à l’aide des contrôles intégrés de la fenêtre MCIWnd. L’exemple crée une fenêtre MCIWnd en utilisant le \_ style de fenêtre d’enregistrement MCIWNDF avec la fonction [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) pour ajouter un bouton d' **enregistrement** à la barre d’outils. La macro [**MCIWndNew**](/windows/desktop/api/Vfw/nf-vfw-mciwndnew) indique qu’un nouveau fichier est associé à la fenêtre MCIWnd et qu’un périphérique Wave-Audio fournit son contenu. Une deuxième commande de menu, IDM \_ SAVEMCIWND, permet à l’utilisateur d’enregistrer l’enregistrement et de sélectionner un nom de fichier à l’aide de la macro [**MCIWndSaveDialog**](/windows/desktop/api/Vfw/nf-vfw-mciwndsavedialog) .


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



 

 




