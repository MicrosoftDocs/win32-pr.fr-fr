---
title: Fonctions de modèle de contrôle déconseillées
description: Fonctions de modèle de contrôle déconseillées
ms.assetid: 06434b07-7592-4909-8c4e-064382bdbf98
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f646f9a9e3139d487785e344b9d3fc242b1a40e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104379685"
---
# <a name="deprecated-control-pattern-functions"></a><span data-ttu-id="27695-103">Fonctions de modèle de contrôle déconseillées</span><span class="sxs-lookup"><span data-stu-id="27695-103">Deprecated Control Pattern Functions</span></span>

> [!Note]  
> <span data-ttu-id="27695-104">Les fonctions de modèle de contrôle décrites dans cette section sont déconseillées.</span><span class="sxs-lookup"><span data-stu-id="27695-104">The control pattern functions described in this section are deprecated.</span></span> <span data-ttu-id="27695-105">Les applications clientes doivent utiliser les interfaces COM (Component Object Model) décrites dans les sections suivantes :</span><span class="sxs-lookup"><span data-stu-id="27695-105">Client applications should use the Component Object Model (COM) interfaces described in the following sections:</span></span>
>
> -   [<span data-ttu-id="27695-106">Interfaces d’élément UI Automation pour les clients</span><span class="sxs-lookup"><span data-stu-id="27695-106">UI Automation Element Interfaces for Clients</span></span>](uiauto-entry-uiautoclientinterfaces.md)
> -   [<span data-ttu-id="27695-107">Interface de condition de propriété pour les clients</span><span class="sxs-lookup"><span data-stu-id="27695-107">Property Condition Interface for Clients</span></span>](uiauto-client-propconditioninterfaces.md)
> -   [<span data-ttu-id="27695-108">Interfaces de modèle de contrôle pour les clients</span><span class="sxs-lookup"><span data-stu-id="27695-108">Control Pattern Interfaces for Clients</span></span>](uiauto-client-controlpatterninterfaces.md)
> -   [<span data-ttu-id="27695-109">Interfaces de gestion des événements pour les clients</span><span class="sxs-lookup"><span data-stu-id="27695-109">Event Handling Interfaces for Clients</span></span>](uiauto-client-eventhandlinginterfaces.md)
> -   [<span data-ttu-id="27695-110">Interfaces de fabrique proxy pour les clients</span><span class="sxs-lookup"><span data-stu-id="27695-110">Proxy Factory Interfaces for Clients</span></span>](uiauto-client-proxyfactoryinterfaces.md)

 

## <a name="in-this-section"></a><span data-ttu-id="27695-111">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="27695-111">In this section</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="27695-112">Fonction</span><span class="sxs-lookup"><span data-stu-id="27695-112">Function</span></span></th>
<th><span data-ttu-id="27695-113">Description</span><span class="sxs-lookup"><span data-stu-id="27695-113">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="27695-114"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-dockpattern_setdockposition"><strong>DockPattern_SetDockPosition</strong></a></span><span class="sxs-lookup"><span data-stu-id="27695-114"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-dockpattern_setdockposition"><strong>DockPattern_SetDockPosition</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="27695-115">Cette fonction est déconseillée.</span><span class="sxs-lookup"><span data-stu-id="27695-115">This function is deprecated.</span></span> <span data-ttu-id="27695-116">Les applications clientes doivent utiliser les interfaces COM UI Automation de Microsoft à la place.</span><span class="sxs-lookup"><span data-stu-id="27695-116">Client applications should use the Microsoft UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="27695-117">Ancre l’élément UI Automation au <em>DockPosition</em> demandé dans un conteneur d’ancrage.</span><span class="sxs-lookup"><span data-stu-id="27695-117">Docks the UI Automation element at the requested <em>dockPosition</em> within a docking container.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="27695-118"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-expandcollapsepattern_collapse"><strong>ExpandCollapsePattern_Collapse</strong></a></span><span class="sxs-lookup"><span data-stu-id="27695-118"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-expandcollapsepattern_collapse"><strong>ExpandCollapsePattern_Collapse</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="27695-119">Cette fonction est déconseillée.</span><span class="sxs-lookup"><span data-stu-id="27695-119">This function is deprecated.</span></span> <span data-ttu-id="27695-120">Les applications clientes doivent utiliser les interfaces COM UI Automation à la place.</span><span class="sxs-lookup"><span data-stu-id="27695-120">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="27695-121">Masque tous les nœuds, contrôles ou contenu descendants de l’élément UI Automation.</span><span class="sxs-lookup"><span data-stu-id="27695-121">Hides all descendant nodes, controls, or content of the UI Automation element.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="27695-122"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-expandcollapsepattern_expand"><strong>ExpandCollapsePattern_Expand</strong></a></span><span class="sxs-lookup"><span data-stu-id="27695-122"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-expandcollapsepattern_expand"><strong>ExpandCollapsePattern_Expand</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="27695-123">Cette fonction est déconseillée.</span><span class="sxs-lookup"><span data-stu-id="27695-123">This function is deprecated.</span></span> <span data-ttu-id="27695-124">Les applications clientes doivent utiliser les interfaces COM UI Automation à la place.</span><span class="sxs-lookup"><span data-stu-id="27695-124">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="27695-125">Développe un contrôle à l’écran pour afficher plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="27695-125">Expands a control on the screen so that it shows more information.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="27695-126"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-gridpattern_getitem"><strong>GridPattern_GetItem</strong></a></span><span class="sxs-lookup"><span data-stu-id="27695-126"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-gridpattern_getitem"><strong>GridPattern_GetItem</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="27695-127">Cette fonction est déconseillée.</span><span class="sxs-lookup"><span data-stu-id="27695-127">This function is deprecated.</span></span> <span data-ttu-id="27695-128">Les applications clientes doivent utiliser les interfaces COM UI Automation à la place.</span><span class="sxs-lookup"><span data-stu-id="27695-128">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="27695-129">Obtient le nœud d’un élément dans une grille.</span><span class="sxs-lookup"><span data-stu-id="27695-129">Gets the node for an item in a grid.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="27695-130"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-invokepattern_invoke"><strong>InvokePattern_Invoke</strong></a></span><span class="sxs-lookup"><span data-stu-id="27695-130"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-invokepattern_invoke"><strong>InvokePattern_Invoke</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="27695-131">Cette fonction est déconseillée.</span><span class="sxs-lookup"><span data-stu-id="27695-131">This function is deprecated.</span></span> <span data-ttu-id="27695-132">Les applications clientes doivent utiliser les interfaces COM UI Automation à la place.</span><span class="sxs-lookup"><span data-stu-id="27695-132">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="27695-133">Envoie une requête pour activer un contrôle et initier son action unique et non équivoque.</span><span class="sxs-lookup"><span data-stu-id="27695-133">Sends a request to activate a control and initiate its single, unambiguous action.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="27695-134"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-itemcontainerpattern_finditembyproperty"><strong>ItemContainerPattern_FindItemByProperty</strong></a></span><span class="sxs-lookup"><span data-stu-id="27695-134"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-itemcontainerpattern_finditembyproperty"><strong>ItemContainerPattern_FindItemByProperty</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="27695-135">Cette fonction est déconseillée.</span><span class="sxs-lookup"><span data-stu-id="27695-135">This function is deprecated.</span></span> <span data-ttu-id="27695-136">Les applications clientes doivent utiliser les interfaces COM UI Automation à la place.</span><span class="sxs-lookup"><span data-stu-id="27695-136">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="27695-137">Récupère un nœud dans un nœud conteneur, en fonction d’une valeur de propriété spécifiée.</span><span class="sxs-lookup"><span data-stu-id="27695-137">Retrieves a node within a containing node, based on a specified property value.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="27695-138"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-legacyiaccessiblepattern_dodefaultaction"><strong>LegacyIAccessiblePattern_DoDefaultAction</strong></a></span><span class="sxs-lookup"><span data-stu-id="27695-138"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-legacyiaccessiblepattern_dodefaultaction"><strong>LegacyIAccessiblePattern_DoDefaultAction</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="27695-139">Cette fonction est déconseillée.</span><span class="sxs-lookup"><span data-stu-id="27695-139">This function is deprecated.</span></span> <span data-ttu-id="27695-140">Les applications clientes doivent utiliser les interfaces COM UI Automation à la place.</span><span class="sxs-lookup"><span data-stu-id="27695-140">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="27695-141">Exécute l’action Microsoft Active Accessibility par défaut pour l’élément.</span><span class="sxs-lookup"><span data-stu-id="27695-141">Performs the Microsoft Active Accessibility default action for the element.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="27695-142"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-legacyiaccessiblepattern_getiaccessible"><strong>LegacyIAccessiblePattern_GetIAccessible</strong></a></span><span class="sxs-lookup"><span data-stu-id="27695-142"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-legacyiaccessiblepattern_getiaccessible"><strong>LegacyIAccessiblePattern_GetIAccessible</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="27695-143">Cette fonction est déconseillée.</span><span class="sxs-lookup"><span data-stu-id="27695-143">This function is deprecated.</span></span> <span data-ttu-id="27695-144">Les applications clientes doivent utiliser les interfaces COM UI Automation à la place.</span><span class="sxs-lookup"><span data-stu-id="27695-144">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="27695-145">Récupère un objet <a href="/windows/desktop/api/oleacc/nn-oleacc-iaccessible"><strong>IAccessible</strong></a> qui correspond à l’élément UI Automation.</span><span class="sxs-lookup"><span data-stu-id="27695-145">Retrieves an <a href="/windows/desktop/api/oleacc/nn-oleacc-iaccessible"><strong>IAccessible</strong></a> object that corresponds to the UI Automation element.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="27695-146"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-legacyiaccessiblepattern_select"><strong>LegacyIAccessiblePattern_Select</strong></a></span><span class="sxs-lookup"><span data-stu-id="27695-146"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-legacyiaccessiblepattern_select"><strong>LegacyIAccessiblePattern_Select</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="27695-147">Cette fonction est déconseillée.</span><span class="sxs-lookup"><span data-stu-id="27695-147">This function is deprecated.</span></span> <span data-ttu-id="27695-148">Les applications clientes doivent utiliser les interfaces COM UI Automation à la place.</span><span class="sxs-lookup"><span data-stu-id="27695-148">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="27695-149">Effectue une sélection Microsoft Active Accessibility.</span><span class="sxs-lookup"><span data-stu-id="27695-149">Performs a Microsoft Active Accessibility selection.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="27695-150"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-legacyiaccessiblepattern_setvalue"><strong>LegacyIAccessiblePattern_SetValue</strong></a></span><span class="sxs-lookup"><span data-stu-id="27695-150"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-legacyiaccessiblepattern_setvalue"><strong>LegacyIAccessiblePattern_SetValue</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="27695-151">Cette fonction est déconseillée.</span><span class="sxs-lookup"><span data-stu-id="27695-151">This function is deprecated.</span></span> <span data-ttu-id="27695-152">Les applications clientes doivent utiliser les interfaces COM UI Automation à la place.</span><span class="sxs-lookup"><span data-stu-id="27695-152">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="27695-153">Définit la propriété de valeur de Active Accessibility Microsoft pour le nœud.</span><span class="sxs-lookup"><span data-stu-id="27695-153">Sets the Microsoft Active Accessibility value property for the node.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="27695-154"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-multipleviewpattern_getviewname"><strong>MultipleViewPattern_GetViewName</strong></a></span><span class="sxs-lookup"><span data-stu-id="27695-154"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-multipleviewpattern_getviewname"><strong>MultipleViewPattern_GetViewName</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="27695-155">Cette fonction est déconseillée.</span><span class="sxs-lookup"><span data-stu-id="27695-155">This function is deprecated.</span></span> <span data-ttu-id="27695-156">Les applications clientes doivent utiliser les interfaces COM UI Automation à la place.</span><span class="sxs-lookup"><span data-stu-id="27695-156">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="27695-157">Récupère le nom d'un affichage spécifique au contrôle.</span><span class="sxs-lookup"><span data-stu-id="27695-157">Retrieves the name of a control-specific view.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="27695-158"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-multipleviewpattern_setcurrentview"><strong>MultipleViewPattern_SetCurrentView</strong></a></span><span class="sxs-lookup"><span data-stu-id="27695-158"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-multipleviewpattern_setcurrentview"><strong>MultipleViewPattern_SetCurrentView</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="27695-159">Cette fonction est déconseillée.</span><span class="sxs-lookup"><span data-stu-id="27695-159">This function is deprecated.</span></span> <span data-ttu-id="27695-160">Les applications clientes doivent utiliser les interfaces COM UI Automation à la place.</span><span class="sxs-lookup"><span data-stu-id="27695-160">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="27695-161">Définit un contrôle sur une disposition différente.</span><span class="sxs-lookup"><span data-stu-id="27695-161">Sets a control to a different layout.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="27695-162"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-rangevaluepattern_setvalue"><strong>RangeValuePattern_SetValue</strong></a></span><span class="sxs-lookup"><span data-stu-id="27695-162"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-rangevaluepattern_setvalue"><strong>RangeValuePattern_SetValue</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="27695-163">Cette fonction est déconseillée.</span><span class="sxs-lookup"><span data-stu-id="27695-163">This function is deprecated.</span></span> <span data-ttu-id="27695-164">Les applications clientes doivent utiliser les interfaces COM UI Automation à la place.</span><span class="sxs-lookup"><span data-stu-id="27695-164">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="27695-165">Définit la valeur d’un contrôle qui a une plage numérique.</span><span class="sxs-lookup"><span data-stu-id="27695-165">Sets the value of a control that has a numerical range.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="27695-166"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-scrollitempattern_scrollintoview"><strong>ScrollItemPattern_ScrollIntoView</strong></a></span><span class="sxs-lookup"><span data-stu-id="27695-166"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-scrollitempattern_scrollintoview"><strong>ScrollItemPattern_ScrollIntoView</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="27695-167">Cette fonction est déconseillée.</span><span class="sxs-lookup"><span data-stu-id="27695-167">This function is deprecated.</span></span> <span data-ttu-id="27695-168">Les applications clientes doivent utiliser les interfaces COM UI Automation à la place.</span><span class="sxs-lookup"><span data-stu-id="27695-168">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="27695-169">Fait défiler la zone de contenu d’un objet conteneur pour afficher l’élément UI Automation dans la zone visible (fenêtre d’affichage) du conteneur.</span><span class="sxs-lookup"><span data-stu-id="27695-169">Scrolls the content area of a container object in order to display the UI Automation element within the visible region (viewport) of the container.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="27695-170"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-scrollpattern_scroll"><strong>ScrollPattern_Scroll</strong></a></span><span class="sxs-lookup"><span data-stu-id="27695-170"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-scrollpattern_scroll"><strong>ScrollPattern_Scroll</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="27695-171">Cette fonction est déconseillée.</span><span class="sxs-lookup"><span data-stu-id="27695-171">This function is deprecated.</span></span> <span data-ttu-id="27695-172">Les applications clientes doivent utiliser les interfaces COM UI Automation à la place.</span><span class="sxs-lookup"><span data-stu-id="27695-172">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="27695-173">Fait défiler la zone actuellement visible de la zone de contenu avec l' <a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-scrollamount"><strong>ScrollAmount</strong></a>spécifié, horizontalement, verticalement, ou les deux.</span><span class="sxs-lookup"><span data-stu-id="27695-173">Scrolls the currently visible region of the content area the specified <a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-scrollamount"><strong>ScrollAmount</strong></a>, horizontally, vertically, or both.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="27695-174"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-scrollpattern_setscrollpercent"><strong>ScrollPattern_SetScrollPercent</strong></a></span><span class="sxs-lookup"><span data-stu-id="27695-174"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-scrollpattern_setscrollpercent"><strong>ScrollPattern_SetScrollPercent</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="27695-175">Cette fonction est déconseillée.</span><span class="sxs-lookup"><span data-stu-id="27695-175">This function is deprecated.</span></span> <span data-ttu-id="27695-176">Les applications clientes doivent utiliser les interfaces COM UI Automation à la place.</span><span class="sxs-lookup"><span data-stu-id="27695-176">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="27695-177">Fait défiler un conteneur vers une position spécifique horizontalement, verticalement, ou les deux.</span><span class="sxs-lookup"><span data-stu-id="27695-177">Scrolls a container to a specific position horizontally, vertically, or both.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="27695-178"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-selectionitempattern_addtoselection"><strong>SelectionItemPattern_AddToSelection</strong></a></span><span class="sxs-lookup"><span data-stu-id="27695-178"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-selectionitempattern_addtoselection"><strong>SelectionItemPattern_AddToSelection</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="27695-179">Cette fonction est déconseillée.</span><span class="sxs-lookup"><span data-stu-id="27695-179">This function is deprecated.</span></span> <span data-ttu-id="27695-180">Les applications clientes doivent utiliser les interfaces COM UI Automation à la place.</span><span class="sxs-lookup"><span data-stu-id="27695-180">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="27695-181">Ajoute un élément non sélectionné à une sélection dans un contrôle.</span><span class="sxs-lookup"><span data-stu-id="27695-181">Adds an unselected element to a selection in a control.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="27695-182"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-selectionitempattern_removefromselection"><strong>SelectionItemPattern_RemoveFromSelection</strong></a></span><span class="sxs-lookup"><span data-stu-id="27695-182"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-selectionitempattern_removefromselection"><strong>SelectionItemPattern_RemoveFromSelection</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="27695-183">Cette fonction est déconseillée.</span><span class="sxs-lookup"><span data-stu-id="27695-183">This function is deprecated.</span></span> <span data-ttu-id="27695-184">Les applications clientes doivent utiliser les interfaces COM UI Automation à la place.</span><span class="sxs-lookup"><span data-stu-id="27695-184">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="27695-185">Supprime un élément de la sélection dans un conteneur de sélection.</span><span class="sxs-lookup"><span data-stu-id="27695-185">Removes an element from the selection in a selection container.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="27695-186"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-selectionitempattern_select"><strong>SelectionItemPattern_Select</strong></a></span><span class="sxs-lookup"><span data-stu-id="27695-186"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-selectionitempattern_select"><strong>SelectionItemPattern_Select</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="27695-187">Cette fonction est déconseillée.</span><span class="sxs-lookup"><span data-stu-id="27695-187">This function is deprecated.</span></span> <span data-ttu-id="27695-188">Les applications clientes doivent utiliser les interfaces COM UI Automation à la place.</span><span class="sxs-lookup"><span data-stu-id="27695-188">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="27695-189">Sélectionne un élément dans un conteneur de sélection.</span><span class="sxs-lookup"><span data-stu-id="27695-189">Selects an element in a selection container.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="27695-190"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-synchronizedinputpattern_cancel"><strong>SynchronizedInputPattern_Cancel</strong></a></span><span class="sxs-lookup"><span data-stu-id="27695-190"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-synchronizedinputpattern_cancel"><strong>SynchronizedInputPattern_Cancel</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="27695-191">Cette fonction est déconseillée.</span><span class="sxs-lookup"><span data-stu-id="27695-191">This function is deprecated.</span></span> <span data-ttu-id="27695-192">Les applications clientes doivent utiliser les interfaces COM UI Automation à la place.</span><span class="sxs-lookup"><span data-stu-id="27695-192">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="27695-193">Fait en sorte que le fournisseur UI Automation arrête d’écouter la souris ou l’entrée au clavier.</span><span class="sxs-lookup"><span data-stu-id="27695-193">Causes the UI Automation provider to stop listening for mouse or keyboard input.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="27695-194"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-synchronizedinputpattern_startlistening"><strong>SynchronizedInputPattern_StartListening</strong></a></span><span class="sxs-lookup"><span data-stu-id="27695-194"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-synchronizedinputpattern_startlistening"><strong>SynchronizedInputPattern_StartListening</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="27695-195">Cette fonction est déconseillée.</span><span class="sxs-lookup"><span data-stu-id="27695-195">This function is deprecated.</span></span> <span data-ttu-id="27695-196">Les applications clientes doivent utiliser les interfaces COM UI Automation à la place.</span><span class="sxs-lookup"><span data-stu-id="27695-196">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="27695-197">Fait en sorte que le fournisseur UI Automation commence à écouter la souris ou l’entrée au clavier.</span><span class="sxs-lookup"><span data-stu-id="27695-197">Causes the UI Automation provider to start listening for mouse or keyboard input.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="27695-198"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textpattern_get_documentrange"><strong>TextPattern_get_DocumentRange</strong></a></span><span class="sxs-lookup"><span data-stu-id="27695-198"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textpattern_get_documentrange"><strong>TextPattern_get_DocumentRange</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="27695-199">Cette fonction est déconseillée.</span><span class="sxs-lookup"><span data-stu-id="27695-199">This function is deprecated.</span></span> <span data-ttu-id="27695-200">Les applications clientes doivent utiliser les interfaces COM UI Automation à la place.</span><span class="sxs-lookup"><span data-stu-id="27695-200">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="27695-201">Obtient la plage de texte pour le document entier.</span><span class="sxs-lookup"><span data-stu-id="27695-201">Gets the text range for the entire document.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="27695-202"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textpattern_get_supportedtextselection"><strong>TextPattern_get_SupportedTextSelection</strong></a></span><span class="sxs-lookup"><span data-stu-id="27695-202"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textpattern_get_supportedtextselection"><strong>TextPattern_get_SupportedTextSelection</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="27695-203">Cette fonction est déconseillée.</span><span class="sxs-lookup"><span data-stu-id="27695-203">This function is deprecated.</span></span> <span data-ttu-id="27695-204">Les applications clientes doivent utiliser les interfaces COM UI Automation à la place.</span><span class="sxs-lookup"><span data-stu-id="27695-204">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="27695-205">Vérifie si le contenu du conteneur de texte peut être sélectionné et désélectionné.</span><span class="sxs-lookup"><span data-stu-id="27695-205">Ascertains whether the text container's contents can be selected and deselected.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="27695-206"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textpattern_getselection"><strong>TextPattern_GetSelection</strong></a></span><span class="sxs-lookup"><span data-stu-id="27695-206"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textpattern_getselection"><strong>TextPattern_GetSelection</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="27695-207">Cette fonction est déconseillée.</span><span class="sxs-lookup"><span data-stu-id="27695-207">This function is deprecated.</span></span> <span data-ttu-id="27695-208">Les applications clientes doivent utiliser les interfaces COM UI Automation à la place.</span><span class="sxs-lookup"><span data-stu-id="27695-208">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="27695-209">Obtient la plage actuelle du texte sélectionné à partir d’un conteneur de texte prenant en charge le modèle de texte.</span><span class="sxs-lookup"><span data-stu-id="27695-209">Gets the current range of selected text from a text container supporting the text pattern.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="27695-210"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textpattern_getvisibleranges"><strong>TextPattern_GetVisibleRanges</strong></a></span><span class="sxs-lookup"><span data-stu-id="27695-210"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textpattern_getvisibleranges"><strong>TextPattern_GetVisibleRanges</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="27695-211">Cette fonction est déconseillée.</span><span class="sxs-lookup"><span data-stu-id="27695-211">This function is deprecated.</span></span> <span data-ttu-id="27695-212">Les applications clientes doivent utiliser les interfaces COM UI Automation à la place.</span><span class="sxs-lookup"><span data-stu-id="27695-212">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="27695-213">Récupère un tableau de plages de texte disjointes à partir d'un conteneur de texte où chaque plage de texte commence à la première ligne partiellement visible et se termine à la dernière ligne partiellement visible.</span><span class="sxs-lookup"><span data-stu-id="27695-213">Retrieves an array of disjoint text ranges from a text container where each text range begins with the first partially visible line through to the end of the last partially visible line.</span></span> <span data-ttu-id="27695-214">Par exemple, une disposition à plusieurs colonnes dans laquelle les colonnes sont partiellement déplacées hors de la zone visible de la fenêtre d’affichage et le contenu se déplace du bas d’une colonne vers le haut de la suivante.</span><span class="sxs-lookup"><span data-stu-id="27695-214">For example, a multi-column layout where the columns are partially scrolled out of the visible area of the viewport and the content flows from the bottom of one column to the top of the next.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="27695-215"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textpattern_rangefromchild"><strong>TextPattern_RangeFromChild</strong></a></span><span class="sxs-lookup"><span data-stu-id="27695-215"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textpattern_rangefromchild"><strong>TextPattern_RangeFromChild</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="27695-216">Cette fonction est déconseillée.</span><span class="sxs-lookup"><span data-stu-id="27695-216">This function is deprecated.</span></span> <span data-ttu-id="27695-217">Les applications clientes doivent utiliser les interfaces COM UI Automation à la place.</span><span class="sxs-lookup"><span data-stu-id="27695-217">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="27695-218">Obtient la plage de texte étendue par un nœud donné.</span><span class="sxs-lookup"><span data-stu-id="27695-218">Gets the text range that a given node spans.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="27695-219"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textpattern_rangefrompoint"><strong>TextPattern_RangeFromPoint</strong></a></span><span class="sxs-lookup"><span data-stu-id="27695-219"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textpattern_rangefrompoint"><strong>TextPattern_RangeFromPoint</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="27695-220">Cette fonction est déconseillée.</span><span class="sxs-lookup"><span data-stu-id="27695-220">This function is deprecated.</span></span> <span data-ttu-id="27695-221">Les applications clientes doivent utiliser les interfaces COM UI Automation à la place.</span><span class="sxs-lookup"><span data-stu-id="27695-221">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="27695-222">Récupère la plage de texte dégénérée (vide) la plus proche des coordonnées d’écran spécifiées.</span><span class="sxs-lookup"><span data-stu-id="27695-222">Retrieves the degenerate (empty) text range nearest to the specified screen coordinates.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="27695-223"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_addtoselection"><strong>TextRange_AddToSelection</strong></a></span><span class="sxs-lookup"><span data-stu-id="27695-223"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_addtoselection"><strong>TextRange_AddToSelection</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="27695-224">Cette fonction est déconseillée.</span><span class="sxs-lookup"><span data-stu-id="27695-224">This function is deprecated.</span></span> <span data-ttu-id="27695-225">Les applications clientes doivent utiliser les interfaces COM UI Automation à la place.</span><span class="sxs-lookup"><span data-stu-id="27695-225">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="27695-226">Ajoute à la collection existante de texte en surbrillance dans un conteneur de texte qui prend en charge les sélections multiples et disjointes en mettant en surbrillance le texte supplémentaire correspondant aux points de terminaison de <em>début</em> et de <em>fin</em> de la plage de texte appelante.</span><span class="sxs-lookup"><span data-stu-id="27695-226">Adds to the existing collection of highlighted text in a text container that supports multiple, disjoint selections by highlighting supplementary text corresponding to the calling text range <em>Start</em> and <em>End</em> endpoints.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="27695-227"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_clone"><strong>TextRange_Clone</strong></a></span><span class="sxs-lookup"><span data-stu-id="27695-227"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_clone"><strong>TextRange_Clone</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="27695-228">Cette fonction est déconseillée.</span><span class="sxs-lookup"><span data-stu-id="27695-228">This function is deprecated.</span></span> <span data-ttu-id="27695-229">Les applications clientes doivent utiliser les interfaces COM UI Automation à la place.</span><span class="sxs-lookup"><span data-stu-id="27695-229">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="27695-230">Copie une plage de texte.</span><span class="sxs-lookup"><span data-stu-id="27695-230">Copies a text range.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="27695-231"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_compare"><strong>TextRange_Compare</strong></a></span><span class="sxs-lookup"><span data-stu-id="27695-231"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_compare"><strong>TextRange_Compare</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="27695-232">Cette fonction est déconseillée.</span><span class="sxs-lookup"><span data-stu-id="27695-232">This function is deprecated.</span></span> <span data-ttu-id="27695-233">Les applications clientes doivent utiliser les interfaces COM UI Automation à la place.</span><span class="sxs-lookup"><span data-stu-id="27695-233">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="27695-234">Compare deux plages de texte.</span><span class="sxs-lookup"><span data-stu-id="27695-234">Compares two text ranges.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="27695-235"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_compareendpoints"><strong>TextRange_CompareEndpoints</strong></a></span><span class="sxs-lookup"><span data-stu-id="27695-235"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_compareendpoints"><strong>TextRange_CompareEndpoints</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="27695-236">Cette fonction est déconseillée.</span><span class="sxs-lookup"><span data-stu-id="27695-236">This function is deprecated.</span></span> <span data-ttu-id="27695-237">Les applications clientes doivent utiliser les interfaces COM UI Automation à la place.</span><span class="sxs-lookup"><span data-stu-id="27695-237">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="27695-238">Retourne une valeur indiquant si deux plages de texte ont des points de terminaison identiques.</span><span class="sxs-lookup"><span data-stu-id="27695-238">Returns a value indicating whether two text ranges have identical endpoints.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="27695-239"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_expandtoenclosingunit"><strong>TextRange_ExpandToEnclosingUnit</strong></a></span><span class="sxs-lookup"><span data-stu-id="27695-239"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_expandtoenclosingunit"><strong>TextRange_ExpandToEnclosingUnit</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="27695-240">Cette fonction est déconseillée.</span><span class="sxs-lookup"><span data-stu-id="27695-240">This function is deprecated.</span></span> <span data-ttu-id="27695-241">Les applications clientes doivent utiliser les interfaces COM UI Automation à la place.</span><span class="sxs-lookup"><span data-stu-id="27695-241">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="27695-242">Développe la plage de texte jusqu’à une unité plus grande ou plus petite, telle qu’un caractère, un mot, une ligne ou une page.</span><span class="sxs-lookup"><span data-stu-id="27695-242">Expands the text range to a larger or smaller unit such as Character, Word, Line, or Page.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="27695-243"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_findattribute"><strong>TextRange_FindAttribute</strong></a></span><span class="sxs-lookup"><span data-stu-id="27695-243"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_findattribute"><strong>TextRange_FindAttribute</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="27695-244">Cette fonction est déconseillée.</span><span class="sxs-lookup"><span data-stu-id="27695-244">This function is deprecated.</span></span> <span data-ttu-id="27695-245">Les applications clientes doivent utiliser les interfaces COM UI Automation à la place.</span><span class="sxs-lookup"><span data-stu-id="27695-245">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="27695-246">Recherche dans une direction spécifiée la première partie du texte prenant en charge un attribut de texte spécifié.</span><span class="sxs-lookup"><span data-stu-id="27695-246">Searches in a specified direction for the first piece of text supporting a specified text attribute.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="27695-247"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_findtext"><strong>TextRange_FindText</strong></a></span><span class="sxs-lookup"><span data-stu-id="27695-247"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_findtext"><strong>TextRange_FindText</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="27695-248">Cette fonction est déconseillée.</span><span class="sxs-lookup"><span data-stu-id="27695-248">This function is deprecated.</span></span> <span data-ttu-id="27695-249">Les applications clientes doivent utiliser les interfaces COM UI Automation à la place.</span><span class="sxs-lookup"><span data-stu-id="27695-249">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="27695-250">Retourne la première plage de texte dans la direction spécifiée qui contient le texte que le client recherche.</span><span class="sxs-lookup"><span data-stu-id="27695-250">Returns the first text range in the specified direction that contains the text the client is searching for.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="27695-251"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_getattributevalue"><strong>TextRange_GetAttributeValue</strong></a></span><span class="sxs-lookup"><span data-stu-id="27695-251"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_getattributevalue"><strong>TextRange_GetAttributeValue</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="27695-252">Cette fonction est déconseillée.</span><span class="sxs-lookup"><span data-stu-id="27695-252">This function is deprecated.</span></span> <span data-ttu-id="27695-253">Les applications clientes doivent utiliser les interfaces COM UI Automation à la place.</span><span class="sxs-lookup"><span data-stu-id="27695-253">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="27695-254">Obtient la valeur d’un attribut de texte pour une plage de texte.</span><span class="sxs-lookup"><span data-stu-id="27695-254">Gets the value of an text attribute for a text range.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="27695-255"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_getboundingrectangles"><strong>TextRange_GetBoundingRectangles</strong></a></span><span class="sxs-lookup"><span data-stu-id="27695-255"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_getboundingrectangles"><strong>TextRange_GetBoundingRectangles</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="27695-256">Cette fonction est déconseillée.</span><span class="sxs-lookup"><span data-stu-id="27695-256">This function is deprecated.</span></span> <span data-ttu-id="27695-257">Les applications clientes doivent utiliser les interfaces COM UI Automation à la place.</span><span class="sxs-lookup"><span data-stu-id="27695-257">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="27695-258">Récupère le nombre minimal de rectangles englobants qui peuvent encadrer la plage, un rectangle par ligne.</span><span class="sxs-lookup"><span data-stu-id="27695-258">Retrieves the minimum number of bounding rectangles that can enclose the range, one rectangle per line.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="27695-259"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_getchildren"><strong>TextRange_GetChildren</strong></a></span><span class="sxs-lookup"><span data-stu-id="27695-259"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_getchildren"><strong>TextRange_GetChildren</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="27695-260">Cette fonction est déconseillée.</span><span class="sxs-lookup"><span data-stu-id="27695-260">This function is deprecated.</span></span> <span data-ttu-id="27695-261">Les applications clientes doivent utiliser les interfaces COM UI Automation à la place.</span><span class="sxs-lookup"><span data-stu-id="27695-261">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="27695-262">Retourne tous les éléments UI Automation contenus dans la plage de texte spécifiée.</span><span class="sxs-lookup"><span data-stu-id="27695-262">Returns all UI Automation elements contained within the specified text range.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="27695-263"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_getenclosingelement"><strong>TextRange_GetEnclosingElement</strong></a></span><span class="sxs-lookup"><span data-stu-id="27695-263"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_getenclosingelement"><strong>TextRange_GetEnclosingElement</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="27695-264">Cette fonction est déconseillée.</span><span class="sxs-lookup"><span data-stu-id="27695-264">This function is deprecated.</span></span> <span data-ttu-id="27695-265">Les applications clientes doivent utiliser les interfaces COM UI Automation à la place.</span><span class="sxs-lookup"><span data-stu-id="27695-265">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="27695-266">Retourne le nœud pour le prochain fournisseur le plus petit qui couvre la plage.</span><span class="sxs-lookup"><span data-stu-id="27695-266">Returns the node for the next smallest provider that covers the range.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="27695-267"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_gettext"><strong>TextRange_GetText</strong></a></span><span class="sxs-lookup"><span data-stu-id="27695-267"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_gettext"><strong>TextRange_GetText</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="27695-268">Cette fonction est déconseillée.</span><span class="sxs-lookup"><span data-stu-id="27695-268">This function is deprecated.</span></span> <span data-ttu-id="27695-269">Les applications clientes doivent utiliser les interfaces COM UI Automation à la place.</span><span class="sxs-lookup"><span data-stu-id="27695-269">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="27695-270">Retourne le texte d’une plage de texte, jusqu’à un nombre spécifié de caractères.</span><span class="sxs-lookup"><span data-stu-id="27695-270">Returns the text in a text range, up to a specified number of characters.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="27695-271"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_move"><strong>TextRange_Move</strong></a></span><span class="sxs-lookup"><span data-stu-id="27695-271"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_move"><strong>TextRange_Move</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="27695-272">Cette fonction est déconseillée.</span><span class="sxs-lookup"><span data-stu-id="27695-272">This function is deprecated.</span></span> <span data-ttu-id="27695-273">Les applications clientes doivent utiliser les interfaces COM UI Automation à la place.</span><span class="sxs-lookup"><span data-stu-id="27695-273">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="27695-274">Déplace la plage de texte du nombre spécifié d’unités demandées par le client.</span><span class="sxs-lookup"><span data-stu-id="27695-274">Moves the text range the specified number of units requested by the client.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="27695-275"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_moveendpointbyrange"><strong>TextRange_MoveEndpointByRange</strong></a></span><span class="sxs-lookup"><span data-stu-id="27695-275"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_moveendpointbyrange"><strong>TextRange_MoveEndpointByRange</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="27695-276">Cette fonction est déconseillée.</span><span class="sxs-lookup"><span data-stu-id="27695-276">This function is deprecated.</span></span> <span data-ttu-id="27695-277">Les applications clientes doivent utiliser les interfaces COM UI Automation à la place.</span><span class="sxs-lookup"><span data-stu-id="27695-277">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="27695-278">Déplace un point de terminaison d’une plage vers le point de terminaison d’une autre plage.</span><span class="sxs-lookup"><span data-stu-id="27695-278">Moves an endpoint of one range to the endpoint of another range.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="27695-279"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_moveendpointbyunit"><strong>TextRange_MoveEndpointByUnit</strong></a></span><span class="sxs-lookup"><span data-stu-id="27695-279"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_moveendpointbyunit"><strong>TextRange_MoveEndpointByUnit</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="27695-280">Cette fonction est déconseillée.</span><span class="sxs-lookup"><span data-stu-id="27695-280">This function is deprecated.</span></span> <span data-ttu-id="27695-281">Les applications clientes doivent utiliser les interfaces COM UI Automation à la place.</span><span class="sxs-lookup"><span data-stu-id="27695-281">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="27695-282">Déplace un point de terminaison de la plage du nombre d’unités spécifié.</span><span class="sxs-lookup"><span data-stu-id="27695-282">Moves an endpoint of the range the specified number of units.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="27695-283"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_removefromselection"><strong>TextRange_RemoveFromSelection</strong></a></span><span class="sxs-lookup"><span data-stu-id="27695-283"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_removefromselection"><strong>TextRange_RemoveFromSelection</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="27695-284">Cette fonction est déconseillée.</span><span class="sxs-lookup"><span data-stu-id="27695-284">This function is deprecated.</span></span> <span data-ttu-id="27695-285">Les applications clientes doivent utiliser les interfaces COM UI Automation à la place.</span><span class="sxs-lookup"><span data-stu-id="27695-285">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="27695-286">Supprime le texte sélectionné, correspondant à la plage de texte appelante <em>TextPatternRangeEndpoint_Start</em> et <em>TextPatternRangeEndpoint_End</em> points de terminaison, à partir d’une collection existante de texte sélectionné dans un conteneur de texte qui prend en charge les sélections multiples et disjointes.</span><span class="sxs-lookup"><span data-stu-id="27695-286">Removes the selected text, corresponding to the calling text range <em>TextPatternRangeEndpoint_Start</em> and <em>TextPatternRangeEndpoint_End</em> endpoints, from an existing collection of selected text in a text container that supports multiple, disjoint selections.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="27695-287"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_scrollintoview"><strong>TextRange_ScrollIntoView</strong></a></span><span class="sxs-lookup"><span data-stu-id="27695-287"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_scrollintoview"><strong>TextRange_ScrollIntoView</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="27695-288">Cette fonction est déconseillée.</span><span class="sxs-lookup"><span data-stu-id="27695-288">This function is deprecated.</span></span> <span data-ttu-id="27695-289">Les applications clientes doivent utiliser les interfaces COM UI Automation à la place.</span><span class="sxs-lookup"><span data-stu-id="27695-289">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="27695-290">Fait défiler le texte afin que la plage spécifiée soit visible dans la fenêtre d’affichage.</span><span class="sxs-lookup"><span data-stu-id="27695-290">Scrolls the text so the specified range is visible in the viewport.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="27695-291"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_select"><strong>TextRange_Select</strong></a></span><span class="sxs-lookup"><span data-stu-id="27695-291"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_select"><strong>TextRange_Select</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="27695-292">Cette fonction est déconseillée.</span><span class="sxs-lookup"><span data-stu-id="27695-292">This function is deprecated.</span></span> <span data-ttu-id="27695-293">Les applications clientes doivent utiliser les interfaces COM UI Automation à la place.</span><span class="sxs-lookup"><span data-stu-id="27695-293">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="27695-294">Sélectionne une plage de texte.</span><span class="sxs-lookup"><span data-stu-id="27695-294">Selects a text range.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="27695-295"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-togglepattern_toggle"><strong>TogglePattern_Toggle</strong></a></span><span class="sxs-lookup"><span data-stu-id="27695-295"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-togglepattern_toggle"><strong>TogglePattern_Toggle</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="27695-296">Cette fonction est déconseillée.</span><span class="sxs-lookup"><span data-stu-id="27695-296">This function is deprecated.</span></span> <span data-ttu-id="27695-297">Les applications clientes doivent utiliser les interfaces COM UI Automation à la place.</span><span class="sxs-lookup"><span data-stu-id="27695-297">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="27695-298">Bascule un contrôle à son prochain état pris en charge.</span><span class="sxs-lookup"><span data-stu-id="27695-298">Toggles a control to its next supported state.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="27695-299"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-transformpattern_move"><strong>TransformPattern_Move</strong></a></span><span class="sxs-lookup"><span data-stu-id="27695-299"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-transformpattern_move"><strong>TransformPattern_Move</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="27695-300">Cette fonction est déconseillée.</span><span class="sxs-lookup"><span data-stu-id="27695-300">This function is deprecated.</span></span> <span data-ttu-id="27695-301">Les applications clientes doivent utiliser les interfaces COM UI Automation à la place.</span><span class="sxs-lookup"><span data-stu-id="27695-301">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="27695-302">Déplace un élément à un emplacement spécifié sur l’écran.</span><span class="sxs-lookup"><span data-stu-id="27695-302">Moves an element to a specified location on the screen.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="27695-303"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-transformpattern_resize"><strong>TransformPattern_Resize</strong></a></span><span class="sxs-lookup"><span data-stu-id="27695-303"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-transformpattern_resize"><strong>TransformPattern_Resize</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="27695-304">Cette fonction est déconseillée.</span><span class="sxs-lookup"><span data-stu-id="27695-304">This function is deprecated.</span></span> <span data-ttu-id="27695-305">Les applications clientes doivent utiliser les interfaces COM UI Automation à la place.</span><span class="sxs-lookup"><span data-stu-id="27695-305">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="27695-306">Redimensionne un élément à l’écran.</span><span class="sxs-lookup"><span data-stu-id="27695-306">Resizes an element on the screen.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="27695-307"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-transformpattern_rotate"><strong>TransformPattern_Rotate</strong></a></span><span class="sxs-lookup"><span data-stu-id="27695-307"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-transformpattern_rotate"><strong>TransformPattern_Rotate</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="27695-308">Cette fonction est déconseillée.</span><span class="sxs-lookup"><span data-stu-id="27695-308">This function is deprecated.</span></span> <span data-ttu-id="27695-309">Les applications clientes doivent utiliser les interfaces COM UI Automation à la place.</span><span class="sxs-lookup"><span data-stu-id="27695-309">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="27695-310">Fait pivoter un élément à l’écran.</span><span class="sxs-lookup"><span data-stu-id="27695-310">Rotates an element on the screen.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="27695-311"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-valuepattern_setvalue"><strong>ValuePattern_SetValue</strong></a></span><span class="sxs-lookup"><span data-stu-id="27695-311"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-valuepattern_setvalue"><strong>ValuePattern_SetValue</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="27695-312">Cette fonction est déconseillée.</span><span class="sxs-lookup"><span data-stu-id="27695-312">This function is deprecated.</span></span> <span data-ttu-id="27695-313">Les applications clientes doivent utiliser les interfaces COM UI Automation à la place.</span><span class="sxs-lookup"><span data-stu-id="27695-313">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="27695-314">Définit la valeur de texte d’un élément.</span><span class="sxs-lookup"><span data-stu-id="27695-314">Sets the text value of an element.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="27695-315"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-virtualizeditempattern_realize"><strong>VirtualizedItemPattern_Realize</strong></a></span><span class="sxs-lookup"><span data-stu-id="27695-315"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-virtualizeditempattern_realize"><strong>VirtualizedItemPattern_Realize</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="27695-316">Cette fonction est déconseillée.</span><span class="sxs-lookup"><span data-stu-id="27695-316">This function is deprecated.</span></span> <span data-ttu-id="27695-317">Les applications clientes doivent utiliser les interfaces COM UI Automation à la place.</span><span class="sxs-lookup"><span data-stu-id="27695-317">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="27695-318">Rend l'élément virtuel totalement accessible en tant qu'élément UI Automation.</span><span class="sxs-lookup"><span data-stu-id="27695-318">Makes the virtual item fully accessible as a UI Automation element.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="27695-319"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-windowpattern_close"><strong>WindowPattern_Close</strong></a></span><span class="sxs-lookup"><span data-stu-id="27695-319"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-windowpattern_close"><strong>WindowPattern_Close</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="27695-320">Cette fonction est déconseillée.</span><span class="sxs-lookup"><span data-stu-id="27695-320">This function is deprecated.</span></span> <span data-ttu-id="27695-321">Les applications clientes doivent utiliser les interfaces COM UI Automation à la place.</span><span class="sxs-lookup"><span data-stu-id="27695-321">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="27695-322">Ferme une fenêtre ouverte.</span><span class="sxs-lookup"><span data-stu-id="27695-322">Closes an open window.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="27695-323"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-windowpattern_setwindowvisualstate"><strong>WindowPattern_SetWindowVisualState</strong></a></span><span class="sxs-lookup"><span data-stu-id="27695-323"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-windowpattern_setwindowvisualstate"><strong>WindowPattern_SetWindowVisualState</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="27695-324">Cette fonction est déconseillée.</span><span class="sxs-lookup"><span data-stu-id="27695-324">This function is deprecated.</span></span> <span data-ttu-id="27695-325">Les applications clientes doivent utiliser les interfaces COM UI Automation à la place.</span><span class="sxs-lookup"><span data-stu-id="27695-325">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="27695-326">Définit l’état visuel d’une fenêtre ; par exemple, pour agrandir une fenêtre.</span><span class="sxs-lookup"><span data-stu-id="27695-326">Sets the visual state of a window; for example, to maximize a window.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="27695-327"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-windowpattern_waitforinputidle"><strong>WindowPattern_WaitForInputIdle</strong></a></span><span class="sxs-lookup"><span data-stu-id="27695-327"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-windowpattern_waitforinputidle"><strong>WindowPattern_WaitForInputIdle</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="27695-328">Cette fonction est déconseillée.</span><span class="sxs-lookup"><span data-stu-id="27695-328">This function is deprecated.</span></span> <span data-ttu-id="27695-329">Les applications clientes doivent utiliser les interfaces COM UI Automation à la place.</span><span class="sxs-lookup"><span data-stu-id="27695-329">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="27695-330">Provoque le blocage du code appelant pendant la durée spécifiée ou jusqu’à ce que le processus associé bascule dans un état d’inactivité (en fonction de l’échéance la plus proche).</span><span class="sxs-lookup"><span data-stu-id="27695-330">Causes the calling code to block for the specified time or until the associated process enters an idle state, whichever completes first.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="27695-331">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="27695-331">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="27695-332">Clients UI Automation</span><span class="sxs-lookup"><span data-stu-id="27695-332">UI Automation Clients</span></span>](uiauto-entry-uiautoclientsforwin32apps.md)
</dt> </dl>

 

 





