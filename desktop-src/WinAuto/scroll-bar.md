---
title: Barre de défilement (référence des éléments d’interface utilisateur MSAA)
description: Les barres de défilement permettent à un utilisateur de choisir la direction et la distance pour faire défiler les informations dans une fenêtre ou une zone de liste associée. Le nom de la classe de fenêtre pour une barre de défilement est \ 0034 ; BARRE DE DÉFILEMENT \ 0034 ;.
ms.assetid: a4ec1708-d751-4526-bd69-9796c43872a0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df381e0d532991f164f2c17d0a261dd3c5006619
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031801"
---
# <a name="scroll-bar-msaa-ui-element-reference"></a><span data-ttu-id="41e23-104">Barre de défilement (référence des éléments d’interface utilisateur MSAA)</span><span class="sxs-lookup"><span data-stu-id="41e23-104">Scroll Bar (MSAA UI Element Reference)</span></span>

> [!Note]  
> <span data-ttu-id="41e23-105">Cette rubrique décrit les objets de **barre de défilement** à des fins de référence des éléments d’interface utilisateur MSAA.</span><span class="sxs-lookup"><span data-stu-id="41e23-105">This topic describes **Scroll Bar** objects for purposes of MSAA UI Element Reference.</span></span> <span data-ttu-id="41e23-106">La création d’objets de **barre de défilement** dans différentes infrastructures d’interface utilisateur n’est pas décrite ici.</span><span class="sxs-lookup"><span data-stu-id="41e23-106">How to create **Scroll Bar** objects in various UI frameworks is not described here.</span></span> <span data-ttu-id="41e23-107">Consultez la documentation de référence sur les API pour l’infrastructure d’interface utilisateur que vous utilisez.</span><span class="sxs-lookup"><span data-stu-id="41e23-107">See the API reference documentation for the UI framework you're using.</span></span>

 

<span data-ttu-id="41e23-108">Les barres de défilement permettent à un utilisateur de choisir la direction et la distance pour faire défiler les informations dans une fenêtre ou une zone de liste associée.</span><span class="sxs-lookup"><span data-stu-id="41e23-108">Scroll bars let a user choose the direction and distance to scroll through information in a related window or list box.</span></span> <span data-ttu-id="41e23-109">Le nom de la classe de fenêtre d’une barre de défilement est « SCROLLBAR ».</span><span class="sxs-lookup"><span data-stu-id="41e23-109">The window class name for a scroll bar is "SCROLLBAR".</span></span>

<span data-ttu-id="41e23-110">Le contenu des propriétés [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) varie selon que la barre de défilement est verticale ou horizontale et sur laquelle des parties suivantes de la barre de défilement sont interrogées par le client :</span><span class="sxs-lookup"><span data-stu-id="41e23-110">The contents of the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties depends on whether the scroll bar is vertical or horizontal and on which of the following parts of the scroll bar is being queried by the client:</span></span>

-   <span data-ttu-id="41e23-111">Barre de défilement elle-même</span><span class="sxs-lookup"><span data-stu-id="41e23-111">The scroll bar itself</span></span>
-   <span data-ttu-id="41e23-112">Bouton flèche haut ou droite</span><span class="sxs-lookup"><span data-stu-id="41e23-112">The top or right arrow button</span></span>
-   <span data-ttu-id="41e23-113">Bouton de flèche bas ou gauche</span><span class="sxs-lookup"><span data-stu-id="41e23-113">The bottom or left arrow button</span></span>
-   <span data-ttu-id="41e23-114">La case de défilement (Thumb)</span><span class="sxs-lookup"><span data-stu-id="41e23-114">The scroll box (thumb)</span></span>
-   <span data-ttu-id="41e23-115">La page précédente ou la région de la page droite</span><span class="sxs-lookup"><span data-stu-id="41e23-115">The page up or page right region</span></span>
-   <span data-ttu-id="41e23-116">La page suivante ou la zone de page de gauche</span><span class="sxs-lookup"><span data-stu-id="41e23-116">The page down or page left region</span></span>

## <a name="iaccessible-methods"></a><span data-ttu-id="41e23-117">Méthodes IAccessible</span><span class="sxs-lookup"><span data-stu-id="41e23-117">IAccessible Methods</span></span>

<span data-ttu-id="41e23-118">Une barre de défilement prend en charge les méthodes [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) suivantes :</span><span class="sxs-lookup"><span data-stu-id="41e23-118">A scroll bar supports the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) methods:</span></span>

-   <span data-ttu-id="41e23-119">[**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction): l’objet de barre de défilement lui-même et le curseur de défilement ne prennent pas en charge la méthode **accDoDefaultAction** .</span><span class="sxs-lookup"><span data-stu-id="41e23-119">[**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction)—The scroll bar object itself and the scroll thumb do not support the **accDoDefaultAction** method.</span></span>

    <span data-ttu-id="41e23-120">Pour les autres parties de la barre de défilement sur une barre de défilement verticale, [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) appelle [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) avec le message [**WM \_ VSCROLL**](/windows/desktop/Controls/wm-vscroll) avec *wParam* défini sur les valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="41e23-120">For the other scroll bar parts on a vertical scroll bar, [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) calls [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) with the [**WM\_VSCROLL**](/windows/desktop/Controls/wm-vscroll) message with *wParam* set to the following values.</span></span>

    

    | <span data-ttu-id="41e23-121">Bouton/région</span><span class="sxs-lookup"><span data-stu-id="41e23-121">Button/Region</span></span>       | <span data-ttu-id="41e23-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="41e23-122">Vaule</span></span>        |
    |---------------------|--------------|
    | <span data-ttu-id="41e23-123">Bouton de flèche haut</span><span class="sxs-lookup"><span data-stu-id="41e23-123">Top arrow button</span></span>    | <span data-ttu-id="41e23-124">\_gamme SB</span><span class="sxs-lookup"><span data-stu-id="41e23-124">SB\_LINEUP</span></span>   |
    | <span data-ttu-id="41e23-125">Bouton de flèche bas</span><span class="sxs-lookup"><span data-stu-id="41e23-125">Bottom arrow button</span></span> | <span data-ttu-id="41e23-126">SB \_ LINEDOWN</span><span class="sxs-lookup"><span data-stu-id="41e23-126">SB\_LINEDOWN</span></span> |
    | <span data-ttu-id="41e23-127">Zone de page précédente</span><span class="sxs-lookup"><span data-stu-id="41e23-127">Page up region</span></span>      | <span data-ttu-id="41e23-128">SB \_ PG PRÉC</span><span class="sxs-lookup"><span data-stu-id="41e23-128">SB\_PAGEUP</span></span>   |
    | <span data-ttu-id="41e23-129">Zone de page suivante</span><span class="sxs-lookup"><span data-stu-id="41e23-129">Page down region</span></span>    | <span data-ttu-id="41e23-130">SB \_ PG.</span><span class="sxs-lookup"><span data-stu-id="41e23-130">SB\_PAGEDOWN</span></span> |

    

     

    <span data-ttu-id="41e23-131">Pour les autres parties de la barre de défilement sur une barre de défilement horizontale, [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) appelle [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) avec le message [**WM \_ HSCROLL**](/windows/desktop/Controls/wm-hscroll) avec *wParam* défini sur les valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="41e23-131">For the other scroll bar parts on a horizontal scroll bar, [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) calls [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) with the [**WM\_HSCROLL**](/windows/desktop/Controls/wm-hscroll) message with *wParam* set to the following values.</span></span>

    

    | <span data-ttu-id="41e23-132">Bouton/région</span><span class="sxs-lookup"><span data-stu-id="41e23-132">Button/Region</span></span>      | <span data-ttu-id="41e23-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="41e23-133">Value</span></span>         |
    |--------------------|---------------|
    | <span data-ttu-id="41e23-134">Bouton de direction gauche</span><span class="sxs-lookup"><span data-stu-id="41e23-134">Left arrow button</span></span>  | <span data-ttu-id="41e23-135">\_LINELEFT SB</span><span class="sxs-lookup"><span data-stu-id="41e23-135">SB\_LINELEFT</span></span>  |
    | <span data-ttu-id="41e23-136">Bouton flèche droite</span><span class="sxs-lookup"><span data-stu-id="41e23-136">Right arrow button</span></span> | <span data-ttu-id="41e23-137">\_LINERIGHT SB</span><span class="sxs-lookup"><span data-stu-id="41e23-137">SB\_LINERIGHT</span></span> |
    | <span data-ttu-id="41e23-138">Zone de gauche de la page</span><span class="sxs-lookup"><span data-stu-id="41e23-138">Page left region</span></span>   | <span data-ttu-id="41e23-139">\_PAGELEFT SB</span><span class="sxs-lookup"><span data-stu-id="41e23-139">SB\_PAGELEFT</span></span>  |
    | <span data-ttu-id="41e23-140">Région de droite de la page</span><span class="sxs-lookup"><span data-stu-id="41e23-140">Page right region</span></span>  | <span data-ttu-id="41e23-141">\_ÉPINGLÉE SB</span><span class="sxs-lookup"><span data-stu-id="41e23-141">SB\_PAGERIGHT</span></span> |

    

     

-   [<span data-ttu-id="41e23-142">**accHitTest**</span><span class="sxs-lookup"><span data-stu-id="41e23-142">**accHitTest**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [<span data-ttu-id="41e23-143">**accLocation**</span><span class="sxs-lookup"><span data-stu-id="41e23-143">**accLocation**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [<span data-ttu-id="41e23-144">**accNavigate**</span><span class="sxs-lookup"><span data-stu-id="41e23-144">**accNavigate**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)

## <a name="iaccessible-properties"></a><span data-ttu-id="41e23-145">Propriétés IAccessible</span><span class="sxs-lookup"><span data-stu-id="41e23-145">IAccessible Properties</span></span>

<span data-ttu-id="41e23-146">Une barre de défilement prend en charge les propriétés [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) suivantes :</span><span class="sxs-lookup"><span data-stu-id="41e23-146">A scroll bar supports the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties:</span></span>

-   <span data-ttu-id="41e23-147">[**obtenir \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount): la propriété **ChildCount** de l’objet de barre de défilement est cinq.</span><span class="sxs-lookup"><span data-stu-id="41e23-147">[**get\_accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)—The **ChildCount** property for the scroll bar object is five.</span></span> <span data-ttu-id="41e23-148">Pour les autres parties de la barre de défilement, la propriété **ChildCount** est égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="41e23-148">For the other scroll bar parts, the **ChildCount** property is zero.</span></span>
-   <span data-ttu-id="41e23-149">[**Obtient \_ accDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction): l’objet de barre de défilement lui-même et le curseur de défilement ne prennent pas en charge la propriété **DefaultAction** .</span><span class="sxs-lookup"><span data-stu-id="41e23-149">[**get\_accDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction)—The scroll bar object itself and the scroll thumb do not support the **DefaultAction** property.</span></span> <span data-ttu-id="41e23-150">La propriété **DefaultAction** pour les boutons fléchés et les zones ombrées de chaque côté du curseur de défilement est « Press ».</span><span class="sxs-lookup"><span data-stu-id="41e23-150">The **DefaultAction** property for the arrow buttons and the shaded areas on either side of the scroll thumb is "Press".</span></span>
-   <span data-ttu-id="41e23-151">[**Obtient \_ accDescription**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdescription)— la propriété **Description** dépend de la partie de la barre de défilement qui est interrogée.</span><span class="sxs-lookup"><span data-stu-id="41e23-151">[**get\_accDescription**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdescription)—The **Description** property depends on the part of the scroll bar that is queried.</span></span>

    <span data-ttu-id="41e23-152">Les parties d’une barre de défilement verticale présentent les descriptions suivantes.</span><span class="sxs-lookup"><span data-stu-id="41e23-152">The parts of a vertical scroll bar have the following descriptions.</span></span>

    

    | <span data-ttu-id="41e23-153">Partie</span><span class="sxs-lookup"><span data-stu-id="41e23-153">Part</span></span>                | <span data-ttu-id="41e23-154">Description</span><span class="sxs-lookup"><span data-stu-id="41e23-154">Description</span></span>                                                                         |
    |---------------------|-------------------------------------------------------------------------------------|
    | <span data-ttu-id="41e23-155">Barre de défilement elle-même</span><span class="sxs-lookup"><span data-stu-id="41e23-155">Scroll bar itself</span></span>   | <span data-ttu-id="41e23-156">« Utilisé pour modifier la zone d’affichage verticale »</span><span class="sxs-lookup"><span data-stu-id="41e23-156">"Used to change the vertical viewing area"</span></span>                                          |
    | <span data-ttu-id="41e23-157">Bouton de flèche haut</span><span class="sxs-lookup"><span data-stu-id="41e23-157">Top arrow button</span></span>    | <span data-ttu-id="41e23-158">"Déplace la position verticale d’une ligne vers le haut"</span><span class="sxs-lookup"><span data-stu-id="41e23-158">"Moves the vertical position up one line"</span></span>                                           |
    | <span data-ttu-id="41e23-159">Bouton de flèche bas</span><span class="sxs-lookup"><span data-stu-id="41e23-159">Bottom arrow button</span></span> | <span data-ttu-id="41e23-160">« Déplace la position verticale d’une ligne vers le dessous »</span><span class="sxs-lookup"><span data-stu-id="41e23-160">"Moves the vertical position down one line"</span></span>                                         |
    | <span data-ttu-id="41e23-161">Défilement de curseur</span><span class="sxs-lookup"><span data-stu-id="41e23-161">Scroll thumb</span></span>        | <span data-ttu-id="41e23-162">« Indique la position verticale actuelle et peut être glissée pour la modifier directement »</span><span class="sxs-lookup"><span data-stu-id="41e23-162">"Indicates the current vertical position, and can be dragged to change it directly"</span></span> |
    | <span data-ttu-id="41e23-163">Zone de page précédente</span><span class="sxs-lookup"><span data-stu-id="41e23-163">Page up region</span></span>      | <span data-ttu-id="41e23-164">"Déplace la position verticale de quelques lignes"</span><span class="sxs-lookup"><span data-stu-id="41e23-164">"Moves the vertical position up a couple of lines"</span></span>                                  |
    | <span data-ttu-id="41e23-165">Zone de page suivante</span><span class="sxs-lookup"><span data-stu-id="41e23-165">Page down region</span></span>    | <span data-ttu-id="41e23-166">« Indique la position verticale actuelle et peut être glissée pour la modifier directement »</span><span class="sxs-lookup"><span data-stu-id="41e23-166">"Indicates the current vertical position, and can be dragged to change it directly"</span></span> |

    

     

    <span data-ttu-id="41e23-167">Les parties d’une barre de défilement horizontale ont les descriptions suivantes.</span><span class="sxs-lookup"><span data-stu-id="41e23-167">The parts of a horizontal scroll bar have the following descriptions.</span></span>

    

    | <span data-ttu-id="41e23-168">Partie</span><span class="sxs-lookup"><span data-stu-id="41e23-168">Part</span></span>               | <span data-ttu-id="41e23-169">Description</span><span class="sxs-lookup"><span data-stu-id="41e23-169">Description</span></span>                                                                           |
    |--------------------|---------------------------------------------------------------------------------------|
    | <span data-ttu-id="41e23-170">Barre de défilement elle-même</span><span class="sxs-lookup"><span data-stu-id="41e23-170">Scroll bar itself</span></span>  | <span data-ttu-id="41e23-171">« Utilisé pour modifier la zone d’affichage horizontale »</span><span class="sxs-lookup"><span data-stu-id="41e23-171">"Used to change the horizontal viewing area"</span></span>                                          |
    | <span data-ttu-id="41e23-172">Bouton de direction gauche</span><span class="sxs-lookup"><span data-stu-id="41e23-172">Left arrow button</span></span>  | <span data-ttu-id="41e23-173">« Déplace la position horizontale d’une colonne vers la gauche »</span><span class="sxs-lookup"><span data-stu-id="41e23-173">"Moves the horizontal position left one column"</span></span>                                       |
    | <span data-ttu-id="41e23-174">Bouton flèche droite</span><span class="sxs-lookup"><span data-stu-id="41e23-174">Right arrow button</span></span> | <span data-ttu-id="41e23-175">'Déplace la position horizontale d’une colonne vers la droite "</span><span class="sxs-lookup"><span data-stu-id="41e23-175">'Moves the horizontal position right one column"</span></span>                                      |
    | <span data-ttu-id="41e23-176">Défilement de curseur</span><span class="sxs-lookup"><span data-stu-id="41e23-176">Scroll thumb</span></span>       | <span data-ttu-id="41e23-177">« Indique la position horizontale actuelle et peut être glissée pour la modifier directement »</span><span class="sxs-lookup"><span data-stu-id="41e23-177">"Indicates the current horizontal position, and can be dragged to change it directly"</span></span> |
    | <span data-ttu-id="41e23-178">Zone de gauche de la page</span><span class="sxs-lookup"><span data-stu-id="41e23-178">Page left region</span></span>   | <span data-ttu-id="41e23-179">"Déplace la position horizontale de deux colonnes"</span><span class="sxs-lookup"><span data-stu-id="41e23-179">"Moves the horizontal position left a couple of columns"</span></span>                              |
    | <span data-ttu-id="41e23-180">Région de droite de la page</span><span class="sxs-lookup"><span data-stu-id="41e23-180">Page right region</span></span>  | <span data-ttu-id="41e23-181">« Indique la position verticale actuelle et peut être glissée pour la modifier directement »</span><span class="sxs-lookup"><span data-stu-id="41e23-181">"Indicates the current vertical position, and can be dragged to change it directly"</span></span>   |

    

     

-   [<span data-ttu-id="41e23-182">**Obtient \_ accHelp**</span><span class="sxs-lookup"><span data-stu-id="41e23-182">**get\_accHelp**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelp)
-   [<span data-ttu-id="41e23-183">**Obtient \_ accHelpTopic**</span><span class="sxs-lookup"><span data-stu-id="41e23-183">**get\_accHelpTopic**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelptopic)
-   <span data-ttu-id="41e23-184">[**Obtient \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname): la propriété **Name** dépend de la partie de la barre de défilement qui est interrogée.</span><span class="sxs-lookup"><span data-stu-id="41e23-184">[**get\_accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)—The **Name** property depends on the part of the scroll bar that is queried.</span></span>

    <span data-ttu-id="41e23-185">Les parties d’une barre de défilement verticale portent les noms suivants.</span><span class="sxs-lookup"><span data-stu-id="41e23-185">The parts of a vertical scroll bar have the following names.</span></span>

    | <span data-ttu-id="41e23-186">Partie</span><span class="sxs-lookup"><span data-stu-id="41e23-186">Part</span></span>                | <span data-ttu-id="41e23-187">Nom</span><span class="sxs-lookup"><span data-stu-id="41e23-187">Name</span></span>        |
    |---------------------|-------------|
    | <span data-ttu-id="41e23-188">Fenêtre barre de défilement</span><span class="sxs-lookup"><span data-stu-id="41e23-188">Scroll bar window</span></span>   | <span data-ttu-id="41e23-189">Barr</span><span class="sxs-lookup"><span data-stu-id="41e23-189">"Vertical"</span></span>  |
    | <span data-ttu-id="41e23-190">Bouton de flèche haut</span><span class="sxs-lookup"><span data-stu-id="41e23-190">Top arrow button</span></span>    | <span data-ttu-id="41e23-191">« Aligner vers le haut »</span><span class="sxs-lookup"><span data-stu-id="41e23-191">"Line up"</span></span>   |
    | <span data-ttu-id="41e23-192">Bouton de flèche bas</span><span class="sxs-lookup"><span data-stu-id="41e23-192">Bottom arrow button</span></span> | <span data-ttu-id="41e23-193">« Ligne inférieure »</span><span class="sxs-lookup"><span data-stu-id="41e23-193">"Line down"</span></span> |
    | <span data-ttu-id="41e23-194">Défilement de curseur</span><span class="sxs-lookup"><span data-stu-id="41e23-194">Scroll thumb</span></span>        | <span data-ttu-id="41e23-195">Endroit</span><span class="sxs-lookup"><span data-stu-id="41e23-195">"Position"</span></span>  |
    | <span data-ttu-id="41e23-196">Zone de page précédente</span><span class="sxs-lookup"><span data-stu-id="41e23-196">Page up region</span></span>      | <span data-ttu-id="41e23-197">« Page précédente »</span><span class="sxs-lookup"><span data-stu-id="41e23-197">"Page up"</span></span>   |
    | <span data-ttu-id="41e23-198">Zone de page suivante</span><span class="sxs-lookup"><span data-stu-id="41e23-198">Page down region</span></span>    | <span data-ttu-id="41e23-199">« Page suivante »</span><span class="sxs-lookup"><span data-stu-id="41e23-199">"Page down"</span></span> |

    

     

    <span data-ttu-id="41e23-200">Les parties d’une barre de défilement horizontale portent les noms suivants.</span><span class="sxs-lookup"><span data-stu-id="41e23-200">The parts of a horizontal scroll bar have the following names.</span></span>

    

    | <span data-ttu-id="41e23-201">Partie</span><span class="sxs-lookup"><span data-stu-id="41e23-201">Part</span></span>               | <span data-ttu-id="41e23-202">Nom</span><span class="sxs-lookup"><span data-stu-id="41e23-202">Name</span></span>           |
    |--------------------|----------------|
    | <span data-ttu-id="41e23-203">Fenêtre barre de défilement</span><span class="sxs-lookup"><span data-stu-id="41e23-203">Scroll bar window</span></span>  | <span data-ttu-id="41e23-204">Horizontal</span><span class="sxs-lookup"><span data-stu-id="41e23-204">"Horizontal"</span></span>   |
    | <span data-ttu-id="41e23-205">Bouton de direction gauche</span><span class="sxs-lookup"><span data-stu-id="41e23-205">Left arrow button</span></span>  | <span data-ttu-id="41e23-206">« Colonne à gauche »</span><span class="sxs-lookup"><span data-stu-id="41e23-206">"Column left"</span></span>  |
    | <span data-ttu-id="41e23-207">Bouton flèche droite</span><span class="sxs-lookup"><span data-stu-id="41e23-207">Right arrow button</span></span> | <span data-ttu-id="41e23-208">« Colonne à droite »</span><span class="sxs-lookup"><span data-stu-id="41e23-208">"Column right"</span></span> |
    | <span data-ttu-id="41e23-209">Défilement de curseur</span><span class="sxs-lookup"><span data-stu-id="41e23-209">Scroll thumb</span></span>       | <span data-ttu-id="41e23-210">Endroit</span><span class="sxs-lookup"><span data-stu-id="41e23-210">"Position"</span></span>     |
    | <span data-ttu-id="41e23-211">Région de droite de la page</span><span class="sxs-lookup"><span data-stu-id="41e23-211">Page right region</span></span>  | <span data-ttu-id="41e23-212">« Page droite »</span><span class="sxs-lookup"><span data-stu-id="41e23-212">"Page right"</span></span>   |
    | <span data-ttu-id="41e23-213">Zone de gauche de la page</span><span class="sxs-lookup"><span data-stu-id="41e23-213">Page left region</span></span>   | <span data-ttu-id="41e23-214">« Page gauche »</span><span class="sxs-lookup"><span data-stu-id="41e23-214">"Page left"</span></span>    |

    

     

-   <span data-ttu-id="41e23-215">[**Obtient \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)— la propriété **parente** des boutons fléchés, le curseur de défilement et la zone ombrée de chaque côté du curseur sont la fenêtre de la barre de défilement.</span><span class="sxs-lookup"><span data-stu-id="41e23-215">[**get\_accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)—The **Parent** property of the arrow buttons, scroll thumb, and the shaded area on either side of the thumb is the scroll bar window.</span></span> <span data-ttu-id="41e23-216">La propriété **parent** de la fenêtre de la barre de défilement est une fenêtre ( \_ fenêtre système de rôle \_ ) qui entoure le contrôle et qui a les mêmes nom de propriété de **nom** et de classe de fenêtre.</span><span class="sxs-lookup"><span data-stu-id="41e23-216">The **Parent** property of the scroll bar window is a window (ROLE\_SYSTEM\_WINDOW) that surrounds the control and has the same **Name** property and window class name.</span></span>
-   <span data-ttu-id="41e23-217">[**Obtient \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole): la propriété **role** dépend de la partie de la barre de défilement qui est interrogée.</span><span class="sxs-lookup"><span data-stu-id="41e23-217">[**get\_accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)—The **Role** property depends on the part of the scroll bar that is queried.</span></span> <span data-ttu-id="41e23-218">Les parties d’une barre de défilement ont les rôles suivants.</span><span class="sxs-lookup"><span data-stu-id="41e23-218">The parts of a scroll bar have the following roles.</span></span> 

    | <span data-ttu-id="41e23-219">Partie</span><span class="sxs-lookup"><span data-stu-id="41e23-219">Part</span></span>                                                  | <span data-ttu-id="41e23-220">Role</span><span class="sxs-lookup"><span data-stu-id="41e23-220">Role</span></span>                                                                    |
    |-------------------------------------------------------|-------------------------------------------------------------------------|
    | <span data-ttu-id="41e23-221">Barre de défilement elle-même</span><span class="sxs-lookup"><span data-stu-id="41e23-221">Scroll bar itself</span></span>                                     | [<span data-ttu-id="41e23-222">**\_ScrollBar système de rôle \_**</span><span class="sxs-lookup"><span data-stu-id="41e23-222">**ROLE\_SYSTEM\_SCROLLBAR**</span></span>](object-roles.md)   |
    | <span data-ttu-id="41e23-223">Boutons haut, bas, gauche et flèche droite</span><span class="sxs-lookup"><span data-stu-id="41e23-223">Top, down, left, and right arrow buttons</span></span>              | [<span data-ttu-id="41e23-224">**\_PUSHBUTTON système de rôle \_**</span><span class="sxs-lookup"><span data-stu-id="41e23-224">**ROLE\_SYSTEM\_PUSHBUTTON**</span></span>](object-roles.md) |
    | <span data-ttu-id="41e23-225">Défilement de curseur</span><span class="sxs-lookup"><span data-stu-id="41e23-225">Scroll thumb</span></span>                                          | [<span data-ttu-id="41e23-226">**\_indicateur de système de rôle \_**</span><span class="sxs-lookup"><span data-stu-id="41e23-226">**ROLE\_SYSTEM\_INDICATOR**</span></span>](object-roles.md)   |
    | <span data-ttu-id="41e23-227">Zones de page précédente, page suivante, page de gauche et page de droite</span><span class="sxs-lookup"><span data-stu-id="41e23-227">Page up, page down, page left, and page right regions</span></span> | [<span data-ttu-id="41e23-228">**\_PUSHBUTTON système de rôle \_**</span><span class="sxs-lookup"><span data-stu-id="41e23-228">**ROLE\_SYSTEM\_PUSHBUTTON**</span></span>](object-roles.md) |

    

     

-   <span data-ttu-id="41e23-229">[**obtenir \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate): la propriété **State** de chaque composant de barre de défilement comprend une combinaison des [valeurs](object-state-constants.md)suivantes.</span><span class="sxs-lookup"><span data-stu-id="41e23-229">[**get\_accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)—The **State** property of each scroll bar component includes a combination of the following [values](object-state-constants.md).</span></span>

    | <span data-ttu-id="41e23-230">State</span><span class="sxs-lookup"><span data-stu-id="41e23-230">State</span></span>                                                                                 | <span data-ttu-id="41e23-231">Valeur</span><span class="sxs-lookup"><span data-stu-id="41e23-231">Value</span></span>                                                                                                                                                                                                                       |
    |---------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | [<span data-ttu-id="41e23-232">**système d’état \_ \_ invisible**</span><span class="sxs-lookup"><span data-stu-id="41e23-232">**STATE\_SYSTEM\_INVISIBLE**</span></span>](object-state-constants.md)     | <span data-ttu-id="41e23-233">Pour la barre de défilement elle-même, cela indique que la barre de défilement verticale ou horizontale spécifiée n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="41e23-233">For the scroll bar itself, this indicates the specified vertical or horizontal scroll bar does not exist.</span></span> <span data-ttu-id="41e23-234">Pour les zones page précédente ou page suivante, cela indique que le curseur est positionné de telle sorte que la région n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="41e23-234">For the page up or page down regions, this indicates the thumb is positioned such that the region does not exist.</span></span> |
    | [<span data-ttu-id="41e23-235">**système d’état \_ \_ hors écran**</span><span class="sxs-lookup"><span data-stu-id="41e23-235">**STATE\_SYSTEM\_OFFSCREEN**</span></span>](object-state-constants.md)     | <span data-ttu-id="41e23-236">Pour la barre de défilement elle-même, cela indique que la fenêtre est dimensionnée de telle sorte que la barre de défilement verticale ou horizontale spécifiée ne soit pas actuellement affichée.</span><span class="sxs-lookup"><span data-stu-id="41e23-236">For the scroll bar itself, this indicates the window is sized such that the specified vertical or horizontal scroll bar is not currently displayed.</span></span>                                                                         |
    | [<span data-ttu-id="41e23-237">**système d’état \_ \_ enfoncé**</span><span class="sxs-lookup"><span data-stu-id="41e23-237">**STATE\_SYSTEM\_PRESSED**</span></span>](object-state-constants.md)         | <span data-ttu-id="41e23-238">Le bouton fléché ou la région de page est enfoncé.</span><span class="sxs-lookup"><span data-stu-id="41e23-238">The arrow button or page region is pressed.</span></span>                                                                                                                                                                                 |
    | [<span data-ttu-id="41e23-239">**système d’état \_ \_ non disponible**</span><span class="sxs-lookup"><span data-stu-id="41e23-239">**STATE\_SYSTEM\_UNAVAILABLE**</span></span>](object-state-constants.md) | <span data-ttu-id="41e23-240">Le composant est désactivé.</span><span class="sxs-lookup"><span data-stu-id="41e23-240">The component is disabled.</span></span>                                                                                                                                                                                                  |

    

     

-   <span data-ttu-id="41e23-241">[**obtenir \_ accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue): la propriété **valeur** de la fenêtre barre de défilement indique la position de la barre de défilement et est une chaîne qui contient un entier compris entre « 0 » et « 100 ».</span><span class="sxs-lookup"><span data-stu-id="41e23-241">[**get\_accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue)—The **Value** property for the scroll bar window indicates the scroll bar position and is a string that contains an integer from "0" through "100".</span></span>

## <a name="related-topics"></a><span data-ttu-id="41e23-242">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="41e23-242">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="41e23-243">IAccessible, interface</span><span class="sxs-lookup"><span data-stu-id="41e23-243">IAccessible Interface</span></span>](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 