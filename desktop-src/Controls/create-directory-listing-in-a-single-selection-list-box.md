---
title: Créer une liste de répertoires dans une zone de liste
description: Cette rubrique montre comment utiliser une zone de liste à sélection unique pour afficher et accéder au contenu d’un répertoire.
ms.assetid: 11C0DB10-59BA-47C4-8687-101A2A85D660
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03829990605271574a2030486ac5aba428867ec3
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/04/2020
ms.locfileid: "103941474"
---
# <a name="how-to-create-a-directory-listing-in-a-single-selection-listbox"></a>Comment créer une liste de répertoires dans une zone de liste à sélection unique

Cette rubrique montre comment utiliser une zone de liste à sélection unique pour afficher et accéder au contenu d’un répertoire. La zone de liste à sélection unique est le type de zone de liste par défaut. Un utilisateur ne peut sélectionner qu’un seul élément à la fois dans une zone de liste à sélection unique.

L’exemple de code C++ de cette rubrique permet à un utilisateur d’afficher une liste de fichiers dans le répertoire actif, de sélectionner un fichier dans la liste et de le supprimer.

## <a name="what-you-need-to-know"></a>Ce que vous devez savoir

### <a name="technologies"></a>Technologies

-   [Contrôles Windows](window-controls.md)

### <a name="prerequisites"></a>Prérequis

-   C/C++
-   Programmation de l’interface utilisateur Windows

## <a name="instructions"></a>Instructions


L’application de liste de répertoires doit effectuer les tâches suivantes liées à la zone de liste :

-   Initialisez la zone de liste.
-   Récupérez la sélection de l’utilisateur dans la zone de liste.
-   Supprimer le nom de fichier de la zone de liste une fois que le fichier sélectionné a été supprimé.

Dans l’exemple de code C++ suivant, la procédure de la boîte de dialogue initialise la zone de liste à sélection unique (IDC \_ filelist) à l’aide de la fonction [**DlgDirList**](/windows/desktop/api/Winuser/nf-winuser-dlgdirlista) pour remplir la zone de liste avec les noms de tous les fichiers dans le répertoire actif. Lorsque l’utilisateur sélectionne un fichier et choisit le bouton **supprimer** , la fonction [**DlgDirSelectEx**](/windows/desktop/api/Winuser/nf-winuser-dlgdirselectexa) récupère le nom du fichier sélectionné. Le code supprime le fichier à l’aide de la fonction [**DeleteFile**](/windows/desktop/api/fileapi/nf-fileapi-deletefilea) et met à jour la zone de liste de répertoire en envoyant le message [**lb \_ DELETESTRING**](lb-deletestring.md) .



```C++
INT_PTR CALLBACK DlgDelFileProc(HWND hDlg, UINT message, 
        UINT wParam, LONG lParam) 
{ 
    PTSTR pszCurDir; 
    PTSTR pszFileToDelete; 
    int iLBItem; 
    int cStringsRemaining; 
    int iRet; 
    TCHAR achBuffer[MAX_PATH]; 
    TCHAR achTemp[MAX_PATH]; 
    BOOL fResult;     
 
    switch (message) 
    { 
        case WM_INITDIALOG: 
 
           // Initialize the list box by filling it with files from 
           // the current directory. 
           pszCurDir = achBuffer; 
           GetCurrentDirectory(MAX_PATH, pszCurDir); 
           DlgDirList(hDlg, pszCurDir, IDC_FILELIST, IDS_PATHTOFILL, 0); 
           SetFocus(GetDlgItem(hDlg, IDC_FILELIST)); 
           return FALSE; 
 
        case WM_COMMAND: 
 
            switch (LOWORD(wParam)) 
            { 
                case IDOK: 
 
                    // When the user presses the DEL (IDOK) button, 
                    // first retrieve the selected file. 
                    pszFileToDelete = achBuffer; 
                    DlgDirSelectEx(hDlg, pszFileToDelete, MAX_PATH, 
                        IDC_FILELIST); 

                    // Make sure the user really wants to delete the file.
                    achTemp[MAX_PATH];
                    StringCbPrintf (achTemp, ARRAYSIZE(achTemp),  
                            TEXT("Are you sure you want to delete %s?"), 
                            pszFileToDelete);
                    iRet = MessageBox(hDlg, achTemp, L"Deleting Files", 
                        MB_YESNO | MB_ICONEXCLAMATION);
                    if (iRet == IDNO)
                        return TRUE;;

                    // Delete the file.
                    fResult = DeleteFile(pszFileToDelete); 
                    if (!fResult) 
                    { 
                        MessageBox(hDlg, L"Could not delete file.", 
                            NULL, MB_OK); 
                    } 
                    else // Remove the filename from the list box.
                    { 
                        // Get the selected item.
                        iLBItem = SendMessage(GetDlgItem(hDlg, IDC_FILELIST), 
                            LB_GETCURSEL, 0, 0); 
 
                        // Delete the selected item.
                        cStringsRemaining = SendMessage(GetDlgItem(hDlg, IDC_FILELIST), 
                            LB_DELETESTRING, iLBItem, 0); 
 
                        // If this is not the last item, set the selection to 
                        // the item immediately following the one just deleted.
                        // Otherwise, set the selection to the last item.
                         if (cStringsRemaining > iLBItem) 
                        { 
                            SendMessage(GetDlgItem(hDlg, IDC_FILELIST), 
                                LB_SETCURSEL, iLBItem, 0); 
                        } 
                        else 
                        { 
                            SendMessage(GetDlgItem(hDlg, IDC_FILELIST), 
                                LB_SETCURSEL, cStringsRemaining, 0); 
                        } 
                    } 
                    return TRUE; 
 
                case IDCANCEL: 
 
                    // Destroy the dialog box. 
                     EndDialog(hDlg, TRUE); 
                    return TRUE; 
 
                default: 
                    return FALSE; 
            } 
 
        default: 
            return FALSE; 
    } 
} 
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence de contrôle de zone de liste](bumper-list-box-list-box-control-reference.md)
</dt> <dt>

[À propos des zones de liste](about-list-boxes.md)
</dt> <dt>

[Utilisation des zones de liste](using-list-boxes.md)
</dt> </dl>

 

 