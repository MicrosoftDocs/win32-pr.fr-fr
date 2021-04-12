---
title: ObjectModel (modèle de contrôle)
description: Fournit des instructions et des conventions pour l’implémentation de IObjectModelProvider, y compris des informations sur les méthodes. Le modèle de contrôle ObjectModel est utilisé pour exposer un pointeur vers le modèle objet sous-jacent d’un document.
ms.assetid: 90A6937E-0E98-41EF-8EEB-E23CB71510E4
keywords:
- UI Automation, implémentation du modèle de contrôle ObjectModel
- UI Automation, modèle de contrôle ObjectModel
- UI Automation, IObjectModelProvider
- IObjectModelProvider
- implémentation du modèle de contrôle ObjectModel d’UI Automation
- ObjectModel (modèle de contrôle)
- modèles de contrôle, IObjectModelProvider
- modèles de contrôle, implémenter UI Automation ObjectModel
- modèles de contrôle, ObjectModel
- interfaces, IObjectModelProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54ff115233faf19f93963153a0b2a0a1ff52c3f8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315780"
---
# <a name="objectmodel-control-pattern"></a><span data-ttu-id="6d72d-114">ObjectModel (modèle de contrôle)</span><span class="sxs-lookup"><span data-stu-id="6d72d-114">ObjectModel Control Pattern</span></span>

<span data-ttu-id="6d72d-115">Fournit des instructions et des conventions pour l’implémentation de [**IObjectModelProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iobjectmodelprovider), y compris des informations sur les méthodes.</span><span class="sxs-lookup"><span data-stu-id="6d72d-115">Describes guidelines and conventions for implementing [**IObjectModelProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iobjectmodelprovider), including information about methods.</span></span> <span data-ttu-id="6d72d-116">Le modèle de contrôle **ObjectModel** est utilisé pour exposer un pointeur vers le modèle objet sous-jacent d’un document.</span><span class="sxs-lookup"><span data-stu-id="6d72d-116">The **ObjectModel** control pattern is used to expose a pointer to the underlying object model of a document.</span></span>

<span data-ttu-id="6d72d-117">De nombreuses applications implémentent des modèles d’objets enrichis qui ajoutent une valeur au-delà de ce que fournit Microsoft UI Automation.</span><span class="sxs-lookup"><span data-stu-id="6d72d-117">Many applications implement rich object models that add value beyond what Microsoft UI Automation provides.</span></span> <span data-ttu-id="6d72d-118">Ce modèle de contrôle permet à un client de naviguer à partir d’un élément UI Automation dans le modèle objet sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="6d72d-118">This control pattern allows a client to navigate from a UI Automation element into the underlying object model.</span></span>

<span data-ttu-id="6d72d-119">Cette rubrique contient les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="6d72d-119">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="6d72d-120">Conventions et directives d'implémentation</span><span class="sxs-lookup"><span data-stu-id="6d72d-120">Implementation Guidelines and Conventions</span></span>](#implementation-guidelines-and-conventions)
-   [<span data-ttu-id="6d72d-121">Membres requis pour **IObjectModelProvider**</span><span class="sxs-lookup"><span data-stu-id="6d72d-121">Required Members for **IObjectModelProvider**</span></span>](#required-members-for-iobjectmodelprovider)
-   [<span data-ttu-id="6d72d-122">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="6d72d-122">Related topics</span></span>](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a><span data-ttu-id="6d72d-123">Conventions et directives d'implémentation</span><span class="sxs-lookup"><span data-stu-id="6d72d-123">Implementation Guidelines and Conventions</span></span>

<span data-ttu-id="6d72d-124">Lorsque vous implémentez le modèle de contrôle **ObjectModel** , notez les conventions et recommandations suivantes :</span><span class="sxs-lookup"><span data-stu-id="6d72d-124">When implementing the **ObjectModel** control pattern, note the following guidelines and conventions:</span></span>

-   <span data-ttu-id="6d72d-125">La méthode [**IObjectModelProvider :: GetUnderlyingObjectModel**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-iobjectmodelprovider-getunderlyingobjectmodel) doit retourner un pointeur vers l’objet le plus proche possible de l’élément d’interface utilisateur source.</span><span class="sxs-lookup"><span data-stu-id="6d72d-125">The [**IObjectModelProvider::GetUnderlyingObjectModel**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-iobjectmodelprovider-getunderlyingobjectmodel) method should return a pointer to the object that is as close as possible to the source UI element.</span></span> <span data-ttu-id="6d72d-126">Par exemple, dans un navigateur Web, un fournisseur UI Automation pour un élément unique doit retourner un pointeur de modèle objet pour l’élément.</span><span class="sxs-lookup"><span data-stu-id="6d72d-126">For example, in a web browser, a UI Automation provider for a single element should return an object model pointer for the element.</span></span> <span data-ttu-id="6d72d-127">Le retour d’un pointeur de modèle objet pour la racine du document serait beaucoup moins utile.</span><span class="sxs-lookup"><span data-stu-id="6d72d-127">Returning an object model pointer for the document root would be far less useful.</span></span>
-   <span data-ttu-id="6d72d-128">Le client du modèle de contrôle **ObjectModel** est supposé avoir l’IID pour l’interface qu’il recherche, ce qui explique pourquoi il suffit de retourner un pointeur [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) simple.</span><span class="sxs-lookup"><span data-stu-id="6d72d-128">The client of the **ObjectModel** control pattern is expected to have the IID for the interface they are seeking, which is why it is enough to return a simple [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) pointer.</span></span>
-   <span data-ttu-id="6d72d-129">Dans la mesure où UI Automation marshale le pointeur vers le processus client, le fournisseur doit s’attendre à ce que le client accède au modèle objet à l’aide des pratiques COM (Component Object Model) standard.</span><span class="sxs-lookup"><span data-stu-id="6d72d-129">Because UI Automation marshals the pointer to the client process, the provider should expect the client to access the object model using standard Component Object Model (COM) practices.</span></span>

## <a name="required-members-for-iobjectmodelprovider"></a><span data-ttu-id="6d72d-130">Membres requis pour **IObjectModelProvider**</span><span class="sxs-lookup"><span data-stu-id="6d72d-130">Required Members for **IObjectModelProvider**</span></span>

<span data-ttu-id="6d72d-131">La méthode suivante est requise pour l’implémentation de l’interface [**IObjectModelProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iobjectmodelprovider) .</span><span class="sxs-lookup"><span data-stu-id="6d72d-131">The following method is required for implementing the [**IObjectModelProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iobjectmodelprovider) interface.</span></span>



| <span data-ttu-id="6d72d-132">Membres nécessaires</span><span class="sxs-lookup"><span data-stu-id="6d72d-132">Required members</span></span>                                                                             | <span data-ttu-id="6d72d-133">Type de membre</span><span class="sxs-lookup"><span data-stu-id="6d72d-133">Member type</span></span> | <span data-ttu-id="6d72d-134">Notes</span><span class="sxs-lookup"><span data-stu-id="6d72d-134">Notes</span></span>                                                                                                                                                                                                   |
|----------------------------------------------------------------------------------------------|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6d72d-135">**GetUnderlyingObjectModel**</span><span class="sxs-lookup"><span data-stu-id="6d72d-135">**GetUnderlyingObjectModel**</span></span>](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-iobjectmodelprovider-getunderlyingobjectmodel) | <span data-ttu-id="6d72d-136">Méthode</span><span class="sxs-lookup"><span data-stu-id="6d72d-136">Method</span></span>      | <span data-ttu-id="6d72d-137">Retourne un pointeur COM vers le modèle objet sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="6d72d-137">Returns a COM pointer to the underlying object model.</span></span> <span data-ttu-id="6d72d-138">Le client est censé appeler la méthode [**IUnknown :: QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) pour récupérer des pointeurs de modèle objet spécifiques.</span><span class="sxs-lookup"><span data-stu-id="6d72d-138">The client is expected to call the [**IUnknown::QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) method to retrieve specific object model pointers.</span></span> |



 

<span data-ttu-id="6d72d-139">Ce modèle de contrôle n’est associé aucun événement.</span><span class="sxs-lookup"><span data-stu-id="6d72d-139">This control pattern has no associated events.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6d72d-140">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="6d72d-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6d72d-141">Types de contrôle et leurs modèles de contrôle pris en charge</span><span class="sxs-lookup"><span data-stu-id="6d72d-141">Control Types and Their Supported Control Patterns</span></span>](uiauto-controlpatternmapping.md)
</dt> <dt>

[<span data-ttu-id="6d72d-142">Vue d'ensemble des modèles de contrôle UI Automation</span><span class="sxs-lookup"><span data-stu-id="6d72d-142">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> <dt>

[<span data-ttu-id="6d72d-143">Vue d’ensemble de l’arborescence UI Automation</span><span class="sxs-lookup"><span data-stu-id="6d72d-143">UI Automation Tree Overview</span></span>](uiauto-treeoverview.md)
</dt> </dl>

 

 