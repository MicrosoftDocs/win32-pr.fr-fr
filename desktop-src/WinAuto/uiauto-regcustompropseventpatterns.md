---
title: Inscrire des propriétés personnalisées, des événements et des modèles de contrôle
description: Avant qu’une propriété, un événement ou un modèle de contrôle personnalisé puisse être utilisé, le fournisseur et le client doivent inscrire la propriété, l’événement ou le modèle de contrôle au moment de l’exécution.
ms.assetid: ae36e404-8432-46ed-930e-b86dd5a88d6d
keywords:
- UI Automation, propriétés personnalisées
- UI Automation, vue d’ensemble des événements
- UI Automation, vue d’ensemble des modèles de contrôle
- UI Automation, inscrire des propriétés personnalisées
- UI Automation, inscrire des événements
- UI Automation, inscrire des modèles de contrôle
- Propriétés personnalisées, inscrire
- événements, inscription
- modèles de contrôle, inscrire
- inscription, propriétés personnalisées
- inscription, événements
- inscription, modèles de contrôle
- modèles de contrôle, personnalisés
- modèles de contrôle, implémenter un personnalisé
- implémentation de modèles de contrôle personnalisés
- modèles de contrôle personnalisés
- wrappers client
- gestionnaires de modèles
- implémentation de gestionnaires de modèles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b6b157e8f08a2c0be74af6b9f53d3578d1e4d03
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031680"
---
# <a name="register-custom-properties-events-and-control-patterns"></a>Inscrire des propriétés personnalisées, des événements et des modèles de contrôle

Avant qu’une propriété, un événement ou un modèle de contrôle personnalisé puisse être utilisé, le fournisseur et le client doivent inscrire la propriété, l’événement ou le modèle de contrôle au moment de l’exécution. L’inscription est effective de manière globale au sein d’un processus d’application et reste effective jusqu’à ce que le processus se ferme ou que le dernier objet d’élément d’automatisation de l’interface utilisateur de Microsoft ([**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) ou [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple)) soit publié au sein du processus.

Le registre implique de passer un GUID à UI Automation, ainsi que des informations détaillées sur la propriété personnalisée, l’événement ou le modèle de contrôle. La tentative d’enregistrement du même GUID une deuxième fois avec les mêmes informations réussira, mais la tentative d’enregistrement d’un même GUID une deuxième fois, mais avec des informations différentes (par exemple, une propriété personnalisée d’un type différent) échouera. À l’avenir, si la spécification personnalisée est acceptée et intégrée dans le noyau UI Automation, l’automatisation d’interface utilisateur validera les informations d’inscription personnalisées et utilisera le code déjà inscrit au lieu de l’implémentation du Framework « officiel », réduisant ainsi les problèmes de compatibilité des applications. Vous ne pouvez pas supprimer des propriétés, des événements ou des modèles de contrôle déjà inscrits.

Cette rubrique contient les sections suivantes :

-   [Enregistrement des propriétés et des événements personnalisés](#registering-custom-properties-and-events)
-   [Implémentation de modèles de contrôle personnalisés](#implementing-custom-control-patterns)
    -   [Le wrapper client et le gestionnaire de modèle](#the-client-wrapper-and-the-pattern-handler)
    -   [Implémentation du wrapper client](#implementing-the-client-wrapper)
    -   [Implémentation du gestionnaire de modèles](#implementing-the-pattern-handler)
    -   [Inscription d’un modèle de contrôle personnalisé](#registering-a-custom-control-pattern)
    -   [Exemple d’implémentation d’un modèle de contrôle personnalisé](#example-implementation-of-a-custom-control-pattern)
-   [Rubriques connexes](#related-topics)

## <a name="registering-custom-properties-and-events"></a>Enregistrement des propriétés et des événements personnalisés

L’inscription d’une propriété ou d’un événement personnalisé permet au fournisseur et au client d’obtenir un ID pour la propriété ou l’événement, qui peut ensuite être passé à différentes méthodes d’API qui prennent des ID en tant que paramètres.

Pour enregistrer une propriété ou un événement :

1.  Définissez un GUID pour la propriété ou l’événement personnalisé.
2.  Remplissez un [**UIAutomationPropertyInfo**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationpropertyinfo) ou une structure [**UIAutomationEventInfo**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationeventinfo) avec des informations sur la propriété ou l’événement, y compris le GUID et une chaîne non localisable contenant le nom de la propriété ou de l’événement personnalisé. Les propriétés personnalisées nécessitent également que le type de données de la propriété soit spécifié, par exemple, si la propriété contient un entier ou une chaîne. Le type de données doit être l’un des types suivants spécifiés par l’énumération [**UIAutomationType**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-uiautomationtype) . Aucun autre type de données n’est pris en charge pour les propriétés personnalisées.
    -   **UIAutomationType \_ bool**
    -   **UIAutomationType \_ double**
    -   **\_Élément UIAutomationType**
    -   **UIAutomationType \_ int**
    -   **\_Point UIAutomationType**
    -   **\_Chaîne UIAutomationType**
3.  Utilisez la fonction [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) pour créer une instance de l’objet [**CUIAutomationRegistrar**](/previous-versions/windows/desktop/legacy/ff384837(v=vs.85)) et récupérer un pointeur vers l’interface [**IUIAutomationRegistrar**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationregistrar) de l’objet.
4.  Appelez la méthode [**IUIAutomationRegistrar :: RegisterProperty**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerproperty) ou [**RegisterEvent**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerevent) et transmettez l’adresse de la structure [**UIAutomationPropertyInfo**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationpropertyinfo) ou de la structure [**UIAutomationEventInfo**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationeventinfo) .

La méthode [**IUIAutomationRegistrar :: RegisterProperty**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerproperty) ou [**REGISTEREVENT**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerevent) retourne un ID de propriété ou un ID d’événement qu’une application peut passer à toute méthode UI Automation qui accepte ce type d’identificateur comme paramètre. Par exemple, vous pouvez passer un ID de propriété inscrite à la méthode [**IUIAutomationElement :: GetCurrentPropertyValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalue) ou à la méthode [**IUIAutomation :: CreatePropertyCondition**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-createpropertycondition) .

L’exemple suivant montre comment inscrire une propriété personnalisée.


```C++
// Declare a variable for holding the custom property ID.
PATTERNID g_MyCustomPropertyID;
// Define a GUID for the custom property.
GUID GUID_MyCustomProperty = { 0x82f383ff, 0x4b4d, 0x40d3, 
    { 0x8e, 0xd2, 0x90, 0xb5, 0x25, 0x8e, 0xaa, 0x19 } };

HRESULT RegisterProperty()
{
    // Fill the structure with the GUID, name, and data type.
    UIAutomationPropertyInfo MyCustomPropertyInfo = 
    {
        GUID_MyCustomProperty,
        L"MyCustomProp",
        UIAutomationType_String
    };

    // Create the registrar object and get the IUIAutomationRegistrar 
    // interface pointer. 
    IUIAutomationRegistrar * pUIARegistrar = NULL;
    CoCreateInstance(CLSID_CUIAutomationRegistrar, NULL, CLSCTX_INPROC_SERVER, 
            IID_IUIAutomationRegistrar, (void **)&pUIARegistrar);

    if (pUIARegistrar == NULL)
        return E_NOINTERFACE;

    // Register the property and retrieve the property ID. 
    HRESULT hr = pUIARegistrar->RegisterProperty(&MyCustomPropertyInfo, &g_MyCustomPropertyID);
    pUIARegistrar->Release();

    return hr;
}
```



Les identificateurs de propriété et d’événement récupérés par les méthodes [**IUIAutomationRegistrar :: RegisterProperty**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerproperty) et [**RegisterEvent**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerevent) sont valides uniquement dans le contexte de l’application qui les récupère et uniquement pendant la durée de vie de l’application. Les méthodes d’inscription peuvent retourner des valeurs entières différentes pour le même GUID lorsqu’elles sont appelées sur différentes instances de Runtime de la même application.

Il n’existe aucune méthode qui annule l’inscription d’une propriété ou d’un événement personnalisé. Au lieu de cela, ils sont désinscrits implicitement lorsque le dernier objet UI Automation est libéré.

> [!IMPORTANT]
> Si votre code est un client Microsoft Active Accessibility (MSAA), vous devez appeler la fonction [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) lorsque vous modifiez la valeur d’une propriété personnalisée.

 

## <a name="implementing-custom-control-patterns"></a>Implémentation de modèles de contrôle personnalisés

Un modèle de contrôle personnalisé n’est pas inclus dans l’API UI Automation, mais est fourni par un tiers au moment de l’exécution. Les développeurs d’applications clientes et de fournisseurs doivent travailler ensemble pour définir un modèle de contrôle personnalisé, y compris les méthodes, propriétés et événements que le modèle de contrôle prendra en charge. Après avoir défini le modèle de contrôle, le client et le fournisseur doivent implémenter des objets COM (Component Object Model) de prise en charge, ainsi que du code pour inscrire le modèle de contrôle au moment de l’exécution. Un modèle de contrôle personnalisé requiert l’implémentation de deux objets COM : un wrapper client et un gestionnaire de modèle.

> [!Note]  
> Les exemples des rubriques suivantes illustrent comment implémenter un modèle de contrôle personnalisé qui duplique les fonctionnalités du modèle de contrôle [value](uiauto-implementingvalue.md) existant. Ces exemples sont fournis à des fins pédagogiques uniquement. Un modèle de contrôle personnalisé réel doit fournir des fonctionnalités qui ne sont pas disponibles à partir des modèles de contrôle UI Automation Standard.

 

### <a name="the-client-wrapper-and-the-pattern-handler"></a>Le wrapper client et le gestionnaire de modèle

Le wrapper client implémente l’API qui est utilisée par le client pour récupérer des propriétés et appeler des méthodes exposées par le modèle de contrôle personnalisé. L’API est implémentée en tant qu’interface COM qui passe toutes les demandes de propriété et les appels de méthode au noyau UI Automation, qui marshale ensuite les demandes et les appels au fournisseur.

Le code qui inscrit un modèle de contrôle personnalisé doit fournir une fabrique de classe qu’UI Automation peut utiliser pour créer des instances de l’objet de wrapper client. Lorsqu’un modèle de contrôle personnalisé est correctement inscrit, UI Automation retourne un pointeur d’interface [**IUIAutomationPatternInstance**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationpatterninstance) utilisé par le client pour transférer les demandes de propriétés et les appels de méthodes au noyau UI Automation.

Côté fournisseur, le noyau UI Automation prend les demandes de propriété et les appels de méthode du client et les transmet à l’objet de gestionnaire de modèles. Le gestionnaire de modèle appelle ensuite les méthodes appropriées sur l’interface du fournisseur pour le modèle de contrôle personnalisé.

Le code qui inscrit un modèle de contrôle personnalisé crée l’objet de gestionnaire de modèles et, lors de l’inscription du modèle de contrôle, fournit l’Automation d’interface utilisateur avec un pointeur vers l’interface [**IUIAutomationPatternHandler**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationpatternhandler) de l’objet.

Le diagramme suivant montre comment un appel de requête ou de méthode de propriété de client passe du wrapper client, via les composants de base d’UI Automation au gestionnaire de modèles, puis à l’interface du fournisseur.

![Diagramme montrant le passage du wrapper client au gestionnaire de modèles et au fournisseur](images/custompatternsupport.jpg)

Les objets qui implémentent les interfaces de wrapper client et de gestionnaire de modèles doivent être à thread libre. En outre, le noyau UI Automation doit être en mesure d’appeler directement les objets sans aucun code de marshaling intermédiaire.

### <a name="implementing-the-client-wrapper"></a>Implémentation du wrapper client

Le wrapper client est un objet qui expose une interface IXxxPattern que le client utilise pour demander des propriétés et appeler des méthodes prises en charge par le modèle de contrôle personnalisé. L’interface se compose d’une paire de méthodes « getter » pour chaque propriété prise en charge (get \_ CurrentXxx et \_ méthode Get CachedXxx), et d’une méthode « Caller » pour chaque méthode prise en charge. Lorsque l’objet est instancié, le constructeur d’objet reçoit un pointeur vers l’interface [**IUIAutomationPatternInstance**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationpatterninstance) , qui est implémentée par le noyau UI Automation. Les méthodes de l’interface IXxxPattern utilisent les méthodes [**IUIAutomationPatternInstance :: GetProperty**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationpatterninstance-getproperty) et [**CallMethod**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationpatterninstance-callmethod) pour transférer les demandes de propriétés et les appels de méthode au noyau UI Automation.

L’exemple suivant montre comment implémenter un objet de wrapper client pour un modèle de contrôle personnalisé simple qui prend en charge une seule propriété. Pour obtenir un exemple plus complexe, consultez [exemple d’implémentation d’un modèle de contrôle personnalisé](#example-implementation-of-a-custom-control-pattern).


```C++
// Define the client interface.
interface __declspec(uuid("c78b266d-b2c0-4e9d-863b-e3f74a721d47"))
IMyCustomPattern : public IUnknown
{
    STDMETHOD (get_CurrentIsReadOnly)(BOOL * pIsReadOnly) = 0;
    STDMETHOD (get_CachedIsReadOnly)(BOOL * pIsReadOnly) = 0;
};

// Implement the client wrapper class.
class CMyValuePatternClientWrapper :
    public IMyCustomPattern
{
    IUIAutomationPatternInstance * _pInstance;
    
public:
    // Get IUIAutomationPatternInstance interface pointer from the
    // UI Automation core.
    CMyValuePatternClientWrapper(IUIAutomationPatternInstance * pInstance)
        : _pInstance(pInstance)
    {
        _pInstance->AddRef();
    }
    
    ~CMyValuePatternClientWrapper()
    {
        _pInstance->Release();
    }

    // Note: Put standard IUnknown implementation here.

    STDMETHODIMP get_CurrentIsReadOnly(BOOL * pIsReadOnly)
    {
        return _pInstance->GetProperty(0, FALSE, UIAutomationType_Bool, pIsReadOnly);
    }

    STDMETHODIMP get_CachedIsReadOnly(BOOL * pIsReadOnly)
    {
        return _pInstance->GetProperty(0, TRUE, UIAutomationType_Bool, pIsReadOnly);
    }
};
```



### <a name="implementing-the-pattern-handler"></a>Implémentation du gestionnaire de modèles

Le gestionnaire de modèle est un objet qui implémente l’interface [**IUIAutomationPatternHandler**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationpatternhandler) . Cette interface a deux méthodes : [**IUIAutomationPatternHandler :: CreateClientWrapper**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationpatternhandler-createclientwrapper) et [**Dispatch**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationpatternhandler-dispatch). La méthode **CreateClientWrapper** est appelée par le noyau UI Automation et reçoit un pointeur vers l’interface [**IUIAutomationPatternInstance**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationpatterninstance) . **CreateClientWrapper** répond en instanciant l’objet de wrapper client et en passant le pointeur d’interface **IUIAutomationPatternInstance** au constructeur de wrapper client.

La méthode de [**distribution**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationpatternhandler-dispatch) est utilisée par le noyau UI Automation pour passer des demandes de propriétés et des appels de méthode à l’interface du fournisseur pour le modèle de contrôle personnalisé. Les paramètres incluent un pointeur vers l’interface du fournisseur, l’index de base zéro de l’accesseur Get de la propriété ou de la méthode appelée, et un tableau de structures [**UIAutomationParameter**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationparameter) qui contiennent les paramètres à passer au fournisseur. Le gestionnaire de modèle répond en vérifiant le paramètre d’index pour déterminer la méthode de fournisseur à appeler, puis appelle cette interface de fournisseur en passant les paramètres contenus dans les structures **UIAutomationParameter** .

L’objet de gestionnaire de modèle est instancié par le même code qui inscrit le modèle de contrôle personnalisé, avant l’inscription du modèle de contrôle. Le code doit passer le pointeur d’interface [**IUIAutomationPatternHandler**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationpatternhandler) de l’objet de gestionnaire de modèle au noyau UI Automation au moment de l’inscription.

L’exemple suivant montre comment implémenter un objet de gestionnaire de modèle pour un modèle de contrôle personnalisé simple qui prend en charge une seule propriété. Pour obtenir un exemple plus complexe, consultez [exemple d’implémentation d’un modèle de contrôle personnalisé](#example-implementation-of-a-custom-control-pattern).


```C++
// Define the provider interface.
interface __declspec(uuid("9f5266dd-f0ab-4562-8175-c383abb2569e"))
IMyValueProvider : public IUnknown
{
    STDMETHOD (get_IsReadOnly)(BOOL * pIsReadOnly) = 0;
};            

// Index used by IUIAutomationPatternHandler::Dispatch.
const int MyValue_GetIsReadOnly = 0; 
            
// Define the pattern handler class.        
class CMyValuePatternHandler : public IUIAutomationPatternHandler
{
public:
    
    // Put standard IUnknown implementation here.

    STDMETHODIMP CreateClientWrapper(
            IUIAutomationPatternInstance * pPatternInstance, 
            IUnknown ** pClientWrapper)
    {
        *pClientWrapper = new CMyValuePatternClientWrapper(pPatternInstance);
        if (*pClientWrapper == NULL)
            return E_INVALIDARG;
        return S_OK;
    }
    
    STDMETHODIMP Dispatch (IUnknown * pTarget, UINT index, 
            const struct UIAutomationParameter *pParams, UINT cParams)
    {
        switch(index)
        {
        case MyValue_GetIsReadOnly:
            return ((IMyValueProvider*)pTarget)->get_IsReadOnly((BOOL*)pParams[0].pData);
        }
        return E_INVALIDARG;
    }
};
```



### <a name="registering-a-custom-control-pattern"></a>Inscription d’un modèle de contrôle personnalisé

Avant de pouvoir être utilisé, un modèle de contrôle personnalisé doit être enregistré par le fournisseur et le client. L’inscription fournit le noyau UI Automation avec des informations détaillées sur le modèle de contrôle, et fournit le fournisseur ou le client avec l’ID de modèle de contrôle, ainsi que des ID pour les propriétés et les événements pris en charge par le modèle de contrôle. Côté fournisseur, le modèle de contrôle personnalisé doit être inscrit avant que le contrôle associé ne gère [**le \_ message WM**](wm-getobject.md) , ou en même temps.

Lors de l’inscription d’un modèle de contrôle personnalisé, le fournisseur ou le client fournit les informations suivantes :

-   GUID du modèle de contrôle personnalisé.
-   Chaîne inlocalisable contenant le nom du modèle de contrôle personnalisé.
-   GUID de l’interface du fournisseur qui prend en charge le modèle de contrôle personnalisé.
-   GUID de l’interface cliente qui prend en charge le modèle de contrôle personnalisé.
-   Tableau de structures [**UIAutomationPropertyInfo**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationpropertyinfo) qui décrivent les propriétés prises en charge par le modèle de contrôle personnalisé. Pour chaque propriété, le GUID, le nom de la propriété et le type de données doivent être spécifiés.
-   Tableau de structures [**UIAutomationMethodInfo**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationmethodinfo) qui décrivent les méthodes prises en charge par le modèle de contrôle personnalisé. Pour chaque méthode, la structure comprend les informations suivantes : le nom de la méthode, un nombre de paramètres, une liste de types de données de paramètres et une liste des noms de paramètres.
-   Tableau de structures [**UIAutomationEventInfo**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationeventinfo) qui décrivent les événements déclenchés par le modèle de contrôle personnalisé. Pour chaque événement, le GUID et le nom de l’événement doivent être spécifiés.
-   Adresse de l’interface [**IUIAutomationPatternHandler**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationpatternhandler) de l’objet de gestionnaire de modèle qui rend le modèle de contrôle personnalisé disponible pour les clients.

Pour inscrire le modèle de contrôle personnalisé, le fournisseur ou le code client doit effectuer les étapes suivantes :

1.  Remplissez une structure [**UIAutomationPatternInfo**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationpatterninfo) avec les informations précédentes.
2.  Utilisez la fonction [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) pour créer une instance de l’objet [**CUIAutomationRegistrar**](/previous-versions/windows/desktop/legacy/ff384837(v=vs.85)) et récupérer un pointeur vers l’interface [**IUIAutomationRegistrar**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationregistrar) de l’objet.
3.  Appelez la méthode [**IUIAutomationRegistrar :: RegisterPattern**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerpattern) , en passant l’adresse de la structure [**UIAutomationPatternInfo**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationpatterninfo) .

La méthode [**RegisterPattern**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerpattern) retourne un ID de modèle de contrôle, ainsi qu’une liste d’ID de propriété et d’ID d’événement. Une application peut passer ces ID à toute méthode UI Automation qui accepte un tel identificateur en tant que paramètre. Par exemple, vous pouvez passer un ID de modèle inscrit à la méthode [**IUIAutomationElement :: GetCurrentPattern**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpattern) pour récupérer un pointeur vers l’interface du fournisseur pour le modèle de contrôle.

Il n’existe aucune méthode qui annule l’inscription d’un modèle de contrôle personnalisé. Au lieu de cela, elle est désinscrite implicitement lorsque le dernier objet UI Automation est libéré.

Pour obtenir un exemple qui montre comment inscrire un modèle de contrôle personnalisé, consultez la section suivante.

### <a name="example-implementation-of-a-custom-control-pattern"></a>Exemple d’implémentation d’un modèle de contrôle personnalisé

Cette section contient un exemple de code qui montre comment implémenter les objets Wrapper client et gestionnaire de modèles pour un modèle de contrôle personnalisé. L’exemple implémente un modèle de contrôle personnalisé basé sur le modèle de contrôle [value](uiauto-implementingvalue.md) .


```C++
// Step 1: Define the public provider and client interfaces using IDL. Interface 
// definitions are in C here to simplify the example.

// Define the provider interface.
interface __declspec(uuid("9f5266dd-f0ab-4562-8175-c383abb2569e"))
IMyValueProvider : public IUnknown
{
    STDMETHOD (get_Value)(BSTR * pValue) = 0;
    STDMETHOD (get_IsReadOnly)(BOOL * pIsReadOnly) = 0;
    STDMETHOD (SetValue)(LPCWSTR pNewValue) = 0;
    STDMETHOD (Reset)() = 0;
};

// Define the client interface.
interface __declspec(uuid("103b8323-b04a-4180-9140-8c1e437713a3"))
IUIAutomationMyValuePattern : public IUnknown
{
    STDMETHOD (get_CurrentValue)(BSTR * pValue) = 0;
    STDMETHOD (get_CachedValue)(BSTR * pValue) = 0;

    STDMETHOD (get_CurrentIsReadOnly)(BOOL * pIsReadOnly) = 0;
    STDMETHOD (get_CachedIsReadOnly)(BOOL * pIsReadOnly) = 0;

    STDMETHOD (SetValue)(LPCWSTR pNewValue) = 0;
    STDMETHOD (Reset)() = 0;
};

// Enumerate the properties and methods starting from 0, and placing the 
// properties first. 
enum
{
    MyValue_GetValue = 0,
    MyValue_GetIsReadOnly = 1,
    MyValue_SetValue = 2,
    MyValue_Reset = 3,
};

// Step 2: Implement the client wrapper class.
class CMyValuePatternClientWrapper :
    public IUIAutomationMyValuePattern
{
    IUIAutomationPatternInstance * _pInstance;

public:
    // Get IUIAutomationPatternInstance interface pointer.
    CMyValuePatternClientWrapper(IUIAutomationPatternInstance * pInstance)
    {
        _pInstance = pInstance;
        _pInstance->AddRef();
    }

    // Put standard IUnknown implementation here.

    STDMETHODIMP get_CurrentValue(BSTR * pValue)
    {
        return _pInstance->GetProperty(MyValue_GetValue, FALSE, 
                UIAutomationType_String, pValue);
    }

    STDMETHODIMP get_CachedValue(BSTR * pValue)
    {
        return _pInstance->GetProperty(MyValue_GetValue, TRUE, 
                UIAutomationType_String, pValue);
    }

    STDMETHODIMP get_CurrentIsReadOnly(BOOL * pIsReadOnly)
    {
        return _pInstance->GetProperty(MyValue_GetIsReadOnly, FALSE, 
                UIAutomationType_Bool, pIsReadOnly);
    }

    STDMETHODIMP get_CachedIsReadOnly(BOOL * pIsReadOnly)
    {
        return _pInstance->GetProperty(MyValue_GetIsReadOnly, TRUE, 
                UIAutomationType_Bool, pIsReadOnly);
    }

    STDMETHODIMP SetValue(LPCWSTR pValue)
    {
        UIAutomationParameter SetValueParams[] = 
                { UIAutomationType_String, &pValue };
        return _pInstance->CallMethod(MyValue_SetValue,  SetValueParams, 
                ARRAYSIZE(SetValueParams));
    }

    STDMETHODIMP Reset()
    {
        return _pInstance->CallMethod(MyValue_Reset, NULL, 0);
    }
};

// Step 3: Implement the pattern handler class.
class CMyValuePatternHandler : public IUIAutomationPatternHandler
{
public:

    // Put standard IUnknown implementation here.
    
    STDMETHODIMP CreateClientWrapper(
            IUIAutomationPatternInstance * pPatternInstance, 
            IUnknown ** pClientWrapper)
    {
        *pClientWrapper = new CMyValuePatternClientWrapper(pPatternInstance);
        if (*pClientWrapper == NULL)
            return E_INVALIDARG;
        return S_OK;
    }
    
    STDMETHODIMP Dispatch (IUnknown * pTarget, UINT index, 
            const struct UIAutomationParameter *pParams, 
            UINT cParams)
    {
        switch(index)
        {
        case MyValue_GetValue:
            return ((IMyValueProvider*)pTarget)->get_Value((BSTR*)pParams[0].pData);

        case MyValue_GetIsReadOnly:
            return ((IMyValueProvider*)pTarget)->get_IsReadOnly((BOOL*)pParams[0].pData);

        case MyValue_SetValue:
            return ((IMyValueProvider*)pTarget)->SetValue(*(LPCWSTR*)pParams[0].pData);

        case MyValue_Reset:
            return ((IMyValueProvider*)pTarget)->Reset();
        }
        return E_INVALIDARG;
    }
};

CMyValuePatternHandler g_MyValuePatternHandler;

// Step 4: Declare information about the properties and methods supported
// by the custom control pattern.

// Define GUIDs for the custom control pattern and each of its properties 
// and events.
static const GUID MyValue_Pattern_Guid = { 0xa49aa3c0, 0xe413, 0x4ecf, 
        { 0xa1, 0xc3, 0x37, 0x42, 0xa7, 0x86, 0x67, 0x3f } };
static const GUID MyValue_Value_Property_Guid = { 0xe58f3f67, 0x22c7, 0x44f0, 
        { 0x83, 0x55, 0xd8, 0x76, 0x14, 0xa1, 0x10, 0x81 } };
static const GUID MyValue_IsReadOnly_Property_Guid = { 0x480540f2, 0x9829, 0x4acd, 
        { 0xb8, 0xea, 0x6e, 0x2a, 0xdc, 0xe5, 0x3a, 0xfb } };
static const GUID MyValue_Reset_Event_Guid = { 0x5b80edd3, 0x67f, 0x4a70, 
        { 0xb0, 0x7, 0x4, 0x12, 0x85, 0x11, 0x1, 0x7a } };

// Declare information about the properties, in the same order as the
// previously defined "MyValue_" enumerated type.
UIAutomationPropertyInfo g_MyValueProperties[] = 
{
    // GUID, name, data type.
    { MyValue_Value_Property_Guid, L"MyValuePattern.Value", 
                                                    UIAutomationType_String },
    { MyValue_IsReadOnly_Property_Guid, L"MyValuePattern.IsReadOnly", 
                                                    UIAutomationType_Bool },
};

// Declare information about the event.
UIAutomationEventInfo g_MyValueEvents [] =
{
    { MyValue_Reset_Event_Guid,  L"MyValuePattern.Reset" },
};

// Declare the data type and name of the SetValue method parameter. 
UIAutomationType g_SetValueParamTypes[] = { UIAutomationType_String };
LPCWSTR g_SetValueParamNames[] = {L"pNewValue"};

// Declare information about the methods.
UIAutomationMethodInfo g_MyValueMethods[] =
{
    // Name, focus flag, count of in parameters, count of out parameters, types, parameter names.
    { L"MyValuePattern.SetValue", TRUE, 1, 0, g_SetValueParamTypes, g_SetValueParamNames },
    { L"MyValuePattern.Reset", TRUE, 0, 0, NULL, NULL },
};

// Declare the custom control pattern using the previously defined information.
UIAutomationPatternInfo g_ValuePatternInfo =
{
    MyValue_Pattern_Guid,
    L"MyValuePattern",
    __uuidof(IMyValueProvider),
    __uuidof(IUIAutomationMyValuePattern),
    ARRAYSIZE(g_MyValueProperties), g_MyValueProperties, // properties
    ARRAYSIZE(g_MyValueMethods), g_MyValueMethods,       // methods
    ARRAYSIZE(g_MyValueEvents), g_MyValueEvents,         // events 
    &g_MyValuePatternHandler
};

// Step 5: Register the custom control pattern and retrieve the control pattern and property 
// identifiers.

// Control pattern, property, and event IDs.
PATTERNID  g_MyValue_PatternID;
PROPERTYID g_MyValue_Value_PropertyID;
PROPERTYID g_MyValue_IsReadOnly_PropertyID;
EVENTID    g_MyValueReset_EventID;

// ID used by the client to determine whether the custom control pattern is available.
PROPERTYID g_IsMyValuePatternAvailable_PropertyID;

HRESULT RegisterPattern()
{
    // Create the registrar object and get the IUIAutomationRegistrar interface pointer. 
    IUIAutomationRegistrar * pUIARegistrar;
    CoCreateInstance(CLSID_CUIAutomationRegistrar, NULL, CLSCTX_INPROC_SERVER, 
            IID_IUIAutomationRegistrar, (void **)&pUIARegistrar);

    if (pUIARegistrar == NULL)
        return E_NOINTERFACE;

    PROPERTYID propIDs[2]; // Array for property IDs.

    // Register the control pattern.
    HRESULT hr = pUIARegistrar->RegisterPattern(
        &g_ValuePatternInfo,
        &g_MyValue_PatternID,
        &g_IsMyValuePatternAvailable_PropertyID,
        ARRAYSIZE(propIDs), 
        propIDs,
        1,
        &g_MyValueReset_EventID);
            
    if (hr == S_OK)
    {
        // Copy the property IDs.
        g_MyValue_Value_PropertyID = propIDs[0];
        g_MyValue_IsReadOnly_PropertyID = propIDs[1];
    }

    pUIARegistrar->Release();
    return hr;
}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**Méthodologique**
</dt> <dt>

[Conception de propriétés, d’événements et de modèles de contrôle personnalisés](uiauto-designingcustompropseventpatterns.md)
</dt> <dt>

[Vue d'ensemble des propriétés UI Automation](uiauto-propertiesoverview.md)
</dt> <dt>

[Vue d'ensemble des événements UI Automation](uiauto-eventsoverview.md)
</dt> <dt>

[Vue d'ensemble des modèles de contrôle UI Automation](uiauto-controlpatternsoverview.md)
</dt> </dl>

 

 