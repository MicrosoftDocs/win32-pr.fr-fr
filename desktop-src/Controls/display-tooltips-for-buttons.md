---
title: Comment afficher des info-bulles pour les boutons
description: Quand vous spécifiez le \_ style des info-bulles TBSTYLE, la barre d’outils crée et gère un contrôle ToolTip. Le contrôle ToolTip est masqué et s’affiche uniquement lorsque les utilisateurs déplacent le pointeur sur un bouton de barre d’outils et le laissent pendant environ une seconde.
ms.assetid: 0383DB63-A10E-4235-A974-AB21551E086B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb37de7c21c904673a1f656533497130d50bd8f7
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/17/2020
ms.locfileid: "103841990"
---
# <a name="how-to-display-tooltips-for-buttons"></a><span data-ttu-id="73802-104">Comment afficher des info-bulles pour les boutons</span><span class="sxs-lookup"><span data-stu-id="73802-104">How to Display Tooltips for Buttons</span></span>

<span data-ttu-id="73802-105">Quand vous spécifiez le style des [**\_ info-bulles TBSTYLE**](toolbar-control-and-button-styles.md) , la barre d’outils crée et gère un contrôle ToolTip.</span><span class="sxs-lookup"><span data-stu-id="73802-105">When you specify the [**TBSTYLE\_TOOLTIPS**](toolbar-control-and-button-styles.md) style, the toolbar creates and manages a tooltip control.</span></span> <span data-ttu-id="73802-106">Le contrôle ToolTip est masqué et s’affiche uniquement lorsque les utilisateurs déplacent le pointeur sur un bouton de barre d’outils et le laissent pendant environ une seconde.</span><span class="sxs-lookup"><span data-stu-id="73802-106">The tooltip control is hidden and appears only when users move the pointer over a toolbar button and leave it there for approximately one second.</span></span>

<span data-ttu-id="73802-107">Votre application peut fournir du texte au contrôle ToolTip de l’une des manières suivantes :</span><span class="sxs-lookup"><span data-stu-id="73802-107">Your application can supply text to the tooltip control in any one of the following ways:</span></span>

-   <span data-ttu-id="73802-108">Définissez le texte d’info-bulle en tant que membre **iString** de la structure [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) pour chaque bouton.</span><span class="sxs-lookup"><span data-stu-id="73802-108">Set the tooltip text as the **iString** member of the [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) structure for each button.</span></span> <span data-ttu-id="73802-109">Vous devez également envoyer un [**message \_ SETMAXTEXTROWS to**](tb-setmaxtextrows.md) et définir le nombre maximal de lignes de texte sur 0, afin que le texte ne s’affiche pas en tant qu’info-bulle plutôt que sous forme d’info-bulle.</span><span class="sxs-lookup"><span data-stu-id="73802-109">You must also send a [**TB\_SETMAXTEXTROWS**](tb-setmaxtextrows.md) message and set the maximum text rows to 0, so that the text does not appear as the button label rather than as a tooltip.</span></span>
-   <span data-ttu-id="73802-110">Créez la barre d’outils avec le style de [**\_ liste TBSTYLE**](toolbar-control-and-button-styles.md) , puis définissez le style étendu [**TBSTYLE \_ ex \_ MIXEDBUTTONS**](toolbar-extended-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="73802-110">Create the toolbar with the [**TBSTYLE\_LIST**](toolbar-control-and-button-styles.md) style and then set the [**TBSTYLE\_EX\_MIXEDBUTTONS**](toolbar-extended-styles.md) extended style.</span></span> <span data-ttu-id="73802-111">Les étiquettes s’affichent uniquement pour les boutons qui ont le style [**BTNS \_ SHOWTEXT**](toolbar-control-and-button-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="73802-111">Labels are shown only for buttons that have the [**BTNS\_SHOWTEXT**](toolbar-control-and-button-styles.md) style.</span></span> <span data-ttu-id="73802-112">Pour les boutons qui n’ont pas ce style, une info-bulle est affichée et contient le texte du bouton.</span><span class="sxs-lookup"><span data-stu-id="73802-112">For buttons that do not have this style, a tooltip is shown that contains the button text.</span></span>
-   <span data-ttu-id="73802-113">Répondez au code de notification [ttn \_ GETDISPINFO](ttn-getdispinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="73802-113">Respond to the [TTN\_GETDISPINFO](ttn-getdispinfo.md) notification code.</span></span>
-   <span data-ttu-id="73802-114">Répondez au code de notification [TBN \_ GETINFOTIP](tbn-getinfotip.md) .</span><span class="sxs-lookup"><span data-stu-id="73802-114">Respond to the [TBN\_GETINFOTIP](tbn-getinfotip.md) notification code.</span></span>

<span data-ttu-id="73802-115">Une application qui doit envoyer des messages directement au contrôle ToolTip peut récupérer le handle du contrôle à l’aide du message [**to \_ GETTOOLTIPS**](tb-gettooltips.md) .</span><span class="sxs-lookup"><span data-stu-id="73802-115">An application that needs to send messages directly to the tooltip control can retrieve the handle to the control by using the [**TB\_GETTOOLTIPS**](tb-gettooltips.md) message.</span></span> <span data-ttu-id="73802-116">Une application peut remplacer le contrôle ToolTip d’une barre d’outils par un autre contrôle ToolTip en utilisant le message [**to \_ SETTOOLTIPS**](tb-settooltips.md) .</span><span class="sxs-lookup"><span data-stu-id="73802-116">An application can replace the tooltip control of a toolbar with another tooltip control by using the [**TB\_SETTOOLTIPS**](tb-settooltips.md) message.</span></span>

<span data-ttu-id="73802-117">La méthode la plus souple pour fournir le texte info-bulle consiste à répondre au code de notification [ttn \_ GETDISPINFO](ttn-getdispinfo.md) ou [TBN \_ GETINFOTIP](tbn-getinfotip.md) envoyé par le contrôle ToolBar à son parent sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="73802-117">The most flexible way of supplying tooltip text is to respond to the [TTN\_GETDISPINFO](ttn-getdispinfo.md) or [TBN\_GETINFOTIP](tbn-getinfotip.md) notification code sent by the toolbar control to its parent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span> <span data-ttu-id="73802-118">Pour [ttn \_ GETDISPINFO](ttn-getdispinfo.md), le paramètre *lParam* comprend un pointeur vers une structure [**NMTTDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmttdispinfoa) (également définie comme **LPTOOLTIPTEXT**) qui spécifie l’identificateur de commande du bouton pour lequel le texte d’aide est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="73802-118">For [TTN\_GETDISPINFO](ttn-getdispinfo.md), the *lParam* parameter includes a pointer to an [**NMTTDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmttdispinfoa) structure (also defined as **LPTOOLTIPTEXT**) that specifies the command identifier of the button for which Help text is needed.</span></span> <span data-ttu-id="73802-119">Cet identificateur se trouve dans le membre **NMTTDISPINFO. HDR. idFrom** .</span><span class="sxs-lookup"><span data-stu-id="73802-119">This identifier is in the **NMTTDISPINFO.hdr.idFrom** member.</span></span> <span data-ttu-id="73802-120">Une application peut copier le texte d’aide dans la structure, spécifier l’adresse d’une chaîne contenant le texte d’aide ou spécifier le handle d’instance et l’identificateur de ressource d’une ressource de type chaîne.</span><span class="sxs-lookup"><span data-stu-id="73802-120">An application can copy the Help text to the structure, specify the address of a string containing the Help text, or specify the instance handle and resource identifier of a string resource.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="73802-121">Ce que vous devez savoir</span><span class="sxs-lookup"><span data-stu-id="73802-121">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="73802-122">Technologies</span><span class="sxs-lookup"><span data-stu-id="73802-122">Technologies</span></span>

-   [<span data-ttu-id="73802-123">Contrôles Windows</span><span class="sxs-lookup"><span data-stu-id="73802-123">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="73802-124">Prérequis</span><span class="sxs-lookup"><span data-stu-id="73802-124">Prerequisites</span></span>

-   <span data-ttu-id="73802-125">C/C++</span><span class="sxs-lookup"><span data-stu-id="73802-125">C/C++</span></span>
-   <span data-ttu-id="73802-126">Programmation de l’interface utilisateur Windows</span><span class="sxs-lookup"><span data-stu-id="73802-126">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="73802-127">Instructions</span><span class="sxs-lookup"><span data-stu-id="73802-127">Instructions</span></span>

### <a name="display-a-tooltip-for-a-button"></a><span data-ttu-id="73802-128">Afficher une info-bulle pour un bouton</span><span class="sxs-lookup"><span data-stu-id="73802-128">Display a Tooltip for a Button</span></span>

<span data-ttu-id="73802-129">L’exemple de code suivant gère le code de notification d’info-bulle [ttn \_ GETDISPINFO](ttn-getdispinfo.md) en fournissant du texte à partir d’identificateurs de ressource.</span><span class="sxs-lookup"><span data-stu-id="73802-129">The following example code handles the [TTN\_GETDISPINFO](ttn-getdispinfo.md) tooltip notification code by providing text from resource identifiers.</span></span>


```C++
case WM_NOTIFY: 
            
    switch (((LPNMHDR) lParam)->code) 
    {
    
    case TTN_GETDISPINFO: 
        { 
            LPTOOLTIPTEXT lpttt = (LPTOOLTIPTEXT)lParam; 
            
            // Set the instance of the module that contains the resource.
            lpttt->hinst = g_hInst; 
            
            UINT_PTR idButton = lpttt->hdr.idFrom;
            
            switch (idButton) 
            { 
            case IDM_NEW: 
                lpttt->lpszText = MAKEINTRESOURCE(IDS_TIPS_NEW); 
                break; 
                
            case IDM_OPEN: 
                lpttt->lpszText = MAKEINTRESOURCE(IDS_TIPS_OPEN); 
                break; 
                
            case IDM_SAVE: 
                lpttt->lpszText = MAKEINTRESOURCE(IDS_TIPS_SAVE); 
                break; 
            } 
            
            break; 
        } 
    }
    return TRUE;
```



## <a name="related-topics"></a><span data-ttu-id="73802-130">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="73802-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="73802-131">Utilisation des contrôles ToolBar</span><span class="sxs-lookup"><span data-stu-id="73802-131">Using Toolbar Controls</span></span>](using-toolbar-controls.md)
</dt> <dt>

<span data-ttu-id="73802-132">[Démonstration des contrôles communs Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="73802-132">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 




