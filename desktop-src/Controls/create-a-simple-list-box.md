---
title: Comment créer une zone de liste simple
description: Cette rubrique montre comment initialiser et récupérer des éléments à partir d’une zone de liste simple.
ms.assetid: 4A717010-A1D3-4FFB-8E4E-D5C4F9D8D952
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ca2230b265d61e9a59a8892e14127d25bf2cfd2
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/04/2020
ms.locfileid: "104032101"
---
# <a name="how-to-create-a-simple-list-box"></a><span data-ttu-id="af2c6-103">Comment créer une zone de liste simple</span><span class="sxs-lookup"><span data-stu-id="af2c6-103">How to Create a Simple List Box</span></span>

<span data-ttu-id="af2c6-104">Cette rubrique montre comment initialiser et récupérer des éléments à partir d’une zone de liste simple.</span><span class="sxs-lookup"><span data-stu-id="af2c6-104">This topic demonstrates how to initialize and retrieve items from a simple list box.</span></span>

<span data-ttu-id="af2c6-105">L’exemple de code C++ fourni dans cette rubrique contient une procédure de boîte de dialogue qui remplit une zone de liste avec des informations sur les joueurs d’une équipe sportive.</span><span class="sxs-lookup"><span data-stu-id="af2c6-105">The C++ code example in this topic includes a dialog box procedure that fills a list box with information about players on a sports team.</span></span> <span data-ttu-id="af2c6-106">Lorsque l’utilisateur sélectionne le nom d’un joueur dans la liste, les informations relatives au lecteur s’affichent dans la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="af2c6-106">When the user selects the name of a player from the list, information about the player is displayed in the dialog box.</span></span> <span data-ttu-id="af2c6-107">Le style de fenêtre pour la zone de liste comprend [**lbs \_ sort**](list-box-styles.md), ce qui donne une liste triée d’éléments.</span><span class="sxs-lookup"><span data-stu-id="af2c6-107">The window style for the list box includes [**LBS\_SORT**](list-box-styles.md), which results in a sorted list of items.</span></span> <span data-ttu-id="af2c6-108">La capture d’écran suivante montre la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="af2c6-108">The following screen shot shows the dialog box.</span></span>

![capture d’écran d’une boîte de dialogue contenant une zone de liste étiquetée, texte à propos de l’élément de zone de liste sélectionné et bouton OK](images/lb-roster.png)

## <a name="what-you-need-to-know"></a><span data-ttu-id="af2c6-110">Ce que vous devez savoir</span><span class="sxs-lookup"><span data-stu-id="af2c6-110">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="af2c6-111">Technologies</span><span class="sxs-lookup"><span data-stu-id="af2c6-111">Technologies</span></span>

-   [<span data-ttu-id="af2c6-112">Contrôles Windows</span><span class="sxs-lookup"><span data-stu-id="af2c6-112">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="af2c6-113">Prérequis</span><span class="sxs-lookup"><span data-stu-id="af2c6-113">Prerequisites</span></span>

-   <span data-ttu-id="af2c6-114">C/C++</span><span class="sxs-lookup"><span data-stu-id="af2c6-114">C/C++</span></span>
-   <span data-ttu-id="af2c6-115">Programmation de l’interface utilisateur Windows</span><span class="sxs-lookup"><span data-stu-id="af2c6-115">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="af2c6-116">Instructions</span><span class="sxs-lookup"><span data-stu-id="af2c6-116">Instructions</span></span>


<span data-ttu-id="af2c6-117">L’application doit effectuer les tâches associées à la zone de liste suivante :</span><span class="sxs-lookup"><span data-stu-id="af2c6-117">The application must perform the following list box–related tasks:</span></span>

-   <span data-ttu-id="af2c6-118">Initialiser la zone de liste</span><span class="sxs-lookup"><span data-stu-id="af2c6-118">Initialize the list box</span></span>
-   <span data-ttu-id="af2c6-119">Récupérer la sélection de l’utilisateur dans la zone de liste</span><span class="sxs-lookup"><span data-stu-id="af2c6-119">Retrieve the user's selection from the list box</span></span>

<span data-ttu-id="af2c6-120">Dans l’exemple de code C++ suivant, les informations sur les lecteurs sont stockées dans un tableau de structures.</span><span class="sxs-lookup"><span data-stu-id="af2c6-120">In the following C++ code example, information about players is stored in an array of structures.</span></span> <span data-ttu-id="af2c6-121">Pendant l’initialisation, la procédure de la boîte de dialogue utilise le message [**lb \_ ADDSTRING**](lb-addstring.md) pour ajouter un par un les noms des membres de l’équipe à la zone de liste (**\_ \_ exemple de ListBox IDC**).</span><span class="sxs-lookup"><span data-stu-id="af2c6-121">During initialization, the dialog box procedure uses the [**LB\_ADDSTRING**](lb-addstring.md) message to add the names of team members to the list box (**IDC\_LISTBOX\_EXAMPLE**) one at a time.</span></span> <span data-ttu-id="af2c6-122">Il utilise également le message [**lb \_ SETITEMDATA**](lb-setitemdata.md) pour ajouter l’index de tableau du lecteur à la zone de liste en tant que données d’élément.</span><span class="sxs-lookup"><span data-stu-id="af2c6-122">It also uses the [**LB\_SETITEMDATA**](lb-setitemdata.md) message to add the array index of the player to the list box as item data.</span></span> <span data-ttu-id="af2c6-123">Plus tard, lorsque l’utilisateur sélectionne un lecteur dans la zone de liste, la procédure de la boîte de dialogue utilise le message [**\_ GETITEMDATA**](lb-getitemdata.md) pour récupérer l’index de tableau correspondant.</span><span class="sxs-lookup"><span data-stu-id="af2c6-123">Later, when the user selects a player from the list box, the dialog box procedure uses the [**LB\_GETITEMDATA**](lb-getitemdata.md) message to retrieve the corresponding array index.</span></span> <span data-ttu-id="af2c6-124">Il utilise ensuite l’index de tableau pour récupérer les informations du joueur à partir du tableau.</span><span class="sxs-lookup"><span data-stu-id="af2c6-124">It then uses the array index to retrieve player information from the array.</span></span>



```C++
typedef struct 
{ 
    TCHAR achName[MAX_PATH]; 
    TCHAR achPosition[12]; 
    int nGamesPlayed; 
    int nGoalsScored; 
} Player; 

Player Roster[] = 
{ 
    {TEXT("Haas, Jonathan"), TEXT("Midfield"), 18, 4 }, 
    {TEXT("Pai, Jyothi"), TEXT("Forward"), 36, 12 }, 
    {TEXT("Hanif, Kerim"), TEXT("Back"), 26, 0 }, 
    {TEXT("Anderberg, Michael"), TEXT("Back"), 24, 2 }, 
    {TEXT("Jelitto, Jacek"), TEXT("Midfield"), 26, 3 }, 
    {TEXT("Raposo, Rui"), TEXT("Back"), 24, 3}, 
    {TEXT("Joseph, Brad"), TEXT("Forward"), 13, 3 }, 
    {TEXT("Bouchard, Thomas"), TEXT("Forward"), 28, 5 }, 
    {TEXT("Salmre, Ivo "), TEXT("Midfield"), 27, 7 }, 
    {TEXT("Camp, David"), TEXT("Midfield"), 22, 3 }, 
    {TEXT("Kohl, Franz"), TEXT("Goalkeeper"), 17, 0 }, 
}; 


INT_PTR CALLBACK ListBoxExampleProc(HWND hDlg, UINT message, 
        WPARAM wParam, LPARAM lParam)
{
    switch (message)
    {
    case WM_INITDIALOG:
        {
            // Add items to list. 
            HWND hwndList = GetDlgItem(hDlg, IDC_LISTBOX_EXAMPLE);  
            for (int i = 0; i < ARRAYSIZE(Roster); i++) 
            { 
                int pos = (int)SendMessage(hwndList, LB_ADDSTRING, 0, 
                    (LPARAM) Roster[i].achName); 
                // Set the array index of the player as item data.
                // This enables us to retrieve the item from the array
                // even after the items are sorted by the list box.
                SendMessage(hwndList, LB_SETITEMDATA, pos, (LPARAM) i); 
            } 
            // Set input focus to the list box.
            SetFocus(hwndList); 
            return TRUE;               
        } 

    case WM_COMMAND:
        switch (LOWORD(wParam))
        {
        case IDOK:
        case IDCANCEL:
            EndDialog(hDlg, LOWORD(wParam));
            return TRUE;

        case IDC_LISTBOX_EXAMPLE:
            {
                switch (HIWORD(wParam)) 
                { 
                case LBN_SELCHANGE:
                    {
                        HWND hwndList = GetDlgItem(hDlg, IDC_LISTBOX_EXAMPLE); 

                        // Get selected index.
                        int lbItem = (int)SendMessage(hwndList, LB_GETCURSEL, 0, 0); 

                        // Get item data.
                        int i = (int)SendMessage(hwndList, LB_GETITEMDATA, lbItem, 0);

                        // Do something with the data from Roster[i]
                        TCHAR buff[MAX_PATH];
                        StringCbPrintf (buff, ARRAYSIZE(buff),  
                            TEXT("Position: %s\nGames played: %d\nGoals: %d"), 
                            Roster[i].achPosition, Roster[i].nGamesPlayed, 
                            Roster[i].nGoalsScored);

                        SetDlgItemText(hDlg, IDC_STATISTICS, buff); 
                        return TRUE; 
                    } 
                }
            }
            return TRUE;
        }
    }
    return FALSE;
}
```



## <a name="related-topics"></a><span data-ttu-id="af2c6-125">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="af2c6-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="af2c6-126">Référence de contrôle de zone de liste</span><span class="sxs-lookup"><span data-stu-id="af2c6-126">List Box Control Reference</span></span>](bumper-list-box-list-box-control-reference.md)
</dt> <dt>

[<span data-ttu-id="af2c6-127">À propos des zones de liste</span><span class="sxs-lookup"><span data-stu-id="af2c6-127">About List Boxes</span></span>](about-list-boxes.md)
</dt> <dt>

[<span data-ttu-id="af2c6-128">Utilisation des zones de liste</span><span class="sxs-lookup"><span data-stu-id="af2c6-128">Using List Boxes</span></span>](using-list-boxes.md)
</dt> </dl>

 

 




