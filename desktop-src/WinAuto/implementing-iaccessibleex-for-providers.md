---
title: Implémentation de IAccessibleEx pour les fournisseurs
description: Cette section explique comment ajouter des fonctionnalités de fournisseur Microsoft UI Automation à un serveur Microsoft Active Accessibility en implémentant l’interface IAccessibleEx.
ms.assetid: c03dc552-7919-4a35-8ff2-4cdd822bc0b7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9460ccbd243aef390b7ade0deb41626173c927a0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106512504"
---
# <a name="implementing-iaccessibleex-for-providers"></a><span data-ttu-id="b297b-103">Implémentation de IAccessibleEx pour les fournisseurs</span><span class="sxs-lookup"><span data-stu-id="b297b-103">Implementing IAccessibleEx for Providers</span></span>

<span data-ttu-id="b297b-104">Cette section explique comment ajouter des fonctionnalités de fournisseur Microsoft UI Automation à un serveur Microsoft Active Accessibility en implémentant l’interface [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) .</span><span class="sxs-lookup"><span data-stu-id="b297b-104">This section explains how to add Microsoft UI Automation provider capabilities to a Microsoft Active Accessibility server by implementing the [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) interface.</span></span>

<span data-ttu-id="b297b-105">Avant d’implémenter [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex), tenez compte des exigences suivantes :</span><span class="sxs-lookup"><span data-stu-id="b297b-105">Before implementing [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex), consider the following requirements:</span></span>

-   <span data-ttu-id="b297b-106">La hiérarchie des objets accessibles par Microsoft Active Accessibility de référence doit être propre.</span><span class="sxs-lookup"><span data-stu-id="b297b-106">The baseline Microsoft Active Accessibility accessible object hierarchy must be clean.</span></span> <span data-ttu-id="b297b-107">[**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) ne peut pas corriger les problèmes liés aux hiérarchies d’objets accessibles existantes.</span><span class="sxs-lookup"><span data-stu-id="b297b-107">[**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) cannot correct problems with existing accessible object hierarchies.</span></span> <span data-ttu-id="b297b-108">Tous les problèmes liés à la structure du modèle objet doivent être corrigés dans l’implémentation de Microsoft Active Accessibility avant d’implémenter **IAccessibleEx**.</span><span class="sxs-lookup"><span data-stu-id="b297b-108">Any problems with the object model structure must be corrected in the Microsoft Active Accessibility implementation before implementing **IAccessibleEx**.</span></span>
-   <span data-ttu-id="b297b-109">L’implémentation de [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) doit être conforme à la spécification Microsoft Active Accessibility et à la spécification UI Automation.</span><span class="sxs-lookup"><span data-stu-id="b297b-109">The [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) implementation must comply with both the Microsoft Active Accessibility specification and the UI Automation specification.</span></span> <span data-ttu-id="b297b-110">Des outils sont disponibles pour valider la conformité dans les deux spécifications.</span><span class="sxs-lookup"><span data-stu-id="b297b-110">Tools are available to validate compliance under both specifications.</span></span> <span data-ttu-id="b297b-111">Pour plus d’informations, consultez [outils de test](testing-tools.md) et vérification d' [UI Automation vérifier (UIA Verify) infrastructure d’automatisation de test](https://www.codeplex.com/UIAutomationVerify/).</span><span class="sxs-lookup"><span data-stu-id="b297b-111">For more information, see [Testing Tools](testing-tools.md) and [UI Automation Verify (UIA Verify) Test Automation Framework](https://www.codeplex.com/UIAutomationVerify/).</span></span>

<span data-ttu-id="b297b-112">L’implémentation de [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) nécessite les étapes principales suivantes :</span><span class="sxs-lookup"><span data-stu-id="b297b-112">Implementing [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) requires these main steps:</span></span>

-   <span data-ttu-id="b297b-113">Implémentez **IServiceProvider** sur l’objet accessible afin que l’interface [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) se trouve sur ce ou sur un objet distinct.</span><span class="sxs-lookup"><span data-stu-id="b297b-113">Implement **IServiceProvider** on the accessible object so that the [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) interface can be found on this or a separate object.</span></span>
-   <span data-ttu-id="b297b-114">Implémentez [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) sur l’objet accessible.</span><span class="sxs-lookup"><span data-stu-id="b297b-114">Implement [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) on the accessible object.</span></span>
-   <span data-ttu-id="b297b-115">Créez des objets accessibles pour tous les éléments enfants Microsoft Active Accessibility, qui, dans Microsoft Active Accessibility, sont représentés par l’interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) sur l’objet parent (par exemple, les éléments de liste).</span><span class="sxs-lookup"><span data-stu-id="b297b-115">Create accessible objects for any Microsoft Active Accessibility child items, which in Microsoft Active Accessibility are represented by the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface on the parent object (for example, list items).</span></span> <span data-ttu-id="b297b-116">Implémentez [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) sur ces objets.</span><span class="sxs-lookup"><span data-stu-id="b297b-116">Implement [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) on these objects.</span></span>
-   <span data-ttu-id="b297b-117">Implémentez [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) sur tous les objets accessibles.</span><span class="sxs-lookup"><span data-stu-id="b297b-117">Implement [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) on all the accessible objects.</span></span>
-   <span data-ttu-id="b297b-118">Implémentez les interfaces de modèle de contrôle appropriées sur les objets accessibles.</span><span class="sxs-lookup"><span data-stu-id="b297b-118">Implement the appropriate control pattern interfaces on the accessible objects.</span></span>

### <a name="implementing-the-iserviceprovider-interface"></a><span data-ttu-id="b297b-119">Implémentation de l’interface IServiceProvider</span><span class="sxs-lookup"><span data-stu-id="b297b-119">Implementing the IServiceProvider Interface</span></span>

<span data-ttu-id="b297b-120">Étant donné que l’implémentation de [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) pour un contrôle peut résider dans un objet séparé, les applications clientes ne peuvent pas compter sur [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) pour obtenir cette interface.</span><span class="sxs-lookup"><span data-stu-id="b297b-120">Because the implementation of [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) for a control may reside in a separate object, client applications cannot rely on [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) to obtain this interface.</span></span> <span data-ttu-id="b297b-121">Au lieu de cela, les clients sont censés appeler **IServiceProvider :: QueryService**.</span><span class="sxs-lookup"><span data-stu-id="b297b-121">Instead, clients are expected to call **IServiceProvider::QueryService**.</span></span> <span data-ttu-id="b297b-122">Dans l’exemple d’implémentation suivant de cette méthode, il est supposé que **IAccessibleEx** n’est pas implémenté sur un objet distinct ; par conséquent, la méthode appelle simplement via **QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="b297b-122">In the following example implementation of this method, it is assumed that **IAccessibleEx** is not implemented on a separate object; therefore the method simply calls through to **QueryInterface**.</span></span>


```C++
           
HRESULT CListboxAccessibleObject::QueryService(REFGUID guidService, REFIID riid, LPVOID *ppvObject)
{
    if (ppvObject == NULL)
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
        return E_NOINTERFACE;
    }
};      
```



### <a name="implementing-the-iaccessibleex-interface"></a><span data-ttu-id="b297b-123">Implémentation de l’interface IAccessibleEx</span><span class="sxs-lookup"><span data-stu-id="b297b-123">Implementing the IAccessibleEx Interface</span></span>

<span data-ttu-id="b297b-124">Dans Microsoft Active Accessibility, un élément d’interface utilisateur est toujours identifié par une interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) et un ID enfant.</span><span class="sxs-lookup"><span data-stu-id="b297b-124">In Microsoft Active Accessibility, a UI element is always identified by an [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface and a child ID.</span></span> <span data-ttu-id="b297b-125">Une seule instance de **IAccessible** peut représenter plusieurs éléments d’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="b297b-125">A single instance of **IAccessible** can represent multiple UI elements.</span></span>

<span data-ttu-id="b297b-126">Étant donné que chaque instance de [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) représente un seul élément d’interface utilisateur, chaque paire [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) /ID enfant doit être mappée à une seule instance **IAccessibleEx** .</span><span class="sxs-lookup"><span data-stu-id="b297b-126">Because each [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) instance represents only a single UI element, each [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) and child ID pair must be mapped to a single **IAccessibleEx** instance.</span></span> <span data-ttu-id="b297b-127">**IAccessibleEx** comprend deux méthodes pour gérer ce mappage :</span><span class="sxs-lookup"><span data-stu-id="b297b-127">**IAccessibleEx** includes two methods to handle this mapping:</span></span>

-   <span data-ttu-id="b297b-128">[**GetObjectForChild**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iaccessibleex-getobjectforchild): récupère l’interface [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) pour l’enfant spécifié.</span><span class="sxs-lookup"><span data-stu-id="b297b-128">[**GetObjectForChild**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iaccessibleex-getobjectforchild)—Retrieves the [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) interface for the specified child.</span></span> <span data-ttu-id="b297b-129">Cette méthode retourne la **valeur null** si l’implémentation de **IAccessibleEx** ne reconnaît pas l’ID enfant spécifié, n’a pas de **IAccessibleEx** pour l’enfant spécifié ou représente un élément enfant.</span><span class="sxs-lookup"><span data-stu-id="b297b-129">This method returns **NULL** if the **IAccessibleEx** implementation does not recognize the specified child ID, does not have an **IAccessibleEx** for the specified child, or represents a child element.</span></span>
-   <span data-ttu-id="b297b-130">[**GetIAccessiblePair**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iaccessibleex-getiaccessiblepair): récupère l’interface [**IACCESSIBLE**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) et l’ID enfant de l’élément [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) .</span><span class="sxs-lookup"><span data-stu-id="b297b-130">[**GetIAccessiblePair**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iaccessibleex-getiaccessiblepair)—Retrieves the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface and child ID for the [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) element.</span></span> <span data-ttu-id="b297b-131">Pour les implémentations **IAccessible** qui n’utilisent pas d’ID enfant, cette méthode récupère l’objet **IAccessible** correspondant et le CHILDID \_ self.</span><span class="sxs-lookup"><span data-stu-id="b297b-131">For **IAccessible** implementations that do not use a child ID, this method retrieves the corresponding **IAccessible** object and CHILDID\_SELF.</span></span>

<span data-ttu-id="b297b-132">L’exemple suivant illustre l’implémentation des méthodes [**GetObjectForChild**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iaccessibleex-getobjectforchild) et [**GetIAccessiblePair**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iaccessibleex-getiaccessiblepair) pour un élément dans un affichage de liste personnalisé.</span><span class="sxs-lookup"><span data-stu-id="b297b-132">The following example shows the implementation of the [**GetObjectForChild**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iaccessibleex-getobjectforchild) and [**GetIAccessiblePair**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iaccessibleex-getiaccessiblepair) methods for an item in a custom list view.</span></span> <span data-ttu-id="b297b-133">Les méthodes permettent à UI Automation de mapper la paire d’ID d’enfant et [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) à une instance [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) correspondante.</span><span class="sxs-lookup"><span data-stu-id="b297b-133">The methods enable UI Automation to map the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) and child ID pair to a corresponding [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) instance.</span></span>


```C++
           
HRESULT CListboxAccessibleObject::GetObjectForChild(
    long idChild, IAccessibleEx **ppRetVal)
{ 
    VARIANT vChild;
    vChild.vt = VT_I4;
    vChild.lVal = idChild;
    HRESULT hr = ValidateChildId(vChild);
    if (FAILED(hr))
    {
        return E_INVALIDARG;
    }
    // List item accessible objects are stored as an array of
    // pointers; for the purpose of this example it is assumed that 
    // the list contents will not change. Accessible objects are
    // created only when needed.
    if (itemProviders[idChild - 1] == NULL)
    {
        // Create an object that supports UI Automation and
        // IAccessibleEx for the item.
        itemProviders[idChild - 1] = 
          new CListItemAccessibleObject(idChild, 
          g_pListboxControl);
        if (itemProviders[idChild - 1] == NULL)
        {
            return E_OUTOFMEMORY;
        }
    }
    IAccessibleEx* pAccEx = static_cast<IAccessibleEx*>
      (itemProviders[idChild - 1]);
    if (pAccEx != NULL)
    {
      pAccEx->AddRef();
    }
    *ppRetVal = pAccEx;
    return S_OK; 
}

HRESULT CListItemAccessibleObject::GetIAccessiblePair(
    IAccessible **ppAcc, long *pidChild)
{ 
    if (ppAcc == NULL || pidChild == NULL)
    {
        return E_INVALIDARG;   
    }

                CListboxAccessibleObject* pParent = 
        m_control->GetAccessibleObject();

    HRESULT hr = pParent->QueryInterface( 
        __uuidof(IAccessible), (void**)ppAcc);
    if (FAILED(hr))
    {
        *pidChild = 0;
        return E_NOINTERFACE;
    }
    *pidChild = m_childID; 
    return S_OK; 
}
}
```



<span data-ttu-id="b297b-134">Si une implémentation d’objet accessible n’utilise pas d’ID enfant, les méthodes peuvent toujours être implémentées comme indiqué dans l’extrait de code suivant.</span><span class="sxs-lookup"><span data-stu-id="b297b-134">If an accessible object implementation does not use a child ID, the methods can still be implemented as shown in the following code snippet.</span></span>


```C++
           

    // This sample implements IAccessibleEx on the same object; it could use a tear-off
    // or inner object instead.
    class MyAccessibleImpl: public IAccessible,
                        public IAccessibleEx,
                        public IRawElementProviderSimple
    {
    public:
    ...
   HRESULT STDMETHODCALLTYPE GetObjectForChild( long idChild, IAccessibleEx **ppRetVal )
    {
        // This implementation does not support child IDs.
        *ppRetVal = NULL;
        return S_OK;
    }

    HRESULT STDMETHODCALLTYPE GetIAccessiblePair( IAccessible ** ppAcc, long * pidChild )
    {
        // This implementation assumes that IAccessibleEx is implemented on same object as
        // IAccessible.
        *ppAcc = static_cast<IAccessible *>(this);
        (*ppAcc)->AddRef();
        *pidChild = CHILDID_SELF;
        return S_OK;
    }
```



### <a name="implement-the-irawelementprovidersimple-interface"></a><span data-ttu-id="b297b-135">Implémenter l’interface IRawElementProviderSimple</span><span class="sxs-lookup"><span data-stu-id="b297b-135">Implement the IRawElementProviderSimple Interface</span></span>

<span data-ttu-id="b297b-136">Les serveurs utilisent [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) pour exposer des informations sur les propriétés UI Automation et les modèles de contrôle.</span><span class="sxs-lookup"><span data-stu-id="b297b-136">Servers use [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) to expose information about UI Automation properties and control patterns.</span></span> <span data-ttu-id="b297b-137">**IRawElementProviderSimple** comprend les méthodes suivantes :</span><span class="sxs-lookup"><span data-stu-id="b297b-137">**IRawElementProviderSimple** includes the following methods:</span></span>

-   <span data-ttu-id="b297b-138">[**GetPatternProvider**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-getpatternprovider): cette méthode est utilisée pour exposer des interfaces de modèle de contrôle.</span><span class="sxs-lookup"><span data-stu-id="b297b-138">[**GetPatternProvider**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-getpatternprovider)—This method is used to expose control pattern interfaces.</span></span> <span data-ttu-id="b297b-139">Elle retourne un objet qui prend en charge le modèle de contrôle spécifié, ou **null** si le modèle de contrôle n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="b297b-139">It returns an object that supports the specified control pattern, or **NULL** if the control pattern is not supported.</span></span>
-   <span data-ttu-id="b297b-140">[**GetPropertyValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-getpropertyvalue): cette méthode est utilisée pour exposer des valeurs de propriété UI Automation.</span><span class="sxs-lookup"><span data-stu-id="b297b-140">[**GetPropertyValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-getpropertyvalue)—This method is used to expose UI Automation property values.</span></span>
-   <span data-ttu-id="b297b-141">[**HostRawElementProvider**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-get_hostrawelementprovider): cette méthode n’est pas utilisée avec les implémentations [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) .</span><span class="sxs-lookup"><span data-stu-id="b297b-141">[**HostRawElementProvider**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-get_hostrawelementprovider)—This method is not used with [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) implementations.</span></span>
-   <span data-ttu-id="b297b-142">[**ProviderOptions**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-get_provideroptions): cette méthode n’est pas utilisée avec les implémentations [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) .</span><span class="sxs-lookup"><span data-stu-id="b297b-142">[**ProviderOptions**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-get_provideroptions)—This method is not used with [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) implementations.</span></span>

<span data-ttu-id="b297b-143">Un serveur [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) expose des modèles de contrôle en implémentant [**IRawElementProviderSimple :: GetPatternProvider**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-getpatternprovider).</span><span class="sxs-lookup"><span data-stu-id="b297b-143">An [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) server exposes control patterns by implementing [**IRawElementProviderSimple::GetPatternProvider**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-getpatternprovider).</span></span> <span data-ttu-id="b297b-144">Cette méthode prend un paramètre entier qui spécifie le modèle de contrôle.</span><span class="sxs-lookup"><span data-stu-id="b297b-144">This method takes an integer parameter that specifies the control pattern.</span></span> <span data-ttu-id="b297b-145">Le serveur retourne la **valeur null** si le modèle n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="b297b-145">The server returns **NULL** if the pattern is not supported.</span></span> <span data-ttu-id="b297b-146">Si l’interface de modèle de contrôle est prise en charge, les serveurs retournent un [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) et le client appelle ensuite [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) pour obtenir le modèle de contrôle approprié.</span><span class="sxs-lookup"><span data-stu-id="b297b-146">If the control pattern interface is supported, servers return an [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) and the client then calls [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) to get the appropriate control pattern.</span></span>

<span data-ttu-id="b297b-147">Un serveur [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) peut prendre en charge les propriétés UI Automation (telles que LabeledBy et IsRequiredForForm) en implémentant [**IRawElementProviderSimple :: GetPropertyValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-getpropertyvalue) et en fournissant un PROPERTYID entier qui identifie la propriété en tant que paramètre.</span><span class="sxs-lookup"><span data-stu-id="b297b-147">An [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) server can support UI Automation properties (such as LabeledBy, and IsRequiredForForm) by implementing [**IRawElementProviderSimple::GetPropertyValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-getpropertyvalue) and supplying an integer PROPERTYID identifying the property as a parameter.</span></span> <span data-ttu-id="b297b-148">Cette technique s’applique uniquement aux propriétés UI Automation qui ne sont pas incluses dans une interface de modèle de contrôle.</span><span class="sxs-lookup"><span data-stu-id="b297b-148">This technique applies only to UI Automation properties that are not included in a control pattern interface.</span></span> <span data-ttu-id="b297b-149">Les propriétés associées à une interface de modèle de contrôle sont exposées par le biais de la méthode d’interface de modèle de contrôle.</span><span class="sxs-lookup"><span data-stu-id="b297b-149">Properties associated with a control pattern interface are exposed through the control pattern interface method.</span></span> <span data-ttu-id="b297b-150">Par exemple, la propriété IsSelected du modèle de contrôle [SelectionItem](uiauto-implementingselectionitem.md) est exposée avec [**ISelectionItemProvider :: obtenir \_ IsSelected**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionitemprovider-get_isselected).</span><span class="sxs-lookup"><span data-stu-id="b297b-150">For example, the IsSelected property from the [SelectionItem](uiauto-implementingselectionitem.md) control pattern would be exposed with [**ISelectionItemProvider::get\_IsSelected**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionitemprovider-get_isselected).</span></span>

 

 