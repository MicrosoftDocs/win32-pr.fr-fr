---
title: Comment utiliser UI Automation pour rendre un contrôle ActiveX sans fenêtre accessible
description: Décrit comment utiliser l’automatisation de l’interface utilisateur de Microsoft \ 32 ; API permettant de s’assurer que votre contrôle Microsoft ActiveX sans fenêtre est accessible aux applications clientes de la technologie d’assistance (AT).
ms.assetid: D584E90D-6537-4F48-8553-0DCA061FAF2A
keywords:
- Contrôle ActiveX sans fenêtre, accessibilité
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba0ada1d26463b0654c1808f6e4fd43f571687d9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728420"
---
# <a name="how-to-use-ui-automation-to-make-a-windowless-activex-control-accessible"></a><span data-ttu-id="c6fee-104">Comment utiliser UI Automation pour rendre un contrôle ActiveX sans fenêtre accessible</span><span class="sxs-lookup"><span data-stu-id="c6fee-104">How to Use UI Automation to Make a Windowless ActiveX Control Accessible</span></span>

<span data-ttu-id="c6fee-105">Décrit comment utiliser l’API d’automatisation d’interface utilisateur de Microsoft pour vous assurer que votre contrôle Microsoft ActiveX sans fenêtre est accessible aux applications clientes de la technologie d’assistance (AT).</span><span class="sxs-lookup"><span data-stu-id="c6fee-105">Describes how to use the Microsoft UI Automation API to ensure that your windowless Microsoft ActiveX control is accessible to assistive technology (AT) client applications.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="c6fee-106">Ce que vous devez savoir</span><span class="sxs-lookup"><span data-stu-id="c6fee-106">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="c6fee-107">Technologies</span><span class="sxs-lookup"><span data-stu-id="c6fee-107">Technologies</span></span>

-   [<span data-ttu-id="c6fee-108">Contrôles ActiveX</span><span class="sxs-lookup"><span data-stu-id="c6fee-108">ActiveX Controls</span></span>](/windows/desktop/com/activex-controls)
-   [<span data-ttu-id="c6fee-109">UI Automation</span><span class="sxs-lookup"><span data-stu-id="c6fee-109">UI Automation</span></span>](entry-uiauto-win32.md)

### <a name="prerequisites"></a><span data-ttu-id="c6fee-110">Prérequis</span><span class="sxs-lookup"><span data-stu-id="c6fee-110">Prerequisites</span></span>

-   <span data-ttu-id="c6fee-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="c6fee-111">C/C++</span></span>
-   <span data-ttu-id="c6fee-112">Programmation Microsoft Win32 et COM (Component Object Model)</span><span class="sxs-lookup"><span data-stu-id="c6fee-112">Microsoft Win32 and Component Object Model (COM) programming</span></span>
-   <span data-ttu-id="c6fee-113">Contrôles ActiveX sans fenêtre</span><span class="sxs-lookup"><span data-stu-id="c6fee-113">Windowless ActiveX Controls</span></span>
-   <span data-ttu-id="c6fee-114">Fournisseurs UI Automation</span><span class="sxs-lookup"><span data-stu-id="c6fee-114">UI Automation providers</span></span>

## <a name="instructions"></a><span data-ttu-id="c6fee-115">Instructions</span><span class="sxs-lookup"><span data-stu-id="c6fee-115">Instructions</span></span>

### <a name="step-1-implement-the-ui-automation-provider-interfaces"></a><span data-ttu-id="c6fee-116">Étape 1 : implémenter les interfaces du fournisseur UI Automation.</span><span class="sxs-lookup"><span data-stu-id="c6fee-116">Step 1: Implement the UI Automation provider interfaces.</span></span>

<span data-ttu-id="c6fee-117">Pour rendre votre application accessible, vous devez implémenter les interfaces du fournisseur UI Automation pour votre contrôle ActiveX sans fenêtre, notamment [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple), [**IRawElementProviderFragment**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragment), [**IRawElementProviderFragmentRoot**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragmentroot)et [**IRawElementProviderAdviseEvents**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovideradviseevents).</span><span class="sxs-lookup"><span data-stu-id="c6fee-117">To make your application accessible, you must implement the UI Automation provider interfaces for your windowless ActiveX control, including [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple), [**IRawElementProviderFragment**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragment), [**IRawElementProviderFragmentRoot**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragmentroot), and [**IRawElementProviderAdviseEvents**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovideradviseevents).</span></span> <span data-ttu-id="c6fee-118">Vous devez implémenter ces interfaces comme vous le feriez pour un contrôle basé sur une fenêtre, sauf comme décrit dans les étapes suivantes.</span><span class="sxs-lookup"><span data-stu-id="c6fee-118">You should implement these interfaces just as you would for a window-based control, except as described in the following steps.</span></span> <span data-ttu-id="c6fee-119">Pour plus d’informations sur l’implémentation des interfaces de fournisseur UIA, consultez le [Guide du programmeur de fournisseur UI Automation](uiauto-providerportal.md).</span><span class="sxs-lookup"><span data-stu-id="c6fee-119">For more information about implementing UIA provider interfaces, see [UI Automation Provider Programmer's Guide](uiauto-providerportal.md).</span></span>

### <a name="step-2-implement-the-iserviceprovider-interface"></a><span data-ttu-id="c6fee-120">Étape 2 : implémenter l’interface IServiceProvider.</span><span class="sxs-lookup"><span data-stu-id="c6fee-120">Step 2: Implement the IServiceProvider interface.</span></span>

<span data-ttu-id="c6fee-121">Lorsqu’un client a besoin d’informations d’accessibilité sur votre contrôle sans fenêtre, le conteneur de contrôle appelle la méthode **IServiceProvider :: QueryService** de votre contrôle pour récupérer le pointeur d’interface [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) pour votre contrôle.</span><span class="sxs-lookup"><span data-stu-id="c6fee-121">When a client needs accessibility information about your windowless control, the control container calls your control's **IServiceProvider::QueryService** method to retrieve the [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) interface pointer for your control.</span></span>

<span data-ttu-id="c6fee-122">L’exemple suivant montre comment implémenter la méthode **QueryService** .</span><span class="sxs-lookup"><span data-stu-id="c6fee-122">The following example shows how to implement the **QueryService** method.</span></span>


```C++
STDMETHODIMP CMyAccessibleUIAControl::QueryService(REFGUID guidService,
        REFIID riid, void **ppvObject)
{  
    if (ppvObject == NULL)
    {
        return E_INVALIDARG;
    }

    *ppvObject = NULL;  
    HRESULT hr = E_FAIL; 
 
    if (guidService == __uuidof(IRawElementProviderSimple))
    {  
        hr = QueryInterface(riid, ppvObject);  
    }  
    return hr;  
}
```



### <a name="step-3-implement-the-irawelementproviderfragmentnavigate-method"></a><span data-ttu-id="c6fee-123">Étape 3 : implémentez la méthode IRawElementProviderFragment :: Navigate.</span><span class="sxs-lookup"><span data-stu-id="c6fee-123">Step 3: Implement the IRawElementProviderFragment::Navigate method.</span></span>

<span data-ttu-id="c6fee-124">Quand la méthode [**IRawElementProviderFragment :: Navigate**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragment-navigate) d’un contrôle sans fenêtre est appelée pour accéder au parent ou à un frère du fournisseur racine du contrôle sans fenêtre, votre méthode **Navigate** doit déléguer à la méthode [**IRawElementProviderWindowlessSite :: GetAdjacentFragment**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderwindowlesssite-getadjacentfragment) du conteneur de contrôle.</span><span class="sxs-lookup"><span data-stu-id="c6fee-124">When your windowless control’s [**IRawElementProviderFragment::Navigate**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragment-navigate) method is called to navigate to the parent or a sibling of the windowless control's root provider, your **Navigate** method should delegate to the [**IRawElementProviderWindowlessSite::GetAdjacentFragment**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderwindowlesssite-getadjacentfragment) method of the control container.</span></span>

<span data-ttu-id="c6fee-125">L’exemple suivant montre comment implémenter la méthode [**Navigate**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragment-navigate) .</span><span class="sxs-lookup"><span data-stu-id="c6fee-125">The following example shows how to implement the [**Navigate**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragment-navigate) method.</span></span>


```C++
STDMETHODIMP CMyAccessibleUIAControl::Navigate(NavigateDirection direction,
     IRawElementProviderFragment **ppRetVal) 
{   
    if (ppRetVal == NULL)
    {
        return E_INVALIDARG;
    }

    *ppRetVal = NULL;  
    HRESULT hr = E_FAIL;
    IRawElementProviderWindowlessSite *pWindowlessSite = NULL;  
    
    if (direction == NavigateDirection_Parent)  
    {  
        // Query the control container's windowless site 
        // for the parent.
         if (SUCCEEDED(m_pClientSite->QueryInterface(
                IID_PPV_ARGS(&pWindowlessSite))))  
        {  
            hr =  pWindowlessSite->GetAdjacentFragment(direction, ppRetVal);  
        }  
    }  

    else if (direction == NavigateDirection_FirstChild)  
    {  
        // GetFragmentForChild is an application-defined function that 
        // retrieves the first or last child fragment.
        hr =  GetFragmentForChild(FIRST, ppRetVal);  
    }  

    else if (direction == NavigateDirection_LastChild)  
    {  
        hr = GetFragmentForChild(LAST, ppRetVal);  
    }  

    SafeRelease(&pWindowlessSite);
    return S_OK;   
}
```



### <a name="step-4-implement-the-irawelementproviderfragmentgetruntimeid-method"></a><span data-ttu-id="c6fee-126">Étape 4 : implémentez la méthode IRawElementProviderFragment :: GetRuntimeId.</span><span class="sxs-lookup"><span data-stu-id="c6fee-126">Step 4: Implement the IRawElementProviderFragment::GetRuntimeId method.</span></span>

<span data-ttu-id="c6fee-127">Lorsque votre contrôle sans fenêtre reçoit un appel à sa méthode [**IRawElementProviderFragment :: GetRuntimeId**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragment-getruntimeid) , le contrôle doit effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="c6fee-127">When your windowless control receives a call to its [**IRawElementProviderFragment::GetRuntimeId**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragment-getruntimeid) method, the control must do the following:</span></span>

1.  <span data-ttu-id="c6fee-128">Récupérez un préfixe d’ID d’exécution en appelant la méthode [**IRawElementProviderWindowlessSite :: GetRuntimeIdPrefix**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderwindowlesssite-getruntimeidprefix) du site de contrôle.</span><span class="sxs-lookup"><span data-stu-id="c6fee-128">Retrieve a runtime ID prefix by calling the control site's [**IRawElementProviderWindowlessSite::GetRuntimeIdPrefix**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderwindowlesssite-getruntimeidprefix) method.</span></span>
2.  <span data-ttu-id="c6fee-129">Créez un ID d’exécution unique pour le contrôle en ajoutant un entier au préfixe d’ID d’exécution.</span><span class="sxs-lookup"><span data-stu-id="c6fee-129">Create a unique runtime ID for the control by appending an integer to the runtime ID prefix.</span></span>
3.  <span data-ttu-id="c6fee-130">Retourne l’ID d’exécution à l’appelant.</span><span class="sxs-lookup"><span data-stu-id="c6fee-130">Return the runtime ID to the caller.</span></span>

<span data-ttu-id="c6fee-131">L’exemple suivant montre comment implémenter la méthode [**GetRuntimeId**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderwindowlesssite-getruntimeidprefix) .</span><span class="sxs-lookup"><span data-stu-id="c6fee-131">The following example shows how to implement the [**GetRuntimeId**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderwindowlesssite-getruntimeidprefix) method.</span></span>


```C++
STDMETHODIMP CMyAccessibleUIAControl::GetRuntimeId(SAFEARRAY **ppRetVal)  
{   
    if (ppRetVal == NULL)
    {
        return E_INVALIDARG;
    }

    *ppRetVal = NULL;  
    HRESULT hr = E_FAIL;
    IRawElementProviderWindowlessSite *pWindowlessSite = NULL;  

    if (SUCCEEDED(m_pClientSite->QueryInterface(IID_PPV_ARGS(&pWindowlessSite))))  
    {  
        // Create a safe array to hold runtime ID.
        SAFEARRAY *psa = SafeArrayCreateVector(VT_I4, 1, 3);  
        if (psa == NULL)
        {
            hr = E_OUTOFMEMORY;
        }

        // Retrieve the runtime ID prefix from the control container. The prefix
        // consists of UiaAppendRuntimeId followed by the windowless site ID.
        if (SUCCEEDED(hr))
        {    
            hr = pWindowlessSite->GetRuntimeIdPrefix(&psa);  
        } 

        if (SUCCEEDED(hr))
        {
        // Append this fragment's ID to the retrieved runtime ID prefix.
            long i = 2;
            hr = SafeArrayPutElement(psa, &i, (void*)&m_Id);        
        }

        if (SUCCEEDED(hr))
        {
            *ppRetVal = psa;  
        }
    }

    SafeRelease(&pWindowlessSite);
    return hr;  
}
```



## <a name="related-topics"></a><span data-ttu-id="c6fee-132">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c6fee-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c6fee-133">Utiliser MSAA pour rendre un contrôle ActiveX sans fenêtre accessible</span><span class="sxs-lookup"><span data-stu-id="c6fee-133">Use MSAA to Make a Windowless ActiveX Control Accessible</span></span>](use-msaa-to-make-an-windowless-activex-control-accessible.md)
</dt> <dt>

[<span data-ttu-id="c6fee-134">Accessibilité des contrôles ActiveX sans fenêtre</span><span class="sxs-lookup"><span data-stu-id="c6fee-134">Windowless ActiveX Control Accessibility</span></span>](windowless-activex-control-accessibility.md)
</dt> </dl>

 

 