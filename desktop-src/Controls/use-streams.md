---
title: Utilisation des flux
description: Vous pouvez utiliser des flux pour transférer des données vers ou à partir d’un contrôle RichEdit. Un flux est défini par une structure EDITSTREAM, qui spécifie une mémoire tampon et une fonction de rappel définie par l’application.
ms.assetid: A7ED47F1-968C-4E41-B1E2-4449072D2FC4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b89a9cc2a8caa157f9c65220fc5cead7564bc555
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/17/2020
ms.locfileid: "104101384"
---
# <a name="how-to-use-streams"></a>Utilisation des flux

Vous pouvez utiliser des flux pour transférer des données vers ou à partir d’un contrôle RichEdit. Un flux est défini par une structure [**EDITSTREAM**](/windows/desktop/api/Richedit/ns-richedit-editstream) , qui spécifie une mémoire tampon et une fonction de rappel définie par l’application.

Pour lire des données dans un contrôle Rich Edit (autrement dit, un flux de données), utilisez le message de [**\_ flux em**](em-streamin.md) . Le contrôle appelle à plusieurs reprises la fonction de rappel de l’application, qui transfère à chaque fois une partie des données dans la mémoire tampon.

Pour enregistrer le contenu d’un contrôle RichEdit (autrement dit, diffuser en continu les données), vous pouvez utiliser le message [**em \_ STREAMOUT**](em-streamout.md) . Le contrôle écrit à plusieurs reprises dans la mémoire tampon, puis appelle la fonction de rappel de l’application. Pour chaque appel, la fonction de rappel enregistre le contenu de la mémoire tampon.

## <a name="what-you-need-to-know"></a>Ce que vous devez savoir

### <a name="technologies"></a>Technologies

-   [Contrôles Windows](window-controls.md)

### <a name="prerequisites"></a>Prérequis

-   C/C++
-   Programmation de l’interface utilisateur Windows

## <a name="instructions"></a>Instructions

### <a name="use-a-stream"></a>Utiliser un flux

L’exemple de code suivant montre comment lire un fichier. rtf dans un contrôle RichEdit. Le descripteur de fichier est passé à la fonction de rappel via le membre **dwCookie** de la structure [**EDITSTREAM**](/windows/desktop/api/Richedit/ns-richedit-editstream) .


```C++
DWORD CALLBACK EditStreamCallback(DWORD_PTR dwCookie, 
                                  LPBYTE lpBuff,
                                  LONG cb, 
                                  PLONG pcb)
{
    HANDLE hFile = (HANDLE)dwCookie;
    
    if (ReadFile(hFile, lpBuff, cb, (DWORD *)pcb, NULL)) 
    {
        return 0;
    }
    
    return -1;
}

BOOL FillRichEditFromFile(HWND hwnd, LPCTSTR pszFile)
{
    BOOL fSuccess = FALSE;
    
    HANDLE hFile = CreateFile(pszFile, GENERIC_READ, 
                              FILE_SHARE_READ, 0, OPEN_EXISTING,
                              FILE_FLAG_SEQUENTIAL_SCAN, NULL);
        
    if (hFile != INVALID_HANDLE_VALUE) 
    {
        EDITSTREAM es = { 0 };
        
        es.pfnCallback = EditStreamCallback;
        es.dwCookie    = (DWORD_PTR)hFile;
        
        if (SendMessage(hwnd, EM_STREAMIN, SF_RTF, (LPARAM)&es) && es.dwError == 0) 
        {
                fSuccess = TRUE;
        }
        
        CloseHandle(hFile);
    }
    
    return fSuccess;
    
}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation de contrôles RichEdit](using-rich-edit-controls.md)
</dt> <dt>

[Démonstration des contrôles communs Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 




