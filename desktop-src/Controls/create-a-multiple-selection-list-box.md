---
title: Comment créer une zone de liste Multiple-Selection
description: Cette rubrique montre comment afficher et accéder au contenu d’un répertoire dans une zone de liste à sélection multiple.
ms.assetid: 5192E171-8CEF-4921-9378-A7C3A52A9024
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abd47b1d582d53a66bc77284927aef4230043e92
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126999382"
---
# <a name="how-to-create-a-multiple-selection-list-box"></a>Comment créer une zone de liste Multiple-Selection

Cette rubrique montre comment afficher et accéder au contenu d’un répertoire dans une zone de liste à sélection multiple. Dans une zone de liste à sélection multiple, l’utilisateur peut sélectionner plusieurs éléments à la fois.

L’exemple de code C++ de cette rubrique permet à un utilisateur d’afficher une liste de fichiers dans le répertoire actif, de sélectionner un groupe de fichiers dans la liste et de les supprimer.

## <a name="what-you-need-to-know"></a>Bon à savoir

### <a name="technologies"></a>Technologies

-   [Windows Commandes](window-controls.md)

### <a name="prerequisites"></a>Prérequis

-   C/C++
-   Windows Programmation de l’interface utilisateur

## <a name="instructions"></a>Instructions


L’application de liste de répertoires doit effectuer les tâches associées à la zone de liste suivante :

-   Initialisez la zone de liste.
-   Récupérez les sélections de l’utilisateur dans la zone de liste.
-   Supprimer les noms de fichiers de la zone de liste une fois que les fichiers sélectionnés ont été supprimés.

Dans l’exemple de code C++ suivant, la procédure de la boîte de dialogue initialise la zone de liste à sélection multiple (IDC \_ filelist) à l’aide de la fonction [**DlgDirList**](/windows/desktop/api/Winuser/nf-winuser-dlgdirlista) pour remplir la zone de liste avec les noms de tous les fichiers dans le répertoire actif.

Lorsque l’utilisateur sélectionne un groupe de fichiers et choisit le bouton **supprimer** , la procédure de boîte de dialogue envoie le message [**\_ GETSELCOUNT**](lb-getselcount.md) , pour récupérer le nombre de fichiers sélectionnés et le [**message \_ GETSELITEMS**](lb-getselitems.md) , pour récupérer un tableau d’éléments de zone de liste sélectionnés. Après la suppression d’un fichier, la procédure de boîte de dialogue supprime l’élément correspondant de la zone de liste en envoyant le message [**lb \_ DELETESTRING**](lb-deletestring.md) .



```C++
#define BIGBUFF 8192 
 
INT_PTR CALLBACK DlgDelFilesProc(HWND hDlg, UINT message, 
        UINT wParam, LONG lParam) 
{ 
    PTSTR pszCurDir; 
    PTSTR pszFileToDelete; 
    int cSelItems; 
    int cSelItemsInBuffer; 
    TCHAR achBuffer[MAX_PATH]; 
    int aSelItems[BIGBUFF]; 
    int i; 
    BOOL fResult; 
    HWND hListBox;
    int iRet;
 
    switch (message) { 
 
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
                    // first retrieve the list of selected files. 
                    pszFileToDelete = achBuffer; 
                    hListBox = GetDlgItem(hDlg, IDC_FILELIST); 
                    cSelItems = SendMessage(hListBox, 
                            LB_GETSELCOUNT, 0, 0); 
 
                    cSelItemsInBuffer = SendMessage(hListBox, 
                            LB_GETSELITEMS, 512, (LPARAM) aSelItems); 
 
                    if (cSelItems > cSelItemsInBuffer) 
                    { 
                        MessageBox(hDlg, L"Too many items selected.", 
                                NULL, MB_OK); 
                    } 
                    else 
                    { 

                        // Make sure the user really wants to delete the files.
                        iRet = MessageBox(hDlg, 
                            L"Are you sure you want to delete these files?", 
                            L"Deleting Files", MB_YESNO | MB_ICONEXCLAMATION);
                        if (iRet == IDNO)
                            return TRUE;

                        // Go through the list backward because after deleting
                        // an item the indices change for every subsequent 
                        // item. By going backward, the indices are never 
                        // invalidated. 
                        for (i = cSelItemsInBuffer - 1; i >= 0; i--) 
                        { 
                            SendMessage(hListBox, LB_GETTEXT, 
                                        aSelItems[i], 
                                        (LPARAM) pszFileToDelete); 
 
                            fResult = DeleteFile(pszFileToDelete); 
                            if (!fResult) 
                            {                     
                                MessageBox(hDlg, L"Could not delete file.", 
                                    NULL, MB_OK);     
                            } 
                            else 
                            { 
                                SendMessage(hListBox, LB_DELETESTRING, 
                                        aSelItems[i], 0); 
                            } 
                        } 
                        SendMessage(hListBox, LB_SETCARETINDEX, 0, 0); 
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

 

 




