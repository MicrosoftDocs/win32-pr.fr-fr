---
title: Prise en charge des interfaces doubles ou de dispatch
description: À l’instar de l’interface de dispatch, toutes les interfaces doubles doivent hériter de IDispatch, qui délègue toutes ses fonctions IDispatch (GetIDsOfNames, Invoke, GetTypeInfo, GetTypeInfoCount) au IDispatch de l’agrégateur (ADSI).
ms.assetid: abd0fcfc-f45c-4022-af95-60615be0adcc
ms.tgt_platform: multiple
keywords:
- Prise en charge des interfaces doubles ou de dispatch ADSI
- interfaces ADSI, interfaces doubles ou Dispatch des extensions
- ADSI ADSI, exemple de code C/C++, délégation de méthodes IDispatch à l’agrégateur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 435a4552b364afbf909d04a759e3713ce69befab
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "106509677"
---
# <a name="supporting-dual-or-dispatch-interfaces"></a><span data-ttu-id="8fdf0-106">Prise en charge des interfaces doubles ou de dispatch</span><span class="sxs-lookup"><span data-stu-id="8fdf0-106">Supporting Dual or Dispatch Interfaces</span></span>

<span data-ttu-id="8fdf0-107">À l’instar de l’interface de dispatch, toutes les interfaces doubles doivent hériter de [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch), qui délègue toutes ses fonctions **IDispatch** ([**GetIDsOfNames**](/windows/win32/api/oaidl/nf-oaidl-idispatch-getidsofnames), [**Invoke**](/windows/win32/api/oaidl/nf-oaidl-idispatch-invoke), [**GetTypeInfo**](/windows/win32/api/oaidl/nf-oaidl-idispatch-gettypeinfo), [**GetTypeInfoCount**](/windows/win32/api/oaidl/nf-oaidl-idispatch-gettypeinfocount)) au **IDispatch** de l’agrégateur (ADSI).</span><span class="sxs-lookup"><span data-stu-id="8fdf0-107">Like the dispatch interface, all dual interfaces must inherit from [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch), which delegates all of its **IDispatch** functions ([**GetIDsOfNames**](/windows/win32/api/oaidl/nf-oaidl-idispatch-getidsofnames), [**Invoke**](/windows/win32/api/oaidl/nf-oaidl-idispatch-invoke), [**GetTypeInfo**](/windows/win32/api/oaidl/nf-oaidl-idispatch-gettypeinfo), [**GetTypeInfoCount**](/windows/win32/api/oaidl/nf-oaidl-idispatch-gettypeinfocount)) back to the **IDispatch** of the aggregator (ADSI).</span></span> <span data-ttu-id="8fdf0-108">Pour pouvoir déléguer, un objet d’extension doit interroger le **IDispatch** de l’agrégateur, appeler la méthode d’agrégation appropriée et libérer le pointeur après l’utilisation.</span><span class="sxs-lookup"><span data-stu-id="8fdf0-108">In order to delegate, an extension object should query for the **IDispatch** of the aggregator, call the appropriate aggregator method, and release the pointer after use.</span></span>

<span data-ttu-id="8fdf0-109">Si l’extension peut être un composant autonome, vérifiez qu’elle est agrégée.</span><span class="sxs-lookup"><span data-stu-id="8fdf0-109">If the extension can be a standalone component, verify that it is aggregated.</span></span> <span data-ttu-id="8fdf0-110">Dans ce cas, redirigez les fonctions de dispatch vers [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) de l’agrégateur. sinon, vous pouvez appeler votre implémentation interne de **IDispatch**, ou vous pouvez appeler votre implémentation de [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension).</span><span class="sxs-lookup"><span data-stu-id="8fdf0-110">If so, reroute the dispatch functions to the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) of the aggregator, otherwise you can call your internal implementation of **IDispatch**, or you can call your implementation of [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension).</span></span>

<span data-ttu-id="8fdf0-111">L’exemple de code suivant montre comment rediriger l’appel [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) vers le **IDispatch** de l’agrégateur.</span><span class="sxs-lookup"><span data-stu-id="8fdf0-111">The following code example shows how to reroute the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) call to the **IDispatch** of the aggregator.</span></span> <span data-ttu-id="8fdf0-112">Cet exemple de code suppose que la variable membre **m \_ pOuterUnknown** a été initialisée au pointeur **IUnknown** de l’agrégateur.</span><span class="sxs-lookup"><span data-stu-id="8fdf0-112">This code example assumes that the **m\_pOuterUnknown** member variable has been initialized to the **IUnknown** pointer of the aggregator.</span></span>


```C++
/////////////////////////////////////////////////// 
// Delegating IDispatch Methods to the aggregator
///////////////////////////////////////////////////
STDMETHODIMP MyExtension::GetTypeInfoCount(UINT* pctinfo)
{
    IDispatch *pDisp = NULL;
    HRESULT    hr = S_OK;
    hr = m_pOuterUnknown->QueryInterface( IID_IDispatch, (void**) &pDisp );
    if ( SUCCEEDED(hr) )
    {
        hr = pDisp->GetTypeInfoCount( pctinfo );
        pDisp->Release();
    }
    return hr;
}
 
 
STDMETHODIMP MyExtension::GetTypeInfo(UINT itinfo, LCID lcid, ITypeInfo** pptinfo)
{
    IDispatch *pDisp = NULL;
    HRESULT    hr = S_OK;
    hr = m_pOuterUnknown->QueryInterface( IID_IDispatch, (void**) &pDisp );
    if ( SUCCEEDED(hr) )
    {
        hr = pDisp->GetTypeInfo( itinfo, lcid, pptinfo );
        pDisp->Release();
    }
    
    return hr;
}
 
STDMETHODIMP MyExtension::GetIDsOfNames(REFIID riid, LPOLESTR* rgszNames, UINT cNames, LCID lcid, DISPID* rgdispid)
{
    IDispatch *pDisp = NULL;
    HRESULT    hr = S_OK;
    hr = m_pOuterUnknown->QueryInterface( IID_IDispatch, (void**) &pDisp );
    if ( SUCCEEDED(hr) )
    {
        hr = pDisp->GetIDsOfNames( riid, rgszNames, cNames, lcid, 
                 rgdispid);
        pDisp->Release();
    }
    
    return hr;
 
}
 
STDMETHODIMP MyExtension::Invoke(DISPID dispidMember, REFIID riid,
        LCID lcid, WORD wFlags, DISPPARAMS* pdispparams, VARIANT* 
                pvarResult, EXCEPINFO* pexcepinfo, UINT* puArgErr)
{
    IDispatch *pDisp = NULL;
    HRESULT    hr = S_OK;
    hr = m_pOuterUnknown->QueryInterface( IID_IDispatch, (void**) &pDisp );
    if ( SUCCEEDED(hr) )
    {
        hr = pDisp->Invoke( dispidMember, riid, lcid, wFlags, 
                 pdispparams, pvarResult, pexcepinfo, puArgErr);
        pDisp->Release();
    }
    
    return hr;
}
```



<span data-ttu-id="8fdf0-113">Les Writers d’extensions sont vivement encouragés à prendre en charge les interfaces doubles au lieu des interfaces de dispatch dans leurs objets d’extension.</span><span class="sxs-lookup"><span data-stu-id="8fdf0-113">Extension writers are strongly encouraged to support dual interfaces instead of dispatch interfaces in their extension objects.</span></span> <span data-ttu-id="8fdf0-114">Une interface double permet à un client d’avoir un accès plus rapide, tant que l’accès à vtable est activé dans le client.</span><span class="sxs-lookup"><span data-stu-id="8fdf0-114">A dual interface enables a client to have faster access, as long as vtable access is enabled in the client.</span></span> <span data-ttu-id="8fdf0-115">Pour plus d’informations, consultez [liaison tardive et accès vtable dans le modèle d’extension ADSI](late-binding-vs--vtable-access-in-the-adsi-extension-model.md).</span><span class="sxs-lookup"><span data-stu-id="8fdf0-115">For more information, see [Late Binding vs. Vtable Access in the ADSI Extension Model](late-binding-vs--vtable-access-in-the-adsi-extension-model.md).</span></span> <span data-ttu-id="8fdf0-116">En fonction du modèle actuel, l’implémentation d’interfaces doubles ne doit pas être plus difficile que l’implémentation d’interfaces de dispatch.</span><span class="sxs-lookup"><span data-stu-id="8fdf0-116">Based on the current model, implementing dual interfaces should not be more difficult than implementing dispatch interfaces.</span></span>

 

 