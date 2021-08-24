---
title: comment utiliser UI Automation pour rendre un contrôle de ActiveX sans fenêtre Accessible
description: Décrit comment utiliser l’automatisation de l’interface utilisateur de Microsoft \ 32 ; API permettant de s’assurer que le contrôle Microsoft ActiveX sans fenêtre est accessible aux applications clientes de la technologie d’assistance (AT).
ms.assetid: D584E90D-6537-4F48-8553-0DCA061FAF2A
keywords:
- contrôle de ActiveX sans fenêtre, accessibilité
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68ef56d5f3a06bbfa21502c791163f2251506a10fda7da9d07ee04941ad39de1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119570359"
---
# <a name="how-to-use-ui-automation-to-make-a-windowless-activex-control-accessible"></a>comment utiliser UI Automation pour rendre un contrôle de ActiveX sans fenêtre Accessible

décrit comment utiliser l’API d’automatisation d’interface utilisateur de microsoft pour vous assurer que le contrôle microsoft ActiveX sans fenêtre est accessible aux applications clientes de la technologie d’assistance (AT).

## <a name="what-you-need-to-know"></a>Bon à savoir

### <a name="technologies"></a>Technologies

-   [ActiveX Commandes](/windows/desktop/com/activex-controls)
-   [UI Automation](entry-uiauto-win32.md)

### <a name="prerequisites"></a>Prérequis

-   C/C++
-   Programmation Microsoft Win32 et COM (Component Object Model)
-   contrôles ActiveX sans fenêtre
-   Fournisseurs UI Automation

## <a name="instructions"></a>Instructions

### <a name="step-1-implement-the-ui-automation-provider-interfaces"></a>Étape 1 : implémenter les interfaces du fournisseur UI Automation.

pour rendre votre application accessible, vous devez implémenter les interfaces du fournisseur UI Automation pour le contrôle ActiveX sans fenêtre, notamment [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple), [**IRawElementProviderFragment**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragment), [**IRawElementProviderFragmentRoot**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragmentroot)et [**IRawElementProviderAdviseEvents**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovideradviseevents). Vous devez implémenter ces interfaces comme vous le feriez pour un contrôle basé sur une fenêtre, sauf comme décrit dans les étapes suivantes. Pour plus d’informations sur l’implémentation des interfaces de fournisseur UIA, consultez le [Guide du programmeur de fournisseur UI Automation](uiauto-providerportal.md).

### <a name="step-2-implement-the-iserviceprovider-interface"></a>Étape 2 : implémenter l’interface IServiceProvider.

Lorsqu’un client a besoin d’informations d’accessibilité sur votre contrôle sans fenêtre, le conteneur de contrôle appelle la méthode **IServiceProvider :: QueryService** de votre contrôle pour récupérer le pointeur d’interface [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) pour votre contrôle.

L’exemple suivant montre comment implémenter la méthode **QueryService** .


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



### <a name="step-3-implement-the-irawelementproviderfragmentnavigate-method"></a>Étape 3 : implémentez la méthode IRawElementProviderFragment :: Navigate.

Quand la méthode [**IRawElementProviderFragment :: Navigate**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragment-navigate) d’un contrôle sans fenêtre est appelée pour accéder au parent ou à un frère du fournisseur racine du contrôle sans fenêtre, votre méthode **Navigate** doit déléguer à la méthode [**IRawElementProviderWindowlessSite :: GetAdjacentFragment**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderwindowlesssite-getadjacentfragment) du conteneur de contrôle.

L’exemple suivant montre comment implémenter la méthode [**Navigate**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragment-navigate) .


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



### <a name="step-4-implement-the-irawelementproviderfragmentgetruntimeid-method"></a>Étape 4 : implémentez la méthode IRawElementProviderFragment :: GetRuntimeId.

Lorsque votre contrôle sans fenêtre reçoit un appel à sa méthode [**IRawElementProviderFragment :: GetRuntimeId**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragment-getruntimeid) , le contrôle doit effectuer les opérations suivantes :

1.  Récupérez un préfixe d’ID d’exécution en appelant la méthode [**IRawElementProviderWindowlessSite :: GetRuntimeIdPrefix**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderwindowlesssite-getruntimeidprefix) du site de contrôle.
2.  Créez un ID d’exécution unique pour le contrôle en ajoutant un entier au préfixe d’ID d’exécution.
3.  Retourne l’ID d’exécution à l’appelant.

L’exemple suivant montre comment implémenter la méthode [**GetRuntimeId**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderwindowlesssite-getruntimeidprefix) .


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



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[utiliser MSAA pour rendre un contrôle de ActiveX sans fenêtre Accessible](use-msaa-to-make-an-windowless-activex-control-accessible.md)
</dt> <dt>

[accessibilité des contrôles ActiveX sans fenêtre](windowless-activex-control-accessibility.md)
</dt> </dl>

 

 