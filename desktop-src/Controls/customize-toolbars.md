---
title: Comment personnaliser les barres d’outils
description: La plupart des applications basées sur Windows utilisent des contrôles de barre d’outils pour fournir aux utilisateurs un accès pratique aux fonctionnalités du programme.
ms.assetid: 0CE2988E-D887-433B-BFB2-5F3442E8E1B7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 091451a139cf846b1106916f28c165d6640699eb
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/17/2020
ms.locfileid: "104030956"
---
# <a name="how-to-customize-toolbars"></a><span data-ttu-id="fe120-103">Comment personnaliser les barres d’outils</span><span class="sxs-lookup"><span data-stu-id="fe120-103">How to Customize Toolbars</span></span>

<span data-ttu-id="fe120-104">La plupart des applications basées sur Windows utilisent des contrôles de barre d’outils pour fournir aux utilisateurs un accès pratique aux fonctionnalités du programme.</span><span class="sxs-lookup"><span data-stu-id="fe120-104">Most Windows-based applications use toolbar controls to provide users with convenient access to the program functionality.</span></span> <span data-ttu-id="fe120-105">Toutefois, les barres d’outils statiques présentent quelques lacunes, par exemple un espace trop faible pour afficher efficacement tous les outils disponibles.</span><span class="sxs-lookup"><span data-stu-id="fe120-105">However, static toolbars have some shortcomings—such as too little space to effectively display all the available tools.</span></span> <span data-ttu-id="fe120-106">La solution à ce problème consiste à rendre les barres d’outils de votre application personnalisables.</span><span class="sxs-lookup"><span data-stu-id="fe120-106">The solution to this problem is to make your application's toolbars user-customizable.</span></span> <span data-ttu-id="fe120-107">Ensuite, les utilisateurs peuvent choisir d’afficher uniquement les outils dont ils ont besoin, et ils peuvent les organiser d’une manière adaptée à leur mode de traitement personnel.</span><span class="sxs-lookup"><span data-stu-id="fe120-107">Then, users can choose to display only the tools they need, and they can organize them in a way that suits their personal workstyle.</span></span>

> [!Note]  
> <span data-ttu-id="fe120-108">Les barres d’outils des boîtes de dialogue ne peuvent pas être personnalisées.</span><span class="sxs-lookup"><span data-stu-id="fe120-108">Toolbars in dialog boxes cannot be customized.</span></span>

 

<span data-ttu-id="fe120-109">Pour activer la personnalisation, incluez l’indicateur de style de contrôles communs [**CCS \_ ajustables**](common-control-styles.md) lors de la création du contrôle de barre d’outils.</span><span class="sxs-lookup"><span data-stu-id="fe120-109">To enable customization, include the [**CCS\_ADJUSTABLE**](common-control-styles.md) common controls style flag when you create the toolbar control.</span></span> <span data-ttu-id="fe120-110">Il existe deux approches de base pour la personnalisation :</span><span class="sxs-lookup"><span data-stu-id="fe120-110">There are two basic approaches to customization:</span></span>

-   <span data-ttu-id="fe120-111">La boîte de dialogue Personnalisation.</span><span class="sxs-lookup"><span data-stu-id="fe120-111">The customization dialog box.</span></span> <span data-ttu-id="fe120-112">Cette boîte de dialogue fournie par le système est l’approche la plus simple.</span><span class="sxs-lookup"><span data-stu-id="fe120-112">This system-provided dialog box is the simplest approach.</span></span> <span data-ttu-id="fe120-113">Il fournit aux utilisateurs une interface utilisateur graphique qui leur permet d’ajouter, de supprimer ou de déplacer des icônes.</span><span class="sxs-lookup"><span data-stu-id="fe120-113">It gives users a graphical user interface that allows them to add, delete, or move icons.</span></span>
-   <span data-ttu-id="fe120-114">Glisser-déplacer des outils.</span><span class="sxs-lookup"><span data-stu-id="fe120-114">Dragging and dropping tools.</span></span> <span data-ttu-id="fe120-115">L’implémentation de la fonctionnalité glisser-déplacer permet aux utilisateurs de déplacer des outils vers un autre emplacement de la barre d’outils ou de les supprimer en les faisant glisser en dehors de la barre d’outils.</span><span class="sxs-lookup"><span data-stu-id="fe120-115">Implementing drag-and-drop functionality allows users to move tools to another location on the toolbar or delete them by dragging them off the toolbar.</span></span> <span data-ttu-id="fe120-116">Il fournit aux utilisateurs un moyen simple et rapide d’organiser leur barre d’outils, mais ne les autorise pas à ajouter des outils.</span><span class="sxs-lookup"><span data-stu-id="fe120-116">It provides users a quick and easy way to organize their toolbar, but does not allow them to add tools.</span></span>

<span data-ttu-id="fe120-117">Vous pouvez implémenter l’une ou l’autre approche, ou les deux, selon les besoins de l’application.</span><span class="sxs-lookup"><span data-stu-id="fe120-117">You can implement either approach or both, depending on the needs of the application.</span></span> <span data-ttu-id="fe120-118">Aucune de ces deux approches de la personnalisation ne fournit un mécanisme intégré, tel qu’un bouton Annuler ou annuler, pour ramener la barre d’outils à son état précédent.</span><span class="sxs-lookup"><span data-stu-id="fe120-118">Neither of these two approaches to customization provides a built-in mechanism, such as a Cancel or Undo button, to return the toolbar to its former state.</span></span> <span data-ttu-id="fe120-119">Vous devez utiliser explicitement l’API de contrôle ToolBar pour stocker l’état de prépersonnalisation de la barre d’outils.</span><span class="sxs-lookup"><span data-stu-id="fe120-119">You must explicitly use the toolbar control API to store the toolbar's precustomization state.</span></span> <span data-ttu-id="fe120-120">Si nécessaire, vous pouvez utiliser ces informations stockées ultérieurement pour rétablir l’état d’origine de la barre d’outils.</span><span class="sxs-lookup"><span data-stu-id="fe120-120">If necessary, you can later use this stored information to restore the toolbar to its original state.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="fe120-121">Ce que vous devez savoir</span><span class="sxs-lookup"><span data-stu-id="fe120-121">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="fe120-122">Technologies</span><span class="sxs-lookup"><span data-stu-id="fe120-122">Technologies</span></span>

-   [<span data-ttu-id="fe120-123">Contrôles Windows</span><span class="sxs-lookup"><span data-stu-id="fe120-123">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="fe120-124">Prérequis</span><span class="sxs-lookup"><span data-stu-id="fe120-124">Prerequisites</span></span>

-   <span data-ttu-id="fe120-125">C/C++</span><span class="sxs-lookup"><span data-stu-id="fe120-125">C/C++</span></span>
-   <span data-ttu-id="fe120-126">Programmation de l’interface utilisateur Windows</span><span class="sxs-lookup"><span data-stu-id="fe120-126">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="fe120-127">Instructions</span><span class="sxs-lookup"><span data-stu-id="fe120-127">Instructions</span></span>

### <a name="customization-dialog-box"></a><span data-ttu-id="fe120-128">Boîte de dialogue Personnalisation</span><span class="sxs-lookup"><span data-stu-id="fe120-128">Customization Dialog Box</span></span>

<span data-ttu-id="fe120-129">La boîte de dialogue Personnalisation est fournie par le contrôle ToolBar pour offrir aux utilisateurs un moyen simple d’ajouter, de déplacer ou de supprimer des outils.</span><span class="sxs-lookup"><span data-stu-id="fe120-129">The customization dialog box is provided by the toolbar control to give users a simple way to add, move, or delete tools.</span></span> <span data-ttu-id="fe120-130">Les utilisateurs peuvent le lancer en double-cliquant sur la barre d’outils.</span><span class="sxs-lookup"><span data-stu-id="fe120-130">Users can launch it by double-clicking the toolbar.</span></span> <span data-ttu-id="fe120-131">Les applications peuvent lancer la boîte de dialogue de personnalisation par programmation en envoyant au contrôle de barre d’outils un message de [**\_ personnalisation to**](tb-customize.md) .</span><span class="sxs-lookup"><span data-stu-id="fe120-131">Applications can launch the customization dialog box programmatically by sending the toolbar control a [**TB\_CUSTOMIZE**](tb-customize.md) message.</span></span>

<span data-ttu-id="fe120-132">L’illustration suivante montre un exemple de la boîte de dialogue Personnalisation de la barre d’outils.</span><span class="sxs-lookup"><span data-stu-id="fe120-132">The following illustration shows an example of the toolbar customization dialog box.</span></span>

![capture d’écran d’une fenêtre avec une barre d’outils à trois éléments et une boîte de dialogue avec des listes des boutons disponibles et de la barre d’outils actuelle](images/tb-customdlg.png)

<span data-ttu-id="fe120-134">Les outils de la zone de liste située à droite sont ceux qui se trouvent actuellement dans la barre d’outils.</span><span class="sxs-lookup"><span data-stu-id="fe120-134">The tools in the list box on the right are those currently on the toolbar.</span></span> <span data-ttu-id="fe120-135">Au départ, cette liste contient les outils que vous spécifiez lors de la création de la barre d’outils.</span><span class="sxs-lookup"><span data-stu-id="fe120-135">Initially, this list will contain the tools that you specify when you create the toolbar.</span></span> <span data-ttu-id="fe120-136">La zone de liste située à gauche contient les outils qui peuvent être ajoutés à la barre d’outils.</span><span class="sxs-lookup"><span data-stu-id="fe120-136">The list box in the left contains the tools that are available to add to the toolbar.</span></span> <span data-ttu-id="fe120-137">Votre application est chargée de remplir cette liste (à l’exception du séparateur, qui apparaît automatiquement).</span><span class="sxs-lookup"><span data-stu-id="fe120-137">Your application is responsible for populating that list (other than with the Separator, which appears automatically).</span></span>

<span data-ttu-id="fe120-138">Le contrôle ToolBar informe votre application qu’elle lance une boîte de dialogue de personnalisation en envoyant sa fenêtre parente un code de notification [TBN \_ BEGINADJUST](tbn-beginadjust.md) suivi d’un code de notification [TBN \_ INITCUSTOMIZE](tbn-initcustomize.md) .</span><span class="sxs-lookup"><span data-stu-id="fe120-138">The toolbar control notifies your application that it is launching a customization dialog box by sending its parent window a [TBN\_BEGINADJUST](tbn-beginadjust.md) notification code followed by a [TBN\_INITCUSTOMIZE](tbn-initcustomize.md) notification code.</span></span> <span data-ttu-id="fe120-139">Dans la plupart des cas, l’application n’a pas besoin de répondre à ces codes de notification.</span><span class="sxs-lookup"><span data-stu-id="fe120-139">In most cases, the application does not need to respond to these notification codes.</span></span> <span data-ttu-id="fe120-140">Toutefois, si vous ne souhaitez pas que la boîte de dialogue Personnaliser la barre d’outils affiche un bouton aide, gérez TBN \_ INITCUSTOMIZE en retournant TBNRF \_ HIDEHELP.</span><span class="sxs-lookup"><span data-stu-id="fe120-140">However, if you do not want the Customize Toolbar dialog box to display a Help button, handle TBN\_INITCUSTOMIZE by returning TBNRF\_HIDEHELP.</span></span>

<span data-ttu-id="fe120-141">Le contrôle ToolBar collecte ensuite les informations dont il a besoin pour initialiser la boîte de dialogue en envoyant trois séries de codes de notification, dans l’ordre suivant :</span><span class="sxs-lookup"><span data-stu-id="fe120-141">The toolbar control then collects the information it needs to initialize the dialog box by sending three series of notification codes, in the following order:</span></span>

-   <span data-ttu-id="fe120-142">Un code de notification [TBN \_ QUERYINSERT](tbn-queryinsert.md) pour chaque bouton de la barre d’outils pour déterminer où les boutons peuvent être insérés.</span><span class="sxs-lookup"><span data-stu-id="fe120-142">A [TBN\_QUERYINSERT](tbn-queryinsert.md) notification code for each button on the toolbar to determine where buttons can be inserted.</span></span> <span data-ttu-id="fe120-143">Retourne **false** pour empêcher l’insertion d’un bouton à gauche du bouton spécifié dans le message de notification.</span><span class="sxs-lookup"><span data-stu-id="fe120-143">Return **FALSE** to prevent a button from being inserted to the left of the button specified in the notification message.</span></span> <span data-ttu-id="fe120-144">Si vous renvoyez la **valeur false** à tous les \_ codes de notification TBN QUERYINSERT, la boîte de dialogue ne s’affichera pas.</span><span class="sxs-lookup"><span data-stu-id="fe120-144">If you return **FALSE** to all TBN\_QUERYINSERT notification codes, the dialog box will not be displayed.</span></span>
-   <span data-ttu-id="fe120-145">Un code de notification [TBN \_ QUERYDELETE](tbn-querydelete.md) pour chaque outil qui se trouve actuellement dans la barre d’outils.</span><span class="sxs-lookup"><span data-stu-id="fe120-145">A [TBN\_QUERYDELETE](tbn-querydelete.md) notification code for each tool that is currently on the toolbar.</span></span> <span data-ttu-id="fe120-146">Retourne la **valeur true** si un outil peut être supprimé ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="fe120-146">Return **TRUE** if a tool can be deleted, or **FALSE** if not.</span></span>
-   <span data-ttu-id="fe120-147">Une série de codes de notification [ \_ GETBUTTONINFO TBN](tbn-getbuttoninfo.md) pour renseigner la liste des boutons disponibles.</span><span class="sxs-lookup"><span data-stu-id="fe120-147">A series of [TBN\_GETBUTTONINFO](tbn-getbuttoninfo.md) notification codes to populate the list of available buttons.</span></span> <span data-ttu-id="fe120-148">Pour ajouter un bouton à la liste, remplissez la structure [**NMTOOLBAR**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara) qui est transmise avec le code de notification et renvoyez **true**.</span><span class="sxs-lookup"><span data-stu-id="fe120-148">To add a button to the list, fill in the [**NMTOOLBAR**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara) structure that is passed with the notification code and return **TRUE**.</span></span> <span data-ttu-id="fe120-149">Si vous n’avez plus d’outils à ajouter, retournez la **valeur false**.</span><span class="sxs-lookup"><span data-stu-id="fe120-149">When you have no more tools to add, return **FALSE**.</span></span> <span data-ttu-id="fe120-150">Notez que vous pouvez retourner des informations pour les boutons qui se trouvent déjà dans la barre d’outils ; Ces boutons ne sont pas ajoutés à la liste.</span><span class="sxs-lookup"><span data-stu-id="fe120-150">Note that you can return information for buttons that are already on the toolbar; these buttons will not be added to the list.</span></span>

<span data-ttu-id="fe120-151">La boîte de dialogue est ensuite affichée et l’utilisateur peut commencer à personnaliser la barre d’outils.</span><span class="sxs-lookup"><span data-stu-id="fe120-151">The dialog box is then displayed, and the user can begin to customize the toolbar.</span></span>

<span data-ttu-id="fe120-152">Quand la boîte de dialogue est ouverte, votre application peut recevoir un grand nombre de codes de notification, en fonction des actions de l’utilisateur :</span><span class="sxs-lookup"><span data-stu-id="fe120-152">When the dialog box is open, your application can receive a variety of notification codes, depending on the user's actions:</span></span>

-   <span data-ttu-id="fe120-153">[TBN \_ QUERYINSERT](tbn-queryinsert.md).</span><span class="sxs-lookup"><span data-stu-id="fe120-153">[TBN\_QUERYINSERT](tbn-queryinsert.md).</span></span> <span data-ttu-id="fe120-154">L’utilisateur a modifié l’emplacement d’un outil sur la barre d’outils ou a ajouté un outil.</span><span class="sxs-lookup"><span data-stu-id="fe120-154">The user has changed the location of a tool on the toolbar or added a tool.</span></span> <span data-ttu-id="fe120-155">Retourne **false** pour empêcher l’insertion de l’outil à cet emplacement.</span><span class="sxs-lookup"><span data-stu-id="fe120-155">Return **FALSE** to prevent the tool from being inserted at that location.</span></span>
-   <span data-ttu-id="fe120-156">[TBN \_ DELETINGBUTTON](tbn-deletingbutton.md).</span><span class="sxs-lookup"><span data-stu-id="fe120-156">[TBN\_DELETINGBUTTON](tbn-deletingbutton.md).</span></span> <span data-ttu-id="fe120-157">L’utilisateur est sur le paragraphe de supprimer un outil de la barre d’outils.</span><span class="sxs-lookup"><span data-stu-id="fe120-157">The user is about to remove a tool from the toolbar.</span></span>
-   <span data-ttu-id="fe120-158">[TBN \_ CUSTHELP](tbn-custhelp.md).</span><span class="sxs-lookup"><span data-stu-id="fe120-158">[TBN\_CUSTHELP](tbn-custhelp.md).</span></span> <span data-ttu-id="fe120-159">L’utilisateur a cliqué sur le bouton aide.</span><span class="sxs-lookup"><span data-stu-id="fe120-159">The user has clicked the Help button.</span></span>
-   <span data-ttu-id="fe120-160">[TBN \_ TOOLBARCHANGE](tbn-toolbarchange.md).</span><span class="sxs-lookup"><span data-stu-id="fe120-160">[TBN\_TOOLBARCHANGE](tbn-toolbarchange.md).</span></span> <span data-ttu-id="fe120-161">L’utilisateur a ajouté, déplacé ou supprimé un outil.</span><span class="sxs-lookup"><span data-stu-id="fe120-161">The user has added, moved, or deleted a tool.</span></span>
-   <span data-ttu-id="fe120-162">[TBN \_ Réinitialisez](tbn-reset.md).</span><span class="sxs-lookup"><span data-stu-id="fe120-162">[TBN\_RESET](tbn-reset.md).</span></span> <span data-ttu-id="fe120-163">L’utilisateur a cliqué sur le bouton Réinitialiser.</span><span class="sxs-lookup"><span data-stu-id="fe120-163">The user has clicked the Reset button.</span></span>

<span data-ttu-id="fe120-164">Une fois la boîte de dialogue détruite, votre application reçoit un code de notification [TBN \_ ENDADJUST](tbn-endadjust.md) .</span><span class="sxs-lookup"><span data-stu-id="fe120-164">After the dialog box is destroyed, your application will receive a [TBN\_ENDADJUST](tbn-endadjust.md) notification code.</span></span>

<span data-ttu-id="fe120-165">L’exemple de code suivant montre une façon d’implémenter la personnalisation de la barre d’outils.</span><span class="sxs-lookup"><span data-stu-id="fe120-165">The following code example shows one way to implement toolbar customization.</span></span>


```C++
// The buttons are stored in an array of TBBUTTON structures. 
//
// Constants such as STD_FILENEW are identifiers for the 
// built-in bitmaps that have already been assigned as the toolbar's 
// image list.
//
// Constants such as IDM_NEW are application-defined command identifiers.

TBBUTTON allButtons[] = 
    {
        { MAKELONG(STD_FILENEW,  ImageListID), IDM_NEW,   TBSTATE_ENABLED, 0, {0}, 0, (INT_PTR)L"New" },
        { MAKELONG(STD_FILEOPEN, ImageListID), IDM_OPEN,  TBSTATE_ENABLED, 0, {0}, 0, (INT_PTR)L"Open"},
        { MAKELONG(STD_FILESAVE, ImageListID), IDM_SAVE,  TBSTATE_ENABLED, 0, {0}, 0, (INT_PTR)L"Save"},
        { MAKELONG(STD_CUT,      ImageListID), IDM_CUT,   TBSTATE_ENABLED, 0, {0}, 0, (INT_PTR)L"Cut" },
        { MAKELONG(STD_COPY,     ImageListID), IDM_COPY,  TBSTATE_ENABLED, 0, {0}, 0, (INT_PTR)L"Copy"},
        { MAKELONG(STD_PASTE,    ImageListID), IDM_PASTE, TBSTATE_ENABLED, 0, {0}, 0, (INT_PTR)L"Paste"}
    };

// The following appears in the window's message handler.

case WM_NOTIFY: 
    {
        switch (((LPNMHDR)lParam)->code) 
        {
        
        case TBN_GETBUTTONINFO:  
            {
                LPTBNOTIFY lpTbNotify = (LPTBNOTIFY)lParam;

                // Pass the next button from the array. There is no need to filter out buttons
                // that are already used—they will be ignored.
                
                int buttonCount = sizeof(allButtons) / sizeof(TBBUTTON);
                
                if (lpTbNotify->iItem < buttonCount)
                {
                    lpTbNotify->tbButton = allButtons[lpTbNotify->iItem];
                    return TRUE;
                }
                
                else
                
                {
                    return FALSE;  // No more buttons.
                }
            }
            
            break;

            case TBN_QUERYINSERT:
            
            case TBN_QUERYDELETE:
                return TRUE; 
        }
    }
```



### <a name="dragging-and-dropping-tools"></a><span data-ttu-id="fe120-166">Glisser-déplacer des outils</span><span class="sxs-lookup"><span data-stu-id="fe120-166">Dragging and Dropping Tools</span></span>

<span data-ttu-id="fe120-167">Les utilisateurs peuvent également réorganiser les boutons d’une barre d’outils en appuyant sur la touche Maj et en faisant glisser le bouton vers un autre emplacement.</span><span class="sxs-lookup"><span data-stu-id="fe120-167">Users can also rearrange the buttons on a toolbar by pressing the SHIFT key and dragging the button to another location.</span></span> <span data-ttu-id="fe120-168">Le processus de glisser-déplacer est géré automatiquement par le contrôle ToolBar.</span><span class="sxs-lookup"><span data-stu-id="fe120-168">The drag-and-drop process is handled automatically by the toolbar control.</span></span> <span data-ttu-id="fe120-169">Elle affiche une image fantôme du bouton au fur et à mesure de son déplacement, puis réorganise la barre d’outils après qu’elle a été supprimée.</span><span class="sxs-lookup"><span data-stu-id="fe120-169">It displays a ghost image of the button as it is dragged, and rearranges the toolbar after it is dropped.</span></span> <span data-ttu-id="fe120-170">Les utilisateurs ne peuvent pas ajouter de boutons de cette manière, mais ils peuvent supprimer un bouton en le supprimant de la barre d’outils.</span><span class="sxs-lookup"><span data-stu-id="fe120-170">Users cannot add buttons in this way, but they can delete a button by dropping it off the toolbar.</span></span>

<span data-ttu-id="fe120-171">Bien que le contrôle ToolBar effectue normalement cette opération automatiquement, il envoie également votre application deux codes de notification : [TBN \_ QUERYDELETE](tbn-querydelete.md) et [TBN \_ QUERYINSERT](tbn-queryinsert.md).</span><span class="sxs-lookup"><span data-stu-id="fe120-171">Although the toolbar control normally does this operation automatically, it also sends your application two notification codes: [TBN\_QUERYDELETE](tbn-querydelete.md) and [TBN\_QUERYINSERT](tbn-queryinsert.md).</span></span> <span data-ttu-id="fe120-172">Pour contrôler le processus de glisser-déplacer, gérez ces codes de notification comme suit :</span><span class="sxs-lookup"><span data-stu-id="fe120-172">To control the drag-and-drop process, handle these notification codes as follows:</span></span>

-   <span data-ttu-id="fe120-173">Le code de notification [TBN \_ QUERYDELETE](tbn-querydelete.md) est envoyé dès que l’utilisateur tente de déplacer le bouton, avant l’affichage du bouton fantôme.</span><span class="sxs-lookup"><span data-stu-id="fe120-173">The [TBN\_QUERYDELETE](tbn-querydelete.md) notification code is sent as soon as the user attempts to move the button, before the ghost button is displayed.</span></span> <span data-ttu-id="fe120-174">Retourne **false** pour empêcher le déplacement du bouton.</span><span class="sxs-lookup"><span data-stu-id="fe120-174">Return **FALSE** to prevent the button from being moved.</span></span> <span data-ttu-id="fe120-175">Si vous renvoyez la **valeur true**, l’utilisateur sera en mesure de déplacer l’outil ou de le supprimer en le supprimant de la barre d’outils.</span><span class="sxs-lookup"><span data-stu-id="fe120-175">If you return **TRUE**, the user will be able to either move the tool or delete it by dropping it off the toolbar.</span></span> <span data-ttu-id="fe120-176">Si un outil peut être déplacé, il peut être supprimé.</span><span class="sxs-lookup"><span data-stu-id="fe120-176">If a tool can be moved, it can be deleted.</span></span> <span data-ttu-id="fe120-177">Toutefois, si l’utilisateur supprime un outil, le contrôle de barre d’outils envoie à votre application un code de notification [TBN \_ DELETINGBUTTON](tbn-deletingbutton.md) , auquel vous pouvez choisir de réinsérer le bouton à son emplacement d’origine, annulant ainsi la suppression.</span><span class="sxs-lookup"><span data-stu-id="fe120-177">However, if the user deletes a tool, the toolbar control will send your application a [TBN\_DELETINGBUTTON](tbn-deletingbutton.md) notification code, at which point you can choose to reinsert the button at its original location, thereby canceling the deletion.</span></span>
-   <span data-ttu-id="fe120-178">Le code de notification [TBN \_ QUERYINSERT](tbn-queryinsert.md) est envoyé lorsque l’utilisateur tente de déposer le bouton dans la barre d’outils.</span><span class="sxs-lookup"><span data-stu-id="fe120-178">The [TBN\_QUERYINSERT](tbn-queryinsert.md) notification code is sent when the user attempts to drop the button on the toolbar.</span></span> <span data-ttu-id="fe120-179">Pour éviter que le bouton déplacé à gauche du bouton spécifié dans la notification, retourne **false**.</span><span class="sxs-lookup"><span data-stu-id="fe120-179">To prevent the button that is being moved from being dropped to the left of the button specified in the notification, return **FALSE**.</span></span> <span data-ttu-id="fe120-180">Ce code de notification n’est pas envoyé si l’utilisateur dépose l’outil en dehors de la barre d’outils.</span><span class="sxs-lookup"><span data-stu-id="fe120-180">This notification code is not sent if the user drops the tool off the toolbar.</span></span>

<span data-ttu-id="fe120-181">Si l’utilisateur tente de faire glisser un bouton sans également appuyer sur la touche Maj, le contrôle ToolBar ne gère pas l’opération de glisser-déplacer.</span><span class="sxs-lookup"><span data-stu-id="fe120-181">If the user attempts to drag a button without also pressing the SHIFT key, the toolbar control will not handle the drag-and-drop operation.</span></span> <span data-ttu-id="fe120-182">Toutefois, il enverra à votre application un code de notification [TBN \_ BEGINDRAG](tbn-begindrag.md) pour indiquer le début d’une opération glisser et un code de notification [TBN \_ ENDDRAG](tbn-enddrag.md) pour indiquer la fin.</span><span class="sxs-lookup"><span data-stu-id="fe120-182">However, it will send your application a [TBN\_BEGINDRAG](tbn-begindrag.md) notification code to indicate the start of a drag operation, and a [TBN\_ENDDRAG](tbn-enddrag.md) notification code to indicate the end.</span></span> <span data-ttu-id="fe120-183">Si vous souhaitez activer cette forme de glisser-déplacer, votre application doit gérer ces codes de notification, fournir l’interface utilisateur nécessaire et modifier la barre d’outils pour refléter les modifications apportées.</span><span class="sxs-lookup"><span data-stu-id="fe120-183">If you want to enable this form of drag-and-drop, your application must handle these notification codes, provide the necessary user interface, and modify the toolbar to reflect any changes.</span></span>

### <a name="saving-and-restoring-toolbars"></a><span data-ttu-id="fe120-184">Enregistrement et restauration des barres d’outils</span><span class="sxs-lookup"><span data-stu-id="fe120-184">Saving and Restoring Toolbars</span></span>

<span data-ttu-id="fe120-185">Dans le processus de personnalisation d’une barre d’outils, votre application peut avoir besoin d’enregistrer des informations pour vous permettre de restaurer la barre d’outils à son état d’origine.</span><span class="sxs-lookup"><span data-stu-id="fe120-185">In the process of customizing a toolbar, your application might need to save information so that you can restore the toolbar to its original state.</span></span> <span data-ttu-id="fe120-186">Pour lancer l’enregistrement ou la restauration d’un état de barre d’outils, envoyez au contrôle de barre d’outils un message [**\_ SAVERESTORE to**](tb-saverestore.md) avec *lParam* défini sur **true**.</span><span class="sxs-lookup"><span data-stu-id="fe120-186">To initiate saving or restoring a toolbar state, send the toolbar control a [**TB\_SAVERESTORE**](tb-saverestore.md) message with the *lParam* set to **TRUE**.</span></span> <span data-ttu-id="fe120-187">La valeur *lParam* de ce message spécifie si vous demandez une opération d’enregistrement ou de restauration.</span><span class="sxs-lookup"><span data-stu-id="fe120-187">The *lParam* value of this message specifies whether you are requesting a save or a restore operation.</span></span> <span data-ttu-id="fe120-188">Une fois le message envoyé, il existe deux façons de gérer l’opération d’enregistrement et de restauration :</span><span class="sxs-lookup"><span data-stu-id="fe120-188">After the message is sent, there are two ways to handle the save/restore operation:</span></span>

-   <span data-ttu-id="fe120-189">Avec les contrôles communs [version 4,72](common-control-versions.md) et antérieures, vous devez implémenter un gestionnaire [TBN \_ GETBUTTONINFO](tbn-getbuttoninfo.md) .</span><span class="sxs-lookup"><span data-stu-id="fe120-189">With common controls [version 4.72](common-control-versions.md) and earlier, you must implement a [TBN\_GETBUTTONINFO](tbn-getbuttoninfo.md) handler.</span></span> <span data-ttu-id="fe120-190">Le contrôle ToolBar envoie ce code de notification pour demander des informations sur chaque bouton lors de sa restauration.</span><span class="sxs-lookup"><span data-stu-id="fe120-190">The toolbar control sends this notification code to request information about each button as it is restored.</span></span>
-   <span data-ttu-id="fe120-191">La version 5,80 comprend une option d’enregistrement/de restauration.</span><span class="sxs-lookup"><span data-stu-id="fe120-191">Version 5.80 includes a save/restore option.</span></span> <span data-ttu-id="fe120-192">Au début du processus, lorsque chaque bouton est enregistré ou restauré, votre application reçoit un code de notification [TBN \_ Save](tbn-save.md) ou [TBN \_ Restore](tbn-restore.md) .</span><span class="sxs-lookup"><span data-stu-id="fe120-192">At the beginning of the process, and as each button is saved or restored, your application will receive a [TBN\_SAVE](tbn-save.md) or [TBN\_RESTORE](tbn-restore.md) notification code.</span></span> <span data-ttu-id="fe120-193">Pour utiliser cette option, vous devez implémenter des gestionnaires de notification pour fournir la bitmap et les informations d’État nécessaires à l’enregistrement ou à la restauration de l’état de la barre d’outils.</span><span class="sxs-lookup"><span data-stu-id="fe120-193">To use this option, you must implement notification handlers to provide the bitmap and state information that is needed to successfully save or restore the toolbar state.</span></span>

<span data-ttu-id="fe120-194">Les États de barre d’outils sont enregistrés dans un flux de données qui comprend des blocs de données définies par l’interpréteur de commandes avec des blocs de données définies par l’application.</span><span class="sxs-lookup"><span data-stu-id="fe120-194">Toolbar states are saved in a data stream that consists of blocks of Shell-defined data alternating with blocks of application-defined data.</span></span> <span data-ttu-id="fe120-195">Un bloc de données de chaque type est stocké pour chaque bouton, ainsi qu’un bloc facultatif de données globales que les applications peuvent placer au début du flux.</span><span class="sxs-lookup"><span data-stu-id="fe120-195">One data block of each type is stored for each button, along with an optional block of global data that applications can place at the beginning of the stream.</span></span> <span data-ttu-id="fe120-196">Pendant le processus d’enregistrement, votre gestionnaire d' [ \_ enregistrement TBN](tbn-save.md) ajoute les blocs définis par l’application au flux de données.</span><span class="sxs-lookup"><span data-stu-id="fe120-196">During the save process, your [TBN\_SAVE](tbn-save.md) handler adds the application-defined blocks to the data stream.</span></span> <span data-ttu-id="fe120-197">Pendant le processus de restauration, le gestionnaire de [ \_ restauration TBN](tbn-restore.md) lit chaque bloc et donne à l’interpréteur de commandes les informations dont il a besoin pour reconstruire la barre d’outils.</span><span class="sxs-lookup"><span data-stu-id="fe120-197">During the restore process, the [TBN\_RESTORE](tbn-restore.md) handler reads each block and gives the Shell the information it needs to reconstruct the toolbar.</span></span>

### <a name="how-to-handle-a-tbn_save-notification"></a><span data-ttu-id="fe120-198">Comment gérer une notification d' \_ enregistrement TBN</span><span class="sxs-lookup"><span data-stu-id="fe120-198">How to Handle a TBN\_SAVE Notification</span></span>

<span data-ttu-id="fe120-199">Le premier code de notification d' [ \_ enregistrement TBN](tbn-save.md) est envoyé au début du processus d’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="fe120-199">The first [TBN\_SAVE](tbn-save.md) notification code is sent at the beginning of the save process.</span></span> <span data-ttu-id="fe120-200">Avant l’enregistrement des boutons, les membres de la structure [**NMTBSAVE**](/windows/win32/api/commctrl/ns-commctrl-nmtbsave) sont définis comme indiqué dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="fe120-200">Before any buttons are saved, the members of the [**NMTBSAVE**](/windows/win32/api/commctrl/ns-commctrl-nmtbsave) structure are set as shown in the following table.</span></span>



| <span data-ttu-id="fe120-201">Membre</span><span class="sxs-lookup"><span data-stu-id="fe120-201">Member</span></span>       | <span data-ttu-id="fe120-202">Paramètre</span><span class="sxs-lookup"><span data-stu-id="fe120-202">Setting</span></span>                                                                                                                                                                                                                                                                                                                                            |
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fe120-203">**iItem**</span><span class="sxs-lookup"><span data-stu-id="fe120-203">**iItem**</span></span>    | <span data-ttu-id="fe120-204">–1</span><span class="sxs-lookup"><span data-stu-id="fe120-204">–1</span></span>                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="fe120-205">**cbData**</span><span class="sxs-lookup"><span data-stu-id="fe120-205">**cbData**</span></span>   | <span data-ttu-id="fe120-206">Quantité de mémoire nécessaire pour les données définies par l’interpréteur de commandes.</span><span class="sxs-lookup"><span data-stu-id="fe120-206">The amount of memory needed for Shell-defined data.</span></span>                                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="fe120-207">**cButtons**</span><span class="sxs-lookup"><span data-stu-id="fe120-207">**cButtons**</span></span> | <span data-ttu-id="fe120-208">Nombre de boutons.</span><span class="sxs-lookup"><span data-stu-id="fe120-208">The number of buttons.</span></span>                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="fe120-209">**pData**</span><span class="sxs-lookup"><span data-stu-id="fe120-209">**pData**</span></span>    | <span data-ttu-id="fe120-210">Quantité de mémoire calculée nécessaire pour les données définies par l’application.</span><span class="sxs-lookup"><span data-stu-id="fe120-210">The calculated amount of memory needed for application-defined data.</span></span> <span data-ttu-id="fe120-211">En règle générale, vous incluez des données globales, ainsi que des données pour chaque bouton.</span><span class="sxs-lookup"><span data-stu-id="fe120-211">Typically, you include some global data, plus data for each button.</span></span> <span data-ttu-id="fe120-212">Ajoutez cette valeur à **cbData** et allouez suffisamment de mémoire à **pData** pour la conserver.</span><span class="sxs-lookup"><span data-stu-id="fe120-212">Add that value to **cbData** and allocate enough memory to **pData** to hold it all.</span></span>                                                                                                                      |
| <span data-ttu-id="fe120-213">**pCurrent**</span><span class="sxs-lookup"><span data-stu-id="fe120-213">**pCurrent**</span></span> | <span data-ttu-id="fe120-214">Premier octet inutilisé dans le flux de données.</span><span class="sxs-lookup"><span data-stu-id="fe120-214">The first unused byte in the data stream.</span></span> <span data-ttu-id="fe120-215">Si vous n’avez pas besoin d’informations globales sur la barre d’outils, définissez **pCurrent**  =  **pData** de manière à ce qu’il pointe vers le début du flux de données.</span><span class="sxs-lookup"><span data-stu-id="fe120-215">If you do not require global toolbar information, set **pCurrent** = **pData** so that it points to the start of the data stream.</span></span> <span data-ttu-id="fe120-216">Si vous avez besoin d’informations de barre d’outils globales, stockez-les sur **pData**, puis définissez **pCurrent** au début de la partie inutilisée du flux de données avant de retourner.</span><span class="sxs-lookup"><span data-stu-id="fe120-216">If you do require global toolbar information, store it at **pData**, then set **pCurrent** to the beginning of the unused portion of the data stream before returning.</span></span> |



 

<span data-ttu-id="fe120-217">Si vous souhaitez ajouter des informations globales sur la barre d’outils, placez-la au début du flux de données.</span><span class="sxs-lookup"><span data-stu-id="fe120-217">If you want to add some global toolbar information, put it at the start of the data stream.</span></span> <span data-ttu-id="fe120-218">Avancez les **pCurrent** à la fin des données globales afin qu’elles pointent vers le début de la partie inutilisée du flux de données, et retournent.</span><span class="sxs-lookup"><span data-stu-id="fe120-218">Advance **pCurrent** to the end of the global data so that it points to the beginning of the unused portion of the data stream, and return.</span></span>

<span data-ttu-id="fe120-219">Une fois que vous avez retourné, l’interpréteur de commandes démarre l’enregistrement des informations du bouton.</span><span class="sxs-lookup"><span data-stu-id="fe120-219">After you return, the Shell starts saving button information.</span></span> <span data-ttu-id="fe120-220">Elle ajoute les données définies par l’interpréteur de commandes pour le premier bouton à **pCurrent** , puis avance **pCurrent** au début de la partie inutilisée.</span><span class="sxs-lookup"><span data-stu-id="fe120-220">It adds the Shell-defined data for the first button at **pCurrent** and then advances **pCurrent** to the start of the unused portion.</span></span>

<span data-ttu-id="fe120-221">Une fois chaque bouton enregistré, un code de notification d' [ \_ enregistrement TBN](tbn-save.md) est envoyé et [**NMTBSAVE**](/windows/win32/api/commctrl/ns-commctrl-nmtbsave) est retourné avec les membres définis comme suit.</span><span class="sxs-lookup"><span data-stu-id="fe120-221">After each button is saved, a [TBN\_SAVE](tbn-save.md) notification code is sent and [**NMTBSAVE**](/windows/win32/api/commctrl/ns-commctrl-nmtbsave) is returned with these members set as follows.</span></span>



| <span data-ttu-id="fe120-222">Membre</span><span class="sxs-lookup"><span data-stu-id="fe120-222">Member</span></span>                       | <span data-ttu-id="fe120-223">Paramètre</span><span class="sxs-lookup"><span data-stu-id="fe120-223">Setting</span></span>                                                                                                                                                                                                                                                              |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fe120-224">**iItem**</span><span class="sxs-lookup"><span data-stu-id="fe120-224">**iItem**</span></span>                    | <span data-ttu-id="fe120-225">Index de base zéro du numéro du bouton.</span><span class="sxs-lookup"><span data-stu-id="fe120-225">The zero-based index of the button number.</span></span>                                                                                                                                                                                                                           |
| <span data-ttu-id="fe120-226">**pCurrent**</span><span class="sxs-lookup"><span data-stu-id="fe120-226">**pCurrent**</span></span>                 | <span data-ttu-id="fe120-227">Pointeur vers le premier octet inutilisé dans le flux de données.</span><span class="sxs-lookup"><span data-stu-id="fe120-227">A pointer to the first unused byte in the data stream.</span></span> <span data-ttu-id="fe120-228">Si vous souhaitez stocker des informations supplémentaires sur le bouton, stockez-le à l’emplacement désigné par **pCurrent** et mettez à jour **pCurrent** pour pointer vers la première partie inutilisée du flux de données.</span><span class="sxs-lookup"><span data-stu-id="fe120-228">If you want to store additional information about the button, store it at the location pointed to by **pCurrent** and update **pCurrent** to point to the first unused portion of the data stream after that.</span></span> |
| [<span data-ttu-id="fe120-229">**TBBUTTON**</span><span class="sxs-lookup"><span data-stu-id="fe120-229">**TBBUTTON**</span></span>](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) | <span data-ttu-id="fe120-230">Structure [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) qui décrit le bouton enregistré.</span><span class="sxs-lookup"><span data-stu-id="fe120-230">A [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) structure that describes the button that is being saved.</span></span>                                                                                                                                                                              |



 

<span data-ttu-id="fe120-231">Lorsque vous recevez le code de notification, vous devez extraire toutes les informations spécifiques au bouton dont vous avez besoin à partir de [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton).</span><span class="sxs-lookup"><span data-stu-id="fe120-231">When you receive the notification code, you should extract any button-specific information you need from [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton).</span></span> <span data-ttu-id="fe120-232">N’oubliez pas que lorsque vous ajoutez un bouton, vous pouvez utiliser le membre **dwData** de **TBBUTTON** pour stocker des données spécifiques à l’application.</span><span class="sxs-lookup"><span data-stu-id="fe120-232">Remember that when you add a button, you can use the **dwData** member of **TBBUTTON** to hold application-specific data.</span></span> <span data-ttu-id="fe120-233">Chargez vos données dans le flux de données sur **pCurrent**.</span><span class="sxs-lookup"><span data-stu-id="fe120-233">Load your data into the data stream at **pCurrent**.</span></span> <span data-ttu-id="fe120-234">Avancez les **pCurrent** à la fin de vos données, en pointant à nouveau sur le début de la partie inutilisée du flux et retournez.</span><span class="sxs-lookup"><span data-stu-id="fe120-234">Advance **pCurrent** to the end of your data, again pointing to the beginning of the unused portion of the stream, and return.</span></span>

<span data-ttu-id="fe120-235">L’interpréteur de commandes passe ensuite au bouton suivant, ajoute ses informations à **pData**, avance **PCurrent**, charge [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton)et envoie un autre code de notification d' [ \_ enregistrement TBN](tbn-save.md) .</span><span class="sxs-lookup"><span data-stu-id="fe120-235">The Shell then goes to the next button, adds its information to **pData**, advances **pCurrent**, loads [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton), and sends another [TBN\_SAVE](tbn-save.md) notification code.</span></span> <span data-ttu-id="fe120-236">Ce processus se poursuit jusqu’à ce que tous les boutons soient enregistrés.</span><span class="sxs-lookup"><span data-stu-id="fe120-236">This process continues until all buttons are saved.</span></span>

### <a name="restoring-saved-toolbars"></a><span data-ttu-id="fe120-237">Restauration des barres d’outils enregistrées</span><span class="sxs-lookup"><span data-stu-id="fe120-237">Restoring Saved Toolbars</span></span>

<span data-ttu-id="fe120-238">Le processus de restauration inverse fondamentalement le processus d’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="fe120-238">The restore process basically reverses the save process.</span></span> <span data-ttu-id="fe120-239">Au début, votre application recevra un code de notification de [ \_ restauration TBN](tbn-restore.md) avec le membre **iItem** de la structure [**NMTBRESTORE**](/windows/win32/api/commctrl/ns-commctrl-nmtbrestore) définie sur – 1.</span><span class="sxs-lookup"><span data-stu-id="fe120-239">At the beginning, your application will receive a [TBN\_RESTORE](tbn-restore.md) notification code with the **iItem** member of the [**NMTBRESTORE**](/windows/win32/api/commctrl/ns-commctrl-nmtbrestore) structure set to –1.</span></span> <span data-ttu-id="fe120-240">Le membre **cbData** est défini sur la taille de **pData** et **cButtons** est défini sur le nombre de boutons.</span><span class="sxs-lookup"><span data-stu-id="fe120-240">The **cbData** member is set to the size of **pData**, and **cButtons** is set to the number of buttons.</span></span>

<span data-ttu-id="fe120-241">Votre gestionnaire de notification doit extraire les informations globales qui ont été placées au début de **pData** pendant l’enregistrement, et avancer **pCurrent** au début du premier bloc de données définies par l’interpréteur de commandes.</span><span class="sxs-lookup"><span data-stu-id="fe120-241">Your notification handler should extract the global information that was placed at the beginning of **pData** during the save, and advance **pCurrent** to the start of the first block of Shell-defined data.</span></span> <span data-ttu-id="fe120-242">Définissez **cBytesPerRecord** sur la taille des blocs de données que vous avez utilisés pour enregistrer les données du bouton.</span><span class="sxs-lookup"><span data-stu-id="fe120-242">Set **cBytesPerRecord** to the size of the data blocks you used to save the button data.</span></span> <span data-ttu-id="fe120-243">Définissez **cButtons** sur le nombre de boutons et retournez.</span><span class="sxs-lookup"><span data-stu-id="fe120-243">Set **cButtons** to the number of buttons, and return.</span></span>

<span data-ttu-id="fe120-244">Le [**NMTBRESTORE**](/windows/win32/api/commctrl/ns-commctrl-nmtbrestore) suivant est pour le premier bouton.</span><span class="sxs-lookup"><span data-stu-id="fe120-244">The next [**NMTBRESTORE**](/windows/win32/api/commctrl/ns-commctrl-nmtbrestore) is for the first button.</span></span> <span data-ttu-id="fe120-245">Le membre **pCurrent** pointe vers le début de votre premier bloc de données de bouton, et **iItem** est défini sur l’index de bouton.</span><span class="sxs-lookup"><span data-stu-id="fe120-245">The **pCurrent** member points to the start of your first block of button data, and **iItem** is set to the button index.</span></span> <span data-ttu-id="fe120-246">Extrayez ces données et avancez **pCurrent**.</span><span class="sxs-lookup"><span data-stu-id="fe120-246">Extract that data and advance **pCurrent**.</span></span> <span data-ttu-id="fe120-247">Charger les données dans [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton)et retourner.</span><span class="sxs-lookup"><span data-stu-id="fe120-247">Load the data into [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton), and return.</span></span> <span data-ttu-id="fe120-248">Pour omettre un bouton à partir de la barre d’outils restaurée, définissez le membre **idCommand** de **TBBUTTON** sur zéro.</span><span class="sxs-lookup"><span data-stu-id="fe120-248">To omit a button from the restored toolbar, set the **idCommand** member of **TBBUTTON** to zero.</span></span> <span data-ttu-id="fe120-249">L’interpréteur de commandes répète le processus pour les boutons restants.</span><span class="sxs-lookup"><span data-stu-id="fe120-249">The Shell will repeat the process for the remaining buttons.</span></span> <span data-ttu-id="fe120-250">En plus des messages [**NMTBSAVE**](/windows/win32/api/commctrl/ns-commctrl-nmtbsave) et **NMTBRESTORE** , vous pouvez également utiliser des messages tels que [TBN \_ Reset](tbn-reset.md) pour enregistrer et restaurer une barre d’outils.</span><span class="sxs-lookup"><span data-stu-id="fe120-250">In addition to the [**NMTBSAVE**](/windows/win32/api/commctrl/ns-commctrl-nmtbsave) and **NMTBRESTORE** messages, you can also use messages such as [TBN\_RESET](tbn-reset.md) to save and restore a toolbar.</span></span>

<span data-ttu-id="fe120-251">L’exemple de code suivant enregistre une barre d’outils avant qu’elle ne soit personnalisée et la restaure si l’application reçoit un message de [ \_ réinitialisation TBN](tbn-reset.md) .</span><span class="sxs-lookup"><span data-stu-id="fe120-251">The following code example saves a toolbar before it is customized, and restores it if the application receives a [TBN\_RESET](tbn-reset.md) message.</span></span>


```C++
int               i;
LPNMHDR           lpnmhdr;
static int        nResetCount;
static LPTBBUTTON lpSaveButtons;
LPARAM            lParam;

switch( lpnmhdr->code)
{
    case TBN_BEGINADJUST: // Begin customizing the toolbar.
    {
        LPTBNOTIFY  lpTB = (LPTBNOTIFY)lparam;
       
        // Allocate memory for the button information.
        
        nResetCount   = SendMessage(lpTB->hdr.hwndFrom, TB_BUTTONCOUNT, 0, 0);
        lpSaveButtons = (LPTBBUTTON)GlobalAlloc(GPTR, sizeof(TBBUTTON) * nResetCount);
      
        // In case the user presses reset, save the current configuration 
        // so the original toolbar can be restored.
        
        for(i = 0; i < nResetCount; i++)
        {
            SendMessage(lpTB->hdr.hwndFrom, 
                        TB_GETBUTTON, i, 
                        (LPARAM)(lpSaveButtons + i));
        }
    }
    
    return TRUE;
   
    case TBN_RESET:
    {
        LPTBNOTIFY lpTB = (LPTBNOTIFY)lparam;
        
        int nCount, i;
    
        // Remove all of the existing buttons, starting with the last one.
        
        nCount = SendMessage(lpTB->hdr.hwndFrom, TB_BUTTONCOUNT, 0, 0);
        
        for(i = nCount - 1; i >= 0; i--)
        {
            SendMessage(lpTB->hdr.hwndFrom, TB_DELETEBUTTON, i, 0);
        }
      
        SendMessage(lpTB->hdr.hwndFrom,      // Restore the saved buttons.
                    TB_ADDBUTTONS, 
                    (WPARAM)nResetCount, 
                    (LPARAM)lpSaveButtons);
    }
    
    return TRUE;
   
    case TBN_ENDADJUST:                // Free up the memory you allocated.
        GlobalFree((HGLOBAL)lpSaveButtons);
        
        return TRUE;
}
```



## <a name="related-topics"></a><span data-ttu-id="fe120-252">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="fe120-252">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fe120-253">Utilisation des contrôles ToolBar</span><span class="sxs-lookup"><span data-stu-id="fe120-253">Using Toolbar Controls</span></span>](using-toolbar-controls.md)
</dt> <dt>

[<span data-ttu-id="fe120-254">**Valeurs d’index d’image du bouton standard de la barre d’outils**</span><span class="sxs-lookup"><span data-stu-id="fe120-254">**Toolbar Standard Button Image Index Values**</span></span>](toolbar-standard-button-image-index-values.md)
</dt> <dt>

<span data-ttu-id="fe120-255">[Démonstration des contrôles communs Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="fe120-255">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 




