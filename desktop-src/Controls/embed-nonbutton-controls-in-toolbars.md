---
title: Comment incorporer des contrôles autres que des boutons dans les barres d’outils
description: Les barres d’outils prennent uniquement en charge les boutons ; par conséquent, si votre application nécessite un type de contrôle différent, vous devez créer une fenêtre enfant. L’illustration suivante montre une barre d’outils avec un contrôle d’édition incorporé.
ms.assetid: 7B4DACEF-96BB-447E-AE8F-F55401C665E9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb8ae2189350b9ea2f4aaa0c3ea0b49727bd3415
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/17/2020
ms.locfileid: "103841989"
---
# <a name="how-to-embed-nonbutton-controls-in-toolbars"></a>Comment incorporer des contrôles autres que des boutons dans les barres d’outils

Les barres d’outils prennent uniquement en charge les boutons ; par conséquent, si votre application nécessite un type de contrôle différent, vous devez créer une fenêtre enfant. L’illustration suivante montre une barre d’outils avec un contrôle d’édition incorporé.

![capture d’écran d’une boîte de dialogue avec un contrôle d’édition dans la barre d’outils, précédant trois icônes de barre d’outils](images/tb-withedit.png)

> [!Note]  
> Envisagez d’utiliser les [contrôles Rebar](rebar-controls.md) au lieu de placer des contrôles dans les barres d’outils.

 

N’importe quel type de fenêtre peut être placé dans une barre d’outils. L’exemple de code suivant ajoute un contrôle d’édition en tant qu’enfant de la fenêtre de contrôle de barre d’outils. Étant donné que la barre d’outils est créée, puis que le contrôle d’édition est ajouté, vous devez fournir de l’espace pour le contrôle d’édition. Pour ce faire, vous pouvez ajouter un séparateur en tant qu’espace réservé dans la barre d’outils, en définissant la largeur du séparateur sur le nombre de pixels que vous souhaitez réserver.

## <a name="what-you-need-to-know"></a>Ce que vous devez savoir

### <a name="technologies"></a>Technologies

-   [Contrôles Windows](window-controls.md)

### <a name="prerequisites"></a>Prérequis

-   C/C++
-   Programmation de l’interface utilisateur Windows

## <a name="instructions"></a>Instructions

### <a name="embed-a-nonbutton-control-in-a-toolbar"></a>Incorporer un contrôle unbutton dans une barre d’outils

L’extrait de code suivant crée la barre d’outils dans l’illustration précédente.


```C++
// IDM_NEW, IDM_OPEN, and IDM_SAVE are application-defined command constants.

HIMAGELIST g_hImageList = NULL;

HWND CreateToolbarWithEdit(HWND hWndParent)
{
    const int ImageListID = 0;    // Define some constants.
    const int bitmapSize  = 16;
    
    const int cx_edit = 100;      // Dimensions of edit control.
    const int cy_edit = 35;  

    TBBUTTON tbButtons[] =        // Toolbar buttons.
    {
        // The separator is set to the width of the edit control. 
        
        {cx_edit, 0, TBSTATE_ENABLED, BTNS_SEP, {0}, 0, -1},
        {STD_FILENEW, IDM_NEW, TBSTATE_ENABLED, BTNS_BUTTON, {0}, 0, 0},
        {STD_FILEOPEN, IDM_OPEN, TBSTATE_ENABLED, BTNS_BUTTON, {0}, 0, 0},
        {STD_FILESAVE, IDM_SAVE, TBSTATE_ENABLED, BTNS_BUTTON, {0}, 0, 0},
        {0, 0, TBSTATE_ENABLED, BTNS_SEP, {0}, 0, 0},
    };

    // Create the toolbar.
    HWND hWndToolbar = CreateWindowEx(0, TOOLBARCLASSNAME, L"Toolbar", 
                                      WS_CHILD | WS_VISIBLE | WS_BORDER, 
                                      0, 0, 0, 0,
                                      hWndParent, NULL, HINST_COMMCTRL, NULL);

    if (!hWndToolbar)
        return NULL;
    
    int numButtons = sizeof(tbButtons) / sizeof(TBBUTTON);

    // Create the image list.
    g_hImageList = ImageList_Create(bitmapSize, bitmapSize, // Dimensions of individual bitmaps.
                                    0,                      // Flags.
                                    numButtons, 0);

    // Set the image list.
    SendMessage(hWndToolbar, TB_SETIMAGELIST, (WPARAM)ImageListID, (LPARAM)g_hImageList);

    // Load the button images.
    SendMessage(hWndToolbar, TB_LOADIMAGES, (WPARAM)IDB_STD_SMALL_COLOR, (LPARAM)HINST_COMMCTRL);

    // Add buttons.
    SendMessage(hWndToolbar, TB_BUTTONSTRUCTSIZE, (WPARAM)sizeof(TBBUTTON), 0);
    SendMessage(hWndToolbar, TB_ADDBUTTONS,       (WPARAM)numButtons,       (LPARAM)&tbButtons);

    // Create the edit control child window.    
    HWND hWndEdit = CreateWindowEx(0L, L"Edit", NULL, 
                                   WS_CHILD | WS_BORDER | WS_VISIBLE | ES_LEFT | ES_AUTOVSCROLL | ES_MULTILINE, 
                                   0, 0, cx_edit, cy_edit, 
                                   hWndToolbar, (HMENU) IDM_EDIT, g_hInst, 0 );
    
    if (!hWndEdit)
    {
        DestroyWindow(hWndToolbar);
        ImageList_Destroy(g_hImageList);
        
        return NULL;
    }
    
    return hWndToolbar;    // Return the toolbar with the embedded edit control.
}
```



Cet exemple code en dur les dimensions de la fenêtre enfant ; Toutefois, pour créer une application plus robuste, déterminez la taille de la barre d’outils et rendez la fenêtre de contrôle d’édition adaptée.

Vous souhaiterez peut-être que les notifications du contrôle d’édition s’affichent dans une autre fenêtre, telle que le parent de la barre d’outils. Pour ce faire, créez le contrôle d’édition en tant qu’enfant de la fenêtre parente de la barre d’outils. Ensuite, remplacez le parent du contrôle d’édition par la barre d’outils comme suit.


```
SetParent (hWndEdit, hWndToolbar);
```



Les notifications sont dirigées vers le parent d’origine. Par conséquent, les messages de contrôle d’édition sont dirigés vers le parent de la barre d’outils, même si la fenêtre d’édition se trouve dans la fenêtre de barre d’outils.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation des contrôles ToolBar](using-toolbar-controls.md)
</dt> <dt>

[Démonstration des contrôles communs Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 




