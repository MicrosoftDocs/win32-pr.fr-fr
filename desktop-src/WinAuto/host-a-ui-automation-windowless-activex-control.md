---
title: Héberger un contrôle ActiveX UI Automation sans fenêtre
description: Découvrez comment créer un conteneur de contrôle qui peut héberger des contrôles Microsoft ActiveX sans fenêtre qui implémentent l’automatisation d’interface utilisateur de Microsoft.
ms.assetid: A0F82968-F434-4F5E-8052-CF7CE65DB120
keywords:
- UI Automation, contrôle ActiveX sans fenêtre
- Contrôle ActiveX sans fenêtre, UI Automation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77026d923ea6f0d2536cbd6a94966ec858443258
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315288"
---
# <a name="host-a-ui-automation-windowless-activex-control"></a><span data-ttu-id="b0222-105">Héberger un contrôle ActiveX UI Automation sans fenêtre</span><span class="sxs-lookup"><span data-stu-id="b0222-105">Host a UI Automation Windowless ActiveX Control</span></span>

<span data-ttu-id="b0222-106">Découvrez comment créer un conteneur de contrôle qui peut héberger des contrôles Microsoft ActiveX sans fenêtre qui implémentent l’automatisation d’interface utilisateur de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="b0222-106">Learn how to create a control container that can host windowless Microsoft ActiveX controls that implement Microsoft UI Automation.</span></span> <span data-ttu-id="b0222-107">En suivant les étapes décrites ici, vous pouvez vous assurer que les contrôles sans fenêtre UI Automation qui sont hébergés dans votre conteneur de contrôle sont accessibles aux applications clientes de technologie d’assistance (AT).</span><span class="sxs-lookup"><span data-stu-id="b0222-107">By using the steps described here, you can ensure that any UI Automation windowless controls that are hosted in your control container are accessible to assistive technology (AT) client applications.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="b0222-108">Ce que vous devez savoir</span><span class="sxs-lookup"><span data-stu-id="b0222-108">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="b0222-109">Technologies</span><span class="sxs-lookup"><span data-stu-id="b0222-109">Technologies</span></span>

-   [<span data-ttu-id="b0222-110">Contrôles ActiveX</span><span class="sxs-lookup"><span data-stu-id="b0222-110">ActiveX Controls</span></span>](/windows/desktop/com/activex-controls)
-   [<span data-ttu-id="b0222-111">UI Automation</span><span class="sxs-lookup"><span data-stu-id="b0222-111">UI Automation</span></span>](entry-uiauto-win32.md)

### <a name="prerequisites"></a><span data-ttu-id="b0222-112">Prérequis</span><span class="sxs-lookup"><span data-stu-id="b0222-112">Prerequisites</span></span>

-   <span data-ttu-id="b0222-113">C/C++</span><span class="sxs-lookup"><span data-stu-id="b0222-113">C/C++</span></span>
-   <span data-ttu-id="b0222-114">Programmation Microsoft Win32 et COM (Component Object Model)</span><span class="sxs-lookup"><span data-stu-id="b0222-114">Microsoft Win32 and Component Object Model (COM) programming</span></span>
-   <span data-ttu-id="b0222-115">Contrôles ActiveX sans fenêtre</span><span class="sxs-lookup"><span data-stu-id="b0222-115">Windowless ActiveX controls</span></span>
-   <span data-ttu-id="b0222-116">Fournisseurs UI Automation</span><span class="sxs-lookup"><span data-stu-id="b0222-116">UI Automation providers</span></span>

## <a name="instructions"></a><span data-ttu-id="b0222-117">Instructions</span><span class="sxs-lookup"><span data-stu-id="b0222-117">Instructions</span></span>

### <a name="step-1-provide-the-irawelementprovidersimple-interface-on-behalf-of-the-windowless-control"></a><span data-ttu-id="b0222-118">Étape 1 : fournissez l’interface IRawElementProviderSimple pour le compte du contrôle sans fenêtre.</span><span class="sxs-lookup"><span data-stu-id="b0222-118">Step 1: Provide the IRawElementProviderSimple interface on behalf of the windowless control.</span></span>

<span data-ttu-id="b0222-119">Chaque fois que le système a besoin du pointeur [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) pour la racine d’un contrôle sans fenêtre, le système interroge le conteneur de contrôle.</span><span class="sxs-lookup"><span data-stu-id="b0222-119">Whenever the system needs the [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) pointer for the root of a windowless control, the system queries the control container.</span></span> <span data-ttu-id="b0222-120">Pour récupérer le pointeur, le conteneur appelle l’implémentation du contrôle sans fenêtre de la méthode [**IServiceProvider :: QueryService**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678966(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="b0222-120">To retrieve the pointer, the container calls the windowless control's implementation of the [**IServiceProvider::QueryService**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678966(v=vs.85)) method.</span></span>

<span data-ttu-id="b0222-121">Si le conteneur de contrôle a une implémentation UI Automation, il peut retourner le pointeur [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) du contrôle sans fenêtre au système.</span><span class="sxs-lookup"><span data-stu-id="b0222-121">If the control container has a UI Automation implementation, it can return the windowless control's [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) pointer to the system.</span></span>

<span data-ttu-id="b0222-122">Si le conteneur de contrôle a une implémentation Microsoft Active Accessibility, appelez la fonction [**UiaIAccessibleFromProvider**](/windows/desktop/api/uiautomationcoreapi/nf-uiautomationcoreapi-uiaiaccessiblefromprovider) pour obtenir un pointeur d’interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) qui représente le contrôle, puis retournez le pointeur d’interface **IAccessible** au système.</span><span class="sxs-lookup"><span data-stu-id="b0222-122">If the control container has a Microsoft Active Accessibility implementation, call the [**UiaIAccessibleFromProvider**](/windows/desktop/api/uiautomationcoreapi/nf-uiautomationcoreapi-uiaiaccessiblefromprovider) function to obtain an [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface pointer that represents the control, and then return the **IAccessible** interface pointer to the system.</span></span>

### <a name="step-2-implement-the-irawelementproviderwindowlesssite-interface"></a><span data-ttu-id="b0222-123">Étape 2 : implémenter l’interface IRawElementProviderWindowlessSite.</span><span class="sxs-lookup"><span data-stu-id="b0222-123">Step 2: Implement the IRawElementProviderWindowlessSite interface.</span></span>

<span data-ttu-id="b0222-124">Un conteneur de contrôle implémente l’interface [**IRawElementProviderWindowlessSite**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-irawelementproviderwindowlesssite) active un contrôle sans fenêtre basé sur UI Automation pour communiquer ses informations d’accessibilité.</span><span class="sxs-lookup"><span data-stu-id="b0222-124">A control container implements the [**IRawElementProviderWindowlessSite**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-irawelementproviderwindowlesssite) interface enable a windowless control that is based on UI Automation to communicate its accessibility information.</span></span>

1.  <span data-ttu-id="b0222-125">Implémentez [**IRawElementProviderWindowlessSite :: GetRuntimeIdPrefix**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderwindowlesssite-getruntimeidprefix).</span><span class="sxs-lookup"><span data-stu-id="b0222-125">Implement [**IRawElementProviderWindowlessSite::GetRuntimeIdPrefix**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderwindowlesssite-getruntimeidprefix).</span></span>

    <span data-ttu-id="b0222-126">Un fragment de contrôle sans fenêtre doit créer un ID d’exécution unique pour lui-même.</span><span class="sxs-lookup"><span data-stu-id="b0222-126">A windowless control fragment must create a unique runtime ID for itself.</span></span> <span data-ttu-id="b0222-127">Pour créer son ID d’exécution, un fragment de contrôle sans fenêtre récupère une valeur de préfixe en appelant la méthode [**GetRuntimeIdPrefix**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderwindowlesssite-getruntimeidprefix) du site de contrôle, puis ajoute au préfixe une valeur entière qui est unique par rapport à tous les autres fragments dans le contrôle sans fenêtre.</span><span class="sxs-lookup"><span data-stu-id="b0222-127">To create its runtime ID, a windowless control fragment retrieves a prefix value by calling the control site's [**GetRuntimeIdPrefix**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderwindowlesssite-getruntimeidprefix) method, and then appends to the prefix an integer value that is unique relative to all other fragments in the windowless control.</span></span>

    <span data-ttu-id="b0222-128">Le site de contrôle d’un contrôle sans fenêtre doit implémenter la méthode [**GetRuntimeIdPrefix**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderwindowlesssite-getruntimeidprefix) en formant un **SAFEARRAY** qui contient la constante **UiaAppendRuntimeId**, suivie d’une valeur entière qui est unique pour le site.</span><span class="sxs-lookup"><span data-stu-id="b0222-128">The control site for a windowless control should implement the [**GetRuntimeIdPrefix**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderwindowlesssite-getruntimeidprefix) method by forming a **SAFEARRAY** that contains the constant **UiaAppendRuntimeId**, followed by an integer value that is unique to the site.</span></span>

    <span data-ttu-id="b0222-129">Cet exemple montre comment retourner un préfixe d’ID d’exécution pour un contrôle sans fenêtre.</span><span class="sxs-lookup"><span data-stu-id="b0222-129">This example shows how to return a runtime ID prefix for a windowless control.</span></span>

    ```C++
    IFACEMETHODIMP CProviderWindowlessSite::GetRuntimeIdPrefix(   
         SAFEARRAY **ppsaPrefix)   
    {   
        if (ppsaPrefix == NULL) 
        {
            return E_INVALIDARG;
        }

        // m_siteIndex is the index of the windowless control's
        // site. It is defined by the control container.
        int rId[] = { UiaAppendRuntimeId, m_siteIndex };
        SAFEARRAY *psa = SafeArrayCreateVector(VT_I4, 0, 2);  
        if (psa == NULL)
        {
            return E_OUTOFMEMORY;
        }

        for (LONG i = 0; i < 2; i++)
        {
            SafeArrayPutElement(psa, &i, (void*)&(rId[i]));
        }

        *ppsaPrefix = psa;  
        return S_OK;  
    }  
    ```

    

2.  <span data-ttu-id="b0222-130">Implémentez la méthode [**IRawElementProviderWindowlessSite :: GetAdjacentFragment**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderwindowlesssite-getadjacentfragment) .</span><span class="sxs-lookup"><span data-stu-id="b0222-130">Implement the [**IRawElementProviderWindowlessSite::GetAdjacentFragment**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderwindowlesssite-getadjacentfragment) method.</span></span>

    <span data-ttu-id="b0222-131">Un contrôle qui implémente UI Automation doit retourner un pointeur vers le fournisseur de fragments parent du contrôle.</span><span class="sxs-lookup"><span data-stu-id="b0222-131">A control that implements UI Automation must return a pointer to the control's parent fragment provider.</span></span>

    <span data-ttu-id="b0222-132">Pour retourner le parent du fragment, un objet qui implémente l’interface [**IRawElementProviderFragment**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragment) doit être en mesure d’implémenter la méthode [**Navigate**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragment-navigate) .</span><span class="sxs-lookup"><span data-stu-id="b0222-132">To return the parent of the fragment, an object that implements the [**IRawElementProviderFragment**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragment) interface must be able to implement the [**Navigate**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragment-navigate) method.</span></span> <span data-ttu-id="b0222-133">L’implémentation de **Navigate** est difficile pour un contrôle sans fenêtre, car le contrôle peut ne pas être en mesure de déterminer son emplacement dans l’arborescence accessible de l’objet parent.</span><span class="sxs-lookup"><span data-stu-id="b0222-133">Implementing **Navigate** is difficult for a windowless control because the control might be unable to determine its location in the accessible tree of the parent object.</span></span> <span data-ttu-id="b0222-134">La méthode [**IRawElementProviderWindowlessSite :: GetAdjacentFragment**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderwindowlesssite-getadjacentfragment) permet au contrôle sans fenêtre d’interroger son site pour le fragment adjacent, puis de retourner ce fragment au client qui a appelé **Navigate**.</span><span class="sxs-lookup"><span data-stu-id="b0222-134">The [**IRawElementProviderWindowlessSite::GetAdjacentFragment**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderwindowlesssite-getadjacentfragment) method enables the windowless control to query its site for the adjacent fragment, and then return that fragment to the client that called **Navigate**.</span></span>

    <span data-ttu-id="b0222-135">Cet exemple montre comment un conteneur de contrôles récupère le fragment parent d’un contrôle sans fenêtre.</span><span class="sxs-lookup"><span data-stu-id="b0222-135">This example shows how a control container retrieves the parent fragment of a windowless control.</span></span>

    ```C++
    IFACEMETHODIMP CProviderWindowlessSite::GetAdjacentFragment(
            enum NavigateDirection direction, IRawElementProviderFragment **ppFragment)   
    {
        if (ppFragment == NULL)
        {
            return E_INVALIDARG;
        }
        
        *ppFragment = NULL;
        HRESULT hr = S_OK;

        switch (direction)
        {
            case NavigateDirection_Parent:
                {  
                    IRawElementProviderSimple *pSimple = NULL;

                    // Call an application-defined function to retrieve the
                    // parent provider interface.
                    hr = GetParentProvider(&pSimple);  
                    if (SUCCEEDED(hr))  
                    {  
                        // Get the parent's IRawElementProviderFragment interface.
                        hr = pSimple->QueryInterface(IID_PPV_ARGS(ppFragment));  
                        pSimple->Release();  
                    } 
                }  
                break;  
      
            case NavigateDirection_FirstChild:
            case NavigateDirection_LastChild:
                hr = E_INVALIDARG;
                break;

            // Ignore NavigateDirection_NextSibling and NavigateDirection_PreviousSibling
            // because there are no adjacent fragments.
            default:  
                break;  
        }  
      
        return hr;  
    }   
    ```

    

### <a name="step-3-optional-implement-the-irawelementproviderhostingaccessibles-interface"></a><span data-ttu-id="b0222-136">Étape 3 : facultatif : implémentez l’interface IRawElementProviderHostingAccessibles.</span><span class="sxs-lookup"><span data-stu-id="b0222-136">Step 3: Optional: Implement the IRawElementProviderHostingAccessibles interface.</span></span>

<span data-ttu-id="b0222-137">Implémentez l’interface [**IRawElementProviderHostingAccessibles**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-irawelementproviderhostingaccessibles) si votre conteneur de contrôle a une implémentation de fournisseur UI Automation qui est la racine d’une arborescence d’accessibilité qui inclut des contrôles ActiveX sans fenêtre qui prennent en charge Microsoft Active Accessibility.</span><span class="sxs-lookup"><span data-stu-id="b0222-137">Implement the [**IRawElementProviderHostingAccessibles**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-irawelementproviderhostingaccessibles) interface if your control container has a UI Automation provider implementation that is the root of an accessibility tree that includes windowless ActiveX controls that support Microsoft Active Accessibility.</span></span> <span data-ttu-id="b0222-138">L’interface **IRawElementProviderHostingAccessibles** possède une méthode unique, [**GetEmbeddedAccessibles**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderhostingaccessibles-getembeddedaccessibles), qui récupère les pointeurs d’interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) de tous les contrôles ActiveX de Microsoft Active Accessibility qui sont hébergés par votre conteneur de contrôle.</span><span class="sxs-lookup"><span data-stu-id="b0222-138">The **IRawElementProviderHostingAccessibles** interface has a single method, [**GetEmbeddedAccessibles**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderhostingaccessibles-getembeddedaccessibles), which retrieves the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface pointers of all Microsoft Active Accessibility-based windowless ActiveX controls that are hosted by your control container.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b0222-139">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b0222-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b0222-140">Comment héberger un contrôle ActiveX sans fenêtre MSAA</span><span class="sxs-lookup"><span data-stu-id="b0222-140">How to Host an MSAA Windowless ActiveX Control</span></span>](host-an-msaa-windowless-activex-control.md)
</dt> <dt>

[<span data-ttu-id="b0222-141">Accessibilité des contrôles ActiveX sans fenêtre</span><span class="sxs-lookup"><span data-stu-id="b0222-141">Windowless ActiveX Control Accessibility</span></span>](windowless-activex-control-accessibility.md)
</dt> </dl>

 

 