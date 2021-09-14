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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127122057"
---
# <a name="supporting-dual-or-dispatch-interfaces"></a>Prise en charge des interfaces doubles ou de dispatch

À l’instar de l’interface de dispatch, toutes les interfaces doubles doivent hériter de [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch), qui délègue toutes ses fonctions **IDispatch** ([**GetIDsOfNames**](/windows/win32/api/oaidl/nf-oaidl-idispatch-getidsofnames), [**Invoke**](/windows/win32/api/oaidl/nf-oaidl-idispatch-invoke), [**GetTypeInfo**](/windows/win32/api/oaidl/nf-oaidl-idispatch-gettypeinfo), [**GetTypeInfoCount**](/windows/win32/api/oaidl/nf-oaidl-idispatch-gettypeinfocount)) au **IDispatch** de l’agrégateur (ADSI). Pour pouvoir déléguer, un objet d’extension doit interroger le **IDispatch** de l’agrégateur, appeler la méthode d’agrégation appropriée et libérer le pointeur après l’utilisation.

Si l’extension peut être un composant autonome, vérifiez qu’elle est agrégée. Dans ce cas, redirigez les fonctions de dispatch vers [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) de l’agrégateur. sinon, vous pouvez appeler votre implémentation interne de **IDispatch**, ou vous pouvez appeler votre implémentation de [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension).

L’exemple de code suivant montre comment rediriger l’appel [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) vers le **IDispatch** de l’agrégateur. Cet exemple de code suppose que la variable membre **m \_ pOuterUnknown** a été initialisée au pointeur **IUnknown** de l’agrégateur.


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



Les Writers d’extensions sont vivement encouragés à prendre en charge les interfaces doubles au lieu des interfaces de dispatch dans leurs objets d’extension. Une interface double permet à un client d’avoir un accès plus rapide, tant que l’accès à vtable est activé dans le client. Pour plus d’informations, consultez [liaison tardive et accès vtable dans le modèle d’extension ADSI](late-binding-vs--vtable-access-in-the-adsi-extension-model.md). En fonction du modèle actuel, l’implémentation d’interfaces doubles ne doit pas être plus difficile que l’implémentation d’interfaces de dispatch.

 

 