---
description: Cette rubrique explique comment utiliser les interfaces qui fournissent l’accès aux références de page dans un modèle d’objet XPS.
ms.assetid: bb227536-3b29-4221-b2d5-bab5e9d91448
title: Utilisation des interfaces IXpsOMPageReference
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f4526e6c561a962b77fa3f2fc62d56431359aa6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127220625"
---
# <a name="working-with-ixpsompagereference-interfaces"></a>Utilisation des interfaces IXpsOMPageReference

Cette rubrique explique comment utiliser les interfaces qui fournissent l’accès aux références de page dans un modèle d’objet XPS.



| Nom de l’interface                                                  | Interfaces enfants logiques                    | Description                                                                                                                                                                                                                                                                                                                                                      |
|-----------------------------------------------------------------|---------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IXpsOMPageReference**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference)<br/>   | [**IXpsOMPage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage)<br/> | Virtualise le contenu d’une page de document. <br/> Une référence de page contient des informations de base sur la page, certaines propriétés de la page et un lien vers le contenu de la page. L’interface [**IXpsOMPage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage) qui comprend le contenu de la page est retournée par la méthode [**IXpsOMPageReference :: GetPage**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompagereference-getpage) .<br/> |
| [**IXpsOMNameCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomnamecollection)<br/> | None<br/>                             | Contient une liste d’éléments de page qui sont des cibles de lien hypertexte. La liste est retournée par la méthode [**IXpsOMPageReference :: CollectLinkTargets**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompagereference-collectlinktargets) .<br/>                                                                                                                                                               |
| [**IXpsOMPartResources**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompartresources)<br/>   | None<br/>                             | Contient une liste des ressources basées sur un composant qui sont associées à la page. Cette liste est retournée par la méthode [**IXpsOMPageReference :: CollectPartResources**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompagereference-collectpartresources) .<br/>                                                                                                                                     |



 

## <a name="code-examples"></a>Exemples de code

Les exemples de code suivants illustrent l’utilisation des interfaces de référence de page dans un programme.

-   [Obtient le contenu de la page](#get-the-page-contents)
-   [Obtient la liste des cibles de lien hypertexte sur cette page](#get-the-list-of-hyperlink-targets-on-this-page)
-   [Obtient les ressources de composant associées à cette page](#get-the-part-resources-that-are-associated-with-this-page)

### <a name="get-the-page-contents"></a>Obtient le contenu de la page

L’exemple de code suivant obtient un pointeur vers l’interface [**IXpsOMPage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage) qui comprend le contenu de la page. Si la page n’a pas été chargée dans le modèle d’objet XPS, comme c’est le cas lorsque le modèle d’objet XPS est initialisé en appelant [**IXpsOMObjectFactory :: CreatePackageFromFile**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createpackagefromfile), l’appel de [**IXpsOMPageReference :: GetPage**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompagereference-getpage) chargera la page dans le modèle d’objet XPS.


```C++
    {
    HRESULT        hr = S_OK;
    IXpsOMPage     *page = NULL;

    // pageRef contains the current page reference
    // and is passed in as a parameter

    // get the page content of this page reference
    hr = pageRef->GetPage (&page);
```



### <a name="get-the-list-of-hyperlink-targets-on-this-page"></a>Obtient la liste des cibles de lien hypertexte sur cette page

L’exemple de code suivant obtient un pointeur vers l’interface [**IXpsOMNameCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomnamecollection) qui contient la liste des éléments de page qui sont des cibles de lien hypertexte. Si la page n’a pas été chargée dans le modèle d’objet XPS, la liste des cibles de lien hypertexte est lue à partir du balisage **PageContent. LinkTargets** . Si la page a été chargée, [**CollectLinkTargets**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompagereference-collectlinktargets) vérifie chaque élément de la page et retourne une liste d’éléments dont l’attribut **IsHyperlinkTarget** a la **valeur true**.


```C++
    HRESULT                         hr = S_OK;
    IXpsOMPage                      *page = NULL;
    IXpsOMNameCollection            *linkTargets = NULL;

    UINT32 numTargets = 0;
    UINT32 thisTarget = 0;
    LPWSTR thisTargetName = NULL;

    // pageRef contains the current page reference 

    // if the page hasn't been loaded yet, for example, if the XPS OM 
    //  was loaded from an XPS document, CollectLinkTargets obtains the
    //  list of link targets from the <PageContent.LinkTargets> markup
    hr = pageRef->CollectLinkTargets(&linkTargets);

    // get the page content of this page reference
    hr = pageRef->GetPage (&page);

    // after the page object has been loaded and calling GetPage or 
    //  by creating a page in the XPS OM, CollectLinkTargets will now check
    //  each of the page elements to return the list so this call to
    //  CollectLinkTargets might take longer to return than the previous
    //  call above if the XPS OM was created from a file
    linkTargets->Release(); // release previous collection
    hr = pageRef->CollectLinkTargets(&linkTargets);
    
    // walk the list of link targets returned
    hr = linkTargets->GetCount( &numTargets );
    thisTarget = 0;
    while (thisTarget < numTargets) {
        hr = linkTargets->GetAt (thisTarget, &thisTargetName);
        printf ("%s\n", thisTargetName);
        // release the target string returned to prevent memory leaks
        CoTaskMemFree (thisTargetName);
        // get next target in list
        thisTarget++;
    }
    // release page and the link target collection
    page->Release();
    linkTargets->Release();
```



### <a name="get-the-part-resources-that-are-associated-with-this-page"></a>Obtient les ressources de composant associées à cette page

L’exemple de code suivant obtient les listes des différentes ressources utilisées par cette page.


```C++
    HRESULT                                   hr = S_OK;
    IXpsOMPartResources                       *resources;

    IXpsOMColorProfileResourceCollection      *colorProfileResources;
    IXpsOMFontResourceCollection              *fontResources;
    IXpsOMImageResourceCollection             *imageResources;
    IXpsOMRemoteDictionaryResourceCollection  *dictionaryResources; 

    // pageRef contains the current page reference 
    hr = pageRef->CollectPartResources ( &resources );

    // Get pointers to each type of resource
    hr = resources->GetColorProfileResources( &colorProfileResources );
    hr = resources->GetFontResources( &fontResources );
    hr = resources->GetImageResources( &imageResources );
    hr = resources->GetRemoteDictionaryResources( &dictionaryResources );
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**IXpsOMNameCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomnamecollection)
</dt> <dt>

[**IXpsOMPage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage)
</dt> <dt>

[**IXpsOMPageReference**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference)
</dt> <dt>

[**IXpsOMPartResources**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompartresources)
</dt> <dt>

[XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 




