---
title: Ajout de la fonctionnalité UI Automation aux serveurs Active Accessibility
description: Les contrôles qui n’ont pas de fournisseur UI Automation de Microsoft, mais qui implémentent IAccessible peuvent facilement être mis à niveau pour fournir des fonctionnalités d’automatisation d’interface utilisateur, en implémentant l’interface IAccessibleEx.
ms.assetid: 7ceab704-3e02-4550-b236-748e4f0a092a
keywords:
- UI Automation, serveurs Active Accessibility
- UI Automation, serveurs Microsoft Active Accessibility
- UI Automation, IAccessible
- UI Automation, IAccessibleEx
- UI Automation, exposer IAccessibleEx
- UI Automation, implémentation de IAccessibleEx
- IAccessible
- IAccessibleEx
- Microsoft Active Accessibility
- Active Accessibility
- exposition de IAccessibleEx
- implémentation de IAccessibleEx
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f45311deb8d3ec20fb8102285cddea1339373f0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103941047"
---
# <a name="adding-ui-automation-functionality-to-active-accessibility-servers"></a><span data-ttu-id="5da03-115">Ajout de la fonctionnalité UI Automation aux serveurs Active Accessibility</span><span class="sxs-lookup"><span data-stu-id="5da03-115">Adding UI Automation Functionality to Active Accessibility Servers</span></span>

<span data-ttu-id="5da03-116">Les contrôles qui n’ont pas de fournisseur UI Automation de Microsoft, mais qui implémentent [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) peuvent facilement être mis à niveau pour fournir des fonctionnalités d’automatisation d’interface utilisateur, en implémentant l’interface [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) .</span><span class="sxs-lookup"><span data-stu-id="5da03-116">Controls that do not have a Microsoft UI Automation provider but that implement [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) can easily be upgraded to provide some UI Automation functionality, by implementing the [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) interface.</span></span> <span data-ttu-id="5da03-117">Cette interface permet au contrôle d’exposer des propriétés UI Automation et des modèles de contrôle, sans avoir besoin d’une implémentation complète des interfaces du fournisseur UI Automation telles que [**IRawElementProviderFragment**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragment).</span><span class="sxs-lookup"><span data-stu-id="5da03-117">This interface enables the control to expose UI Automation properties and control patterns, without the need for a full implementation of UI Automation provider interfaces such as [**IRawElementProviderFragment**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragment).</span></span> <span data-ttu-id="5da03-118">Pour implémenter **IAccessibleEx**, la hiérarchie d’objets Microsoft Active Accessibility de référence ne doit pas contenir d’erreurs ou d’incohérences (par exemple, un objet enfant dont l’objet parent ne la répertorie pas comme enfant) et ne doit pas être en conflit avec les spécifications UI Automation.</span><span class="sxs-lookup"><span data-stu-id="5da03-118">To implement **IAccessibleEx**, the baseline Microsoft Active Accessibility object hierarchy must contain no errors or inconsistencies (such as a child object whose parent object does not list it as a child), and must not conflict with UI Automation specifications.</span></span> <span data-ttu-id="5da03-119">Si la hiérarchie d’objets Microsoft Active Accessibility répond à ces exigences, il s’agit d’un bon candidat à l’ajout de fonctionnalités à l’aide de **IAccessibleEx**. dans le cas contraire, vous devez implémenter UI Automation seul ou parallèlement à l’implémentation de Microsoft Active Accessibility.</span><span class="sxs-lookup"><span data-stu-id="5da03-119">If the Microsoft Active Accessibility object hierarchy meets these requirements, it is a good candidate for adding functionality by using **IAccessibleEx**; otherwise, you must implement UI Automation alone or alongside the Microsoft Active Accessibility implementation.</span></span>

<span data-ttu-id="5da03-120">Prenons le cas d’un contrôle personnalisé qui a une valeur de plage.</span><span class="sxs-lookup"><span data-stu-id="5da03-120">Take the case of a custom control that has a range value.</span></span> <span data-ttu-id="5da03-121">Le serveur Microsoft Active Accessibility pour le contrôle définit son rôle et peut retourner sa valeur actuelle, mais n’a pas la possibilité de retourner les valeurs minimales et maximales du contrôle, car ces propriétés ne sont pas définies dans Microsoft Active Accessibility.</span><span class="sxs-lookup"><span data-stu-id="5da03-121">The Microsoft Active Accessibility server for the control defines its role, and is able to return its current value, but lacks the means to return the minimum and maximum values of the control, because these properties are not defined in Microsoft Active Accessibility.</span></span> <span data-ttu-id="5da03-122">Un client UI Automation est en mesure de récupérer le rôle du contrôle, la valeur actuelle et d’autres propriétés de Active Accessibility Microsoft, car le noyau UI Automation peut les obtenir via [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible).</span><span class="sxs-lookup"><span data-stu-id="5da03-122">A UI Automation client is able to retrieve the control's role, current value, and other Microsoft Active Accessibility properties, because the UI Automation core can obtain these through [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible).</span></span> <span data-ttu-id="5da03-123">Toutefois, sans accès à une interface [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider) sur l’objet, UI Automation ne peut pas non plus récupérer les valeurs maximale et minimale.</span><span class="sxs-lookup"><span data-stu-id="5da03-123">However, without access to an [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider) interface on the object, UI Automation is also unable to retrieve the maximum and minimum values.</span></span>

<span data-ttu-id="5da03-124">Le développeur de contrôle peut fournir un fournisseur UI Automation complet pour le contrôle, mais cela signifierait la duplication d’une grande partie des fonctionnalités existantes de l’implémentation de [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) : par exemple, la navigation et les propriétés communes.</span><span class="sxs-lookup"><span data-stu-id="5da03-124">The control developer could supply a complete UI Automation provider for the control, but this would mean duplicating much of the existing functionality of the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) implementation: for example, navigation and common properties.</span></span> <span data-ttu-id="5da03-125">Au lieu de cela, le développeur peut continuer à s’appuyer sur **IAccessible** pour fournir cette fonctionnalité, tout en ajoutant la prise en charge des propriétés spécifiques au contrôle par le biais de [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider).</span><span class="sxs-lookup"><span data-stu-id="5da03-125">Instead, the developer can continue to rely on **IAccessible** to supply this functionality, while adding support for control-specific properties through [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider).</span></span>

<span data-ttu-id="5da03-126">Pour mettre à jour le contrôle personnalisé, vous devez suivre les étapes principales suivantes :</span><span class="sxs-lookup"><span data-stu-id="5da03-126">Updating the custom control requires these main steps:</span></span>

-   <span data-ttu-id="5da03-127">Implémentez [IServiceProvider](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678965(v=vs.85)) sur l’objet accessible afin que l’interface [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) se trouve sur ce ou sur un objet distinct.</span><span class="sxs-lookup"><span data-stu-id="5da03-127">Implement [IServiceProvider](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678965(v=vs.85)) on the accessible object so that the [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) interface can be found on this or a separate object.</span></span>
-   <span data-ttu-id="5da03-128">Implémentez [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) sur l’objet accessible.</span><span class="sxs-lookup"><span data-stu-id="5da03-128">Implement [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) on the accessible object.</span></span>
-   <span data-ttu-id="5da03-129">Créez des objets accessibles distincts pour tous les éléments enfants Microsoft Active Accessibility, qui, dans Microsoft Active Accessibility, ont pu être représentés par l’interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) sur l’objet parent (par exemple, les éléments de liste).</span><span class="sxs-lookup"><span data-stu-id="5da03-129">Create distinct accessible objects for any Microsoft Active Accessibility child items, which in Microsoft Active Accessibility might have been represented by the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface on the parent object (for example, list items).</span></span> <span data-ttu-id="5da03-130">Implémentez [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) sur ces objets.</span><span class="sxs-lookup"><span data-stu-id="5da03-130">Implement [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) on these objects.</span></span>
-   <span data-ttu-id="5da03-131">Implémentez [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) sur tous les objets accessibles.</span><span class="sxs-lookup"><span data-stu-id="5da03-131">Implement [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) on all the accessible objects.</span></span>
-   <span data-ttu-id="5da03-132">Implémentez les interfaces de modèle de contrôle appropriées sur les objets accessibles.</span><span class="sxs-lookup"><span data-stu-id="5da03-132">Implement the appropriate control pattern interfaces on the accessible objects.</span></span>

<span data-ttu-id="5da03-133">Cette rubrique contient les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="5da03-133">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="5da03-134">Exposition de IAccessibleEx</span><span class="sxs-lookup"><span data-stu-id="5da03-134">Exposing IAccessibleEx</span></span>](#exposing-iaccessibleex)
-   [<span data-ttu-id="5da03-135">Implémentation de IAccessibleEx</span><span class="sxs-lookup"><span data-stu-id="5da03-135">Implementing IAccessibleEx</span></span>](#implementing-iaccessibleex)
-   [<span data-ttu-id="5da03-136">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="5da03-136">Related topics</span></span>](#related-topics)

## <a name="exposing-iaccessibleex"></a><span data-ttu-id="5da03-137">Exposition de IAccessibleEx</span><span class="sxs-lookup"><span data-stu-id="5da03-137">Exposing IAccessibleEx</span></span>

<span data-ttu-id="5da03-138">Étant donné que l’implémentation de [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) pour un contrôle peut résider dans un objet séparé, les applications clientes ne peuvent pas compter sur [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) pour obtenir cette interface.</span><span class="sxs-lookup"><span data-stu-id="5da03-138">Because the implementation of [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) for a control may reside in a separate object, client applications cannot rely on [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) to obtain this interface.</span></span> <span data-ttu-id="5da03-139">Au lieu de cela, les clients sont censés appeler [**IServiceProvider :: QueryService**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678966(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="5da03-139">Instead, clients are expected to call [**IServiceProvider::QueryService**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678966(v=vs.85)).</span></span> <span data-ttu-id="5da03-140">Dans l’exemple d’implémentation suivant de cette méthode, il est supposé que **IAccessibleEx** n’est pas implémenté sur un objet distinct ; par conséquent, la méthode appelle simplement via **QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="5da03-140">In the following example implementation of this method, it is assumed that **IAccessibleEx** is not implemented on a separate object; therefore the method simply calls through to **QueryInterface**.</span></span>


```C++
HRESULT CListboxAccessibleObject::QueryService(REFGUID guidService, REFIID riid, LPVOID *ppvObject)
{
    if (!ppvObject)
    {
        return E_INVALIDARG;
    }
    *ppvObject = NULL;
    if (guidService == __uuidof(IAccessibleEx))
    {
        return QueryInterface(riid, ppvObject);
    }
    else 
    {
        return E_INVALIDARG;
    }
};
```



## <a name="implementing-iaccessibleex"></a><span data-ttu-id="5da03-141">Implémentation de IAccessibleEx</span><span class="sxs-lookup"><span data-stu-id="5da03-141">Implementing IAccessibleEx</span></span>

<span data-ttu-id="5da03-142">La méthode de [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) qui est la plus intéressante est [**GetObjectForChild**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iaccessibleex-getobjectforchild).</span><span class="sxs-lookup"><span data-stu-id="5da03-142">The method of [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) that is of most interest is [**GetObjectForChild**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iaccessibleex-getobjectforchild).</span></span> <span data-ttu-id="5da03-143">Cette méthode donne à Microsoft Active Accessibility Server la possibilité de créer un objet accessible (un qui expose, au minimum, **IAccessibleEx**) pour un élément enfant.</span><span class="sxs-lookup"><span data-stu-id="5da03-143">This method gives the Microsoft Active Accessibility server an opportunity to create an accessible object (one that exposes, at a minimum, **IAccessibleEx**) for a child item.</span></span> <span data-ttu-id="5da03-144">Dans Microsoft Active Accessibility, les éléments enfants ne sont généralement pas représentés en tant qu’objets accessibles, mais en tant qu’enfants d’un objet accessible.</span><span class="sxs-lookup"><span data-stu-id="5da03-144">In Microsoft Active Accessibility, child items typically are not represented as accessible objects but as children of an accessible object.</span></span> <span data-ttu-id="5da03-145">Toutefois, étant donné qu’UI Automation requiert que chaque élément soit représenté par un objet accessible distinct, **GetObjectForChild** doit créer un objet distinct pour chaque enfant à la demande.</span><span class="sxs-lookup"><span data-stu-id="5da03-145">However, because UI Automation requires that each element be represented by a separate accessible object, **GetObjectForChild** must create a separate object for each child on demand.</span></span>

<span data-ttu-id="5da03-146">L’exemple d’implémentation suivant retourne un objet accessible pour un élément dans un affichage de liste personnalisé.</span><span class="sxs-lookup"><span data-stu-id="5da03-146">The following example implementation returns an accessible object for an item in a custom list view.</span></span>


```C++
HRESULT CListboxAccessibleObject::GetObjectForChild(long idChild, IAccessibleEx **pRetVal)
{ 
    *pRetVal = NULL;
    VARIANT vChild;
    vChild.vt = VT_I4;
    vChild.lVal = idChild;

    // ValidateChildId is an application-defined function that checks whether
    // the child ID is valid. This is similar to code that validates the varChild
    // parameter in IAccessible methods.
    //
    // Additionally, if this idChild corresponds to a child that has its own
    // IAccessible, we should also return E_INVALIDARG here. (The caller
    // should instead be using the IAccessibleEx from that child's own
    // IAccessible in that case.)
    if (idChild == CHILDID_SELF || FAILED(ValidateChildId(vChild)))
    {
        return E_INVALIDARG;
    }

    // Return a suitable provider for this specific child.
    // This implementation returns a new instance each time; an implementation
    // can cache these if desired.

    // _pListboxControl is a member variable pointer to the owning control.
    IAccessibleEx* pAccEx  = new CListItemAccessibleObject(idChild, _pListboxControl);
    if (pAccEx == NULL)
    {
        return E_OUTOFMEMORY;
    }
    *pRetVal = pAccEx;
    return S_OK; 
}
```



<span data-ttu-id="5da03-147">Pour obtenir un exemple complet d’implémentation, consultez [rendre des contrôles personnalisés accessibles, partie 5 : utilisation de IAccessibleEx pour ajouter la prise en charge d’UI Automation à un contrôle personnalisé](/previous-versions/msdn10/cc307850(v=msdn.10)) sur MSDN.</span><span class="sxs-lookup"><span data-stu-id="5da03-147">For a complete sample implementation, see [Making Custom Controls Accessible, Part 5: Using IAccessibleEx to Add UI Automation Support to a Custom Control](/previous-versions/msdn10/cc307850(v=msdn.10)) on MSDN.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5da03-148">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="5da03-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5da03-149">Guide du programmeur du fournisseur UI Automation</span><span class="sxs-lookup"><span data-stu-id="5da03-149">UI Automation Provider Programmer's Guide</span></span>](uiauto-providerportal.md)
</dt> </dl>

 

 