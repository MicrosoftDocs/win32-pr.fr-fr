---
title: Fonctions de nœud déconseillées
description: Fonctions de nœud déconseillées
ms.assetid: 72833757-a356-4727-8fc8-77a60e26aa99
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7273ffd6c704c9db6408165d1eba3a293f3d1cf
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/08/2020
ms.locfileid: "103941436"
---
# <a name="deprecated-node-functions"></a><span data-ttu-id="50b0e-103">Fonctions de nœud déconseillées</span><span class="sxs-lookup"><span data-stu-id="50b0e-103">Deprecated Node Functions</span></span>

> [!Note]  
> <span data-ttu-id="50b0e-104">Les fonctions de modèle de contrôle décrites dans cette section sont déconseillées.</span><span class="sxs-lookup"><span data-stu-id="50b0e-104">The control pattern functions described in this section are deprecated.</span></span> <span data-ttu-id="50b0e-105">Les applications clientes doivent utiliser les interfaces COM (Component Object Model) décrites dans les sections suivantes :</span><span class="sxs-lookup"><span data-stu-id="50b0e-105">Client applications should use the Component Object Model (COM) interfaces described in the following sections:</span></span>
>
> -   [<span data-ttu-id="50b0e-106">Interfaces d’élément UI Automation pour les clients</span><span class="sxs-lookup"><span data-stu-id="50b0e-106">UI Automation Element Interfaces for Clients</span></span>](uiauto-entry-uiautoclientinterfaces.md)
> -   [<span data-ttu-id="50b0e-107">Interface de condition de propriété pour les clients</span><span class="sxs-lookup"><span data-stu-id="50b0e-107">Property Condition Interface for Clients</span></span>](uiauto-client-propconditioninterfaces.md)
> -   [<span data-ttu-id="50b0e-108">Interfaces de modèle de contrôle pour les clients</span><span class="sxs-lookup"><span data-stu-id="50b0e-108">Control Pattern Interfaces for Clients</span></span>](uiauto-client-controlpatterninterfaces.md)
> -   [<span data-ttu-id="50b0e-109">Interfaces de gestion des événements pour les clients</span><span class="sxs-lookup"><span data-stu-id="50b0e-109">Event Handling Interfaces for Clients</span></span>](uiauto-client-eventhandlinginterfaces.md)
> -   [<span data-ttu-id="50b0e-110">Interfaces de fabrique proxy pour les clients</span><span class="sxs-lookup"><span data-stu-id="50b0e-110">Proxy Factory Interfaces for Clients</span></span>](uiauto-client-proxyfactoryinterfaces.md)

 

## <a name="in-this-section"></a><span data-ttu-id="50b0e-111">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="50b0e-111">In this section</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="50b0e-112">Fonction</span><span class="sxs-lookup"><span data-stu-id="50b0e-112">Function</span></span></th>
<th><span data-ttu-id="50b0e-113">Description</span><span class="sxs-lookup"><span data-stu-id="50b0e-113">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="50b0e-114"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaaddevent"><strong>UiaAddEvent</strong></a></span><span class="sxs-lookup"><span data-stu-id="50b0e-114"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaaddevent"><strong>UiaAddEvent</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="50b0e-115">Cette fonction est déconseillée.</span><span class="sxs-lookup"><span data-stu-id="50b0e-115">This function is deprecated.</span></span> <span data-ttu-id="50b0e-116">Les applications clientes doivent utiliser les interfaces COM UI Automation de Microsoft à la place.</span><span class="sxs-lookup"><span data-stu-id="50b0e-116">Client applications should use the Microsoft UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="50b0e-117">Ajoute un écouteur pour les événements sur un nœud dans l’arborescence UI Automation.</span><span class="sxs-lookup"><span data-stu-id="50b0e-117">Adds a listener for events on a node in the UI Automation tree.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="50b0e-118"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaeventaddwindow"><strong>UiaEventAddWindow</strong></a></span><span class="sxs-lookup"><span data-stu-id="50b0e-118"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaeventaddwindow"><strong>UiaEventAddWindow</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="50b0e-119">Cette fonction est déconseillée.</span><span class="sxs-lookup"><span data-stu-id="50b0e-119">This function is deprecated.</span></span> <span data-ttu-id="50b0e-120">Les applications clientes doivent utiliser les interfaces COM UI Automation à la place.</span><span class="sxs-lookup"><span data-stu-id="50b0e-120">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="50b0e-121">Ajoute une fenêtre à l’écouteur d’événements.</span><span class="sxs-lookup"><span data-stu-id="50b0e-121">Adds a window to the event listener.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="50b0e-122"><a href="/windows/desktop/api/UIAutomationCoreApi/nc-uiautomationcoreapi-uiaeventcallback"><em>UiaEventCallback</em></a></span><span class="sxs-lookup"><span data-stu-id="50b0e-122"><a href="/windows/desktop/api/UIAutomationCoreApi/nc-uiautomationcoreapi-uiaeventcallback"><em>UiaEventCallback</em></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="50b0e-123">Cette fonction est déconseillée.</span><span class="sxs-lookup"><span data-stu-id="50b0e-123">This function is deprecated.</span></span> <span data-ttu-id="50b0e-124">Les applications clientes doivent utiliser les interfaces COM UI Automation à la place.</span><span class="sxs-lookup"><span data-stu-id="50b0e-124">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="50b0e-125">Fonction implémentée par le client qui est appelée par UI Automation lorsqu’un événement est déclenché auquel le client s’est abonné.</span><span class="sxs-lookup"><span data-stu-id="50b0e-125">A client-implemented function that is called by UI Automation when an event is raised that the client has subscribed to.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="50b0e-126"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaeventremovewindow"><strong>UiaEventRemoveWindow</strong></a></span><span class="sxs-lookup"><span data-stu-id="50b0e-126"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaeventremovewindow"><strong>UiaEventRemoveWindow</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="50b0e-127">Cette fonction est déconseillée.</span><span class="sxs-lookup"><span data-stu-id="50b0e-127">This function is deprecated.</span></span> <span data-ttu-id="50b0e-128">Les applications clientes doivent utiliser les interfaces COM UI Automation à la place.</span><span class="sxs-lookup"><span data-stu-id="50b0e-128">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="50b0e-129">Supprime une fenêtre de l’écouteur d’événements.</span><span class="sxs-lookup"><span data-stu-id="50b0e-129">Removes a window from the event listener.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="50b0e-130"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiafind"><strong>UiaFind</strong></a></span><span class="sxs-lookup"><span data-stu-id="50b0e-130"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiafind"><strong>UiaFind</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="50b0e-131">Cette fonction est déconseillée.</span><span class="sxs-lookup"><span data-stu-id="50b0e-131">This function is deprecated.</span></span> <span data-ttu-id="50b0e-132">Les applications clientes doivent utiliser les interfaces COM UI Automation à la place.</span><span class="sxs-lookup"><span data-stu-id="50b0e-132">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="50b0e-133">Récupère un ou plusieurs nœuds UI Automation qui correspondent aux critères de recherche.</span><span class="sxs-lookup"><span data-stu-id="50b0e-133">Retrieves one or more UI Automation nodes that match the search criteria.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="50b0e-134"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiageterrordescription"><strong>UiaGetErrorDescription</strong></a></span><span class="sxs-lookup"><span data-stu-id="50b0e-134"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiageterrordescription"><strong>UiaGetErrorDescription</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="50b0e-135">Cette fonction est déconseillée.</span><span class="sxs-lookup"><span data-stu-id="50b0e-135">This function is deprecated.</span></span> <span data-ttu-id="50b0e-136">Les applications clientes doivent utiliser les interfaces COM UI Automation à la place.</span><span class="sxs-lookup"><span data-stu-id="50b0e-136">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="50b0e-137">Obtient une chaîne d’erreur pour qu’elle puisse être passée au client.</span><span class="sxs-lookup"><span data-stu-id="50b0e-137">Gets an error string so that it can be passed to the client.</span></span> <span data-ttu-id="50b0e-138">Cette méthode n’est pas utilisée directement par les clients.</span><span class="sxs-lookup"><span data-stu-id="50b0e-138">This method is not used directly by clients.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="50b0e-139"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiagetpatternprovider"><strong>UiaGetPatternProvider</strong></a></span><span class="sxs-lookup"><span data-stu-id="50b0e-139"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiagetpatternprovider"><strong>UiaGetPatternProvider</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="50b0e-140">Cette fonction est déconseillée.</span><span class="sxs-lookup"><span data-stu-id="50b0e-140">This function is deprecated.</span></span> <span data-ttu-id="50b0e-141">Les applications clientes doivent utiliser les interfaces COM UI Automation à la place.</span><span class="sxs-lookup"><span data-stu-id="50b0e-141">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="50b0e-142">Récupère un <em>modèle de contrôle</em>.</span><span class="sxs-lookup"><span data-stu-id="50b0e-142">Retrieves a <em>control pattern</em>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="50b0e-143"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiagetpropertyvalue"><strong>UiaGetPropertyValue</strong></a></span><span class="sxs-lookup"><span data-stu-id="50b0e-143"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiagetpropertyvalue"><strong>UiaGetPropertyValue</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="50b0e-144">Cette fonction est déconseillée.</span><span class="sxs-lookup"><span data-stu-id="50b0e-144">This function is deprecated.</span></span> <span data-ttu-id="50b0e-145">Les applications clientes doivent utiliser les interfaces COM UI Automation à la place.</span><span class="sxs-lookup"><span data-stu-id="50b0e-145">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="50b0e-146">Récupère la valeur d’une propriété UI Automation.</span><span class="sxs-lookup"><span data-stu-id="50b0e-146">Retrieves the value of a UI Automation property.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="50b0e-147"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiagetrootnode"><strong>UiaGetRootNode</strong></a></span><span class="sxs-lookup"><span data-stu-id="50b0e-147"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiagetrootnode"><strong>UiaGetRootNode</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="50b0e-148">Cette fonction est déconseillée.</span><span class="sxs-lookup"><span data-stu-id="50b0e-148">This function is deprecated.</span></span> <span data-ttu-id="50b0e-149">Les applications clientes doivent utiliser les interfaces COM UI Automation à la place.</span><span class="sxs-lookup"><span data-stu-id="50b0e-149">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="50b0e-150">Récupère le nœud UI Automation racine.</span><span class="sxs-lookup"><span data-stu-id="50b0e-150">Retrieves the root UI Automation node.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="50b0e-151"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiagetruntimeid"><strong>UiaGetRuntimeId</strong></a></span><span class="sxs-lookup"><span data-stu-id="50b0e-151"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiagetruntimeid"><strong>UiaGetRuntimeId</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="50b0e-152">Cette fonction est déconseillée.</span><span class="sxs-lookup"><span data-stu-id="50b0e-152">This function is deprecated.</span></span> <span data-ttu-id="50b0e-153">Les applications clientes doivent utiliser les interfaces COM UI Automation à la place.</span><span class="sxs-lookup"><span data-stu-id="50b0e-153">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="50b0e-154">Récupère l’identificateur d’exécution d’un nœud UI Automation.</span><span class="sxs-lookup"><span data-stu-id="50b0e-154">Retrieves the runtime identifier of a UI Automation node.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="50b0e-155"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiagetupdatedcache"><strong>UiaGetUpdatedCache</strong></a></span><span class="sxs-lookup"><span data-stu-id="50b0e-155"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiagetupdatedcache"><strong>UiaGetUpdatedCache</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="50b0e-156">Cette fonction est déconseillée.</span><span class="sxs-lookup"><span data-stu-id="50b0e-156">This function is deprecated.</span></span> <span data-ttu-id="50b0e-157">Les applications clientes doivent utiliser les interfaces COM UI Automation à la place.</span><span class="sxs-lookup"><span data-stu-id="50b0e-157">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="50b0e-158">Met à jour le cache des valeurs de propriété et des modèles de contrôle.</span><span class="sxs-lookup"><span data-stu-id="50b0e-158">Updates the cache of property values and control patterns.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="50b0e-159"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiahpatternobjectfromvariant"><strong>UiaHPatternObjectFromVariant</strong></a></span><span class="sxs-lookup"><span data-stu-id="50b0e-159"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiahpatternobjectfromvariant"><strong>UiaHPatternObjectFromVariant</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="50b0e-160">Cette fonction est déconseillée.</span><span class="sxs-lookup"><span data-stu-id="50b0e-160">This function is deprecated.</span></span> <span data-ttu-id="50b0e-161">Les applications clientes doivent utiliser les interfaces COM UI Automation à la place.</span><span class="sxs-lookup"><span data-stu-id="50b0e-161">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="50b0e-162">Obtient un objet de modèle de contrôle à partir d’un type <a href="/windows/win32/api/oaidl/ns-oaidl-variant"><strong>Variant</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="50b0e-162">Gets a control pattern object from a <a href="/windows/win32/api/oaidl/ns-oaidl-variant"><strong>VARIANT</strong></a> type.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="50b0e-163"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiahtextrangefromvariant"><strong>UiaHTextRangeFromVariant</strong></a></span><span class="sxs-lookup"><span data-stu-id="50b0e-163"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiahtextrangefromvariant"><strong>UiaHTextRangeFromVariant</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="50b0e-164">Cette fonction est déconseillée.</span><span class="sxs-lookup"><span data-stu-id="50b0e-164">This function is deprecated.</span></span> <span data-ttu-id="50b0e-165">Les applications clientes doivent utiliser les interfaces COM UI Automation à la place.</span><span class="sxs-lookup"><span data-stu-id="50b0e-165">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="50b0e-166">Obtient une plage de texte à partir d’un type <a href="/windows/win32/api/oaidl/ns-oaidl-variant"><strong>Variant</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="50b0e-166">Gets a text range from a <a href="/windows/win32/api/oaidl/ns-oaidl-variant"><strong>VARIANT</strong></a> type.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="50b0e-167"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiahuianodefromvariant"><strong>UiaHUiaNodeFromVariant</strong></a></span><span class="sxs-lookup"><span data-stu-id="50b0e-167"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiahuianodefromvariant"><strong>UiaHUiaNodeFromVariant</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="50b0e-168">Cette fonction est déconseillée.</span><span class="sxs-lookup"><span data-stu-id="50b0e-168">This function is deprecated.</span></span> <span data-ttu-id="50b0e-169">Les applications clientes doivent utiliser les interfaces COM UI Automation à la place.</span><span class="sxs-lookup"><span data-stu-id="50b0e-169">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="50b0e-170">Obtient un HUIANODE à partir d’un type <a href="/windows/win32/api/oaidl/ns-oaidl-variant"><strong>Variant</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="50b0e-170">Gets an HUIANODE from a <a href="/windows/win32/api/oaidl/ns-oaidl-variant"><strong>VARIANT</strong></a> type.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="50b0e-171"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uialookupid"><strong>UiaLookupId</strong></a></span><span class="sxs-lookup"><span data-stu-id="50b0e-171"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uialookupid"><strong>UiaLookupId</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="50b0e-172">Cette fonction est déconseillée.</span><span class="sxs-lookup"><span data-stu-id="50b0e-172">This function is deprecated.</span></span> <span data-ttu-id="50b0e-173">Les applications clientes doivent utiliser les interfaces COM UI Automation à la place.</span><span class="sxs-lookup"><span data-stu-id="50b0e-173">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="50b0e-174">Obtient l’identificateur entier qui peut être utilisé dans les méthodes qui requièrent un PROPERTYID, PATTERNID, CONTROLTYPEID, TEXTATTRIBUTEID ou EVENTID.</span><span class="sxs-lookup"><span data-stu-id="50b0e-174">Gets the integer identifier that can be used in methods that require a PROPERTYID, PATTERNID, CONTROLTYPEID, TEXTATTRIBUTEID, or EVENTID.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="50b0e-175"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uianavigate"><strong>UiaNavigate</strong></a></span><span class="sxs-lookup"><span data-stu-id="50b0e-175"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uianavigate"><strong>UiaNavigate</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="50b0e-176">Cette fonction est déconseillée.</span><span class="sxs-lookup"><span data-stu-id="50b0e-176">This function is deprecated.</span></span> <span data-ttu-id="50b0e-177">Les applications clientes doivent utiliser les interfaces COM UI Automation à la place.</span><span class="sxs-lookup"><span data-stu-id="50b0e-177">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="50b0e-178">Navigue dans l’arborescence UI Automation, en extrayant éventuellement les informations mises en cache.</span><span class="sxs-lookup"><span data-stu-id="50b0e-178">Navigates in the UI Automation tree, optionally retrieving cached information.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="50b0e-179"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uianodefromfocus"><strong>UiaNodeFromFocus</strong></a></span><span class="sxs-lookup"><span data-stu-id="50b0e-179"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uianodefromfocus"><strong>UiaNodeFromFocus</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="50b0e-180">Cette fonction est déconseillée.</span><span class="sxs-lookup"><span data-stu-id="50b0e-180">This function is deprecated.</span></span> <span data-ttu-id="50b0e-181">Les applications clientes doivent utiliser les interfaces COM UI Automation à la place.</span><span class="sxs-lookup"><span data-stu-id="50b0e-181">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="50b0e-182">Récupère le nœud UI Automation pour l’élément d’interface utilisateur qui a actuellement le focus d’entrée.</span><span class="sxs-lookup"><span data-stu-id="50b0e-182">Retrieves the UI Automation node for the UI element that currently has input focus.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="50b0e-183"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uianodefromhandle"><strong>UiaNodeFromHandle</strong></a></span><span class="sxs-lookup"><span data-stu-id="50b0e-183"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uianodefromhandle"><strong>UiaNodeFromHandle</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="50b0e-184">Cette fonction est déconseillée.</span><span class="sxs-lookup"><span data-stu-id="50b0e-184">This function is deprecated.</span></span> <span data-ttu-id="50b0e-185">Les applications clientes doivent utiliser les interfaces COM UI Automation à la place.</span><span class="sxs-lookup"><span data-stu-id="50b0e-185">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="50b0e-186">Récupère le nœud UI Automation associé à une fenêtre.</span><span class="sxs-lookup"><span data-stu-id="50b0e-186">Retrieves the UI Automation node associated with a window.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="50b0e-187"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uianodefrompoint"><strong>UiaNodeFromPoint</strong></a></span><span class="sxs-lookup"><span data-stu-id="50b0e-187"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uianodefrompoint"><strong>UiaNodeFromPoint</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="50b0e-188">Cette fonction est déconseillée.</span><span class="sxs-lookup"><span data-stu-id="50b0e-188">This function is deprecated.</span></span> <span data-ttu-id="50b0e-189">Les applications clientes doivent utiliser les interfaces COM UI Automation à la place.</span><span class="sxs-lookup"><span data-stu-id="50b0e-189">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="50b0e-190">Récupère le nœud UI Automation pour l’élément au point spécifié.</span><span class="sxs-lookup"><span data-stu-id="50b0e-190">Retrieves the UI Automation node for the element at the specified point.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="50b0e-191"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uianodefromprovider"><strong>UiaNodeFromProvider</strong></a></span><span class="sxs-lookup"><span data-stu-id="50b0e-191"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uianodefromprovider"><strong>UiaNodeFromProvider</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="50b0e-192">Cette fonction est déconseillée.</span><span class="sxs-lookup"><span data-stu-id="50b0e-192">This function is deprecated.</span></span> <span data-ttu-id="50b0e-193">Les applications clientes doivent utiliser les interfaces COM UI Automation à la place.</span><span class="sxs-lookup"><span data-stu-id="50b0e-193">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="50b0e-194">Récupère le nœud UI Automation pour un fournisseur d’éléments bruts.</span><span class="sxs-lookup"><span data-stu-id="50b0e-194">Retrieves the UI Automation node for a raw element provider.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="50b0e-195"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uianoderelease"><strong>UiaNodeRelease</strong></a></span><span class="sxs-lookup"><span data-stu-id="50b0e-195"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uianoderelease"><strong>UiaNodeRelease</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="50b0e-196">Cette fonction est déconseillée.</span><span class="sxs-lookup"><span data-stu-id="50b0e-196">This function is deprecated.</span></span> <span data-ttu-id="50b0e-197">Les applications clientes doivent utiliser les interfaces COM UI Automation à la place.</span><span class="sxs-lookup"><span data-stu-id="50b0e-197">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="50b0e-198">Supprime un nœud de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="50b0e-198">Deletes a node from memory.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="50b0e-199"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiapatternrelease"><strong>UiaPatternRelease</strong></a></span><span class="sxs-lookup"><span data-stu-id="50b0e-199"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiapatternrelease"><strong>UiaPatternRelease</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="50b0e-200">Cette fonction est déconseillée.</span><span class="sxs-lookup"><span data-stu-id="50b0e-200">This function is deprecated.</span></span> <span data-ttu-id="50b0e-201">Les applications clientes doivent utiliser les interfaces COM UI Automation à la place.</span><span class="sxs-lookup"><span data-stu-id="50b0e-201">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="50b0e-202">Supprime un objet de modèle alloué de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="50b0e-202">Deletes an allocated pattern object from memory.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="50b0e-203"><a href="/windows/desktop/api/UIAutomationCoreApi/nc-uiautomationcoreapi-uiaprovidercallback"><em>UiaProviderCallback</em></a></span><span class="sxs-lookup"><span data-stu-id="50b0e-203"><a href="/windows/desktop/api/UIAutomationCoreApi/nc-uiautomationcoreapi-uiaprovidercallback"><em>UiaProviderCallback</em></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="50b0e-204">Cette fonction est déconseillée.</span><span class="sxs-lookup"><span data-stu-id="50b0e-204">This function is deprecated.</span></span> <span data-ttu-id="50b0e-205">Les applications clientes doivent utiliser les interfaces COM UI Automation à la place.</span><span class="sxs-lookup"><span data-stu-id="50b0e-205">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="50b0e-206">Fonction définie par l’application qui est appelée par UI Automation pour obtenir un fournisseur côté client pour un élément.</span><span class="sxs-lookup"><span data-stu-id="50b0e-206">An application-defined function that is called by UI Automation to obtain a client-side provider for an element.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="50b0e-207"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiarectisempty"><strong>UiaRectIsEmpty</strong></a></span><span class="sxs-lookup"><span data-stu-id="50b0e-207"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiarectisempty"><strong>UiaRectIsEmpty</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="50b0e-208">Cette fonction est déconseillée.</span><span class="sxs-lookup"><span data-stu-id="50b0e-208">This function is deprecated.</span></span> <span data-ttu-id="50b0e-209">Les applications clientes doivent utiliser les interfaces COM UI Automation à la place.</span><span class="sxs-lookup"><span data-stu-id="50b0e-209">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="50b0e-210">Obtient une valeur booléenne qui spécifie si les coordonnées de tous les rectangles sont égales à 0.</span><span class="sxs-lookup"><span data-stu-id="50b0e-210">Gets a Boolean value that specifies whether a rectangle has all its coordinates set to 0.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="50b0e-211"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiarectsetempty"><strong>UiaRectSetEmpty</strong></a></span><span class="sxs-lookup"><span data-stu-id="50b0e-211"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiarectsetempty"><strong>UiaRectSetEmpty</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="50b0e-212">Cette fonction est déconseillée.</span><span class="sxs-lookup"><span data-stu-id="50b0e-212">This function is deprecated.</span></span> <span data-ttu-id="50b0e-213">Les applications clientes doivent utiliser les interfaces COM UI Automation à la place.</span><span class="sxs-lookup"><span data-stu-id="50b0e-213">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="50b0e-214">Affecte la valeur 0 aux éléments d’une structure <a href="/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiarect"><strong>UiaRect</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="50b0e-214">Sets the elements of a <a href="/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiarect"><strong>UiaRect</strong></a> structure to 0.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="50b0e-215"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaregisterprovidercallback"><strong>UiaRegisterProviderCallback</strong></a></span><span class="sxs-lookup"><span data-stu-id="50b0e-215"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaregisterprovidercallback"><strong>UiaRegisterProviderCallback</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="50b0e-216">Cette fonction est déconseillée.</span><span class="sxs-lookup"><span data-stu-id="50b0e-216">This function is deprecated.</span></span> <span data-ttu-id="50b0e-217">Les applications clientes doivent utiliser les interfaces COM UI Automation à la place.</span><span class="sxs-lookup"><span data-stu-id="50b0e-217">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="50b0e-218">Inscrit la méthode définie par l’application qui est appelée par UI Automation pour obtenir un fournisseur pour un élément.</span><span class="sxs-lookup"><span data-stu-id="50b0e-218">Registers the application-defined method that is called by UI Automation to obtain a provider for an element.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="50b0e-219"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaremoveevent"><strong>UiaRemoveEvent</strong></a></span><span class="sxs-lookup"><span data-stu-id="50b0e-219"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaremoveevent"><strong>UiaRemoveEvent</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="50b0e-220">Cette fonction est déconseillée.</span><span class="sxs-lookup"><span data-stu-id="50b0e-220">This function is deprecated.</span></span> <span data-ttu-id="50b0e-221">Les applications clientes doivent utiliser les interfaces COM UI Automation à la place.</span><span class="sxs-lookup"><span data-stu-id="50b0e-221">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="50b0e-222">Supprime un écouteur pour les événements sur un nœud dans l’arborescence UI Automation.</span><span class="sxs-lookup"><span data-stu-id="50b0e-222">Removes a listener for events on a node in the UI Automation tree.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="50b0e-223"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiasetfocus"><strong>UiaSetFocus</strong></a></span><span class="sxs-lookup"><span data-stu-id="50b0e-223"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiasetfocus"><strong>UiaSetFocus</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="50b0e-224">Cette fonction est déconseillée.</span><span class="sxs-lookup"><span data-stu-id="50b0e-224">This function is deprecated.</span></span> <span data-ttu-id="50b0e-225">Les applications clientes doivent utiliser les interfaces COM UI Automation à la place.</span><span class="sxs-lookup"><span data-stu-id="50b0e-225">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="50b0e-226">Définit le focus d’entrée sur l’élément spécifié dans l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="50b0e-226">Sets the input focus to the specified element in the UI.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="50b0e-227"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiatextrangerelease"><strong>UiaTextRangeRelease</strong></a></span><span class="sxs-lookup"><span data-stu-id="50b0e-227"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiatextrangerelease"><strong>UiaTextRangeRelease</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="50b0e-228">Cette fonction est déconseillée.</span><span class="sxs-lookup"><span data-stu-id="50b0e-228">This function is deprecated.</span></span> <span data-ttu-id="50b0e-229">Les applications clientes doivent utiliser les interfaces COM UI Automation à la place.</span><span class="sxs-lookup"><span data-stu-id="50b0e-229">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="50b0e-230">Supprime un objet de la plage de texte allouée de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="50b0e-230">Deletes an allocated text range object from memory.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="50b0e-231">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="50b0e-231">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="50b0e-232">Clients UI Automation</span><span class="sxs-lookup"><span data-stu-id="50b0e-232">UI Automation Clients</span></span>](uiauto-entry-uiautoclientsforwin32apps.md)
</dt> </dl>

 

