---
title: Guide pratique pour créer une feuille de propriétés
description: L’exemple de cette section crée une feuille de propriétés qui contient deux pages \ 8212 ; une pour définir les propriétés de police d’une cellule dans une feuille de calcul et une autre pour définir les propriétés de bordure de la cellule.
ms.assetid: 61ACF87A-938C-4487-ACEB-484FCB677C6A
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fa99c3e678fa7d8e6aa70cd3f5c6e4c7bc514f94114c7bb7a411fa7df1caac3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117831845"
---
# <a name="how-to-create-a-property-sheet"></a>Guide pratique pour créer une feuille de propriétés

L’exemple de cette section crée une feuille de propriétés qui contient deux pages : une pour définir les propriétés de police d’une cellule dans une feuille de calcul et une autre pour définir les propriétés de bordure de la cellule.

L’exemple définit les pages en remplissant une paire de structures [**PROPSHEETPAGE**](pss-propsheetpage.md) et en spécifiant l’adresse dans la structure [**PROPSHEETHEADER**](pss-propsheetheader.md) qui est transmise à la fonction [**feuille**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) .

## <a name="what-you-need-to-know"></a>Bon à savoir

### <a name="technologies"></a>Technologies

-   [Windows Commandes](window-controls.md)

### <a name="prerequisites"></a>Prérequis

-   C/C++
-   Windows Programmation de l’interface utilisateur

## <a name="instructions"></a>Instructions

### <a name="create-a-property-sheet"></a>Créer une feuille de propriétés

L’exemple de code suivant montre comment créer une feuille de propriétés à deux pages.


```C++
// DoPropertySheet - creates a property sheet that contains two pages.
//
// hwndOwner - handle to the owner window of the property sheet.
//
// Global variables
//     g_hinst - instance handle

extern HINSTANCE g_hinst;

VOID DoPropertySheet(HWND hwndOwner)
{
    PROPSHEETPAGE psp[2];
    
    PROPSHEETHEADER psh;
    
    psp[0].dwSize      = sizeof(PROPSHEETPAGE);
    psp[0].dwFlags     = PSP_USEICONID | PSP_USETITLE;
    psp[0].hInstance   = g_hinst;
    psp[0].pszTemplate = MAKEINTRESOURCE(DLG_FONT);
    psp[0].pszIcon     = MAKEINTRESOURCE(IDI_FONT);
    psp[0].pfnDlgProc  = FontDialogProc;
    psp[0].pszTitle    = MAKEINTRESOURCE(IDS_FONT)
    psp[0].lParam      = 0;
    psp[0].pfnCallback = NULL;
    psp[1].dwSize      = sizeof(PROPSHEETPAGE);
    psp[1].dwFlags     = PSP_USEICONID | PSP_USETITLE;
    psp[1].hInstance   = g_hinst;
    psp[1].pszTemplate = MAKEINTRESOURCE(DLG_BORDER);
    psp[1].pszIcon     = MAKEINTRESOURCE(IDI_BORDER);
    psp[1].pfnDlgProc  = BorderDialogProc;
    psp[1].pszTitle    = MAKEINTRESOURCE(IDS_BORDER);
    psp[1].lParam      = 0;
    psp[1].pfnCallback = NULL;
    
    psh.dwSize      = sizeof(PROPSHEETHEADER);
    psh.dwFlags     = PSH_USEICONID | PSH_PROPSHEETPAGE;
    psh.hwndParent  = hwndOwner;
    psh.hInstance   = g_hinst;
    psh.pszIcon     = MAKEINTRESOURCE(IDI_CELL_PROPERTIES);
    psh.pszCaption  = (LPSTR) "Cell Properties";
    psh.nPages      = sizeof(psp) / sizeof(PROPSHEETPAGE);
    psh.nStartPage  = 0;
    psh.ppsp        = (LPCPROPSHEETPAGE) &psp;
    psh.pfnCallback = NULL;
    
    PropertySheet(&psh);
    
    return;
}
```



## <a name="remarks"></a>Remarques

Les modèles de boîte de dialogue, les icônes et les étiquettes des pages sont chargés à partir des ressources contenues dans le fichier exécutable de l’application. L’icône de la feuille de propriétés est également chargée à partir des ressources de l’application.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation des feuilles de propriétés](using-property-sheets.md)
</dt> <dt>

[Exemple de propriété](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/controls/common/property)
</dt> </dl>

 

 




