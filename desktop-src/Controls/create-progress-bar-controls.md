---
title: Comment utiliser les contrôles de barre de progression
description: Cette rubrique explique comment utiliser une barre de progression pour indiquer la progression d’une opération longue d’analyse de fichiers.
ms.assetid: 4CC25F3A-9CAF-4ADC-B29C-3FACDD73D5A0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e65d47d6b41422853d401a1fb2686e03e3d3f5bc378b78b7ba762b86fc7ffe30
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119826419"
---
# <a name="how-to-use-progress-bar-controls"></a>Comment utiliser les contrôles de barre de progression

Cette rubrique explique comment utiliser une barre de progression pour indiquer la progression d’une opération longue d’analyse de fichiers.

## <a name="what-you-need-to-know"></a>Bon à savoir

### <a name="technologies"></a>Technologies

-   [Windows Commandes](window-controls.md)

### <a name="prerequisites"></a>Prérequis

-   C/C++
-   Windows Programmation de l’interface utilisateur

## <a name="instructions"></a>Instructions

### <a name="create-a-progress-bar-control"></a>Créer un contrôle de barre de progression

L’exemple de code suivant crée une barre de progression et la positionne le long de la partie inférieure de la zone cliente de la fenêtre parente. La hauteur de la barre de progression est basée sur la hauteur de la bitmap de direction utilisée dans une barre de défilement. La plage est basée sur la taille du fichier divisée par 2 048, qui correspond à la taille de chaque « segment » des données lues à partir du fichier. L’exemple définit également un incrément et avance la position actuelle de la barre de progression par incrément après l’analyse de chaque segment.


```C++
// ParseALargeFile - uses a progress bar to indicate the progress of a parsing operation.
//
// Returns TRUE if successful, or FALSE otherwise.
//
// hwndParent - parent window of the progress bar.
//
// lpszFileName - name of the file to parse. 
// 
// Global variable 
//     g_hinst - instance handle.
//

extern HINSTANCE g_hinst; 

BOOL ParseALargeFile(HWND hwndParent, LPTSTR lpszFileName) 
{ 
    RECT rcClient;  // Client area of parent window.
    int cyVScroll;  // Height of scroll bar arrow.
    HWND hwndPB;    // Handle of progress bar.
    HANDLE hFile;   // Handle of file.
    DWORD cb;       // Size of file and count of bytes read.
    LPCH pch;       // Address of data read from file.
    LPCH pchTmp;    // Temporary pointer.

    // Ensure that the common control DLL is loaded, and create a progress bar 
    // along the bottom of the client area of the parent window. 
    //
    // Base the height of the progress bar on the height of a scroll bar arrow.
    
    InitCommonControls(); 
    
    GetClientRect(hwndParent, &rcClient); 
    
    cyVScroll = GetSystemMetrics(SM_CYVSCROLL); 

    hwndPB = CreateWindowEx(0, PROGRESS_CLASS, (LPTSTR) NULL, 
                            WS_CHILD | WS_VISIBLE, rcClient.left, 
                            rcClient.bottom - cyVScroll, 
                            rcClient.right, cyVScroll, 
                            hwndParent, (HMENU) 0, g_hinst, NULL);

    // Open the file for reading, and retrieve the size of the file. 

    hFile = CreateFile(lpszFileName, GENERIC_READ, FILE_SHARE_READ, 
                       (LPSECURITY_ATTRIBUTES) NULL, OPEN_EXISTING, 
                       FILE_ATTRIBUTE_NORMAL, (HANDLE) NULL); 

    if (hFile == (HANDLE) INVALID_HANDLE_VALUE)
        return FALSE; 

    cb = GetFileSize(hFile, (LPDWORD) NULL); 

    // Set the range and increment of the progress bar. 

    SendMessage(hwndPB, PBM_SETRANGE, 0, MAKELPARAM(0, cb / 2048));
    
    SendMessage(hwndPB, PBM_SETSTEP, (WPARAM) 1, 0); 

    // Parse the file. 
    pch = (LPCH) LocalAlloc(LPTR, sizeof(char) * 2048); 
    
    pchTmp = pch; 
    
    do { 
        ReadFile(hFile, pchTmp, sizeof(char) * 2048, &cb, (LPOVERLAPPED) NULL);
        
        // TODO: Write an error handler to check that all the
        // requested data was read.
        //
        // Include here any code that parses the
        // file. 
        //  
        //  
        //  
        // Advance the current position of the progress bar by the increment.
        
        SendMessage(hwndPB, PBM_STEPIT, 0, 0); 
        
    } while (cb); 

    CloseHandle((HANDLE) hFile);
    
    DestroyWindow(hwndPB);

    return TRUE; 
}
```



## <a name="remarks"></a>Remarques

Vous devez veiller à utiliser la fonction [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) correctement pour garantir la sécurité de votre application. Par exemple, dans l’exemple de code, vous devez vérifier que `ReadFile` lit réellement toutes les données demandées.

Notez également que le quatrième paramètre de [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea)(( \_ attributs LPSECURITY)**null**) définit les valeurs de sécurité par défaut. Si vous avez besoin de paramètres de sécurité spécifiques, vous devez définir les valeurs appropriées dans les membres de la structure. Appelez **sizeof** pour définir la taille correcte de la structure d' **\_ attributs LPSECURITY** .

pour plus d’informations, consultez [considérations sur la sécurité : contrôles Microsoft Windows](sec-comctls.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation des contrôles de barre de progression](using-progress-bar-controls.md)
</dt> <dt>

[considérations relatives à la sécurité : contrôles Microsoft Windows](sec-comctls.md)
</dt> </dl>

 

 