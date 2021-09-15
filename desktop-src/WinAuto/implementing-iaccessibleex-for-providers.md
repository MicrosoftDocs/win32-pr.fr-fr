---
title: Implémentation de IAccessibleEx pour les fournisseurs
description: Cette section explique comment ajouter des fonctionnalités de fournisseur Microsoft UI Automation à un serveur Microsoft Active Accessibility en implémentant l’interface IAccessibleEx.
ms.assetid: c03dc552-7919-4a35-8ff2-4cdd822bc0b7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9460ccbd243aef390b7ade0deb41626173c927a0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127518289"
---
# <a name="implementing-iaccessibleex-for-providers"></a>Implémentation de IAccessibleEx pour les fournisseurs

Cette section explique comment ajouter des fonctionnalités de fournisseur Microsoft UI Automation à un serveur Microsoft Active Accessibility en implémentant l’interface [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) .

Avant d’implémenter [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex), tenez compte des exigences suivantes :

-   La hiérarchie des objets accessibles par Microsoft Active Accessibility de référence doit être propre. [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) ne peut pas corriger les problèmes liés aux hiérarchies d’objets accessibles existantes. Tous les problèmes liés à la structure du modèle objet doivent être corrigés dans l’implémentation de Microsoft Active Accessibility avant d’implémenter **IAccessibleEx**.
-   L’implémentation de [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) doit être conforme à la spécification Microsoft Active Accessibility et à la spécification UI Automation. Des outils sont disponibles pour valider la conformité dans les deux spécifications. Pour plus d’informations, consultez [outils de test](testing-tools.md) et vérification d' [UI Automation vérifier (UIA Verify) infrastructure d’automatisation de test](https://www.codeplex.com/UIAutomationVerify/).

L’implémentation de [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) nécessite les étapes principales suivantes :

-   Implémentez **IServiceProvider** sur l’objet accessible afin que l’interface [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) se trouve sur ce ou sur un objet distinct.
-   Implémentez [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) sur l’objet accessible.
-   Créez des objets accessibles pour tous les éléments enfants Microsoft Active Accessibility, qui, dans Microsoft Active Accessibility, sont représentés par l’interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) sur l’objet parent (par exemple, les éléments de liste). Implémentez [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) sur ces objets.
-   Implémentez [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) sur tous les objets accessibles.
-   Implémentez les interfaces de modèle de contrôle appropriées sur les objets accessibles.

### <a name="implementing-the-iserviceprovider-interface"></a>Implémentation de l’interface IServiceProvider

Étant donné que l’implémentation de [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) pour un contrôle peut résider dans un objet séparé, les applications clientes ne peuvent pas compter sur [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) pour obtenir cette interface. Au lieu de cela, les clients sont censés appeler **IServiceProvider :: QueryService**. Dans l’exemple d’implémentation suivant de cette méthode, il est supposé que **IAccessibleEx** n’est pas implémenté sur un objet distinct ; par conséquent, la méthode appelle simplement via **QueryInterface**.


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



### <a name="implementing-the-iaccessibleex-interface"></a>Implémentation de l’interface IAccessibleEx

Dans Microsoft Active Accessibility, un élément d’interface utilisateur est toujours identifié par une interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) et un ID enfant. Une seule instance de **IAccessible** peut représenter plusieurs éléments d’interface utilisateur.

Étant donné que chaque instance de [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) représente un seul élément d’interface utilisateur, chaque paire [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) /ID enfant doit être mappée à une seule instance **IAccessibleEx** . **IAccessibleEx** comprend deux méthodes pour gérer ce mappage :

-   [**GetObjectForChild**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iaccessibleex-getobjectforchild): récupère l’interface [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) pour l’enfant spécifié. Cette méthode retourne la **valeur null** si l’implémentation de **IAccessibleEx** ne reconnaît pas l’ID enfant spécifié, n’a pas de **IAccessibleEx** pour l’enfant spécifié ou représente un élément enfant.
-   [**GetIAccessiblePair**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iaccessibleex-getiaccessiblepair): récupère l’interface [**IACCESSIBLE**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) et l’ID enfant de l’élément [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) . Pour les implémentations **IAccessible** qui n’utilisent pas d’ID enfant, cette méthode récupère l’objet **IAccessible** correspondant et le CHILDID \_ self.

L’exemple suivant illustre l’implémentation des méthodes [**GetObjectForChild**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iaccessibleex-getobjectforchild) et [**GetIAccessiblePair**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iaccessibleex-getiaccessiblepair) pour un élément dans un affichage de liste personnalisé. Les méthodes permettent à UI Automation de mapper la paire d’ID d’enfant et [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) à une instance [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) correspondante.


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



Si une implémentation d’objet accessible n’utilise pas d’ID enfant, les méthodes peuvent toujours être implémentées comme indiqué dans l’extrait de code suivant.


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



### <a name="implement-the-irawelementprovidersimple-interface"></a>Implémenter l’interface IRawElementProviderSimple

Les serveurs utilisent [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) pour exposer des informations sur les propriétés UI Automation et les modèles de contrôle. **IRawElementProviderSimple** comprend les méthodes suivantes :

-   [**GetPatternProvider**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-getpatternprovider): cette méthode est utilisée pour exposer des interfaces de modèle de contrôle. Elle retourne un objet qui prend en charge le modèle de contrôle spécifié, ou **null** si le modèle de contrôle n’est pas pris en charge.
-   [**GetPropertyValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-getpropertyvalue): cette méthode est utilisée pour exposer des valeurs de propriété UI Automation.
-   [**HostRawElementProvider**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-get_hostrawelementprovider): cette méthode n’est pas utilisée avec les implémentations [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) .
-   [**ProviderOptions**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-get_provideroptions): cette méthode n’est pas utilisée avec les implémentations [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) .

Un serveur [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) expose des modèles de contrôle en implémentant [**IRawElementProviderSimple :: GetPatternProvider**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-getpatternprovider). Cette méthode prend un paramètre entier qui spécifie le modèle de contrôle. Le serveur retourne la **valeur null** si le modèle n’est pas pris en charge. Si l’interface de modèle de contrôle est prise en charge, les serveurs retournent un [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) et le client appelle ensuite [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) pour obtenir le modèle de contrôle approprié.

Un serveur [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) peut prendre en charge les propriétés UI Automation (telles que LabeledBy et IsRequiredForForm) en implémentant [**IRawElementProviderSimple :: GetPropertyValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-getpropertyvalue) et en fournissant un PROPERTYID entier qui identifie la propriété en tant que paramètre. Cette technique s’applique uniquement aux propriétés UI Automation qui ne sont pas incluses dans une interface de modèle de contrôle. Les propriétés associées à une interface de modèle de contrôle sont exposées par le biais de la méthode d’interface de modèle de contrôle. Par exemple, la propriété IsSelected du modèle de contrôle [SelectionItem](uiauto-implementingselectionitem.md) est exposée avec [**ISelectionItemProvider :: obtenir \_ IsSelected**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionitemprovider-get_isselected).

 

 