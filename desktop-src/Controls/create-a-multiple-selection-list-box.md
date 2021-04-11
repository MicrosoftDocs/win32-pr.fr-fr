---
title: Comment créer une zone de liste Multiple-Selection
description: Cette rubrique montre comment afficher et accéder au contenu d’un répertoire dans une zone de liste à sélection multiple.
ms.assetid: 5192E171-8CEF-4921-9378-A7C3A52A9024
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abd47b1d582d53a66bc77284927aef4230043e92
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/04/2020
ms.locfileid: "104032107"
---
# <a name="how-to-create-a-multiple-selection-list-box"></a><span data-ttu-id="3b820-103">Comment créer une zone de liste Multiple-Selection</span><span class="sxs-lookup"><span data-stu-id="3b820-103">How to Create a Multiple-Selection List Box</span></span>

<span data-ttu-id="3b820-104">Cette rubrique montre comment afficher et accéder au contenu d’un répertoire dans une zone de liste à sélection multiple.</span><span class="sxs-lookup"><span data-stu-id="3b820-104">This topic demonstrates how to display and access the contents of a directory in a multiple-selection list box.</span></span> <span data-ttu-id="3b820-105">Dans une zone de liste à sélection multiple, l’utilisateur peut sélectionner plusieurs éléments à la fois.</span><span class="sxs-lookup"><span data-stu-id="3b820-105">In a multiple-selection list box, the user can select more than one item at a time.</span></span>

<span data-ttu-id="3b820-106">L’exemple de code C++ de cette rubrique permet à un utilisateur d’afficher une liste de fichiers dans le répertoire actif, de sélectionner un groupe de fichiers dans la liste et de les supprimer.</span><span class="sxs-lookup"><span data-stu-id="3b820-106">The C++ code example in this topic enables a user to view a list of files in the current directory, select a group of files from the list, and delete them.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="3b820-107">Ce que vous devez savoir</span><span class="sxs-lookup"><span data-stu-id="3b820-107">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="3b820-108">Technologies</span><span class="sxs-lookup"><span data-stu-id="3b820-108">Technologies</span></span>

-   [<span data-ttu-id="3b820-109">Contrôles Windows</span><span class="sxs-lookup"><span data-stu-id="3b820-109">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="3b820-110">Prérequis</span><span class="sxs-lookup"><span data-stu-id="3b820-110">Prerequisites</span></span>

-   <span data-ttu-id="3b820-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="3b820-111">C/C++</span></span>
-   <span data-ttu-id="3b820-112">Programmation de l’interface utilisateur Windows</span><span class="sxs-lookup"><span data-stu-id="3b820-112">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="3b820-113">Instructions</span><span class="sxs-lookup"><span data-stu-id="3b820-113">Instructions</span></span>


<span data-ttu-id="3b820-114">L’application de liste de répertoires doit effectuer les tâches associées à la zone de liste suivante :</span><span class="sxs-lookup"><span data-stu-id="3b820-114">The directory listing application must perform the following list box–related tasks:</span></span>

-   <span data-ttu-id="3b820-115">Initialisez la zone de liste.</span><span class="sxs-lookup"><span data-stu-id="3b820-115">Initialize the list box.</span></span>
-   <span data-ttu-id="3b820-116">Récupérez les sélections de l’utilisateur dans la zone de liste.</span><span class="sxs-lookup"><span data-stu-id="3b820-116">Retrieve the user's selections from the list box.</span></span>
-   <span data-ttu-id="3b820-117">Supprimer les noms de fichiers de la zone de liste une fois que les fichiers sélectionnés ont été supprimés.</span><span class="sxs-lookup"><span data-stu-id="3b820-117">Remove the file names from the list box after the selected files have been deleted.</span></span>

<span data-ttu-id="3b820-118">Dans l’exemple de code C++ suivant, la procédure de la boîte de dialogue initialise la zone de liste à sélection multiple (IDC \_ filelist) à l’aide de la fonction [**DlgDirList**](/windows/desktop/api/Winuser/nf-winuser-dlgdirlista) pour remplir la zone de liste avec les noms de tous les fichiers dans le répertoire actif.</span><span class="sxs-lookup"><span data-stu-id="3b820-118">In the following C++ code example, the dialog box procedure initializes the multiple-selection list box (IDC\_FILELIST) by using the [**DlgDirList**](/windows/desktop/api/Winuser/nf-winuser-dlgdirlista) function to fill the list box with the names of all the files in the current directory.</span></span>

<span data-ttu-id="3b820-119">Lorsque l’utilisateur sélectionne un groupe de fichiers et choisit le bouton **supprimer** , la procédure de boîte de dialogue envoie le message [**\_ GETSELCOUNT**](lb-getselcount.md) , pour récupérer le nombre de fichiers sélectionnés et le [**message \_ GETSELITEMS**](lb-getselitems.md) , pour récupérer un tableau d’éléments de zone de liste sélectionnés.</span><span class="sxs-lookup"><span data-stu-id="3b820-119">When the user selects a group of files and chooses the **Delete** button, the dialog box procedure sends the [**LB\_GETSELCOUNT**](lb-getselcount.md) message, to retrieve the number of files selected, and the [**LB\_GETSELITEMS**](lb-getselitems.md) message, to retrieve an array of selected list box items.</span></span> <span data-ttu-id="3b820-120">Après la suppression d’un fichier, la procédure de boîte de dialogue supprime l’élément correspondant de la zone de liste en envoyant le message [**lb \_ DELETESTRING**](lb-deletestring.md) .</span><span class="sxs-lookup"><span data-stu-id="3b820-120">After deleting a file, the dialog procedure removes the corresponding item from the list box by sending the [**LB\_DELETESTRING**](lb-deletestring.md) message.</span></span>



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



## <a name="related-topics"></a><span data-ttu-id="3b820-121">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3b820-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3b820-122">Référence de contrôle de zone de liste</span><span class="sxs-lookup"><span data-stu-id="3b820-122">List Box Control Reference</span></span>](bumper-list-box-list-box-control-reference.md)
</dt> <dt>

[<span data-ttu-id="3b820-123">À propos des zones de liste</span><span class="sxs-lookup"><span data-stu-id="3b820-123">About List Boxes</span></span>](about-list-boxes.md)
</dt> <dt>

[<span data-ttu-id="3b820-124">Utilisation des zones de liste</span><span class="sxs-lookup"><span data-stu-id="3b820-124">Using List Boxes</span></span>](using-list-boxes.md)
</dt> </dl>

 

 




