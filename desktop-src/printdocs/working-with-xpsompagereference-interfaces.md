---
description: Cette rubrique explique comment utiliser les interfaces qui fournissent l’accès aux références de page dans un modèle d’objet XPS.
ms.assetid: bb227536-3b29-4221-b2d5-bab5e9d91448
title: Utilisation des interfaces IXpsOMPageReference
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f4526e6c561a962b77fa3f2fc62d56431359aa6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865865"
---
# <a name="working-with-ixpsompagereference-interfaces"></a><span data-ttu-id="a0223-103">Utilisation des interfaces IXpsOMPageReference</span><span class="sxs-lookup"><span data-stu-id="a0223-103">Working with IXpsOMPageReference Interfaces</span></span>

<span data-ttu-id="a0223-104">Cette rubrique explique comment utiliser les interfaces qui fournissent l’accès aux références de page dans un modèle d’objet XPS.</span><span class="sxs-lookup"><span data-stu-id="a0223-104">This topic describes how to use the interfaces that provide access to page references in an XPS OM.</span></span>



| <span data-ttu-id="a0223-105">Nom de l’interface</span><span class="sxs-lookup"><span data-stu-id="a0223-105">Interface name</span></span>                                                  | <span data-ttu-id="a0223-106">Interfaces enfants logiques</span><span class="sxs-lookup"><span data-stu-id="a0223-106">Logical child interfaces</span></span>                    | <span data-ttu-id="a0223-107">Description</span><span class="sxs-lookup"><span data-stu-id="a0223-107">Description</span></span>                                                                                                                                                                                                                                                                                                                                                      |
|-----------------------------------------------------------------|---------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a0223-108">**IXpsOMPageReference**</span><span class="sxs-lookup"><span data-stu-id="a0223-108">**IXpsOMPageReference**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference)<br/>   | [<span data-ttu-id="a0223-109">**IXpsOMPage**</span><span class="sxs-lookup"><span data-stu-id="a0223-109">**IXpsOMPage**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage)<br/> | <span data-ttu-id="a0223-110">Virtualise le contenu d’une page de document.</span><span class="sxs-lookup"><span data-stu-id="a0223-110">Virtualizes the content of a document page.</span></span> <br/> <span data-ttu-id="a0223-111">Une référence de page contient des informations de base sur la page, certaines propriétés de la page et un lien vers le contenu de la page.</span><span class="sxs-lookup"><span data-stu-id="a0223-111">A page reference contains basic information about the page, some page properties, and a link to the page contents.</span></span> <span data-ttu-id="a0223-112">L’interface [**IXpsOMPage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage) qui comprend le contenu de la page est retournée par la méthode [**IXpsOMPageReference :: GetPage**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompagereference-getpage) .</span><span class="sxs-lookup"><span data-stu-id="a0223-112">The [**IXpsOMPage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage) interface that comprises page contents is returned by the [**IXpsOMPageReference::GetPage**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompagereference-getpage) method.</span></span><br/> |
| [<span data-ttu-id="a0223-113">**IXpsOMNameCollection**</span><span class="sxs-lookup"><span data-stu-id="a0223-113">**IXpsOMNameCollection**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomnamecollection)<br/> | <span data-ttu-id="a0223-114">Aucun</span><span class="sxs-lookup"><span data-stu-id="a0223-114">None</span></span><br/>                             | <span data-ttu-id="a0223-115">Contient une liste d’éléments de page qui sont des cibles de lien hypertexte.</span><span class="sxs-lookup"><span data-stu-id="a0223-115">Contains a list of page items that are hyperlink targets.</span></span> <span data-ttu-id="a0223-116">La liste est retournée par la méthode [**IXpsOMPageReference :: CollectLinkTargets**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompagereference-collectlinktargets) .</span><span class="sxs-lookup"><span data-stu-id="a0223-116">The list is returned by the [**IXpsOMPageReference::CollectLinkTargets**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompagereference-collectlinktargets) method.</span></span><br/>                                                                                                                                                               |
| [<span data-ttu-id="a0223-117">**IXpsOMPartResources**</span><span class="sxs-lookup"><span data-stu-id="a0223-117">**IXpsOMPartResources**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompartresources)<br/>   | <span data-ttu-id="a0223-118">Aucun</span><span class="sxs-lookup"><span data-stu-id="a0223-118">None</span></span><br/>                             | <span data-ttu-id="a0223-119">Contient une liste des ressources basées sur un composant qui sont associées à la page.</span><span class="sxs-lookup"><span data-stu-id="a0223-119">Contains a list of the part-based resources that are associated with the page.</span></span> <span data-ttu-id="a0223-120">Cette liste est retournée par la méthode [**IXpsOMPageReference :: CollectPartResources**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompagereference-collectpartresources) .</span><span class="sxs-lookup"><span data-stu-id="a0223-120">This list is returned by the [**IXpsOMPageReference::CollectPartResources**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompagereference-collectpartresources) method.</span></span><br/>                                                                                                                                     |



 

## <a name="code-examples"></a><span data-ttu-id="a0223-121">Exemples de code</span><span class="sxs-lookup"><span data-stu-id="a0223-121">Code Examples</span></span>

<span data-ttu-id="a0223-122">Les exemples de code suivants illustrent l’utilisation des interfaces de référence de page dans un programme.</span><span class="sxs-lookup"><span data-stu-id="a0223-122">The following code examples illustrate how to work with the page reference interfaces in a program.</span></span>

-   [<span data-ttu-id="a0223-123">Obtient le contenu de la page</span><span class="sxs-lookup"><span data-stu-id="a0223-123">Get the page contents</span></span>](#get-the-page-contents)
-   [<span data-ttu-id="a0223-124">Obtient la liste des cibles de lien hypertexte sur cette page</span><span class="sxs-lookup"><span data-stu-id="a0223-124">Get the list of hyperlink targets on this page</span></span>](#get-the-list-of-hyperlink-targets-on-this-page)
-   [<span data-ttu-id="a0223-125">Obtient les ressources de composant associées à cette page</span><span class="sxs-lookup"><span data-stu-id="a0223-125">Get the part resources that are associated with this page</span></span>](#get-the-part-resources-that-are-associated-with-this-page)

### <a name="get-the-page-contents"></a><span data-ttu-id="a0223-126">Obtient le contenu de la page</span><span class="sxs-lookup"><span data-stu-id="a0223-126">Get the page contents</span></span>

<span data-ttu-id="a0223-127">L’exemple de code suivant obtient un pointeur vers l’interface [**IXpsOMPage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage) qui comprend le contenu de la page.</span><span class="sxs-lookup"><span data-stu-id="a0223-127">The following code example gets a pointer to the [**IXpsOMPage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage) interface that comprises the page contents.</span></span> <span data-ttu-id="a0223-128">Si la page n’a pas été chargée dans le modèle d’objet XPS, comme c’est le cas lorsque le modèle d’objet XPS est initialisé en appelant [**IXpsOMObjectFactory :: CreatePackageFromFile**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createpackagefromfile), l’appel de [**IXpsOMPageReference :: GetPage**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompagereference-getpage) chargera la page dans le modèle d’objet XPS.</span><span class="sxs-lookup"><span data-stu-id="a0223-128">If the page has not been loaded into the XPS OM, as happens when the XPS OM is initialized by calling [**IXpsOMObjectFactory::CreatePackageFromFile**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createpackagefromfile), calling [**IXpsOMPageReference::GetPage**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompagereference-getpage) will load the page into the XPS OM.</span></span>


```C++
    {
    HRESULT        hr = S_OK;
    IXpsOMPage     *page = NULL;

    // pageRef contains the current page reference
    // and is passed in as a parameter

    // get the page content of this page reference
    hr = pageRef->GetPage (&page);
```



### <a name="get-the-list-of-hyperlink-targets-on-this-page"></a><span data-ttu-id="a0223-129">Obtient la liste des cibles de lien hypertexte sur cette page</span><span class="sxs-lookup"><span data-stu-id="a0223-129">Get the list of hyperlink targets on this page</span></span>

<span data-ttu-id="a0223-130">L’exemple de code suivant obtient un pointeur vers l’interface [**IXpsOMNameCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomnamecollection) qui contient la liste des éléments de page qui sont des cibles de lien hypertexte.</span><span class="sxs-lookup"><span data-stu-id="a0223-130">The following code example gets a pointer to the [**IXpsOMNameCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomnamecollection) interface that contains the list of page items that are hyperlink targets.</span></span> <span data-ttu-id="a0223-131">Si la page n’a pas été chargée dans le modèle d’objet XPS, la liste des cibles de lien hypertexte est lue à partir du balisage **PageContent. LinkTargets** .</span><span class="sxs-lookup"><span data-stu-id="a0223-131">If the page has not been loaded into the XPS OM, the list of hyperlink targets is read from the **PageContent.LinkTargets** markup.</span></span> <span data-ttu-id="a0223-132">Si la page a été chargée, [**CollectLinkTargets**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompagereference-collectlinktargets) vérifie chaque élément de la page et retourne une liste d’éléments dont l’attribut **IsHyperlinkTarget** a la **valeur true**.</span><span class="sxs-lookup"><span data-stu-id="a0223-132">If the page has been loaded, [**CollectLinkTargets**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompagereference-collectlinktargets) checks each element in the page and returns a list of elements whose **IsHyperlinkTarget** attribute is **TRUE**.</span></span>


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



### <a name="get-the-part-resources-that-are-associated-with-this-page"></a><span data-ttu-id="a0223-133">Obtient les ressources de composant associées à cette page</span><span class="sxs-lookup"><span data-stu-id="a0223-133">Get the part resources that are associated with this page</span></span>

<span data-ttu-id="a0223-134">L’exemple de code suivant obtient les listes des différentes ressources utilisées par cette page.</span><span class="sxs-lookup"><span data-stu-id="a0223-134">The following code example gets the lists of the different resources that are used by this page.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="a0223-135">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a0223-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a0223-136">**IXpsOMNameCollection**</span><span class="sxs-lookup"><span data-stu-id="a0223-136">**IXpsOMNameCollection**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomnamecollection)
</dt> <dt>

[<span data-ttu-id="a0223-137">**IXpsOMPage**</span><span class="sxs-lookup"><span data-stu-id="a0223-137">**IXpsOMPage**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage)
</dt> <dt>

[<span data-ttu-id="a0223-138">**IXpsOMPageReference**</span><span class="sxs-lookup"><span data-stu-id="a0223-138">**IXpsOMPageReference**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference)
</dt> <dt>

[<span data-ttu-id="a0223-139">**IXpsOMPartResources**</span><span class="sxs-lookup"><span data-stu-id="a0223-139">**IXpsOMPartResources**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompartresources)
</dt> <dt>

[<span data-ttu-id="a0223-140">XML Paper Specification</span><span class="sxs-lookup"><span data-stu-id="a0223-140">XML Paper Specification</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 




