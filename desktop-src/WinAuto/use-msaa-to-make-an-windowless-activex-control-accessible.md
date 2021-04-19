---
title: Utiliser MSAA pour rendre un contrôle ActiveX sans fenêtre accessible
description: Décrit comment utiliser le Active Accessibility Microsoft \ 32 ; API permettant de s’assurer que votre contrôle Microsoft ActiveX sans fenêtre est accessible aux applications clientes de la technologie d’assistance (AT).
ms.assetid: 30F874F9-EA45-4365-8798-FEA011C62DA9
keywords:
- Contrôle ActiveX, accessibilité
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a3a76aa72fadef502a6a4319284ab34fdd5214d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106511306"
---
# <a name="use-msaa-to-make-a-windowless-activex-control-accessible"></a><span data-ttu-id="6419e-104">Utiliser MSAA pour rendre un contrôle ActiveX sans fenêtre accessible</span><span class="sxs-lookup"><span data-stu-id="6419e-104">Use MSAA to make a windowless ActiveX control accessible</span></span>

<span data-ttu-id="6419e-105">Décrit comment utiliser l’API Microsoft Active Accessibility pour vous assurer que votre contrôle Microsoft ActiveX sans fenêtre est accessible aux applications clientes de la technologie d’assistance (AT).</span><span class="sxs-lookup"><span data-stu-id="6419e-105">Describes how to use the Microsoft Active Accessibility API to ensure that your windowless Microsoft ActiveX control is accessible to assistive technology (AT) client applications.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="6419e-106">Ce que vous devez savoir</span><span class="sxs-lookup"><span data-stu-id="6419e-106">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="6419e-107">Technologies</span><span class="sxs-lookup"><span data-stu-id="6419e-107">Technologies</span></span>

-   [<span data-ttu-id="6419e-108">Contrôles ActiveX</span><span class="sxs-lookup"><span data-stu-id="6419e-108">ActiveX Controls</span></span>](/windows/desktop/com/activex-controls)
-   [<span data-ttu-id="6419e-109">Microsoft Active Accessibility</span><span class="sxs-lookup"><span data-stu-id="6419e-109">Microsoft Active Accessibility</span></span>](microsoft-active-accessibility.md)

### <a name="prerequisites"></a><span data-ttu-id="6419e-110">Prérequis</span><span class="sxs-lookup"><span data-stu-id="6419e-110">Prerequisites</span></span>

-   <span data-ttu-id="6419e-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="6419e-111">C/C++</span></span>
-   <span data-ttu-id="6419e-112">Programmation Microsoft Win32 et COM (Component Object Model)</span><span class="sxs-lookup"><span data-stu-id="6419e-112">Microsoft Win32 and Component Object Model (COM) programming</span></span>
-   <span data-ttu-id="6419e-113">Contrôles ActiveX sans fenêtre</span><span class="sxs-lookup"><span data-stu-id="6419e-113">Windowless ActiveX Controls</span></span>
-   <span data-ttu-id="6419e-114">Serveurs Microsoft Active Accessibility</span><span class="sxs-lookup"><span data-stu-id="6419e-114">Microsoft Active Accessibility servers</span></span>

## <a name="instructions"></a><span data-ttu-id="6419e-115">Instructions</span><span class="sxs-lookup"><span data-stu-id="6419e-115">Instructions</span></span>

### <a name="step-1-implement-the-iaccessible-interface"></a><span data-ttu-id="6419e-116">Étape 1 : implémenter l’interface IAccessible.</span><span class="sxs-lookup"><span data-stu-id="6419e-116">Step 1: Implement the IAccessible interface.</span></span>

<span data-ttu-id="6419e-117">Pour rendre votre contrôle ActiveX sans fenêtre accessible, vous devez implémenter l’interface Microsoft Active Accessibility [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) , comme vous le feriez pour un contrôle basé sur une fenêtre, sauf comme décrit dans les étapes suivantes.</span><span class="sxs-lookup"><span data-stu-id="6419e-117">To make your windowless ActiveX control accessible, you must implement the Microsoft Active Accessibility [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface, just as you would for a window-based control, except as described in the following steps.</span></span> <span data-ttu-id="6419e-118">Pour plus d’informations sur l’implémentation de **IAccessible**, consultez [Guide du développeur pour les serveurs Active Accessibility](developer-s-guide-for-active-accessibility-servers.md).</span><span class="sxs-lookup"><span data-stu-id="6419e-118">For more information about implementing **IAccessible**, see [Developer's Guide for Active Accessibility Servers](developer-s-guide-for-active-accessibility-servers.md).</span></span>

### <a name="step-2-implement-the-iserviceprovider-interface"></a><span data-ttu-id="6419e-119">Étape 2 : implémenter l’interface IServiceProvider.</span><span class="sxs-lookup"><span data-stu-id="6419e-119">Step 2: Implement the IServiceProvider interface.</span></span>

<span data-ttu-id="6419e-120">Lorsqu’un client demande des informations d’accessibilité sur votre contrôle sans fenêtre, le conteneur appelle la méthode [**IServiceProvider :: QueryService**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678966(v=vs.85)) de votre contrôle pour récupérer le pointeur d’interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) .</span><span class="sxs-lookup"><span data-stu-id="6419e-120">When a client requests accessibility information about your windowless control, the container calls your control's [**IServiceProvider::QueryService**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678966(v=vs.85)) method to retrieve the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface pointer.</span></span>

<span data-ttu-id="6419e-121">Cet exemple montre comment implémenter la méthode [**QueryService**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678966(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="6419e-121">This example shows how to implement the [**QueryService**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678966(v=vs.85)) method.</span></span>


```C++
STDMETHODIMP CMyAccessibleMSAAControl::QueryService(REFGUID guidService, 
        REFIID riid, void **ppvObject)
{      
    if (ppvObject == NULL)
    {
        return E_INVALIDARG;
    }

    *ppvObject = NULL;  
    HRESULT hr = E_FAIL;  

    if (guidService == __uuidof(IAccessible))
    {  
        hr = QueryInterface(riid, ppvObject);  
    }  
    return hr;  
}
```



### <a name="step-3-delegate-iaccessibleget_accparent-method-calls-to-the-control-sites-iaccessiblewindowlesssitegetparentaccessible-method"></a><span data-ttu-id="6419e-122">Étape 3 : déléguez \_ les appels de méthode IAccessible :: accParent à la méthode IAccessibleWindowlessSite :: GetParentAccessible du site de contrôle.</span><span class="sxs-lookup"><span data-stu-id="6419e-122">Step 3: Delegate IAccessible::get\_accParent method calls to the control site's IAccessibleWindowlessSite::GetParentAccessible method.</span></span>

<span data-ttu-id="6419e-123">Lorsqu’un client demande l’objet parent de votre contrôle sans fenêtre, le conteneur appelle la méthode [**IAccessible :: obtenir \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) de votre contrôle.</span><span class="sxs-lookup"><span data-stu-id="6419e-123">When a client requests the parent object of your windowless control, the container calls your control's [**IAccessible::get\_accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) method.</span></span> <span data-ttu-id="6419e-124">Votre implémentation de **\_ accParent** doit déléguer à la méthode [**IAccessibleWindowlessSite :: GetParentAccessible**](/windows/desktop/api/oleacc/nf-oleacc-iaccessiblewindowlesssite-getparentaccessible) du conteneur.</span><span class="sxs-lookup"><span data-stu-id="6419e-124">Your **get\_accParent** implementation should delegate to the [**IAccessibleWindowlessSite::GetParentAccessible**](/windows/desktop/api/oleacc/nf-oleacc-iaccessiblewindowlesssite-getparentaccessible) method of the container.</span></span>

<span data-ttu-id="6419e-125">Cet exemple montre comment implémenter la [**méthode \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) .</span><span class="sxs-lookup"><span data-stu-id="6419e-125">This example shows how to implement the [**get\_accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) method.</span></span>


```C++
HRESULT CMyAccessibleMSAAControl::get_accParent(IDispatch **ppdispParent)  
{  
    if (ppdispParent == NULL)
    {
        return E_INVALIDARG;
    }

    HRESULT hr = S_FALSE;  
    *ppdispParent = NULL;  

    IAccessibleWindowlessSite *pWindowlessSite = NULL;  

    if (SUCCEEDED(m_pClientSite->QueryInterface(IID_PPV_ARGS(&pWindowlessSite))))  
    {  
        IAccessible *pParentAcc = NULL;
        if (SUCCEEDED(pWindowlessSite->GetParentAccessible(&pParentAcc)))
        {
            hr = pParentAcc->QueryInterface(IID_PPV_ARGS(ppdispParent));  
        }
    }  

    SafeRelease(&pWindowlessSite);
    return hr;  
}
```



### <a name="step-4-acquire-a-range-of-object-ids-to-assign-to-the-event-sources-in-your-windowless-control"></a><span data-ttu-id="6419e-126">Étape 4 : acquérir une plage d’ID d’objet à assigner aux sources d’événements dans votre contrôle sans fenêtre.</span><span class="sxs-lookup"><span data-stu-id="6419e-126">Step 4: Acquire a range of object IDs to assign to the event sources in your windowless control.</span></span>

<span data-ttu-id="6419e-127">Comme les contrôles basés sur des fenêtres, un contrôle ActiveX sans fenêtre appelle la fonction [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) pour informer les clients des événements importants.</span><span class="sxs-lookup"><span data-stu-id="6419e-127">Like window-based controls, a windowless ActiveX control calls the [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) function to notify clients of important events.</span></span> <span data-ttu-id="6419e-128">Les paramètres de fonction incluent l’ID d’objet de l’élément qui déclenche l’événement.</span><span class="sxs-lookup"><span data-stu-id="6419e-128">The function parameters include the object ID of the item that is raising the event.</span></span> <span data-ttu-id="6419e-129">Votre contrôle sans fenêtre doit affecter des ID d’objet à l’aide d’une valeur d’une plage acquise en appelant la méthode [**IAccessibleWindowlessSite :: AcquireObjectIdRange**](/windows/desktop/api/oleacc/nf-oleacc-iaccessiblewindowlesssite-acquireobjectidrange) du site de contrôle.</span><span class="sxs-lookup"><span data-stu-id="6419e-129">Your windowless control must assign object IDs by using a value from a range acquired by calling the control site’s [**IAccessibleWindowlessSite::AcquireObjectIdRange**](/windows/desktop/api/oleacc/nf-oleacc-iaccessiblewindowlesssite-acquireobjectidrange) method.</span></span>

<span data-ttu-id="6419e-130">Cet exemple montre comment obtenir une plage de valeurs d’ID d’objet à partir du conteneur de contrôle.</span><span class="sxs-lookup"><span data-stu-id="6419e-130">This example shows how to acquire a range of object ID values from the control container.</span></span>


```C++
IAccessibleWindowlessSite *pWindowlessSite = NULL;

if (SUCCEEDED(m_pClientSite->QueryInterface(
        IID_PPV_ARGS(&pWindowlessSite))))  
{  
    if (FAILED(pWindowlessSite->AcquireObjectIdRange(100, this, 
            &m_idObjectBase)))  
    {  
        m_idObjectBase = -1;  
    } 
}

SafeRelease(&pWindowlessSite);
```



### <a name="step-5-implement-the-iaccessiblehandler-interface"></a><span data-ttu-id="6419e-131">Étape 5 : implémenter l’interface IAccessibleHandler.</span><span class="sxs-lookup"><span data-stu-id="6419e-131">Step 5: Implement the IAccessibleHandler interface.</span></span>

<span data-ttu-id="6419e-132">Lorsqu’un contrôle sans fenêtre appelle la fonction [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) , le contrôle spécifie l’ID d’objet de l’élément d’interface utilisateur qui déclenche l’événement et spécifie le conteneur de contrôle comme fenêtre qui répondra aux messages [**WM \_ GETOBJECT**](wm-getobject.md) pour le compte du contrôle.</span><span class="sxs-lookup"><span data-stu-id="6419e-132">When a windowless control calls the [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) function, the control specifies the object ID of the UI item that is raising the event, and specifies the control container as the window that will respond to [**WM\_GETOBJECT**](wm-getobject.md) messages on behalf of the control.</span></span>

<span data-ttu-id="6419e-133">Si une application cliente répond à l’événement, le conteneur de contrôle reçoit un message [**WM \_ GETOBJECT**](wm-getobject.md) qui comprend l’ID d’objet de l’élément d’interface utilisateur qui a déclenché l’événement.</span><span class="sxs-lookup"><span data-stu-id="6419e-133">If a client application responds to the event, the control container receives a [**WM\_GETOBJECT**](wm-getobject.md) message that includes the object ID of the UI item that raised the event.</span></span> <span data-ttu-id="6419e-134">Le conteneur de contrôle répond en recherchant le contrôle sans fenêtre qui « possède » l’ID de l’objet, puis en appelant la méthode [**IAccessibleHandler :: AccessibleObjectFromID**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessiblehandler-accessibleobjectfromid) de ce contrôle.</span><span class="sxs-lookup"><span data-stu-id="6419e-134">The control container responds by looking up the windowless control that "owns" the object ID, and then calling that control's [**IAccessibleHandler::AccessibleObjectFromID**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessiblehandler-accessibleobjectfromid) method.</span></span> <span data-ttu-id="6419e-135">La méthode **AccessibleObjectFromID** retourne le pointeur d’interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) pour l’élément d’interface utilisateur, et le conteneur de contrôle transfère le pointeur vers l’application cliente.</span><span class="sxs-lookup"><span data-stu-id="6419e-135">The **AccessibleObjectFromID** method returns the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface pointer for the UI item, and the control container forwards the pointer to the client application.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6419e-136">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="6419e-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6419e-137">Utiliser UI Automation pour rendre un contrôle ActiveX sans fenêtre accessible</span><span class="sxs-lookup"><span data-stu-id="6419e-137">Use UI Automation to Make a Windowless ActiveX Control Accessible</span></span>](use-ui-automation-to-make-an-windowless-activex-control-accessible.md)
</dt> <dt>

[<span data-ttu-id="6419e-138">Accessibilité des contrôles ActiveX sans fenêtre</span><span class="sxs-lookup"><span data-stu-id="6419e-138">Windowless ActiveX Control Accessibility</span></span>](windowless-activex-control-accessibility.md)
</dt> </dl>

 

 