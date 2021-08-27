---
title: Comment créer une zone de liste simple
description: Cette rubrique montre comment initialiser et récupérer des éléments à partir d’une zone de liste simple.
ms.assetid: 4A717010-A1D3-4FFB-8E4E-D5C4F9D8D952
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83a037bfbdb5232cd30d3e13fbc251c22c18c71a76398a351939602301a745d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120063172"
---
# <a name="how-to-create-a-simple-list-box"></a>Comment créer une zone de liste simple

Cette rubrique montre comment initialiser et récupérer des éléments à partir d’une zone de liste simple.

L’exemple de code C++ fourni dans cette rubrique contient une procédure de boîte de dialogue qui remplit une zone de liste avec des informations sur les joueurs d’une équipe sportive. Lorsque l’utilisateur sélectionne le nom d’un joueur dans la liste, les informations relatives au lecteur s’affichent dans la boîte de dialogue. Le style de fenêtre pour la zone de liste comprend [**lbs \_ sort**](list-box-styles.md), ce qui donne une liste triée d’éléments. La capture d’écran suivante montre la boîte de dialogue.

![capture d’écran d’une boîte de dialogue contenant une zone de liste étiquetée, texte à propos de l’élément de zone de liste sélectionné et bouton OK](images/lb-roster.png)

## <a name="what-you-need-to-know"></a>Bon à savoir

### <a name="technologies"></a>Technologies

-   [Windows Commandes](window-controls.md)

### <a name="prerequisites"></a>Prérequis

-   C/C++
-   Windows Programmation de l’interface utilisateur

## <a name="instructions"></a>Instructions


L’application doit effectuer les tâches associées à la zone de liste suivante :

-   Initialiser la zone de liste
-   Récupérer la sélection de l’utilisateur dans la zone de liste

Dans l’exemple de code C++ suivant, les informations sur les lecteurs sont stockées dans un tableau de structures. Pendant l’initialisation, la procédure de la boîte de dialogue utilise le message [**lb \_ ADDSTRING**](lb-addstring.md) pour ajouter un par un les noms des membres de l’équipe à la zone de liste (**\_ \_ exemple de ListBox IDC**). Il utilise également le message [**lb \_ SETITEMDATA**](lb-setitemdata.md) pour ajouter l’index de tableau du lecteur à la zone de liste en tant que données d’élément. Plus tard, lorsque l’utilisateur sélectionne un lecteur dans la zone de liste, la procédure de la boîte de dialogue utilise le message [**\_ GETITEMDATA**](lb-getitemdata.md) pour récupérer l’index de tableau correspondant. Il utilise ensuite l’index de tableau pour récupérer les informations du joueur à partir du tableau.



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



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence de contrôle de zone de liste](bumper-list-box-list-box-control-reference.md)
</dt> <dt>

[À propos des zones de liste](about-list-boxes.md)
</dt> <dt>

[Utilisation des zones de liste](using-list-boxes.md)
</dt> </dl>

 

 




