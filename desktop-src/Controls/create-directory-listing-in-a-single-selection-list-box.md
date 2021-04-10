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
# <a name="how-to-create-a-directory-listing-in-a-single-selection-listbox"></a><span data-ttu-id="43354-103">Comment créer une liste de répertoires dans une zone de liste à sélection unique</span><span class="sxs-lookup"><span data-stu-id="43354-103">How to create a directory listing in a single-selection ListBox</span></span>

<span data-ttu-id="43354-104">Cette rubrique montre comment utiliser une zone de liste à sélection unique pour afficher et accéder au contenu d’un répertoire.</span><span class="sxs-lookup"><span data-stu-id="43354-104">This topic demonstrates how to use a single-selection list box to display and access the contents of a directory.</span></span> <span data-ttu-id="43354-105">La zone de liste à sélection unique est le type de zone de liste par défaut.</span><span class="sxs-lookup"><span data-stu-id="43354-105">The single-selection list box is the default list box type.</span></span> <span data-ttu-id="43354-106">Un utilisateur ne peut sélectionner qu’un seul élément à la fois dans une zone de liste à sélection unique.</span><span class="sxs-lookup"><span data-stu-id="43354-106">A user can only select one item at a time from a single-selection list box.</span></span>

<span data-ttu-id="43354-107">L’exemple de code C++ de cette rubrique permet à un utilisateur d’afficher une liste de fichiers dans le répertoire actif, de sélectionner un fichier dans la liste et de le supprimer.</span><span class="sxs-lookup"><span data-stu-id="43354-107">The C++ code example in this topic enables a user to view a list of files in the current directory, select a file from the list, and delete it.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="43354-108">Ce que vous devez savoir</span><span class="sxs-lookup"><span data-stu-id="43354-108">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="43354-109">Technologies</span><span class="sxs-lookup"><span data-stu-id="43354-109">Technologies</span></span>

-   [<span data-ttu-id="43354-110">Contrôles Windows</span><span class="sxs-lookup"><span data-stu-id="43354-110">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="43354-111">Prérequis</span><span class="sxs-lookup"><span data-stu-id="43354-111">Prerequisites</span></span>

-   <span data-ttu-id="43354-112">C/C++</span><span class="sxs-lookup"><span data-stu-id="43354-112">C/C++</span></span>
-   <span data-ttu-id="43354-113">Programmation de l’interface utilisateur Windows</span><span class="sxs-lookup"><span data-stu-id="43354-113">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="43354-114">Instructions</span><span class="sxs-lookup"><span data-stu-id="43354-114">Instructions</span></span>


<span data-ttu-id="43354-115">L’application de liste de répertoires doit effectuer les tâches suivantes liées à la zone de liste :</span><span class="sxs-lookup"><span data-stu-id="43354-115">The directory listing application must perform the following list box related tasks:</span></span>

-   <span data-ttu-id="43354-116">Initialisez la zone de liste.</span><span class="sxs-lookup"><span data-stu-id="43354-116">Initialize the list box.</span></span>
-   <span data-ttu-id="43354-117">Récupérez la sélection de l’utilisateur dans la zone de liste.</span><span class="sxs-lookup"><span data-stu-id="43354-117">Retrieve the user's selection from the list box.</span></span>
-   <span data-ttu-id="43354-118">Supprimer le nom de fichier de la zone de liste une fois que le fichier sélectionné a été supprimé.</span><span class="sxs-lookup"><span data-stu-id="43354-118">Remove the file name from the list box after the selected file has been deleted.</span></span>

<span data-ttu-id="43354-119">Dans l’exemple de code C++ suivant, la procédure de la boîte de dialogue initialise la zone de liste à sélection unique (IDC \_ filelist) à l’aide de la fonction [**DlgDirList**](/windows/desktop/api/Winuser/nf-winuser-dlgdirlista) pour remplir la zone de liste avec les noms de tous les fichiers dans le répertoire actif.</span><span class="sxs-lookup"><span data-stu-id="43354-119">In the following C++ code example, the dialog box procedure initializes the single-selection list box (IDC\_FILELIST) by using the [**DlgDirList**](/windows/desktop/api/Winuser/nf-winuser-dlgdirlista) function to fill the list box with the names of all the files in the current directory.</span></span> <span data-ttu-id="43354-120">Lorsque l’utilisateur sélectionne un fichier et choisit le bouton **supprimer** , la fonction [**DlgDirSelectEx**](/windows/desktop/api/Winuser/nf-winuser-dlgdirselectexa) récupère le nom du fichier sélectionné.</span><span class="sxs-lookup"><span data-stu-id="43354-120">When the user selects a file and chooses the **Delete** button, the [**DlgDirSelectEx**](/windows/desktop/api/Winuser/nf-winuser-dlgdirselectexa) function retrieves the name of the selected file.</span></span> <span data-ttu-id="43354-121">Le code supprime le fichier à l’aide de la fonction [**DeleteFile**](/windows/desktop/api/fileapi/nf-fileapi-deletefilea) et met à jour la zone de liste de répertoire en envoyant le message [**lb \_ DELETESTRING**](lb-deletestring.md) .</span><span class="sxs-lookup"><span data-stu-id="43354-121">The code deletes the file by using the [**DeleteFile**](/windows/desktop/api/fileapi/nf-fileapi-deletefilea) function and updates the directory list box by sending the [**LB\_DELETESTRING**](lb-deletestring.md) message.</span></span>



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



## <a name="related-topics"></a><span data-ttu-id="43354-122">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="43354-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="43354-123">Référence de contrôle de zone de liste</span><span class="sxs-lookup"><span data-stu-id="43354-123">List Box Control Reference</span></span>](bumper-list-box-list-box-control-reference.md)
</dt> <dt>

[<span data-ttu-id="43354-124">À propos des zones de liste</span><span class="sxs-lookup"><span data-stu-id="43354-124">About List Boxes</span></span>](about-list-boxes.md)
</dt> <dt>

[<span data-ttu-id="43354-125">Utilisation des zones de liste</span><span class="sxs-lookup"><span data-stu-id="43354-125">Using List Boxes</span></span>](using-list-boxes.md)
</dt> </dl>

 

 