---
title: Inscrire des propriétés personnalisées, des événements et des modèles de contrôle
description: Avant qu’une propriété, un événement ou un modèle de contrôle personnalisé puisse être utilisé, le fournisseur et le client doivent inscrire la propriété, l’événement ou le modèle de contrôle au moment de l’exécution.
ms.assetid: ae36e404-8432-46ed-930e-b86dd5a88d6d
keywords:
- UI Automation, propriétés personnalisées
- UI Automation, vue d’ensemble des événements
- UI Automation, vue d’ensemble des modèles de contrôle
- UI Automation, inscrire des propriétés personnalisées
- UI Automation, inscrire des événements
- UI Automation, inscrire des modèles de contrôle
- Propriétés personnalisées, inscrire
- événements, inscription
- modèles de contrôle, inscrire
- inscription, propriétés personnalisées
- inscription, événements
- inscription, modèles de contrôle
- modèles de contrôle, personnalisés
- modèles de contrôle, implémenter un personnalisé
- implémentation de modèles de contrôle personnalisés
- modèles de contrôle personnalisés
- wrappers client
- gestionnaires de modèles
- implémentation de gestionnaires de modèles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b6b157e8f08a2c0be74af6b9f53d3578d1e4d03
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031680"
---
# <a name="register-custom-properties-events-and-control-patterns"></a><span data-ttu-id="fb6ea-122">Inscrire des propriétés personnalisées, des événements et des modèles de contrôle</span><span class="sxs-lookup"><span data-stu-id="fb6ea-122">Register custom properties, events, and control patterns</span></span>

<span data-ttu-id="fb6ea-123">Avant qu’une propriété, un événement ou un modèle de contrôle personnalisé puisse être utilisé, le fournisseur et le client doivent inscrire la propriété, l’événement ou le modèle de contrôle au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="fb6ea-123">Before a custom property, event, or control pattern can be used, both the provider and the client must register the property, event, or control pattern at run time.</span></span> <span data-ttu-id="fb6ea-124">L’inscription est effective de manière globale au sein d’un processus d’application et reste effective jusqu’à ce que le processus se ferme ou que le dernier objet d’élément d’automatisation de l’interface utilisateur de Microsoft ([**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) ou [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple)) soit publié au sein du processus.</span><span class="sxs-lookup"><span data-stu-id="fb6ea-124">The registration is effective globally within an application process, and remains effective until the process closes or the last Microsoft UI Automation element object ([**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) or [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple)) is released within the process.</span></span>

<span data-ttu-id="fb6ea-125">Le registre implique de passer un GUID à UI Automation, ainsi que des informations détaillées sur la propriété personnalisée, l’événement ou le modèle de contrôle.</span><span class="sxs-lookup"><span data-stu-id="fb6ea-125">Registation involves passing a GUID to UI Automation, along with detailed information about the custom property, event, or control pattern.</span></span> <span data-ttu-id="fb6ea-126">La tentative d’enregistrement du même GUID une deuxième fois avec les mêmes informations réussira, mais la tentative d’enregistrement d’un même GUID une deuxième fois, mais avec des informations différentes (par exemple, une propriété personnalisée d’un type différent) échouera.</span><span class="sxs-lookup"><span data-stu-id="fb6ea-126">Attempting to register the same GUID a second time with the same information will succeed, but attempting to register the same GUID a second time but with different information (for example, a custom property of a different type) will fail.</span></span> <span data-ttu-id="fb6ea-127">À l’avenir, si la spécification personnalisée est acceptée et intégrée dans le noyau UI Automation, l’automatisation d’interface utilisateur validera les informations d’inscription personnalisées et utilisera le code déjà inscrit au lieu de l’implémentation du Framework « officiel », réduisant ainsi les problèmes de compatibilité des applications.</span><span class="sxs-lookup"><span data-stu-id="fb6ea-127">In the future, if the custom specification is accepted and integrated into the UI Automation core, UI Automation will validate the custom registration information and use the already registered code instead of the "official" framework implementation, thereby minimizing application compatibility issues.</span></span> <span data-ttu-id="fb6ea-128">Vous ne pouvez pas supprimer des propriétés, des événements ou des modèles de contrôle déjà inscrits.</span><span class="sxs-lookup"><span data-stu-id="fb6ea-128">You cannot remove properties, events, or control patterns that are already registered.</span></span>

<span data-ttu-id="fb6ea-129">Cette rubrique contient les sections suivantes :</span><span class="sxs-lookup"><span data-stu-id="fb6ea-129">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="fb6ea-130">Enregistrement des propriétés et des événements personnalisés</span><span class="sxs-lookup"><span data-stu-id="fb6ea-130">Registering Custom Properties and Events</span></span>](#registering-custom-properties-and-events)
-   [<span data-ttu-id="fb6ea-131">Implémentation de modèles de contrôle personnalisés</span><span class="sxs-lookup"><span data-stu-id="fb6ea-131">Implementing Custom Control Patterns</span></span>](#implementing-custom-control-patterns)
    -   [<span data-ttu-id="fb6ea-132">Le wrapper client et le gestionnaire de modèle</span><span class="sxs-lookup"><span data-stu-id="fb6ea-132">The Client Wrapper and the Pattern Handler</span></span>](#the-client-wrapper-and-the-pattern-handler)
    -   [<span data-ttu-id="fb6ea-133">Implémentation du wrapper client</span><span class="sxs-lookup"><span data-stu-id="fb6ea-133">Implementing the Client Wrapper</span></span>](#implementing-the-client-wrapper)
    -   [<span data-ttu-id="fb6ea-134">Implémentation du gestionnaire de modèles</span><span class="sxs-lookup"><span data-stu-id="fb6ea-134">Implementing the Pattern Handler</span></span>](#implementing-the-pattern-handler)
    -   [<span data-ttu-id="fb6ea-135">Inscription d’un modèle de contrôle personnalisé</span><span class="sxs-lookup"><span data-stu-id="fb6ea-135">Registering a Custom Control Pattern</span></span>](#registering-a-custom-control-pattern)
    -   [<span data-ttu-id="fb6ea-136">Exemple d’implémentation d’un modèle de contrôle personnalisé</span><span class="sxs-lookup"><span data-stu-id="fb6ea-136">Example Implementation of a Custom Control Pattern</span></span>](#example-implementation-of-a-custom-control-pattern)
-   [<span data-ttu-id="fb6ea-137">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="fb6ea-137">Related topics</span></span>](#related-topics)

## <a name="registering-custom-properties-and-events"></a><span data-ttu-id="fb6ea-138">Enregistrement des propriétés et des événements personnalisés</span><span class="sxs-lookup"><span data-stu-id="fb6ea-138">Registering Custom Properties and Events</span></span>

<span data-ttu-id="fb6ea-139">L’inscription d’une propriété ou d’un événement personnalisé permet au fournisseur et au client d’obtenir un ID pour la propriété ou l’événement, qui peut ensuite être passé à différentes méthodes d’API qui prennent des ID en tant que paramètres.</span><span class="sxs-lookup"><span data-stu-id="fb6ea-139">Registering a custom property or event enables the provider and client to obtain an ID for the property or event, which can then be passed to various API methods that take IDs as parameters.</span></span>

<span data-ttu-id="fb6ea-140">Pour enregistrer une propriété ou un événement :</span><span class="sxs-lookup"><span data-stu-id="fb6ea-140">To register a property or event:</span></span>

1.  <span data-ttu-id="fb6ea-141">Définissez un GUID pour la propriété ou l’événement personnalisé.</span><span class="sxs-lookup"><span data-stu-id="fb6ea-141">Define a GUID for the custom property or event.</span></span>
2.  <span data-ttu-id="fb6ea-142">Remplissez un [**UIAutomationPropertyInfo**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationpropertyinfo) ou une structure [**UIAutomationEventInfo**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationeventinfo) avec des informations sur la propriété ou l’événement, y compris le GUID et une chaîne non localisable contenant le nom de la propriété ou de l’événement personnalisé.</span><span class="sxs-lookup"><span data-stu-id="fb6ea-142">Fill a [**UIAutomationPropertyInfo**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationpropertyinfo) or a [**UIAutomationEventInfo**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationeventinfo) structure with information about the property or event, including the GUID and a nonlocalizable string that contains the name of the custom property or event.</span></span> <span data-ttu-id="fb6ea-143">Les propriétés personnalisées nécessitent également que le type de données de la propriété soit spécifié, par exemple, si la propriété contient un entier ou une chaîne.</span><span class="sxs-lookup"><span data-stu-id="fb6ea-143">Custom properties also require the data type of the property to be specified, for example, whether the property holds an integer or a string.</span></span> <span data-ttu-id="fb6ea-144">Le type de données doit être l’un des types suivants spécifiés par l’énumération [**UIAutomationType**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-uiautomationtype) .</span><span class="sxs-lookup"><span data-stu-id="fb6ea-144">The data type must be one of the following types specified by the [**UIAutomationType**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-uiautomationtype) enumeration.</span></span> <span data-ttu-id="fb6ea-145">Aucun autre type de données n’est pris en charge pour les propriétés personnalisées.</span><span class="sxs-lookup"><span data-stu-id="fb6ea-145">No other data types are supported for custom properties.</span></span>
    -   <span data-ttu-id="fb6ea-146">**UIAutomationType \_ bool**</span><span class="sxs-lookup"><span data-stu-id="fb6ea-146">**UIAutomationType\_Bool**</span></span>
    -   <span data-ttu-id="fb6ea-147">**UIAutomationType \_ double**</span><span class="sxs-lookup"><span data-stu-id="fb6ea-147">**UIAutomationType\_Double**</span></span>
    -   <span data-ttu-id="fb6ea-148">**\_Élément UIAutomationType**</span><span class="sxs-lookup"><span data-stu-id="fb6ea-148">**UIAutomationType\_Element**</span></span>
    -   <span data-ttu-id="fb6ea-149">**UIAutomationType \_ int**</span><span class="sxs-lookup"><span data-stu-id="fb6ea-149">**UIAutomationType\_Int**</span></span>
    -   <span data-ttu-id="fb6ea-150">**\_Point UIAutomationType**</span><span class="sxs-lookup"><span data-stu-id="fb6ea-150">**UIAutomationType\_Point**</span></span>
    -   <span data-ttu-id="fb6ea-151">**\_Chaîne UIAutomationType**</span><span class="sxs-lookup"><span data-stu-id="fb6ea-151">**UIAutomationType\_String**</span></span>
3.  <span data-ttu-id="fb6ea-152">Utilisez la fonction [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) pour créer une instance de l’objet [**CUIAutomationRegistrar**](/previous-versions/windows/desktop/legacy/ff384837(v=vs.85)) et récupérer un pointeur vers l’interface [**IUIAutomationRegistrar**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationregistrar) de l’objet.</span><span class="sxs-lookup"><span data-stu-id="fb6ea-152">Use the [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) function to create an instance of the [**CUIAutomationRegistrar**](/previous-versions/windows/desktop/legacy/ff384837(v=vs.85)) object and retrieve a pointer to the object's [**IUIAutomationRegistrar**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationregistrar) interface.</span></span>
4.  <span data-ttu-id="fb6ea-153">Appelez la méthode [**IUIAutomationRegistrar :: RegisterProperty**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerproperty) ou [**RegisterEvent**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerevent) et transmettez l’adresse de la structure [**UIAutomationPropertyInfo**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationpropertyinfo) ou de la structure [**UIAutomationEventInfo**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationeventinfo) .</span><span class="sxs-lookup"><span data-stu-id="fb6ea-153">Call the [**IUIAutomationRegistrar::RegisterProperty**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerproperty) or [**RegisterEvent**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerevent) method and pass the address of the [**UIAutomationPropertyInfo**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationpropertyinfo) structure or the [**UIAutomationEventInfo**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationeventinfo) structure.</span></span>

<span data-ttu-id="fb6ea-154">La méthode [**IUIAutomationRegistrar :: RegisterProperty**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerproperty) ou [**REGISTEREVENT**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerevent) retourne un ID de propriété ou un ID d’événement qu’une application peut passer à toute méthode UI Automation qui accepte ce type d’identificateur comme paramètre.</span><span class="sxs-lookup"><span data-stu-id="fb6ea-154">The [**IUIAutomationRegistrar::RegisterProperty**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerproperty) or [**RegisterEvent**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerevent) method returns a property ID or event ID that an application can pass to any UI Automation method that takes such an identifier as a parameter.</span></span> <span data-ttu-id="fb6ea-155">Par exemple, vous pouvez passer un ID de propriété inscrite à la méthode [**IUIAutomationElement :: GetCurrentPropertyValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalue) ou à la méthode [**IUIAutomation :: CreatePropertyCondition**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-createpropertycondition) .</span><span class="sxs-lookup"><span data-stu-id="fb6ea-155">For example, you can pass a registered property ID to the [**IUIAutomationElement::GetCurrentPropertyValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalue) method or to the [**IUIAutomation::CreatePropertyCondition**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-createpropertycondition) method.</span></span>

<span data-ttu-id="fb6ea-156">L’exemple suivant montre comment inscrire une propriété personnalisée.</span><span class="sxs-lookup"><span data-stu-id="fb6ea-156">The following example demonstrates how to register a custom property.</span></span>


```C++
// Declare a variable for holding the custom property ID.
PATTERNID g_MyCustomPropertyID;
// Define a GUID for the custom property.
GUID GUID_MyCustomProperty = { 0x82f383ff, 0x4b4d, 0x40d3, 
    { 0x8e, 0xd2, 0x90, 0xb5, 0x25, 0x8e, 0xaa, 0x19 } };

HRESULT RegisterProperty()
{
    // Fill the structure with the GUID, name, and data type.
    UIAutomationPropertyInfo MyCustomPropertyInfo = 
    {
        GUID_MyCustomProperty,
        L"MyCustomProp",
        UIAutomationType_String
    };

    // Create the registrar object and get the IUIAutomationRegistrar 
    // interface pointer. 
    IUIAutomationRegistrar * pUIARegistrar = NULL;
    CoCreateInstance(CLSID_CUIAutomationRegistrar, NULL, CLSCTX_INPROC_SERVER, 
            IID_IUIAutomationRegistrar, (void **)&pUIARegistrar);

    if (pUIARegistrar == NULL)
        return E_NOINTERFACE;

    // Register the property and retrieve the property ID. 
    HRESULT hr = pUIARegistrar->RegisterProperty(&MyCustomPropertyInfo, &g_MyCustomPropertyID);
    pUIARegistrar->Release();

    return hr;
}
```



<span data-ttu-id="fb6ea-157">Les identificateurs de propriété et d’événement récupérés par les méthodes [**IUIAutomationRegistrar :: RegisterProperty**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerproperty) et [**RegisterEvent**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerevent) sont valides uniquement dans le contexte de l’application qui les récupère et uniquement pendant la durée de vie de l’application.</span><span class="sxs-lookup"><span data-stu-id="fb6ea-157">The property and event identifiers retrieved by the [**IUIAutomationRegistrar::RegisterProperty**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerproperty) and [**RegisterEvent**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerevent) methods are valid only in the context of the application that retrieves them, and only for the duration of the application's lifetime.</span></span> <span data-ttu-id="fb6ea-158">Les méthodes d’inscription peuvent retourner des valeurs entières différentes pour le même GUID lorsqu’elles sont appelées sur différentes instances de Runtime de la même application.</span><span class="sxs-lookup"><span data-stu-id="fb6ea-158">The registration methods can return different integer values for the same GUID when it is called over different runtime instances of the same application.</span></span>

<span data-ttu-id="fb6ea-159">Il n’existe aucune méthode qui annule l’inscription d’une propriété ou d’un événement personnalisé.</span><span class="sxs-lookup"><span data-stu-id="fb6ea-159">There is no method that unregisters a custom property or event.</span></span> <span data-ttu-id="fb6ea-160">Au lieu de cela, ils sont désinscrits implicitement lorsque le dernier objet UI Automation est libéré.</span><span class="sxs-lookup"><span data-stu-id="fb6ea-160">Instead, they are implicitly unregistered when the last UI Automation object is released.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="fb6ea-161">Si votre code est un client Microsoft Active Accessibility (MSAA), vous devez appeler la fonction [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) lorsque vous modifiez la valeur d’une propriété personnalisée.</span><span class="sxs-lookup"><span data-stu-id="fb6ea-161">If your code is a Microsoft Active Accessibility (MSAA) client, you must call the [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) function when you change the value of a custom property.</span></span>

 

## <a name="implementing-custom-control-patterns"></a><span data-ttu-id="fb6ea-162">Implémentation de modèles de contrôle personnalisés</span><span class="sxs-lookup"><span data-stu-id="fb6ea-162">Implementing Custom Control Patterns</span></span>

<span data-ttu-id="fb6ea-163">Un modèle de contrôle personnalisé n’est pas inclus dans l’API UI Automation, mais est fourni par un tiers au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="fb6ea-163">A custom control pattern is not included in the UI Automation API, but is provided by a third party at run time.</span></span> <span data-ttu-id="fb6ea-164">Les développeurs d’applications clientes et de fournisseurs doivent travailler ensemble pour définir un modèle de contrôle personnalisé, y compris les méthodes, propriétés et événements que le modèle de contrôle prendra en charge.</span><span class="sxs-lookup"><span data-stu-id="fb6ea-164">Developers of client and provider applications must work together to define a custom control pattern, including the methods, properties, and events that the control pattern will support.</span></span> <span data-ttu-id="fb6ea-165">Après avoir défini le modèle de contrôle, le client et le fournisseur doivent implémenter des objets COM (Component Object Model) de prise en charge, ainsi que du code pour inscrire le modèle de contrôle au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="fb6ea-165">After defining the control pattern, both the client and the provider must implement supporting Component Object Model (COM) objects, along with code to register the control pattern at run time.</span></span> <span data-ttu-id="fb6ea-166">Un modèle de contrôle personnalisé requiert l’implémentation de deux objets COM : un wrapper client et un gestionnaire de modèle.</span><span class="sxs-lookup"><span data-stu-id="fb6ea-166">A custom control pattern requires the implementation of two COM objects: a client wrapper and a pattern handler.</span></span>

> [!Note]  
> <span data-ttu-id="fb6ea-167">Les exemples des rubriques suivantes illustrent comment implémenter un modèle de contrôle personnalisé qui duplique les fonctionnalités du modèle de contrôle [value](uiauto-implementingvalue.md) existant.</span><span class="sxs-lookup"><span data-stu-id="fb6ea-167">The examples in the following topics illustrate how to implement a custom control pattern that duplicates the functionality of the existing [Value](uiauto-implementingvalue.md) control pattern.</span></span> <span data-ttu-id="fb6ea-168">Ces exemples sont fournis à des fins pédagogiques uniquement.</span><span class="sxs-lookup"><span data-stu-id="fb6ea-168">These examples are for instructional purposes only.</span></span> <span data-ttu-id="fb6ea-169">Un modèle de contrôle personnalisé réel doit fournir des fonctionnalités qui ne sont pas disponibles à partir des modèles de contrôle UI Automation Standard.</span><span class="sxs-lookup"><span data-stu-id="fb6ea-169">An actual custom control pattern should provide functionality that is not available from the standard UI Automation control patterns.</span></span>

 

### <a name="the-client-wrapper-and-the-pattern-handler"></a><span data-ttu-id="fb6ea-170">Le wrapper client et le gestionnaire de modèle</span><span class="sxs-lookup"><span data-stu-id="fb6ea-170">The Client Wrapper and the Pattern Handler</span></span>

<span data-ttu-id="fb6ea-171">Le wrapper client implémente l’API qui est utilisée par le client pour récupérer des propriétés et appeler des méthodes exposées par le modèle de contrôle personnalisé.</span><span class="sxs-lookup"><span data-stu-id="fb6ea-171">The client wrapper implements the API that is used by the client to retrieve properties and call methods exposed by the custom control pattern.</span></span> <span data-ttu-id="fb6ea-172">L’API est implémentée en tant qu’interface COM qui passe toutes les demandes de propriété et les appels de méthode au noyau UI Automation, qui marshale ensuite les demandes et les appels au fournisseur.</span><span class="sxs-lookup"><span data-stu-id="fb6ea-172">The API is implemented as a COM interface that passes all property requests and method calls to the UI Automation core, which then marshals the requests and calls to the provider.</span></span>

<span data-ttu-id="fb6ea-173">Le code qui inscrit un modèle de contrôle personnalisé doit fournir une fabrique de classe qu’UI Automation peut utiliser pour créer des instances de l’objet de wrapper client.</span><span class="sxs-lookup"><span data-stu-id="fb6ea-173">The code that registers a custom control pattern must supply a class factory that UI Automation can use to create instances of the client wrapper object.</span></span> <span data-ttu-id="fb6ea-174">Lorsqu’un modèle de contrôle personnalisé est correctement inscrit, UI Automation retourne un pointeur d’interface [**IUIAutomationPatternInstance**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationpatterninstance) utilisé par le client pour transférer les demandes de propriétés et les appels de méthodes au noyau UI Automation.</span><span class="sxs-lookup"><span data-stu-id="fb6ea-174">When a custom control pattern is successfully registered, UI Automation returns an [**IUIAutomationPatternInstance**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationpatterninstance) interface pointer that is used by the client to forward property requests and methods calls to the UI Automation core.</span></span>

<span data-ttu-id="fb6ea-175">Côté fournisseur, le noyau UI Automation prend les demandes de propriété et les appels de méthode du client et les transmet à l’objet de gestionnaire de modèles.</span><span class="sxs-lookup"><span data-stu-id="fb6ea-175">On the provider side, the UI Automation core takes the property requests and method calls from the client and passes them to the pattern handler object.</span></span> <span data-ttu-id="fb6ea-176">Le gestionnaire de modèle appelle ensuite les méthodes appropriées sur l’interface du fournisseur pour le modèle de contrôle personnalisé.</span><span class="sxs-lookup"><span data-stu-id="fb6ea-176">The pattern handler then calls the appropriate methods on the provider interface for the custom control pattern.</span></span>

<span data-ttu-id="fb6ea-177">Le code qui inscrit un modèle de contrôle personnalisé crée l’objet de gestionnaire de modèles et, lors de l’inscription du modèle de contrôle, fournit l’Automation d’interface utilisateur avec un pointeur vers l’interface [**IUIAutomationPatternHandler**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationpatternhandler) de l’objet.</span><span class="sxs-lookup"><span data-stu-id="fb6ea-177">The code that registers a custom control pattern creates the pattern handler object and, when registering the control pattern, provides UI Automation with a pointer to the object's [**IUIAutomationPatternHandler**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationpatternhandler) interface.</span></span>

<span data-ttu-id="fb6ea-178">Le diagramme suivant montre comment un appel de requête ou de méthode de propriété de client passe du wrapper client, via les composants de base d’UI Automation au gestionnaire de modèles, puis à l’interface du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="fb6ea-178">The following diagram shows how a client property request or method call flows from the client wrapper, through the UI Automation core components to the pattern handler, and then to the provider interface.</span></span>

![Diagramme montrant le passage du wrapper client au gestionnaire de modèles et au fournisseur](images/custompatternsupport.jpg)

<span data-ttu-id="fb6ea-180">Les objets qui implémentent les interfaces de wrapper client et de gestionnaire de modèles doivent être à thread libre.</span><span class="sxs-lookup"><span data-stu-id="fb6ea-180">The objects that implement the client wrapper and pattern handler interfaces must be free-threaded.</span></span> <span data-ttu-id="fb6ea-181">En outre, le noyau UI Automation doit être en mesure d’appeler directement les objets sans aucun code de marshaling intermédiaire.</span><span class="sxs-lookup"><span data-stu-id="fb6ea-181">Also, the UI Automation core must be able to call the objects directly without any intermediate marshaling code.</span></span>

### <a name="implementing-the-client-wrapper"></a><span data-ttu-id="fb6ea-182">Implémentation du wrapper client</span><span class="sxs-lookup"><span data-stu-id="fb6ea-182">Implementing the Client Wrapper</span></span>

<span data-ttu-id="fb6ea-183">Le wrapper client est un objet qui expose une interface IXxxPattern que le client utilise pour demander des propriétés et appeler des méthodes prises en charge par le modèle de contrôle personnalisé.</span><span class="sxs-lookup"><span data-stu-id="fb6ea-183">The client wrapper is an object that exposes an IXxxPattern interface that the client uses to request properties and call methods supported by the custom control pattern.</span></span> <span data-ttu-id="fb6ea-184">L’interface se compose d’une paire de méthodes « getter » pour chaque propriété prise en charge (get \_ CurrentXxx et \_ méthode Get CachedXxx), et d’une méthode « Caller » pour chaque méthode prise en charge.</span><span class="sxs-lookup"><span data-stu-id="fb6ea-184">The interface consists of a pair of "getter" methods for each supported property (get\_CurrentXxx and get\_CachedXxx method), and a "caller" method for each supported method.</span></span> <span data-ttu-id="fb6ea-185">Lorsque l’objet est instancié, le constructeur d’objet reçoit un pointeur vers l’interface [**IUIAutomationPatternInstance**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationpatterninstance) , qui est implémentée par le noyau UI Automation.</span><span class="sxs-lookup"><span data-stu-id="fb6ea-185">When the object is instantiated, the object constructor receives a pointer to the [**IUIAutomationPatternInstance**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationpatterninstance) interface, which is implemented by the UI Automation core.</span></span> <span data-ttu-id="fb6ea-186">Les méthodes de l’interface IXxxPattern utilisent les méthodes [**IUIAutomationPatternInstance :: GetProperty**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationpatterninstance-getproperty) et [**CallMethod**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationpatterninstance-callmethod) pour transférer les demandes de propriétés et les appels de méthode au noyau UI Automation.</span><span class="sxs-lookup"><span data-stu-id="fb6ea-186">The methods of the IXxxPattern interface use the [**IUIAutomationPatternInstance::GetProperty**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationpatterninstance-getproperty) and [**CallMethod**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationpatterninstance-callmethod) methods to forward property requests and method calls to the UI Automation core.</span></span>

<span data-ttu-id="fb6ea-187">L’exemple suivant montre comment implémenter un objet de wrapper client pour un modèle de contrôle personnalisé simple qui prend en charge une seule propriété.</span><span class="sxs-lookup"><span data-stu-id="fb6ea-187">The following example shows how to implement a client wrapper object for a simple custom control pattern that supports a single property.</span></span> <span data-ttu-id="fb6ea-188">Pour obtenir un exemple plus complexe, consultez [exemple d’implémentation d’un modèle de contrôle personnalisé](#example-implementation-of-a-custom-control-pattern).</span><span class="sxs-lookup"><span data-stu-id="fb6ea-188">For a more complex example, see [Example Implementation of a Custom Control Pattern](#example-implementation-of-a-custom-control-pattern).</span></span>


```C++
// Define the client interface.
interface __declspec(uuid("c78b266d-b2c0-4e9d-863b-e3f74a721d47"))
IMyCustomPattern : public IUnknown
{
    STDMETHOD (get_CurrentIsReadOnly)(BOOL * pIsReadOnly) = 0;
    STDMETHOD (get_CachedIsReadOnly)(BOOL * pIsReadOnly) = 0;
};

// Implement the client wrapper class.
class CMyValuePatternClientWrapper :
    public IMyCustomPattern
{
    IUIAutomationPatternInstance * _pInstance;
    
public:
    // Get IUIAutomationPatternInstance interface pointer from the
    // UI Automation core.
    CMyValuePatternClientWrapper(IUIAutomationPatternInstance * pInstance)
        : _pInstance(pInstance)
    {
        _pInstance->AddRef();
    }
    
    ~CMyValuePatternClientWrapper()
    {
        _pInstance->Release();
    }

    // Note: Put standard IUnknown implementation here.

    STDMETHODIMP get_CurrentIsReadOnly(BOOL * pIsReadOnly)
    {
        return _pInstance->GetProperty(0, FALSE, UIAutomationType_Bool, pIsReadOnly);
    }

    STDMETHODIMP get_CachedIsReadOnly(BOOL * pIsReadOnly)
    {
        return _pInstance->GetProperty(0, TRUE, UIAutomationType_Bool, pIsReadOnly);
    }
};
```



### <a name="implementing-the-pattern-handler"></a><span data-ttu-id="fb6ea-189">Implémentation du gestionnaire de modèles</span><span class="sxs-lookup"><span data-stu-id="fb6ea-189">Implementing the Pattern Handler</span></span>

<span data-ttu-id="fb6ea-190">Le gestionnaire de modèle est un objet qui implémente l’interface [**IUIAutomationPatternHandler**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationpatternhandler) .</span><span class="sxs-lookup"><span data-stu-id="fb6ea-190">The pattern handler is an object that implements the [**IUIAutomationPatternHandler**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationpatternhandler) interface.</span></span> <span data-ttu-id="fb6ea-191">Cette interface a deux méthodes : [**IUIAutomationPatternHandler :: CreateClientWrapper**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationpatternhandler-createclientwrapper) et [**Dispatch**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationpatternhandler-dispatch).</span><span class="sxs-lookup"><span data-stu-id="fb6ea-191">This interface has two methods: [**IUIAutomationPatternHandler::CreateClientWrapper**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationpatternhandler-createclientwrapper) and [**Dispatch**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationpatternhandler-dispatch).</span></span> <span data-ttu-id="fb6ea-192">La méthode **CreateClientWrapper** est appelée par le noyau UI Automation et reçoit un pointeur vers l’interface [**IUIAutomationPatternInstance**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationpatterninstance) .</span><span class="sxs-lookup"><span data-stu-id="fb6ea-192">The **CreateClientWrapper** method is called by the UI Automation core and receives a pointer to the [**IUIAutomationPatternInstance**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationpatterninstance) interface.</span></span> <span data-ttu-id="fb6ea-193">**CreateClientWrapper** répond en instanciant l’objet de wrapper client et en passant le pointeur d’interface **IUIAutomationPatternInstance** au constructeur de wrapper client.</span><span class="sxs-lookup"><span data-stu-id="fb6ea-193">**CreateClientWrapper** responds by instantiating the client wrapper object and passing the **IUIAutomationPatternInstance** interface pointer to the client wrapper constructor.</span></span>

<span data-ttu-id="fb6ea-194">La méthode de [**distribution**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationpatternhandler-dispatch) est utilisée par le noyau UI Automation pour passer des demandes de propriétés et des appels de méthode à l’interface du fournisseur pour le modèle de contrôle personnalisé.</span><span class="sxs-lookup"><span data-stu-id="fb6ea-194">The [**Dispatch**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationpatternhandler-dispatch) method is used by the UI Automation core to pass property requests and method calls to the provider interface for the custom control pattern.</span></span> <span data-ttu-id="fb6ea-195">Les paramètres incluent un pointeur vers l’interface du fournisseur, l’index de base zéro de l’accesseur Get de la propriété ou de la méthode appelée, et un tableau de structures [**UIAutomationParameter**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationparameter) qui contiennent les paramètres à passer au fournisseur.</span><span class="sxs-lookup"><span data-stu-id="fb6ea-195">Parameters include a pointer to the provider interface, the zero-based index of the property getter or method being called, and an array of [**UIAutomationParameter**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationparameter) structures that contain the parameters to pass to the provider.</span></span> <span data-ttu-id="fb6ea-196">Le gestionnaire de modèle répond en vérifiant le paramètre d’index pour déterminer la méthode de fournisseur à appeler, puis appelle cette interface de fournisseur en passant les paramètres contenus dans les structures **UIAutomationParameter** .</span><span class="sxs-lookup"><span data-stu-id="fb6ea-196">The pattern handler responds by checking the index parameter to determine which provider method to call, and then calls that provider interface, passing the parameters contained in the **UIAutomationParameter** structures.</span></span>

<span data-ttu-id="fb6ea-197">L’objet de gestionnaire de modèle est instancié par le même code qui inscrit le modèle de contrôle personnalisé, avant l’inscription du modèle de contrôle.</span><span class="sxs-lookup"><span data-stu-id="fb6ea-197">The pattern handler object is instantiated by the same code that registers the custom control pattern, before the control pattern is registered.</span></span> <span data-ttu-id="fb6ea-198">Le code doit passer le pointeur d’interface [**IUIAutomationPatternHandler**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationpatternhandler) de l’objet de gestionnaire de modèle au noyau UI Automation au moment de l’inscription.</span><span class="sxs-lookup"><span data-stu-id="fb6ea-198">The code must pass the pattern handler object's [**IUIAutomationPatternHandler**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationpatternhandler) interface pointer to the UI Automation core at registration time.</span></span>

<span data-ttu-id="fb6ea-199">L’exemple suivant montre comment implémenter un objet de gestionnaire de modèle pour un modèle de contrôle personnalisé simple qui prend en charge une seule propriété.</span><span class="sxs-lookup"><span data-stu-id="fb6ea-199">The following example shows how to implement a pattern handler object for a simple custom control pattern that supports a single property.</span></span> <span data-ttu-id="fb6ea-200">Pour obtenir un exemple plus complexe, consultez [exemple d’implémentation d’un modèle de contrôle personnalisé](#example-implementation-of-a-custom-control-pattern).</span><span class="sxs-lookup"><span data-stu-id="fb6ea-200">For a more complex example, see [Example Implementation of a Custom Control Pattern](#example-implementation-of-a-custom-control-pattern).</span></span>


```C++
// Define the provider interface.
interface __declspec(uuid("9f5266dd-f0ab-4562-8175-c383abb2569e"))
IMyValueProvider : public IUnknown
{
    STDMETHOD (get_IsReadOnly)(BOOL * pIsReadOnly) = 0;
};            

// Index used by IUIAutomationPatternHandler::Dispatch.
const int MyValue_GetIsReadOnly = 0; 
            
// Define the pattern handler class.        
class CMyValuePatternHandler : public IUIAutomationPatternHandler
{
public:
    
    // Put standard IUnknown implementation here.

    STDMETHODIMP CreateClientWrapper(
            IUIAutomationPatternInstance * pPatternInstance, 
            IUnknown ** pClientWrapper)
    {
        *pClientWrapper = new CMyValuePatternClientWrapper(pPatternInstance);
        if (*pClientWrapper == NULL)
            return E_INVALIDARG;
        return S_OK;
    }
    
    STDMETHODIMP Dispatch (IUnknown * pTarget, UINT index, 
            const struct UIAutomationParameter *pParams, UINT cParams)
    {
        switch(index)
        {
        case MyValue_GetIsReadOnly:
            return ((IMyValueProvider*)pTarget)->get_IsReadOnly((BOOL*)pParams[0].pData);
        }
        return E_INVALIDARG;
    }
};
```



### <a name="registering-a-custom-control-pattern"></a><span data-ttu-id="fb6ea-201">Inscription d’un modèle de contrôle personnalisé</span><span class="sxs-lookup"><span data-stu-id="fb6ea-201">Registering a Custom Control Pattern</span></span>

<span data-ttu-id="fb6ea-202">Avant de pouvoir être utilisé, un modèle de contrôle personnalisé doit être enregistré par le fournisseur et le client.</span><span class="sxs-lookup"><span data-stu-id="fb6ea-202">Before it can be used, a custom control pattern must be registered by both the provider and the client.</span></span> <span data-ttu-id="fb6ea-203">L’inscription fournit le noyau UI Automation avec des informations détaillées sur le modèle de contrôle, et fournit le fournisseur ou le client avec l’ID de modèle de contrôle, ainsi que des ID pour les propriétés et les événements pris en charge par le modèle de contrôle.</span><span class="sxs-lookup"><span data-stu-id="fb6ea-203">Registering provides the UI Automation core with detailed information about the control pattern, and supplies the provider or client with the control pattern ID, and IDs for the properties and events that are supported by the control pattern.</span></span> <span data-ttu-id="fb6ea-204">Côté fournisseur, le modèle de contrôle personnalisé doit être inscrit avant que le contrôle associé ne gère [**le \_ message WM**](wm-getobject.md) , ou en même temps.</span><span class="sxs-lookup"><span data-stu-id="fb6ea-204">On the provider side, the custom control pattern must be registered before the associated control handles the [**WM\_GETOBJECT**](wm-getobject.md) message, or at the same time.</span></span>

<span data-ttu-id="fb6ea-205">Lors de l’inscription d’un modèle de contrôle personnalisé, le fournisseur ou le client fournit les informations suivantes :</span><span class="sxs-lookup"><span data-stu-id="fb6ea-205">When registering a custom control pattern, the provider or client supplies the following information:</span></span>

-   <span data-ttu-id="fb6ea-206">GUID du modèle de contrôle personnalisé.</span><span class="sxs-lookup"><span data-stu-id="fb6ea-206">The GUID of the custom control pattern.</span></span>
-   <span data-ttu-id="fb6ea-207">Chaîne inlocalisable contenant le nom du modèle de contrôle personnalisé.</span><span class="sxs-lookup"><span data-stu-id="fb6ea-207">A nonlocalizable string containing the name of the custom control pattern.</span></span>
-   <span data-ttu-id="fb6ea-208">GUID de l’interface du fournisseur qui prend en charge le modèle de contrôle personnalisé.</span><span class="sxs-lookup"><span data-stu-id="fb6ea-208">The GUID of the provider interface that supports the custom control pattern.</span></span>
-   <span data-ttu-id="fb6ea-209">GUID de l’interface cliente qui prend en charge le modèle de contrôle personnalisé.</span><span class="sxs-lookup"><span data-stu-id="fb6ea-209">The GUID of the client interface that supports the custom control pattern.</span></span>
-   <span data-ttu-id="fb6ea-210">Tableau de structures [**UIAutomationPropertyInfo**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationpropertyinfo) qui décrivent les propriétés prises en charge par le modèle de contrôle personnalisé.</span><span class="sxs-lookup"><span data-stu-id="fb6ea-210">An array of [**UIAutomationPropertyInfo**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationpropertyinfo) structures that describe the properties supported by the custom control pattern.</span></span> <span data-ttu-id="fb6ea-211">Pour chaque propriété, le GUID, le nom de la propriété et le type de données doivent être spécifiés.</span><span class="sxs-lookup"><span data-stu-id="fb6ea-211">For each property, the GUID, property name, and data type must be specified.</span></span>
-   <span data-ttu-id="fb6ea-212">Tableau de structures [**UIAutomationMethodInfo**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationmethodinfo) qui décrivent les méthodes prises en charge par le modèle de contrôle personnalisé.</span><span class="sxs-lookup"><span data-stu-id="fb6ea-212">An array of [**UIAutomationMethodInfo**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationmethodinfo) structures that describe the methods supported by the custom control pattern.</span></span> <span data-ttu-id="fb6ea-213">Pour chaque méthode, la structure comprend les informations suivantes : le nom de la méthode, un nombre de paramètres, une liste de types de données de paramètres et une liste des noms de paramètres.</span><span class="sxs-lookup"><span data-stu-id="fb6ea-213">For each method, the structure includes the following information: the method name, a count of parameters, a list of parameter data types, and a list of the parameter names.</span></span>
-   <span data-ttu-id="fb6ea-214">Tableau de structures [**UIAutomationEventInfo**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationeventinfo) qui décrivent les événements déclenchés par le modèle de contrôle personnalisé.</span><span class="sxs-lookup"><span data-stu-id="fb6ea-214">An array of [**UIAutomationEventInfo**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationeventinfo) structures that describe the events raised by the custom control pattern.</span></span> <span data-ttu-id="fb6ea-215">Pour chaque événement, le GUID et le nom de l’événement doivent être spécifiés.</span><span class="sxs-lookup"><span data-stu-id="fb6ea-215">For each event, the GUID and event name must be specified.</span></span>
-   <span data-ttu-id="fb6ea-216">Adresse de l’interface [**IUIAutomationPatternHandler**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationpatternhandler) de l’objet de gestionnaire de modèle qui rend le modèle de contrôle personnalisé disponible pour les clients.</span><span class="sxs-lookup"><span data-stu-id="fb6ea-216">The address of the [**IUIAutomationPatternHandler**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationpatternhandler) interface of the pattern handler object that makes the custom control pattern available to clients.</span></span>

<span data-ttu-id="fb6ea-217">Pour inscrire le modèle de contrôle personnalisé, le fournisseur ou le code client doit effectuer les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="fb6ea-217">To register the custom control pattern, the provider or client code must perform the following steps:</span></span>

1.  <span data-ttu-id="fb6ea-218">Remplissez une structure [**UIAutomationPatternInfo**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationpatterninfo) avec les informations précédentes.</span><span class="sxs-lookup"><span data-stu-id="fb6ea-218">Fill a [**UIAutomationPatternInfo**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationpatterninfo) structure with the preceding information.</span></span>
2.  <span data-ttu-id="fb6ea-219">Utilisez la fonction [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) pour créer une instance de l’objet [**CUIAutomationRegistrar**](/previous-versions/windows/desktop/legacy/ff384837(v=vs.85)) et récupérer un pointeur vers l’interface [**IUIAutomationRegistrar**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationregistrar) de l’objet.</span><span class="sxs-lookup"><span data-stu-id="fb6ea-219">Use the [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) function to create an instance of the [**CUIAutomationRegistrar**](/previous-versions/windows/desktop/legacy/ff384837(v=vs.85)) object and retrieve a pointer to the object's [**IUIAutomationRegistrar**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationregistrar) interface.</span></span>
3.  <span data-ttu-id="fb6ea-220">Appelez la méthode [**IUIAutomationRegistrar :: RegisterPattern**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerpattern) , en passant l’adresse de la structure [**UIAutomationPatternInfo**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationpatterninfo) .</span><span class="sxs-lookup"><span data-stu-id="fb6ea-220">Call the [**IUIAutomationRegistrar::RegisterPattern**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerpattern) method, passing the address of the [**UIAutomationPatternInfo**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationpatterninfo) structure.</span></span>

<span data-ttu-id="fb6ea-221">La méthode [**RegisterPattern**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerpattern) retourne un ID de modèle de contrôle, ainsi qu’une liste d’ID de propriété et d’ID d’événement.</span><span class="sxs-lookup"><span data-stu-id="fb6ea-221">The [**RegisterPattern**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerpattern) method returns a control pattern ID, along with a list of property IDs and event IDs.</span></span> <span data-ttu-id="fb6ea-222">Une application peut passer ces ID à toute méthode UI Automation qui accepte un tel identificateur en tant que paramètre.</span><span class="sxs-lookup"><span data-stu-id="fb6ea-222">An application can pass these IDs to any UI Automation method that takes such an identifier as a parameter.</span></span> <span data-ttu-id="fb6ea-223">Par exemple, vous pouvez passer un ID de modèle inscrit à la méthode [**IUIAutomationElement :: GetCurrentPattern**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpattern) pour récupérer un pointeur vers l’interface du fournisseur pour le modèle de contrôle.</span><span class="sxs-lookup"><span data-stu-id="fb6ea-223">For example, you can pass a registered pattern ID to the [**IUIAutomationElement::GetCurrentPattern**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpattern) method to retrieve a pointer to the provider interface for the control pattern.</span></span>

<span data-ttu-id="fb6ea-224">Il n’existe aucune méthode qui annule l’inscription d’un modèle de contrôle personnalisé.</span><span class="sxs-lookup"><span data-stu-id="fb6ea-224">There is no method that unregisters a custom control pattern.</span></span> <span data-ttu-id="fb6ea-225">Au lieu de cela, elle est désinscrite implicitement lorsque le dernier objet UI Automation est libéré.</span><span class="sxs-lookup"><span data-stu-id="fb6ea-225">Instead, it is implicitly unregistered when the last UI Automation object is released.</span></span>

<span data-ttu-id="fb6ea-226">Pour obtenir un exemple qui montre comment inscrire un modèle de contrôle personnalisé, consultez la section suivante.</span><span class="sxs-lookup"><span data-stu-id="fb6ea-226">For an example that shows how to register a custom control pattern, see the following section.</span></span>

### <a name="example-implementation-of-a-custom-control-pattern"></a><span data-ttu-id="fb6ea-227">Exemple d’implémentation d’un modèle de contrôle personnalisé</span><span class="sxs-lookup"><span data-stu-id="fb6ea-227">Example Implementation of a Custom Control Pattern</span></span>

<span data-ttu-id="fb6ea-228">Cette section contient un exemple de code qui montre comment implémenter les objets Wrapper client et gestionnaire de modèles pour un modèle de contrôle personnalisé.</span><span class="sxs-lookup"><span data-stu-id="fb6ea-228">This section contains example code that demonstrates how to implement the client wrapper and pattern handler objects for a custom control pattern.</span></span> <span data-ttu-id="fb6ea-229">L’exemple implémente un modèle de contrôle personnalisé basé sur le modèle de contrôle [value](uiauto-implementingvalue.md) .</span><span class="sxs-lookup"><span data-stu-id="fb6ea-229">The example implements a custom control pattern that is based on the [Value](uiauto-implementingvalue.md) control pattern.</span></span>


```C++
// Step 1: Define the public provider and client interfaces using IDL. Interface 
// definitions are in C here to simplify the example.

// Define the provider interface.
interface __declspec(uuid("9f5266dd-f0ab-4562-8175-c383abb2569e"))
IMyValueProvider : public IUnknown
{
    STDMETHOD (get_Value)(BSTR * pValue) = 0;
    STDMETHOD (get_IsReadOnly)(BOOL * pIsReadOnly) = 0;
    STDMETHOD (SetValue)(LPCWSTR pNewValue) = 0;
    STDMETHOD (Reset)() = 0;
};

// Define the client interface.
interface __declspec(uuid("103b8323-b04a-4180-9140-8c1e437713a3"))
IUIAutomationMyValuePattern : public IUnknown
{
    STDMETHOD (get_CurrentValue)(BSTR * pValue) = 0;
    STDMETHOD (get_CachedValue)(BSTR * pValue) = 0;

    STDMETHOD (get_CurrentIsReadOnly)(BOOL * pIsReadOnly) = 0;
    STDMETHOD (get_CachedIsReadOnly)(BOOL * pIsReadOnly) = 0;

    STDMETHOD (SetValue)(LPCWSTR pNewValue) = 0;
    STDMETHOD (Reset)() = 0;
};

// Enumerate the properties and methods starting from 0, and placing the 
// properties first. 
enum
{
    MyValue_GetValue = 0,
    MyValue_GetIsReadOnly = 1,
    MyValue_SetValue = 2,
    MyValue_Reset = 3,
};

// Step 2: Implement the client wrapper class.
class CMyValuePatternClientWrapper :
    public IUIAutomationMyValuePattern
{
    IUIAutomationPatternInstance * _pInstance;

public:
    // Get IUIAutomationPatternInstance interface pointer.
    CMyValuePatternClientWrapper(IUIAutomationPatternInstance * pInstance)
    {
        _pInstance = pInstance;
        _pInstance->AddRef();
    }

    // Put standard IUnknown implementation here.

    STDMETHODIMP get_CurrentValue(BSTR * pValue)
    {
        return _pInstance->GetProperty(MyValue_GetValue, FALSE, 
                UIAutomationType_String, pValue);
    }

    STDMETHODIMP get_CachedValue(BSTR * pValue)
    {
        return _pInstance->GetProperty(MyValue_GetValue, TRUE, 
                UIAutomationType_String, pValue);
    }

    STDMETHODIMP get_CurrentIsReadOnly(BOOL * pIsReadOnly)
    {
        return _pInstance->GetProperty(MyValue_GetIsReadOnly, FALSE, 
                UIAutomationType_Bool, pIsReadOnly);
    }

    STDMETHODIMP get_CachedIsReadOnly(BOOL * pIsReadOnly)
    {
        return _pInstance->GetProperty(MyValue_GetIsReadOnly, TRUE, 
                UIAutomationType_Bool, pIsReadOnly);
    }

    STDMETHODIMP SetValue(LPCWSTR pValue)
    {
        UIAutomationParameter SetValueParams[] = 
                { UIAutomationType_String, &pValue };
        return _pInstance->CallMethod(MyValue_SetValue,  SetValueParams, 
                ARRAYSIZE(SetValueParams));
    }

    STDMETHODIMP Reset()
    {
        return _pInstance->CallMethod(MyValue_Reset, NULL, 0);
    }
};

// Step 3: Implement the pattern handler class.
class CMyValuePatternHandler : public IUIAutomationPatternHandler
{
public:

    // Put standard IUnknown implementation here.
    
    STDMETHODIMP CreateClientWrapper(
            IUIAutomationPatternInstance * pPatternInstance, 
            IUnknown ** pClientWrapper)
    {
        *pClientWrapper = new CMyValuePatternClientWrapper(pPatternInstance);
        if (*pClientWrapper == NULL)
            return E_INVALIDARG;
        return S_OK;
    }
    
    STDMETHODIMP Dispatch (IUnknown * pTarget, UINT index, 
            const struct UIAutomationParameter *pParams, 
            UINT cParams)
    {
        switch(index)
        {
        case MyValue_GetValue:
            return ((IMyValueProvider*)pTarget)->get_Value((BSTR*)pParams[0].pData);

        case MyValue_GetIsReadOnly:
            return ((IMyValueProvider*)pTarget)->get_IsReadOnly((BOOL*)pParams[0].pData);

        case MyValue_SetValue:
            return ((IMyValueProvider*)pTarget)->SetValue(*(LPCWSTR*)pParams[0].pData);

        case MyValue_Reset:
            return ((IMyValueProvider*)pTarget)->Reset();
        }
        return E_INVALIDARG;
    }
};

CMyValuePatternHandler g_MyValuePatternHandler;

// Step 4: Declare information about the properties and methods supported
// by the custom control pattern.

// Define GUIDs for the custom control pattern and each of its properties 
// and events.
static const GUID MyValue_Pattern_Guid = { 0xa49aa3c0, 0xe413, 0x4ecf, 
        { 0xa1, 0xc3, 0x37, 0x42, 0xa7, 0x86, 0x67, 0x3f } };
static const GUID MyValue_Value_Property_Guid = { 0xe58f3f67, 0x22c7, 0x44f0, 
        { 0x83, 0x55, 0xd8, 0x76, 0x14, 0xa1, 0x10, 0x81 } };
static const GUID MyValue_IsReadOnly_Property_Guid = { 0x480540f2, 0x9829, 0x4acd, 
        { 0xb8, 0xea, 0x6e, 0x2a, 0xdc, 0xe5, 0x3a, 0xfb } };
static const GUID MyValue_Reset_Event_Guid = { 0x5b80edd3, 0x67f, 0x4a70, 
        { 0xb0, 0x7, 0x4, 0x12, 0x85, 0x11, 0x1, 0x7a } };

// Declare information about the properties, in the same order as the
// previously defined "MyValue_" enumerated type.
UIAutomationPropertyInfo g_MyValueProperties[] = 
{
    // GUID, name, data type.
    { MyValue_Value_Property_Guid, L"MyValuePattern.Value", 
                                                    UIAutomationType_String },
    { MyValue_IsReadOnly_Property_Guid, L"MyValuePattern.IsReadOnly", 
                                                    UIAutomationType_Bool },
};

// Declare information about the event.
UIAutomationEventInfo g_MyValueEvents [] =
{
    { MyValue_Reset_Event_Guid,  L"MyValuePattern.Reset" },
};

// Declare the data type and name of the SetValue method parameter. 
UIAutomationType g_SetValueParamTypes[] = { UIAutomationType_String };
LPCWSTR g_SetValueParamNames[] = {L"pNewValue"};

// Declare information about the methods.
UIAutomationMethodInfo g_MyValueMethods[] =
{
    // Name, focus flag, count of in parameters, count of out parameters, types, parameter names.
    { L"MyValuePattern.SetValue", TRUE, 1, 0, g_SetValueParamTypes, g_SetValueParamNames },
    { L"MyValuePattern.Reset", TRUE, 0, 0, NULL, NULL },
};

// Declare the custom control pattern using the previously defined information.
UIAutomationPatternInfo g_ValuePatternInfo =
{
    MyValue_Pattern_Guid,
    L"MyValuePattern",
    __uuidof(IMyValueProvider),
    __uuidof(IUIAutomationMyValuePattern),
    ARRAYSIZE(g_MyValueProperties), g_MyValueProperties, // properties
    ARRAYSIZE(g_MyValueMethods), g_MyValueMethods,       // methods
    ARRAYSIZE(g_MyValueEvents), g_MyValueEvents,         // events 
    &g_MyValuePatternHandler
};

// Step 5: Register the custom control pattern and retrieve the control pattern and property 
// identifiers.

// Control pattern, property, and event IDs.
PATTERNID  g_MyValue_PatternID;
PROPERTYID g_MyValue_Value_PropertyID;
PROPERTYID g_MyValue_IsReadOnly_PropertyID;
EVENTID    g_MyValueReset_EventID;

// ID used by the client to determine whether the custom control pattern is available.
PROPERTYID g_IsMyValuePatternAvailable_PropertyID;

HRESULT RegisterPattern()
{
    // Create the registrar object and get the IUIAutomationRegistrar interface pointer. 
    IUIAutomationRegistrar * pUIARegistrar;
    CoCreateInstance(CLSID_CUIAutomationRegistrar, NULL, CLSCTX_INPROC_SERVER, 
            IID_IUIAutomationRegistrar, (void **)&pUIARegistrar);

    if (pUIARegistrar == NULL)
        return E_NOINTERFACE;

    PROPERTYID propIDs[2]; // Array for property IDs.

    // Register the control pattern.
    HRESULT hr = pUIARegistrar->RegisterPattern(
        &g_ValuePatternInfo,
        &g_MyValue_PatternID,
        &g_IsMyValuePatternAvailable_PropertyID,
        ARRAYSIZE(propIDs), 
        propIDs,
        1,
        &g_MyValueReset_EventID);
            
    if (hr == S_OK)
    {
        // Copy the property IDs.
        g_MyValue_Value_PropertyID = propIDs[0];
        g_MyValue_IsReadOnly_PropertyID = propIDs[1];
    }

    pUIARegistrar->Release();
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="fb6ea-230">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="fb6ea-230">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="fb6ea-231">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="fb6ea-231">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="fb6ea-232">Conception de propriétés, d’événements et de modèles de contrôle personnalisés</span><span class="sxs-lookup"><span data-stu-id="fb6ea-232">Designing Custom Properties, Events, and Control Patterns</span></span>](uiauto-designingcustompropseventpatterns.md)
</dt> <dt>

[<span data-ttu-id="fb6ea-233">Vue d'ensemble des propriétés UI Automation</span><span class="sxs-lookup"><span data-stu-id="fb6ea-233">UI Automation Properties Overview</span></span>](uiauto-propertiesoverview.md)
</dt> <dt>

[<span data-ttu-id="fb6ea-234">Vue d'ensemble des événements UI Automation</span><span class="sxs-lookup"><span data-stu-id="fb6ea-234">UI Automation Events Overview</span></span>](uiauto-eventsoverview.md)
</dt> <dt>

[<span data-ttu-id="fb6ea-235">Vue d'ensemble des modèles de contrôle UI Automation</span><span class="sxs-lookup"><span data-stu-id="fb6ea-235">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> </dl>

 

 