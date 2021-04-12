---
title: Cursor (référence des éléments d’interface utilisateur MSAA)
description: Un curseur est une petite image dont l’emplacement sur l’écran est contrôlé par un dispositif de pointage, tel qu’une souris, un stylet ou un Trackball. Lorsque l’utilisateur déplace le dispositif de pointage, le système d’exploitation Windows déplace le curseur.
ms.assetid: ff97d474-7c96-4f89-bc34-2cf320381ce0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff351040d342adccda8cb03d56d91f9dc429074f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309466"
---
# <a name="cursor-msaa-ui-element-reference"></a><span data-ttu-id="ee5fb-104">Cursor (référence des éléments d’interface utilisateur MSAA)</span><span class="sxs-lookup"><span data-stu-id="ee5fb-104">Cursor (MSAA UI Element Reference)</span></span>

> [!Note]  
> <span data-ttu-id="ee5fb-105">Cette rubrique décrit les curseurs à des fins de référence des éléments d’interface utilisateur MSAA.</span><span class="sxs-lookup"><span data-stu-id="ee5fb-105">This topic describes cursors for purposes of MSAA UI Element Reference.</span></span> <span data-ttu-id="ee5fb-106">L’utilisation de curseurs dans différentes infrastructures d’interface utilisateur n’est pas décrite ici.</span><span class="sxs-lookup"><span data-stu-id="ee5fb-106">How to use cursors in various UI frameworks is not described here.</span></span> <span data-ttu-id="ee5fb-107">Consultez la documentation de référence sur les API pour l’infrastructure d’interface utilisateur que vous utilisez.</span><span class="sxs-lookup"><span data-stu-id="ee5fb-107">See the API reference documentation for the UI framework you're using.</span></span>

 

<span data-ttu-id="ee5fb-108">Un curseur est une petite image dont l’emplacement sur l’écran est contrôlé par un dispositif de pointage, tel qu’une souris, un stylet ou un Trackball.</span><span class="sxs-lookup"><span data-stu-id="ee5fb-108">A cursor is a small picture whose location on the screen is controlled by a pointing device, such as a mouse, pen, or trackball.</span></span> <span data-ttu-id="ee5fb-109">Lorsque l’utilisateur déplace le dispositif de pointage, le système d’exploitation Windows déplace le curseur.</span><span class="sxs-lookup"><span data-stu-id="ee5fb-109">When the user moves the pointing device, the Windows operating system moves the cursor.</span></span>

## <a name="iaccessible-methods"></a><span data-ttu-id="ee5fb-110">Méthodes IAccessible</span><span class="sxs-lookup"><span data-stu-id="ee5fb-110">IAccessible Methods</span></span>

<span data-ttu-id="ee5fb-111">Un curseur prend en charge les méthodes [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) suivantes :</span><span class="sxs-lookup"><span data-stu-id="ee5fb-111">A cursor supports the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) methods:</span></span>

-   [<span data-ttu-id="ee5fb-112">**accHitTest**</span><span class="sxs-lookup"><span data-stu-id="ee5fb-112">**accHitTest**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [<span data-ttu-id="ee5fb-113">**accLocation**</span><span class="sxs-lookup"><span data-stu-id="ee5fb-113">**accLocation**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)

## <a name="iaccessible-properties"></a><span data-ttu-id="ee5fb-114">Propriétés IAccessible</span><span class="sxs-lookup"><span data-stu-id="ee5fb-114">IAccessible Properties</span></span>

<span data-ttu-id="ee5fb-115">Un curseur prend en charge les propriétés [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) suivantes :</span><span class="sxs-lookup"><span data-stu-id="ee5fb-115">A cursor supports the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties:</span></span>

-   <span data-ttu-id="ee5fb-116">[**Obtient \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount): la propriété **ChildCount** est égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="ee5fb-116">[**get\_accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)—The **ChildCount** property is zero.</span></span>
-   <span data-ttu-id="ee5fb-117">[**Obtient \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname): les développeurs peuvent créer des curseurs personnalisés ou utiliser les curseurs prédéfinis qui sont identifiés par leur ID de curseur.</span><span class="sxs-lookup"><span data-stu-id="ee5fb-117">[**get\_accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)—Developers can create custom cursors or use the predefined cursors that are identified by their cursor ID.</span></span> <span data-ttu-id="ee5fb-118">La propriété **Name** du curseur dépend de sa forme et est l’un des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="ee5fb-118">The **Name** property of the cursor depends on its shape and is one of the following:</span></span> 

    | <span data-ttu-id="ee5fb-119">Forme de curseur</span><span class="sxs-lookup"><span data-stu-id="ee5fb-119">Cursor shape</span></span>     | <span data-ttu-id="ee5fb-120">Nom</span><span class="sxs-lookup"><span data-stu-id="ee5fb-120">Name</span></span>              |
    |------------------|-------------------|
    | <span data-ttu-id="ee5fb-121">Curseur personnalisé</span><span class="sxs-lookup"><span data-stu-id="ee5fb-121">Custom cursor</span></span>    | <span data-ttu-id="ee5fb-122">Connue</span><span class="sxs-lookup"><span data-stu-id="ee5fb-122">"Unknown"</span></span>         |
    | <span data-ttu-id="ee5fb-123">\_flèche IDC</span><span class="sxs-lookup"><span data-stu-id="ee5fb-123">IDC\_ARROW</span></span>       | <span data-ttu-id="ee5fb-124">"Normal"</span><span class="sxs-lookup"><span data-stu-id="ee5fb-124">"Normal"</span></span>          |
    | <span data-ttu-id="ee5fb-125">\_pointeur en I IDC</span><span class="sxs-lookup"><span data-stu-id="ee5fb-125">IDC\_IBEAM</span></span>       | <span data-ttu-id="ee5fb-126">Modifiés</span><span class="sxs-lookup"><span data-stu-id="ee5fb-126">"Edit"</span></span>            |
    | <span data-ttu-id="ee5fb-127">\_attente IDC</span><span class="sxs-lookup"><span data-stu-id="ee5fb-127">IDC\_WAIT</span></span>        | <span data-ttu-id="ee5fb-128">Qu'</span><span class="sxs-lookup"><span data-stu-id="ee5fb-128">"Wait"</span></span>            |
    | <span data-ttu-id="ee5fb-129">Inter. IDC \_</span><span class="sxs-lookup"><span data-stu-id="ee5fb-129">IDC\_CROSS</span></span>       | <span data-ttu-id="ee5fb-130">Représentation</span><span class="sxs-lookup"><span data-stu-id="ee5fb-130">"Graphic"</span></span>         |
    | <span data-ttu-id="ee5fb-131">\_flèche vers le haut IDC</span><span class="sxs-lookup"><span data-stu-id="ee5fb-131">IDC\_UPARROW</span></span>     | <span data-ttu-id="ee5fb-132">Les</span><span class="sxs-lookup"><span data-stu-id="ee5fb-132">"Up"</span></span>              |
    | <span data-ttu-id="ee5fb-133">\_SIZENWSE IDC</span><span class="sxs-lookup"><span data-stu-id="ee5fb-133">IDC\_SIZENWSE</span></span>    | <span data-ttu-id="ee5fb-134">"Nose size"</span><span class="sxs-lookup"><span data-stu-id="ee5fb-134">"NWSE size"</span></span>       |
    | <span data-ttu-id="ee5fb-135">\_SIZENESW IDC</span><span class="sxs-lookup"><span data-stu-id="ee5fb-135">IDC\_SIZENESW</span></span>    | <span data-ttu-id="ee5fb-136">« Taille NESO »</span><span class="sxs-lookup"><span data-stu-id="ee5fb-136">"NESW size"</span></span>       |
    | <span data-ttu-id="ee5fb-137">\_SIZEWE IDC</span><span class="sxs-lookup"><span data-stu-id="ee5fb-137">IDC\_SIZEWE</span></span>      | <span data-ttu-id="ee5fb-138">« Taille horizontale »</span><span class="sxs-lookup"><span data-stu-id="ee5fb-138">"Horizontal size"</span></span> |
    | <span data-ttu-id="ee5fb-139">\_SIZENS IDC</span><span class="sxs-lookup"><span data-stu-id="ee5fb-139">IDC\_SIZENS</span></span>      | <span data-ttu-id="ee5fb-140">"Taille verticale"</span><span class="sxs-lookup"><span data-stu-id="ee5fb-140">"Vertical size"</span></span>   |
    | <span data-ttu-id="ee5fb-141">\_SIZEALL IDC</span><span class="sxs-lookup"><span data-stu-id="ee5fb-141">IDC\_SIZEALL</span></span>     | <span data-ttu-id="ee5fb-142">Activer</span><span class="sxs-lookup"><span data-stu-id="ee5fb-142">"Move"</span></span>            |
    | <span data-ttu-id="ee5fb-143">IDC \_ non</span><span class="sxs-lookup"><span data-stu-id="ee5fb-143">IDC\_NO</span></span>          | <span data-ttu-id="ee5fb-144">Forbidden</span><span class="sxs-lookup"><span data-stu-id="ee5fb-144">"Forbidden"</span></span>       |
    | <span data-ttu-id="ee5fb-145">\_APPSTARTING IDC</span><span class="sxs-lookup"><span data-stu-id="ee5fb-145">IDC\_APPSTARTING</span></span> | <span data-ttu-id="ee5fb-146">« Démarrage de l’application »</span><span class="sxs-lookup"><span data-stu-id="ee5fb-146">"App start"</span></span>       |
    | <span data-ttu-id="ee5fb-147">\_aide d’IDC</span><span class="sxs-lookup"><span data-stu-id="ee5fb-147">IDC\_HELP</span></span>        | <span data-ttu-id="ee5fb-148">Sur</span><span class="sxs-lookup"><span data-stu-id="ee5fb-148">"Help"</span></span>            |

    

     

-   <span data-ttu-id="ee5fb-149">[**Obtient \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole): la propriété **role** est [**un \_ \_ curseur de système de rôle**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="ee5fb-149">[**get\_accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)—The **Role** property is [**ROLE\_SYSTEM\_CURSOR**](object-roles.md).</span></span>
-   <span data-ttu-id="ee5fb-150">[**obtenir \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate): la propriété **State** est une combinaison d’une ou plusieurs des [valeurs](object-state-constants.md)suivantes :</span><span class="sxs-lookup"><span data-stu-id="ee5fb-150">[**get\_accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)—The **State** property is a combination of one or more of the following [values](object-state-constants.md):</span></span>

    <span data-ttu-id="ee5fb-151">[**État \_ système \_**](object-state-constants.md) d’État invisible du système, \| [ **\_ \_ flottant**](object-state-constants.md)</span><span class="sxs-lookup"><span data-stu-id="ee5fb-151">[**STATE\_SYSTEM\_INVISIBLE**](object-state-constants.md) \| [**STATE\_SYSTEM\_FLOATING**](object-state-constants.md)</span></span>

## <a name="notes"></a><span data-ttu-id="ee5fb-152">Notes</span><span class="sxs-lookup"><span data-stu-id="ee5fb-152">Notes</span></span>

-   <span data-ttu-id="ee5fb-153">Contrairement à d’autres éléments d’interface utilisateur, l’objet Cursor n’a pas de handle de fenêtre associé.</span><span class="sxs-lookup"><span data-stu-id="ee5fb-153">Unlike other UI elements, the cursor object does not have an associated window handle.</span></span> <span data-ttu-id="ee5fb-154">Pour obtenir l’accès à l’objet Cursor, les clients doivent définir un [*WinEventProc*](/windows/desktop/api/Winuser/nc-winuser-wineventproc) et attendre que l’objet Cursor génère des événements.</span><span class="sxs-lookup"><span data-stu-id="ee5fb-154">To obtain access to the cursor object, clients must set a [*WinEventProc*](/windows/desktop/api/Winuser/nc-winuser-wineventproc) and wait for the cursor object to generate events.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ee5fb-155">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ee5fb-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ee5fb-156">IAccessible, interface</span><span class="sxs-lookup"><span data-stu-id="ee5fb-156">IAccessible Interface</span></span>](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 




