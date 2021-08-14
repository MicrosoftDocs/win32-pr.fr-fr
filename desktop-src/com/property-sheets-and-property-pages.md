---
title: Pages et feuilles de propriétés
description: Pages et feuilles de propriétés
ms.assetid: 6bcd1c1c-9b66-4422-bb07-67a856b3295d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7991ea650838e9980292257c14d26909e9476f0f35422fa21deab2b0b5ecbbdd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118104931"
---
# <a name="property-sheets-and-property-pages"></a>Pages et feuilles de propriétés

Les propriétés d’un objet sont exposées aux clients de la même façon que les méthodes via les interfaces COM ou l’implémentation **IDispatch** de l’objet, ce qui permet aux programmes qui appellent ces méthodes de modifier les propriétés. la technologie OLE des pages de propriétés fournit les moyens de créer une interface utilisateur pour les propriétés d’un objet en fonction de Windows normes de l’interface utilisateur. Ainsi, les propriétés sont exposées aux utilisateurs finaux. La feuille de propriétés d’un objet est une boîte de dialogue à onglets dans laquelle chaque onglet correspond à une page de propriétés spécifique. Le modèle OLE pour l’utilisation des pages de propriétés est constitué des fonctionnalités suivantes :

-   Chaque page de propriétés est gérée par un objet in-process qui implémente [**IPropertyPage**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertypage) ou [**IPropertyPage2**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertypage2). Chaque page est identifiée avec son propre CLSID unique.
-   Un objet spécifie sa prise en charge pour les pages de propriétés en implémentant [**ISpecifyPropertyPages**](/windows/desktop/api/OCIdl/nn-ocidl-ispecifypropertypages). Via cette interface, l’appelant peut obtenir une liste de CLSID identifiant les pages de propriétés spécifiques que l’objet prend en charge. Si l’objet spécifie un CLSID de page de propriétés, l’objet doit être en mesure de recevoir des modifications de propriété à partir de la page de propriétés.
-   Tout morceau de code (client ou objet) qui souhaite afficher la feuille de propriétés d’un objet passe le pointeur [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) de l’objet (ou un tableau si plusieurs objets doivent être affectés), ainsi qu’un tableau de CLSID de page à [**OleCreatePropertyFrame**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepropertyframe) ou [**OleCreatePropertyFrameIndirect**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepropertyframeindirect), ce qui crée la boîte de dialogue à onglets.
-   La boîte de dialogue frame de propriété instancie une seule instance de chaque page de propriétés, à l’aide de [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) sur chaque CLSID. Le frame de propriété obtient au moins un pointeur [**IPropertyPage**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertypage) pour chaque page. En outre, le frame crée un objet de site de page de propriétés en lui-même pour chaque page. Chaque site implémente [**IPropertyPageSite**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertypagesite) et ce pointeur est transmis à chaque page. La page communique ensuite avec le site via ce pointeur d’interface.
-   Chaque page est également consciente de l’objet ou des objets pour lesquels elle a été appelée ; autrement dit, le frame de propriété passe les pointeurs [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown)des objets à chaque page. Lorsque vous êtes invité à appliquer les modifications aux objets, chaque page interroge le pointeur d’interface approprié et passe les nouvelles valeurs de propriété aux objets de la manière souhaitée. Il n’existe aucune stipulation sur la façon dont cette communication doit se produire.
-   Un objet peut également prendre en charge la navigation par propriété via l’interface [**IPerPropertyBrowsing**](/windows/desktop/api/OCIdl/nn-ocidl-iperpropertybrowsing) , ce qui permet à l’objet de spécifier quelle propriété doit recevoir le focus initial lorsque la page de propriétés est affichée et spécifier des chaînes et des valeurs qui peuvent être affichées par le client dans sa propre interface utilisateur.

Ces fonctionnalités sont illustrées dans le diagramme suivant :

![Diagramme qui montre les fonctionnalités des feuilles de propriétés et des pages de propriétés.](images/7ea02938-c2fc-4ad0-a8b1-25222ca890ea.png)

Ces interfaces sont définies comme suit :

``` syntax
interface ISpecifyPropertyPages : IUnknown 
  { 
    HRESULT GetPages([out] CAUUID *pPages); 
  }; 
 
 
interface IPropertyPage : IUnknown 
  { 
    HRESULT SetPageSite([in] IPropertyPageSite *pPageSite); 
    HRESULT Activate([in] HWND hWndParent, [in] LPCRECT prc 
        , [in] BOOL bModal); 
    HRESULT Deactivate(void); 
    HRESULT GetPageInfo([out] PROPPAGEINFO *pPageInfo); 
    HRESULT SetObjects([in] ULONG cObjects 
        , [in, max_is(cObjects)] IUnknown **ppunk); 
    HRESULT Show([in] UINT nCmdShow); 
    HRESULT Move([in] LPCRECT prc); 
    HRESULT IsPageDirty(void); 
    HRESULT Apply(void); 
    HRESULT Help([in] LPCOLESTR pszHelpDir); 
    HRESULT TranslateAccelerator([in] LPMSG pMsg); 
  } 
 
interface IPropertyPageSite : IUnknown 
  { 
    HRESULT OnStatusChange([in] DWORD dwFlags); 
    HRESULT GetLocaleID([out] LCID *pLocaleID); 
    HRESULT GetPageContainer([out] IUnknown **ppUnk); 
    HRESULT TranslateAccelerator([in] LPMSG pMsg); 
  } 
 
```

La méthode [**ISpecifyPropertyPages :: GetPages**](/windows/desktop/api/OCIdl/nf-ocidl-ispecifypropertypages-getpages) retourne un tableau compté de valeurs UUID (Guid) qui décrivent chacune le CLSID d’une page de propriétés que l’objet souhaite afficher. Quiconque appelle la feuille de propriétés avec [**OleCreatePropertyFrame**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepropertyframe) ou [**OleCreatePropertyFrameIndirect**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepropertyframeindirect) passe ce tableau à la fonction. Notez que si l’appelant souhaite afficher des pages de propriétés pour plusieurs objets, il doit uniquement transmettre l’intersection des listes CLSID de tous les objets à ces fonctions. En d’autres termes, l’appelant doit uniquement appeler les pages de propriétés qui sont communes à tous les objets.

En outre, l’appelant transmet également les pointeurs [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) aux objets affectés aux fonctions d’API. Les deux fonctions API créent une boîte de dialogue de frame de propriété et instancient un site de page avec [**IPropertyPageSite**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertypagesite) pour chaque page qu’il chargera. Grâce à cette interface, une page de propriétés peut :

-   Récupérez la langue actuelle utilisée dans la feuille de propriétés par le biais de [**GetLocaleID**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypagesite-getlocaleid).
-   Demandez au frame de traiter les séquences de touches via [**TranslateAccelerator**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypagesite-translateaccelerator).
-   Notifiez le frame des modifications de la page via [**OnStatusChange**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypagesite-onstatuschange).
-   Obtenez un pointeur d’interface pour le frame lui-même via [**GetPageContainer**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypagesite-getpagecontainer), bien qu’il n’y ait pas d’interfaces définies pour le frame à ce stade pour cette fonction, retourne toujours E \_ NOTIMPL.

Le frame de propriété instancie chaque objet de page de propriétés et obtient l’interface [**IPropertyPage**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertypage) de chaque page. Via cette interface, le frame informe la page de son site de page ([**SetPageSite**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypage-setpagesite)), récupère les dimensions et les chaînes de page ([**GetPageInfo**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypage-getpageinfo)), passe les pointeurs d’interface aux objets affectés ([**SetObjects**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypage-setobjects)), indique à la page quand créer et détruire ses contrôles ([**activation**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypage-activate) et [**désactivation**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypage-deactivate)). indique à la page d’afficher ou de se repositionner ([**Afficher**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypage-show) et [**déplacer**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypage-move)), demande à la page d’appliquer ses valeurs actuelles aux objets affectés ([**appliquer**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypage-apply)), vérifie l’état d’intégrité de la page ([**IsPageDirty**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypage-ispagedirty)), appelle l’aide ([**aide**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypage-help)) et passe des séquences de touches à la page ([**TranslateAccelerator**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypage-translateaccelerator)).

Un objet peut également prendre en charge la navigation par propriété, qui fournit :

1.  Une méthode (via [**IPerPropertyBrowsing**](/windows/desktop/api/OCIdl/nn-ocidl-iperpropertybrowsing) et [**IPropertyPage2**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertypage2)) pour spécifier la propriété sur laquelle la page de propriétés doit recevoir le focus initial lorsqu’une feuille de propriétés est affichée pour la première fois
2.  Méthode (via [**IPerPropertyBrowsing**](/windows/desktop/api/OCIdl/nn-ocidl-iperpropertybrowsing)) pour l’objet qui spécifie des valeurs prédéfinies et des chaînes descriptives correspondantes qui peuvent être affichées dans l’interface utilisateur propre à un client pour les propriétés.

Un objet peut choisir de prendre en charge (2) sans prendre en charge (1), comme lorsque l’objet n’a aucune feuille de propriétés.

Les interfaces [**IPropertyPage2**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertypage2) et [**IPerPropertyBrowsing**](/windows/desktop/api/OCIdl/nn-ocidl-iperpropertybrowsing) sont définies comme suit :

``` syntax
interface IPerPropertyBrowsing : IUnknown 
  { 
    HRESULT GetDisplayString([in] DISPID dispID, [out] BSTR *pbstr); 
    HRESULT MapPropertyToPage([in] DISPID dispID, [out] CLSID *pclsid); 
    HRESULT GetPredefinedStrings([in] DISPID dispID, [out] CALPOLESTR *pcaStringsOut, [out] CADWORD *pcaCookiesOut); 
    HRESULT GetPredefinedValue([in] DISPID dispID, [in] DWORD dwCookie, [out] VARIANT *pvarOut); 
  } 
 
interface IPropertyPage2 : IPropertyPage 
  { 
    HRESULT EditProperty([in] DISPID dispID); 
  } 
 
```

Pour spécifier sa prise en charge de telles fonctionnalités, l’objet implémente [**IPerPropertyBrowsing**](/windows/desktop/api/OCIdl/nn-ocidl-iperpropertybrowsing). Grâce à cette interface, l’appelant peut demander les informations nécessaires pour accomplir l’exploration, telles que les chaînes prédéfinies ([**GetPredefinedStrings**](/windows/desktop/api/OCIdl/nf-ocidl-iperpropertybrowsing-getpredefinedstrings)) et les valeurs ([**GetPredefinedValue**](/windows/desktop/api/OCIdl/nf-ocidl-iperpropertybrowsing-getpredefinedvalue)), ainsi qu’une chaîne d’affichage pour une propriété donnée ([**GetDisplayString**](/windows/desktop/api/OCIdl/nf-ocidl-iperpropertybrowsing-getdisplaystring)).

En outre, le client peut obtenir le CLSID de la page de propriétés qui permet à l’utilisateur de modifier une propriété donnée identifiée par un DISPID ([**MapPropertyToPage**](/windows/desktop/api/OCIdl/nf-ocidl-iperpropertybrowsing-mappropertytopage)). Le client demande ensuite au frame de propriété d’activer cette page initialement en passant le CLSID et le DISPID à [**OleCreatePropertyFrameIndirect**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepropertyframeindirect). Le frame active d’abord cette page et passe le DISPID à la page via [**IPropertyPage2 :: EditProperty**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypage2-editproperty). La page définit ensuite le focus sur le champ d’édition de cette propriété. De cette façon, un client peut passer d’un nom de propriété dans sa propre interface utilisateur à la page de propriétés qui peut manipuler cette propriété.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Pages de propriétés et feuilles de propriétés](property-pages-and-property-sheets.md)
</dt> </dl>

 

 




