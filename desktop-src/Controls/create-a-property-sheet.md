---
title: Guide pratique pour créer une feuille de propriétés
description: L’exemple de cette section crée une feuille de propriétés qui contient deux pages \ 8212 ; une pour définir les propriétés de police d’une cellule dans une feuille de calcul et une autre pour définir les propriétés de bordure de la cellule.
ms.assetid: 61ACF87A-938C-4487-ACEB-484FCB677C6A
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d15abd44f3a583afd99c5d943b9105c8734b73c1
ms.sourcegitcommit: 11f52354f570aacaf1ba2a266b2e507abd73352a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/19/2021
ms.locfileid: "106532695"
---
# <a name="how-to-create-a-property-sheet"></a><span data-ttu-id="22889-103">Guide pratique pour créer une feuille de propriétés</span><span class="sxs-lookup"><span data-stu-id="22889-103">How to Create a Property Sheet</span></span>

<span data-ttu-id="22889-104">L’exemple de cette section crée une feuille de propriétés qui contient deux pages : une pour définir les propriétés de police d’une cellule dans une feuille de calcul et une autre pour définir les propriétés de bordure de la cellule.</span><span class="sxs-lookup"><span data-stu-id="22889-104">The example in this section creates a property sheet that contains two pages—one for setting the font properties of a cell in a spreadsheet, and another for setting the border properties of the cell.</span></span>

<span data-ttu-id="22889-105">L’exemple définit les pages en remplissant une paire de structures [**PROPSHEETPAGE**](pss-propsheetpage.md) et en spécifiant l’adresse dans la structure [**PROPSHEETHEADER**](pss-propsheetheader.md) qui est transmise à la fonction [**feuille**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) .</span><span class="sxs-lookup"><span data-stu-id="22889-105">The example defines the pages by filling a pair of [**PROPSHEETPAGE**](pss-propsheetpage.md) structures and specifying the address in the [**PROPSHEETHEADER**](pss-propsheetheader.md) structure that is passed to the [**PropertySheet**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) function.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="22889-106">Ce que vous devez savoir</span><span class="sxs-lookup"><span data-stu-id="22889-106">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="22889-107">Technologies</span><span class="sxs-lookup"><span data-stu-id="22889-107">Technologies</span></span>

-   [<span data-ttu-id="22889-108">Contrôles Windows</span><span class="sxs-lookup"><span data-stu-id="22889-108">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="22889-109">Prérequis</span><span class="sxs-lookup"><span data-stu-id="22889-109">Prerequisites</span></span>

-   <span data-ttu-id="22889-110">C/C++</span><span class="sxs-lookup"><span data-stu-id="22889-110">C/C++</span></span>
-   <span data-ttu-id="22889-111">Programmation de l’interface utilisateur Windows</span><span class="sxs-lookup"><span data-stu-id="22889-111">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="22889-112">Instructions</span><span class="sxs-lookup"><span data-stu-id="22889-112">Instructions</span></span>

### <a name="create-a-property-sheet"></a><span data-ttu-id="22889-113">Créer une feuille de propriétés</span><span class="sxs-lookup"><span data-stu-id="22889-113">Create a Property Sheet</span></span>

<span data-ttu-id="22889-114">L’exemple de code suivant montre comment créer une feuille de propriétés à deux pages.</span><span class="sxs-lookup"><span data-stu-id="22889-114">The following code example demonstrates how to create a two–page property sheet.</span></span>


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



## <a name="remarks"></a><span data-ttu-id="22889-115">Notes</span><span class="sxs-lookup"><span data-stu-id="22889-115">Remarks</span></span>

<span data-ttu-id="22889-116">Les modèles de boîte de dialogue, les icônes et les étiquettes des pages sont chargés à partir des ressources contenues dans le fichier exécutable de l’application.</span><span class="sxs-lookup"><span data-stu-id="22889-116">The dialog box templates, icons, and labels for the pages are loaded from the resources contained in the application's executable file.</span></span> <span data-ttu-id="22889-117">L’icône de la feuille de propriétés est également chargée à partir des ressources de l’application.</span><span class="sxs-lookup"><span data-stu-id="22889-117">The icon for the property sheet is also loaded from the application's resources.</span></span>

## <a name="related-topics"></a><span data-ttu-id="22889-118">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="22889-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="22889-119">Utilisation des feuilles de propriétés</span><span class="sxs-lookup"><span data-stu-id="22889-119">Using Property Sheets</span></span>](using-property-sheets.md)
</dt> <dt>

[<span data-ttu-id="22889-120">Exemple de propriété</span><span class="sxs-lookup"><span data-stu-id="22889-120">Property sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/controls/common/property)
</dt> </dl>

 

 




