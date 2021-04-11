---
title: Utilisation de Hot-Tracking avec des barres d’outils
description: Quand un pointeur de la souris est placé sur un élément, l’élément devient réactif. Si le suivi à chaud est activé, l’élément réactif est mis en surbrillance. Une barre d’outils créée avec le \_ style à deux dimensions TBSTYLE, ou une barre d’outils qui utilise des styles visuels, prend en charge le suivi à chaud par défaut.
ms.assetid: E77B15D7-F0C9-41F7-8BE9-30260FA4BB0C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a486407b8dafade1e3bba083c5a56f3a9be2adcf
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/17/2020
ms.locfileid: "104030958"
---
# <a name="how-to-use-hot-tracking-with-toolbars"></a><span data-ttu-id="889c6-105">Utilisation de Hot-Tracking avec des barres d’outils</span><span class="sxs-lookup"><span data-stu-id="889c6-105">How to Use Hot-Tracking with Toolbars</span></span>

<span data-ttu-id="889c6-106">Quand un pointeur de la souris est placé sur un élément, l’élément devient réactif.</span><span class="sxs-lookup"><span data-stu-id="889c6-106">When a mouse pointer hovers over an item, the item becomes hot.</span></span> <span data-ttu-id="889c6-107">Si le suivi à chaud est activé, l’élément réactif est mis en surbrillance.</span><span class="sxs-lookup"><span data-stu-id="889c6-107">If hot-tracking is enabled, the hot item is highlighted.</span></span> <span data-ttu-id="889c6-108">Une barre d’outils créée avec le style à [**\_ deux dimensions TBSTYLE**](toolbar-control-and-button-styles.md) , ou une barre d’outils qui utilise des [styles visuels](themes-overview.md), prend en charge le suivi à chaud par défaut.</span><span class="sxs-lookup"><span data-stu-id="889c6-108">A toolbar that is created with the [**TBSTYLE\_FLAT**](toolbar-control-and-button-styles.md) style, or one that uses [Visual Styles](themes-overview.md), supports hot-tracking by default.</span></span>

<span data-ttu-id="889c6-109">Le suivi à chaud requiert la création de listes d’images ; par conséquent, vous ne pouvez pas utiliser le message [**to \_ ADDBITMAP**](tb-addbitmap.md) ou la fonction [**CreateToolbarEx**](/windows/desktop/api/Commctrl/nf-commctrl-createtoolbarex) pour créer votre barre d’outils.</span><span class="sxs-lookup"><span data-stu-id="889c6-109">Hot-tracking requires that you create image lists; therefore, you cannot use the [**TB\_ADDBITMAP**](tb-addbitmap.md) message or the [**CreateToolbarEx**](/windows/desktop/api/Commctrl/nf-commctrl-createtoolbarex) function to create your toolbar.</span></span>

<span data-ttu-id="889c6-110">Lorsque la souris pointe sur un bouton de barre d’outils, le bouton est entouré pour le mettre en surbrillance.</span><span class="sxs-lookup"><span data-stu-id="889c6-110">When the mouse hovers over a toolbar button, the button is outlined to highlight it.</span></span> <span data-ttu-id="889c6-111">L’illustration suivante montre une barre d’outils avec le suivi actif activé ; le pointeur de la souris est positionné sur le bouton enregistrer au moment où la capture d’écran a été effectuée.</span><span class="sxs-lookup"><span data-stu-id="889c6-111">The following illustration shows a toolbar with hot-tracking enabled; the mouse pointer was hovering on the Save button when the screen shot was taken.</span></span>

![capture d’écran d’une boîte de dialogue avec une barre d’outils à trois éléments ; l’icône sélectionnée est entourée](images/tb-withstyles.png)

<span data-ttu-id="889c6-113">Si vous souhaitez qu’une image bitmap de bouton de barre d’outils change lorsque l’état du contrôle change, stockez les différentes images dans les [listes d’images](image-lists.md).</span><span class="sxs-lookup"><span data-stu-id="889c6-113">If you want a toolbar button bitmap to change when the state of the control changes, store the different images in [image lists](image-lists.md).</span></span> <span data-ttu-id="889c6-114">Par exemple, certaines applications ont des boutons de barre d’outils noir et blanc qui deviennent colorés lorsqu’ils sont sélectionnés.</span><span class="sxs-lookup"><span data-stu-id="889c6-114">For example, some applications have black and white toolbar buttons that become colored when they are selected.</span></span> <span data-ttu-id="889c6-115">Les deux images différentes sont stockées dans des listes d’images.</span><span class="sxs-lookup"><span data-stu-id="889c6-115">The two different images are stored in image lists.</span></span> <span data-ttu-id="889c6-116">Les barres d’outils prennent en charge l’utilisation de trois listes d’images.</span><span class="sxs-lookup"><span data-stu-id="889c6-116">Toolbars support using up to three image lists.</span></span> <span data-ttu-id="889c6-117">En général, une application a une liste d’images par défaut, désactivée et de suivi à chaud.</span><span class="sxs-lookup"><span data-stu-id="889c6-117">Typically an application has a default, disabled, and hot-tracking list of images.</span></span> <span data-ttu-id="889c6-118">Pour définir et récupérer des listes d’images pour les boutons de barre d’outils à chaud, utilisez les messages [**to \_ SETHOTIMAGELIST**](tb-sethotimagelist.md) et [**to \_ GETHOTIMAGELIST**](tb-gethotimagelist.md) .</span><span class="sxs-lookup"><span data-stu-id="889c6-118">To set and retrieve image lists for hot toolbar buttons, use the [**TB\_SETHOTIMAGELIST**](tb-sethotimagelist.md) and [**TB\_GETHOTIMAGELIST**](tb-gethotimagelist.md) messages.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="889c6-119">Ce que vous devez savoir</span><span class="sxs-lookup"><span data-stu-id="889c6-119">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="889c6-120">Technologies</span><span class="sxs-lookup"><span data-stu-id="889c6-120">Technologies</span></span>

-   [<span data-ttu-id="889c6-121">Contrôles Windows</span><span class="sxs-lookup"><span data-stu-id="889c6-121">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="889c6-122">Prérequis</span><span class="sxs-lookup"><span data-stu-id="889c6-122">Prerequisites</span></span>

-   <span data-ttu-id="889c6-123">C/C++</span><span class="sxs-lookup"><span data-stu-id="889c6-123">C/C++</span></span>
-   <span data-ttu-id="889c6-124">Programmation de l’interface utilisateur Windows</span><span class="sxs-lookup"><span data-stu-id="889c6-124">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="889c6-125">Instructions</span><span class="sxs-lookup"><span data-stu-id="889c6-125">Instructions</span></span>

### <a name="use-hot-tracking-with-a-toolbar"></a><span data-ttu-id="889c6-126">Utiliser Hot-Tracking avec une barre d’outils</span><span class="sxs-lookup"><span data-stu-id="889c6-126">Use Hot-Tracking with a Toolbar</span></span>

<span data-ttu-id="889c6-127">L’exemple de code suivant crée, remplit et assigne une liste d’images pour les boutons actifs.</span><span class="sxs-lookup"><span data-stu-id="889c6-127">The following code example creates, fills, and assigns an image list for hot buttons.</span></span>


```C++
// Create the image list, himlHot.
g_himlHot = ImageList_Create(MYICON_CX,MYICON_CY,ILC_COLOR8,0,4);

// Load a bitmap from a resource file, and add the images to the image list.
// Note that the bitmap contains four images.

hBitmapHot = LoadBitmap(g_hinst, MAKEINTRESOURCE(IDB_HOT));

ImageList_Add(g_himlHot, hBitmapHot, NULL);
   
// Set the image list. 
SendMessage(hwndTB, TB_SETHOTIMAGELIST, 0, (LPARAM)g_himlHot);
   
// Loop to fill the array of TBBUTTON structures.  
for(i=0;i<MAX_BUTTONS;i++)
{
    tbArray[i].iBitmap   = i;                   // Bitmap from image list.
    tbArray[i].idCommand = IDM_BUTTONSTART + i;
    tbArray[i].fsState   = TBSTATE_ENABLED;
    tbArray[i].fsStyle   = BTNS_DROPDOWN;
    tbArray[i].dwData    = 0;
    tbArray[i].iString   = i;
}

DeleteObject(hBitmapHot);    // Delete the loaded bitmap.
```



## <a name="related-topics"></a><span data-ttu-id="889c6-128">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="889c6-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="889c6-129">Utilisation des contrôles ToolBar</span><span class="sxs-lookup"><span data-stu-id="889c6-129">Using Toolbar Controls</span></span>](using-toolbar-controls.md)
</dt> <dt>

<span data-ttu-id="889c6-130">[Démonstration des contrôles communs Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="889c6-130">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 




