---
title: héberger un contrôle de ActiveX sans fenêtre UI Automation
description: découvrez comment créer un conteneur de contrôle qui peut héberger des contrôles microsoft ActiveX sans fenêtre qui implémentent l’automatisation de l’interface utilisateur de microsoft.
ms.assetid: A0F82968-F434-4F5E-8052-CF7CE65DB120
keywords:
- UI Automation, contrôle de ActiveX sans fenêtre
- contrôle de ActiveX sans fenêtre, UI Automation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77026d923ea6f0d2536cbd6a94966ec858443258
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127519381"
---
# <a name="host-a-ui-automation-windowless-activex-control"></a>héberger un contrôle de ActiveX sans fenêtre UI Automation

découvrez comment créer un conteneur de contrôle qui peut héberger des contrôles microsoft ActiveX sans fenêtre qui implémentent l’automatisation de l’interface utilisateur de microsoft. En suivant les étapes décrites ici, vous pouvez vous assurer que les contrôles sans fenêtre UI Automation qui sont hébergés dans votre conteneur de contrôle sont accessibles aux applications clientes de technologie d’assistance (AT).

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

### <a name="step-1-provide-the-irawelementprovidersimple-interface-on-behalf-of-the-windowless-control"></a>Étape 1 : fournissez l’interface IRawElementProviderSimple pour le compte du contrôle sans fenêtre.

Chaque fois que le système a besoin du pointeur [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) pour la racine d’un contrôle sans fenêtre, le système interroge le conteneur de contrôle. Pour récupérer le pointeur, le conteneur appelle l’implémentation du contrôle sans fenêtre de la méthode [**IServiceProvider :: QueryService**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678966(v=vs.85)) .

Si le conteneur de contrôle a une implémentation UI Automation, il peut retourner le pointeur [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) du contrôle sans fenêtre au système.

Si le conteneur de contrôle a une implémentation Microsoft Active Accessibility, appelez la fonction [**UiaIAccessibleFromProvider**](/windows/desktop/api/uiautomationcoreapi/nf-uiautomationcoreapi-uiaiaccessiblefromprovider) pour obtenir un pointeur d’interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) qui représente le contrôle, puis retournez le pointeur d’interface **IAccessible** au système.

### <a name="step-2-implement-the-irawelementproviderwindowlesssite-interface"></a>Étape 2 : implémenter l’interface IRawElementProviderWindowlessSite.

Un conteneur de contrôle implémente l’interface [**IRawElementProviderWindowlessSite**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-irawelementproviderwindowlesssite) active un contrôle sans fenêtre basé sur UI Automation pour communiquer ses informations d’accessibilité.

1.  Implémentez [**IRawElementProviderWindowlessSite :: GetRuntimeIdPrefix**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderwindowlesssite-getruntimeidprefix).

    Un fragment de contrôle sans fenêtre doit créer un ID d’exécution unique pour lui-même. Pour créer son ID d’exécution, un fragment de contrôle sans fenêtre récupère une valeur de préfixe en appelant la méthode [**GetRuntimeIdPrefix**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderwindowlesssite-getruntimeidprefix) du site de contrôle, puis ajoute au préfixe une valeur entière qui est unique par rapport à tous les autres fragments dans le contrôle sans fenêtre.

    Le site de contrôle d’un contrôle sans fenêtre doit implémenter la méthode [**GetRuntimeIdPrefix**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderwindowlesssite-getruntimeidprefix) en formant un **SAFEARRAY** qui contient la constante **UiaAppendRuntimeId**, suivie d’une valeur entière qui est unique pour le site.

    Cet exemple montre comment retourner un préfixe d’ID d’exécution pour un contrôle sans fenêtre.

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

    

2.  Implémentez la méthode [**IRawElementProviderWindowlessSite :: GetAdjacentFragment**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderwindowlesssite-getadjacentfragment) .

    Un contrôle qui implémente UI Automation doit retourner un pointeur vers le fournisseur de fragments parent du contrôle.

    Pour retourner le parent du fragment, un objet qui implémente l’interface [**IRawElementProviderFragment**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragment) doit être en mesure d’implémenter la méthode [**Navigate**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragment-navigate) . L’implémentation de **Navigate** est difficile pour un contrôle sans fenêtre, car le contrôle peut ne pas être en mesure de déterminer son emplacement dans l’arborescence accessible de l’objet parent. La méthode [**IRawElementProviderWindowlessSite :: GetAdjacentFragment**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderwindowlesssite-getadjacentfragment) permet au contrôle sans fenêtre d’interroger son site pour le fragment adjacent, puis de retourner ce fragment au client qui a appelé **Navigate**.

    Cet exemple montre comment un conteneur de contrôles récupère le fragment parent d’un contrôle sans fenêtre.

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

    

### <a name="step-3-optional-implement-the-irawelementproviderhostingaccessibles-interface"></a>Étape 3 : facultatif : implémentez l’interface IRawElementProviderHostingAccessibles.

implémentez l’interface [**IRawElementProviderHostingAccessibles**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-irawelementproviderhostingaccessibles) si votre conteneur de contrôle a une implémentation de fournisseur UI Automation qui est la racine d’une arborescence d’accessibilité qui inclut des contrôles de ActiveX sans fenêtre qui prennent en charge Microsoft Active Accessibility. l’interface **IRawElementProviderHostingAccessibles** possède une méthode unique, [**GetEmbeddedAccessibles**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderhostingaccessibles-getembeddedaccessibles), qui récupère les pointeurs d’interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) de tous les contrôles de ActiveX sans fenêtre basés sur Microsoft Active Accessibility qui sont hébergés par votre conteneur de contrôle.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[comment héberger un contrôle de ActiveX sans fenêtre MSAA](host-an-msaa-windowless-activex-control.md)
</dt> <dt>

[accessibilité des contrôles ActiveX sans fenêtre](windowless-activex-control-accessibility.md)
</dt> </dl>

 

 