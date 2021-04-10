---
title: Slider, contrôle (référence des éléments d’interface utilisateur MSAA)
description: Un contrôle Slider, également appelé contrôle TrackBar, permet à un utilisateur de sélectionner une plage de valeurs en déplaçant un curseur. Les contrôles de volume dans le système d'exploitation Windows sont des contrôles Slider.
ms.assetid: 8df4ed1d-d63c-49d7-94f1-df2113643484
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b03c39d6638557b9dfff90740132d3e22a7e2511
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029782"
---
# <a name="slider-control-msaa-ui-element-reference"></a><span data-ttu-id="1a80a-104">Slider, contrôle (référence des éléments d’interface utilisateur MSAA)</span><span class="sxs-lookup"><span data-stu-id="1a80a-104">Slider Control (MSAA UI Element Reference)</span></span>

> [!Note]  
> <span data-ttu-id="1a80a-105">Cette rubrique décrit les objets de **contrôle Slider** à des fins de référence des éléments d’interface utilisateur MSAA.</span><span class="sxs-lookup"><span data-stu-id="1a80a-105">This topic describes **Slider Control** objects for purposes of MSAA UI Element Reference.</span></span> <span data-ttu-id="1a80a-106">La création d’objets de **contrôle Slider** dans différentes infrastructures d’interface utilisateur n’est pas décrite ici.</span><span class="sxs-lookup"><span data-stu-id="1a80a-106">How to create **Slider Control** objects in various UI frameworks is not described here.</span></span> <span data-ttu-id="1a80a-107">Consultez la documentation de référence sur les API pour l’infrastructure d’interface utilisateur que vous utilisez.</span><span class="sxs-lookup"><span data-stu-id="1a80a-107">See the API reference documentation for the UI framework you're using.</span></span>

 

<span data-ttu-id="1a80a-108">Un contrôle Slider, également appelé contrôle TrackBar, permet à un utilisateur de sélectionner une plage de valeurs en déplaçant un curseur.</span><span class="sxs-lookup"><span data-stu-id="1a80a-108">A slider control, also called a trackbar control, lets a user select from a range of values by moving a slider.</span></span> <span data-ttu-id="1a80a-109">Les contrôles de volume dans le système d'exploitation Windows sont des contrôles Slider.</span><span class="sxs-lookup"><span data-stu-id="1a80a-109">The volume controls in the Windows operating system are slider controls.</span></span>

<span data-ttu-id="1a80a-110">Le nom de la classe de fenêtre pour un contrôle Slider est la \_ classe TrackBar, qui est définie comme « msctls \_ TrackBar » dans commctrl. h.</span><span class="sxs-lookup"><span data-stu-id="1a80a-110">The window class name for a slider control is TRACKBAR\_CLASS, which is defined as "msctls\_trackbar" in Commctrl.h.</span></span>

<span data-ttu-id="1a80a-111">Le contenu des propriétés [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) varie selon que le curseur est vertical ou horizontal et sur lequel des parties suivantes du contrôle Slider sont interrogées par le client :</span><span class="sxs-lookup"><span data-stu-id="1a80a-111">The contents of the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties depend on whether the slider is vertical or horizontal and on which of the following parts of the slider control is queried by the client:</span></span>

-   <span data-ttu-id="1a80a-112">Fenêtre curseur</span><span class="sxs-lookup"><span data-stu-id="1a80a-112">Slider window</span></span>
-   <span data-ttu-id="1a80a-113">Curseur curseur</span><span class="sxs-lookup"><span data-stu-id="1a80a-113">Slider thumb</span></span>
-   <span data-ttu-id="1a80a-114">Zone grise au-dessus (ou à</span><span class="sxs-lookup"><span data-stu-id="1a80a-114">Shaded area above (or to</span></span>
-   <span data-ttu-id="1a80a-115">Zone ombrée en dessous (ou à droite de) curseur de défilement</span><span class="sxs-lookup"><span data-stu-id="1a80a-115">Shaded area below (or to the right of) the slider thumb</span></span>

## <a name="iaccessible-methods"></a><span data-ttu-id="1a80a-116">Méthodes IAccessible</span><span class="sxs-lookup"><span data-stu-id="1a80a-116">IAccessible Methods</span></span>

<span data-ttu-id="1a80a-117">Un contrôle Slider prend en charge les méthodes [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) suivantes :</span><span class="sxs-lookup"><span data-stu-id="1a80a-117">A slider control supports the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) methods:</span></span>

-   [<span data-ttu-id="1a80a-118">**accHitTest**</span><span class="sxs-lookup"><span data-stu-id="1a80a-118">**accHitTest**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [<span data-ttu-id="1a80a-119">**accLocation**</span><span class="sxs-lookup"><span data-stu-id="1a80a-119">**accLocation**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [<span data-ttu-id="1a80a-120">**accNavigate**</span><span class="sxs-lookup"><span data-stu-id="1a80a-120">**accNavigate**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [<span data-ttu-id="1a80a-121">**accSelect**</span><span class="sxs-lookup"><span data-stu-id="1a80a-121">**accSelect**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a><span data-ttu-id="1a80a-122">Propriétés IAccessible</span><span class="sxs-lookup"><span data-stu-id="1a80a-122">IAccessible Properties</span></span>

<span data-ttu-id="1a80a-123">Un contrôle Slider prend en charge les propriétés [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) suivantes :</span><span class="sxs-lookup"><span data-stu-id="1a80a-123">A slider control supports the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties:</span></span>

-   [<span data-ttu-id="1a80a-124">**Obtient \_ accChild**</span><span class="sxs-lookup"><span data-stu-id="1a80a-124">**get\_accChild**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild)
-   [<span data-ttu-id="1a80a-125">**Obtient \_ accChildCount**</span><span class="sxs-lookup"><span data-stu-id="1a80a-125">**get\_accChildCount**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)
-   [<span data-ttu-id="1a80a-126">**Obtient \_ accDescription**</span><span class="sxs-lookup"><span data-stu-id="1a80a-126">**get\_accDescription**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdescription)
-   [<span data-ttu-id="1a80a-127">**Obtient \_ accHelp**</span><span class="sxs-lookup"><span data-stu-id="1a80a-127">**get\_accHelp**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelp)
-   [<span data-ttu-id="1a80a-128">**Obtient \_ accHelpTopic**</span><span class="sxs-lookup"><span data-stu-id="1a80a-128">**get\_accHelpTopic**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelptopic)
-   <span data-ttu-id="1a80a-129">[**obtenir \_ accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut): la propriété **KeyboardShortcut** est la clé d’accès de la fenêtre du curseur, qui est un caractère souligné dans le texte de l’étiquette du curseur.</span><span class="sxs-lookup"><span data-stu-id="1a80a-129">[**get\_accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut)—The **KeyboardShortcut** property is the slider window's access key, which is an underlined character in the text of the label for the slider.</span></span> <span data-ttu-id="1a80a-130">La chaîne retournée contient le caractère clé d’accès ajouté à la chaîne « ALT + ».</span><span class="sxs-lookup"><span data-stu-id="1a80a-130">The returned string contains the access key character appended to the string "Alt+".</span></span>
-   <span data-ttu-id="1a80a-131">[**Obtient \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname): la propriété **Name** dépend de la partie du curseur interrogée.</span><span class="sxs-lookup"><span data-stu-id="1a80a-131">[**get\_accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)—The **Name** property depends on the part of the slider that is queried.</span></span>

    <span data-ttu-id="1a80a-132">Les parties d’un curseur vertical portent les noms suivants :</span><span class="sxs-lookup"><span data-stu-id="1a80a-132">The parts of a vertical slider have the following names:</span></span>

    

    | <span data-ttu-id="1a80a-133">Composant Slider</span><span class="sxs-lookup"><span data-stu-id="1a80a-133">Slider part</span></span>                    | <span data-ttu-id="1a80a-134">Nom</span><span class="sxs-lookup"><span data-stu-id="1a80a-134">Name</span></span>                                |
    |--------------------------------|-------------------------------------|
    | <span data-ttu-id="1a80a-135">Fenêtre curseur</span><span class="sxs-lookup"><span data-stu-id="1a80a-135">Slider window</span></span>                  | <span data-ttu-id="1a80a-136">Contrôle de texte statique utilisé comme étiquette</span><span class="sxs-lookup"><span data-stu-id="1a80a-136">Static text control used as a label</span></span> |
    | <span data-ttu-id="1a80a-137">Curseur curseur</span><span class="sxs-lookup"><span data-stu-id="1a80a-137">Slider thumb</span></span>                   | <span data-ttu-id="1a80a-138">Endroit</span><span class="sxs-lookup"><span data-stu-id="1a80a-138">"Position"</span></span>                          |
    | <span data-ttu-id="1a80a-139">Curseur de la zone ombrée au-dessus du curseur</span><span class="sxs-lookup"><span data-stu-id="1a80a-139">Shaded area above slider thumb</span></span> | <span data-ttu-id="1a80a-140">« Page précédente »</span><span class="sxs-lookup"><span data-stu-id="1a80a-140">"Page up"</span></span>                           |
    | <span data-ttu-id="1a80a-141">Zone ombrée en dessous du curseur de curseur</span><span class="sxs-lookup"><span data-stu-id="1a80a-141">Shaded area below slider thumb</span></span> | <span data-ttu-id="1a80a-142">« Page suivante »</span><span class="sxs-lookup"><span data-stu-id="1a80a-142">"Page down"</span></span>                         |

    

     

    <span data-ttu-id="1a80a-143">Les parties d’un curseur horizontal portent les noms suivants :</span><span class="sxs-lookup"><span data-stu-id="1a80a-143">The parts of a horizontal slider have the following names:</span></span>

    

    | <span data-ttu-id="1a80a-144">Composant Slider</span><span class="sxs-lookup"><span data-stu-id="1a80a-144">Slider part</span></span>                              | <span data-ttu-id="1a80a-145">Nom</span><span class="sxs-lookup"><span data-stu-id="1a80a-145">Name</span></span>                                |
    |------------------------------------------|-------------------------------------|
    | <span data-ttu-id="1a80a-146">Fenêtre curseur</span><span class="sxs-lookup"><span data-stu-id="1a80a-146">Slider window</span></span>                            | <span data-ttu-id="1a80a-147">Contrôle de texte statique utilisé comme étiquette</span><span class="sxs-lookup"><span data-stu-id="1a80a-147">Static text control used as a label</span></span> |
    | <span data-ttu-id="1a80a-148">Curseur curseur</span><span class="sxs-lookup"><span data-stu-id="1a80a-148">Slider thumb</span></span>                             | <span data-ttu-id="1a80a-149">Endroit</span><span class="sxs-lookup"><span data-stu-id="1a80a-149">"Position"</span></span>                          |
    | <span data-ttu-id="1a80a-150">Zone ombrée à gauche du curseur de curseur</span><span class="sxs-lookup"><span data-stu-id="1a80a-150">Shaded area to the left of slider thumb</span></span>  | <span data-ttu-id="1a80a-151">« Page gauche »</span><span class="sxs-lookup"><span data-stu-id="1a80a-151">"Page left"</span></span>                         |
    | <span data-ttu-id="1a80a-152">Zone ombrée à droite du curseur de curseur</span><span class="sxs-lookup"><span data-stu-id="1a80a-152">Shaded area to the right of slider thumb</span></span> | <span data-ttu-id="1a80a-153">« Page droite »</span><span class="sxs-lookup"><span data-stu-id="1a80a-153">"Page right"</span></span>                        |

    

     

-   <span data-ttu-id="1a80a-154">[**Obtient \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent): la propriété **parente** des boutons fléchés, Scroll Thumb et la zone ombrée de chaque côté du curseur de défilement est la fenêtre de curseur.</span><span class="sxs-lookup"><span data-stu-id="1a80a-154">[**get\_accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)—The **Parent** property of the arrow buttons, scroll thumb, and the shaded area on either side of the thumb is the slider window.</span></span> <span data-ttu-id="1a80a-155">La propriété **parent** de la fenêtre de curseur est une fenêtre ( [**\_ \_ fenêtre système de rôle**](object-roles.md) ) qui entoure le contrôle et qui a les mêmes nom de propriété de **nom** et de classe de fenêtre.</span><span class="sxs-lookup"><span data-stu-id="1a80a-155">The **Parent** property of the slider window is a window ( [**ROLE\_SYSTEM\_WINDOW**](object-roles.md) ) that surrounds the control and has the same **Name** property and window class name.</span></span>
-   <span data-ttu-id="1a80a-156">[**Obtient \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole): la propriété **role** dépend de la partie du curseur interrogée.</span><span class="sxs-lookup"><span data-stu-id="1a80a-156">[**get\_accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)—The **Role** property depends on the part of the slider that is queried.</span></span> 

    | <span data-ttu-id="1a80a-157">Composant Slider</span><span class="sxs-lookup"><span data-stu-id="1a80a-157">Slider part</span></span>                                     | [<span data-ttu-id="1a80a-158">Rôle</span><span class="sxs-lookup"><span data-stu-id="1a80a-158">Role</span></span>](object-roles.md)                                                |
    |-------------------------------------------------|-------------------------------------------------------------------------|
    | <span data-ttu-id="1a80a-159">Fenêtre curseur</span><span class="sxs-lookup"><span data-stu-id="1a80a-159">Slider window</span></span>                                   | [<span data-ttu-id="1a80a-160">**\_curseur système de rôle \_**</span><span class="sxs-lookup"><span data-stu-id="1a80a-160">**ROLE\_SYSTEM\_SLIDER**</span></span>](object-roles.md)         |
    | <span data-ttu-id="1a80a-161">Curseur curseur</span><span class="sxs-lookup"><span data-stu-id="1a80a-161">Slider thumb</span></span>                                    | [<span data-ttu-id="1a80a-162">**\_indicateur de système de rôle \_**</span><span class="sxs-lookup"><span data-stu-id="1a80a-162">**ROLE\_SYSTEM\_INDICATOR**</span></span>](object-roles.md)   |
    | <span data-ttu-id="1a80a-163">Zones ombrées de part et d’autre du curseur de curseur</span><span class="sxs-lookup"><span data-stu-id="1a80a-163">Shaded areas on either side of the slider thumb</span></span> | [<span data-ttu-id="1a80a-164">**\_PUSHBUTTON système de rôle \_**</span><span class="sxs-lookup"><span data-stu-id="1a80a-164">**ROLE\_SYSTEM\_PUSHBUTTON**</span></span>](object-roles.md) |

    

     

-   <span data-ttu-id="1a80a-165">[**obtenir \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate): les [valeurs](object-state-constants.md) de la propriété **State** dépendent de la partie du curseur interrogée.</span><span class="sxs-lookup"><span data-stu-id="1a80a-165">[**get\_accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)—[Values](object-state-constants.md) for the **State** property depend on the part of the slider that is queried.</span></span> 

    | <span data-ttu-id="1a80a-166">Composant Slider</span><span class="sxs-lookup"><span data-stu-id="1a80a-166">Slider Part</span></span>                                     | <span data-ttu-id="1a80a-167">Valeurs d’État possibles</span><span class="sxs-lookup"><span data-stu-id="1a80a-167">Possible state values</span></span>                                                                                                                                                                                                                                                                                                                                                                                                           |
    |-------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="1a80a-168">Fenêtre curseur</span><span class="sxs-lookup"><span data-stu-id="1a80a-168">Slider window</span></span>                                   | <span data-ttu-id="1a80a-169">[**État \_ système \_ d'**](object-state-constants.md) État indisponible système d’État indisponible système d’état \| [**\_ \_ non disponible**](object-state-constants.md) système d’état \| [**\_ \_ centré**](object-state-constants.md) \| [**\_ \_**](object-state-constants.md) \| [**\_ \_ normal**](object-state-constants.md)</span><span class="sxs-lookup"><span data-stu-id="1a80a-169">[**STATE\_SYSTEM\_INVISIBLE**](object-state-constants.md) \| [**STATE\_SYSTEM\_UNAVAILABLE**](object-state-constants.md) \| [**STATE\_SYSTEM\_FOCUSED**](object-state-constants.md) \| [**STATE\_SYSTEM\_FOCUSABLE**](object-state-constants.md) \| [**STATE\_SYSTEM\_NORMAL**](object-state-constants.md)</span></span> |
    | <span data-ttu-id="1a80a-170">Curseur curseur</span><span class="sxs-lookup"><span data-stu-id="1a80a-170">Slider thumb</span></span>                                    | <span data-ttu-id="1a80a-171">Zéro (0), ce qui signifie que l’objet est visible, ou le système d’état [**système état \_ \_**](object-state-constants.md) non disponible système d’état \| [**\_ \_ non disponible**](object-state-constants.md) \| [**\_ \_ normal**](object-state-constants.md)</span><span class="sxs-lookup"><span data-stu-id="1a80a-171">Zero (0), which means the object is visible, or [**STATE\_SYSTEM\_INVISIBLE**](object-state-constants.md) \| [**STATE\_SYSTEM\_UNAVAILABLE**](object-state-constants.md) \| [**STATE\_SYSTEM\_NORMAL**](object-state-constants.md)</span></span>                                                                                                                       |
    | <span data-ttu-id="1a80a-172">Zones ombrées de part et d’autre du curseur de curseur</span><span class="sxs-lookup"><span data-stu-id="1a80a-172">Shaded areas on either side of the slider thumb</span></span> | <span data-ttu-id="1a80a-173">Zéro (0), ce qui signifie que l’objet est visible, ou le système d’état [**système état \_ \_**](object-state-constants.md) non disponible système d’état \| [**\_ \_ non disponible**](object-state-constants.md) \| [**\_ \_ normal**](object-state-constants.md)</span><span class="sxs-lookup"><span data-stu-id="1a80a-173">Zero (0), which means the object is visible, or [**STATE\_SYSTEM\_INVISIBLE**](object-state-constants.md) \| [**STATE\_SYSTEM\_UNAVAILABLE**](object-state-constants.md) \| [**STATE\_SYSTEM\_NORMAL**](object-state-constants.md)</span></span>                                                                                                                       |

    

     

-   <span data-ttu-id="1a80a-174">[**obtenir \_ accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue): la propriété **value** de la fenêtre Slider indique la position du curseur et est une chaîne qui contient un entier compris entre « 0 » et « 100 ».</span><span class="sxs-lookup"><span data-stu-id="1a80a-174">[**get\_accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue)—The **Value** property for the slider window indicates the position of the thumb and is a string that contains an integer from "0" through "100".</span></span>

## <a name="related-topics"></a><span data-ttu-id="1a80a-175">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="1a80a-175">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1a80a-176">IAccessible, interface</span><span class="sxs-lookup"><span data-stu-id="1a80a-176">IAccessible Interface</span></span>](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> <dt>

[<span data-ttu-id="1a80a-177">**Barre de défilement**</span><span class="sxs-lookup"><span data-stu-id="1a80a-177">**Scroll Bar**</span></span>](scroll-bar.md)
</dt> </dl>

 

 




