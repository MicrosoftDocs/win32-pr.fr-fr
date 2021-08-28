---
title: utiliser MSAA pour rendre un contrôle de ActiveX sans fenêtre accessible
description: Décrit comment utiliser le Active Accessibility Microsoft \ 32 ; API permettant de s’assurer que le contrôle Microsoft ActiveX sans fenêtre est accessible aux applications clientes de la technologie d’assistance (AT).
ms.assetid: 30F874F9-EA45-4365-8798-FEA011C62DA9
keywords:
- ActiveX Contrôle, accessibilité
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bac5c4d2a27e5f069f2242999438eebe85e2ea7df1a6bc94890aec142db246c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120098109"
---
# <a name="use-msaa-to-make-a-windowless-activex-control-accessible"></a>utiliser MSAA pour rendre un contrôle de ActiveX sans fenêtre accessible

décrit comment utiliser l’API microsoft Active Accessibility pour garantir que le contrôle microsoft ActiveX sans fenêtre est accessible aux applications clientes de la technologie d’assistance (AT).

## <a name="what-you-need-to-know"></a>Bon à savoir

### <a name="technologies"></a>Technologies

-   [ActiveX Commandes](/windows/desktop/com/activex-controls)
-   [Microsoft Active Accessibility](microsoft-active-accessibility.md)

### <a name="prerequisites"></a>Prérequis

-   C/C++
-   Programmation Microsoft Win32 et COM (Component Object Model)
-   contrôles ActiveX sans fenêtre
-   Serveurs Microsoft Active Accessibility

## <a name="instructions"></a>Instructions

### <a name="step-1-implement-the-iaccessible-interface"></a>Étape 1 : implémenter l’interface IAccessible.

pour rendre votre contrôle de ActiveX sans fenêtre accessible, vous devez implémenter l’interface Microsoft Active Accessibility [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) , comme vous le feriez pour un contrôle basé sur une fenêtre, sauf comme décrit dans les étapes suivantes. Pour plus d’informations sur l’implémentation de **IAccessible**, consultez [Guide du développeur pour les serveurs Active Accessibility](developer-s-guide-for-active-accessibility-servers.md).

### <a name="step-2-implement-the-iserviceprovider-interface"></a>Étape 2 : implémenter l’interface IServiceProvider.

Lorsqu’un client demande des informations d’accessibilité sur votre contrôle sans fenêtre, le conteneur appelle la méthode [**IServiceProvider :: QueryService**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678966(v=vs.85)) de votre contrôle pour récupérer le pointeur d’interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) .

Cet exemple montre comment implémenter la méthode [**QueryService**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678966(v=vs.85)) .


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



### <a name="step-3-delegate-iaccessibleget_accparent-method-calls-to-the-control-sites-iaccessiblewindowlesssitegetparentaccessible-method"></a>Étape 3 : déléguez \_ les appels de méthode IAccessible :: accParent à la méthode IAccessibleWindowlessSite :: GetParentAccessible du site de contrôle.

Lorsqu’un client demande l’objet parent de votre contrôle sans fenêtre, le conteneur appelle la méthode [**IAccessible :: obtenir \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) de votre contrôle. Votre implémentation de **\_ accParent** doit déléguer à la méthode [**IAccessibleWindowlessSite :: GetParentAccessible**](/windows/desktop/api/oleacc/nf-oleacc-iaccessiblewindowlesssite-getparentaccessible) du conteneur.

Cet exemple montre comment implémenter la [**méthode \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) .


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



### <a name="step-4-acquire-a-range-of-object-ids-to-assign-to-the-event-sources-in-your-windowless-control"></a>Étape 4 : acquérir une plage d’ID d’objet à assigner aux sources d’événements dans votre contrôle sans fenêtre.

comme les contrôles basés sur une fenêtre, un contrôle de ActiveX sans fenêtre appelle la fonction [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) pour informer les clients des événements importants. Les paramètres de fonction incluent l’ID d’objet de l’élément qui déclenche l’événement. Votre contrôle sans fenêtre doit affecter des ID d’objet à l’aide d’une valeur d’une plage acquise en appelant la méthode [**IAccessibleWindowlessSite :: AcquireObjectIdRange**](/windows/desktop/api/oleacc/nf-oleacc-iaccessiblewindowlesssite-acquireobjectidrange) du site de contrôle.

Cet exemple montre comment obtenir une plage de valeurs d’ID d’objet à partir du conteneur de contrôle.


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



### <a name="step-5-implement-the-iaccessiblehandler-interface"></a>Étape 5 : implémenter l’interface IAccessibleHandler.

Lorsqu’un contrôle sans fenêtre appelle la fonction [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) , le contrôle spécifie l’ID d’objet de l’élément d’interface utilisateur qui déclenche l’événement et spécifie le conteneur de contrôle comme fenêtre qui répondra aux messages [**WM \_ GETOBJECT**](wm-getobject.md) pour le compte du contrôle.

Si une application cliente répond à l’événement, le conteneur de contrôle reçoit un message [**WM \_ GETOBJECT**](wm-getobject.md) qui comprend l’ID d’objet de l’élément d’interface utilisateur qui a déclenché l’événement. Le conteneur de contrôle répond en recherchant le contrôle sans fenêtre qui « possède » l’ID de l’objet, puis en appelant la méthode [**IAccessibleHandler :: AccessibleObjectFromID**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessiblehandler-accessibleobjectfromid) de ce contrôle. La méthode **AccessibleObjectFromID** retourne le pointeur d’interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) pour l’élément d’interface utilisateur, et le conteneur de contrôle transfère le pointeur vers l’application cliente.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[utiliser UI Automation pour rendre un contrôle de ActiveX sans fenêtre Accessible](use-ui-automation-to-make-an-windowless-activex-control-accessible.md)
</dt> <dt>

[accessibilité des contrôles ActiveX sans fenêtre](windowless-activex-control-accessibility.md)
</dt> </dl>

 

 