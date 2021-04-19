---
description: Cette rubrique explique comment créer un modèle OM XPS vide.
ms.assetid: 5b6f12ba-9a41-4252-96c4-391bb8d75cd4
title: Créer un modèle d’objet XPS vide
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0588fc11deb4b3d980e978dfe8a5370bc170d506
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106527881"
---
# <a name="create-a-blank-xps-om"></a><span data-ttu-id="9463a-103">Créer un modèle d’objet XPS vide</span><span class="sxs-lookup"><span data-stu-id="9463a-103">Create a Blank XPS OM</span></span>

<span data-ttu-id="9463a-104">Cette rubrique explique comment créer un modèle OM XPS vide.</span><span class="sxs-lookup"><span data-stu-id="9463a-104">This topic describes how to create a blank XPS OM.</span></span> <span data-ttu-id="9463a-105">Il présente les exemples de code qui illustrent l’utilisation d’un modèle d’objet XPS pour créer la structure de document d’un document XPS qui comporte une page vierge.</span><span class="sxs-lookup"><span data-stu-id="9463a-105">It presents the code examples that illustrate how to use an XPS OM to build the document structure of an XPS document that has one blank page.</span></span>

<span data-ttu-id="9463a-106">Pour être enregistré en tant que document XPS, le modèle d’objet XPS requiert au moins les composants suivants :</span><span class="sxs-lookup"><span data-stu-id="9463a-106">To be saved as an XPS document, the XPS OM requires at least the following components:</span></span>

-   <span data-ttu-id="9463a-107">[**IXpsOMPackage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage) décrivant le package de documents XPS</span><span class="sxs-lookup"><span data-stu-id="9463a-107">An [**IXpsOMPackage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage) that describes the XPS document package</span></span>
-   <span data-ttu-id="9463a-108">[**IXpsOMDocumentSequence**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence) qui contient le Framework du contenu du package</span><span class="sxs-lookup"><span data-stu-id="9463a-108">An [**IXpsOMDocumentSequence**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence) that contains the framework of the package contents</span></span>
-   <span data-ttu-id="9463a-109">[**IXpsOMDocument**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocument) qui contient l’infrastructure d’un document dans le package</span><span class="sxs-lookup"><span data-stu-id="9463a-109">An [**IXpsOMDocument**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocument) that contains the framework of a document within the package</span></span>
-   <span data-ttu-id="9463a-110">[**IXpsOMPageReference**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference) qui contient la collection de pages dans le document</span><span class="sxs-lookup"><span data-stu-id="9463a-110">An [**IXpsOMPageReference**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference) that contains the collection of pages in the document</span></span>
-   <span data-ttu-id="9463a-111">[**IXpsOMPage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage) qui contient une page vierge</span><span class="sxs-lookup"><span data-stu-id="9463a-111">An [**IXpsOMPage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage) that contains a blank page</span></span>

<span data-ttu-id="9463a-112">Lorsque ces interfaces sont utilisées, le modèle d’objet XPS contient un document qui contient une page vierge.</span><span class="sxs-lookup"><span data-stu-id="9463a-112">When these interfaces are used, the XPS OM will contain a document that has one blank page.</span></span> <span data-ttu-id="9463a-113">Pour créer ce document dans un modèle d’objet XPS, le programme doit d’abord créer les composants individuels, puis les lier ensemble.</span><span class="sxs-lookup"><span data-stu-id="9463a-113">To create this document in an XPS OM, the program must first create the individual components and then link them together.</span></span>

<span data-ttu-id="9463a-114">Avant d’utiliser les exemples de code suivants, lisez l’exclusion de responsabilité dans les [tâches de programmation de document XPS courantes](common-xps-document-tasks.md).</span><span class="sxs-lookup"><span data-stu-id="9463a-114">Before using the following code examples, read the disclaimer in [Common XPS Document Programming Tasks](common-xps-document-tasks.md).</span></span>

## <a name="code-examples"></a><span data-ttu-id="9463a-115">Exemples de code</span><span class="sxs-lookup"><span data-stu-id="9463a-115">Code Examples</span></span>

<span data-ttu-id="9463a-116">L’exemple de code suivant suppose que l’initialisation, décrite dans [initialiser un modèle d’objet XPS](xps-object-model-initialization.md), a réussi.</span><span class="sxs-lookup"><span data-stu-id="9463a-116">The following code example assumes that the initialization, described in [Initialize an XPS OM](xps-object-model-initialization.md), has succeeded.</span></span>


```C++
    // Declare the variables used in this section.
    HRESULT                       hr = S_OK;
    IOpcPartUri                   *opcPartUri = NULL;
    IXpsOMPackage                 *xpsPackage = NULL;
    IXpsOMDocumentSequence        *xpsFDS = NULL;
    IXpsOMDocumentCollection      *fixedDocuments = NULL;
    IXpsOMDocument                *xpsFD = NULL;
    IXpsOMPage                    *xpsPage = NULL;
    IXpsOMPageReferenceCollection *pageRefs = NULL;
    IXpsOMPageReference           *xpsPageRef = NULL;
    // These values are set outside of this code example.
    XPS_SIZE pageSize = {width, height}; 
    
    // Create the package.
    hr = xpsFactory->CreatePackage( &xpsPackage );

    // Create the URI for the fixed document sequence part and then  
    //  create the fixed document sequence
    hr = xpsFactory->CreatePartUri( 
        L"/FixedDocumentSequence.fdseq", &opcPartUri );
    hr = xpsFactory->CreateDocumentSequence( opcPartUri, &xpsFDS );
    // Release this URI to reuse the interface pointer.
    if (NULL != opcPartUri) {opcPartUri->Release(); opcPartUri = NULL;}

    // Create the URI for the document part and then create the document.
    hr = xpsFactory->CreatePartUri( 
        L"/Documents/1/FixedDocument.fdoc", &opcPartUri );
    hr = xpsFactory->CreateDocument( opcPartUri, &xpsFD );
    // Release this URI to reuse the interface pointer.
    if (NULL != opcPartUri) {opcPartUri->Release(); opcPartUri = NULL;}

    // Create a blank page.
    hr = xpsFactory->CreatePartUri( 
        L"/Documents/1/Pages/1.fpage", &opcPartUri );
    hr = xpsFactory->CreatePage(
        &pageSize,                  // Page size
        L"en-US",                   // Page language
        opcPartUri,                 // Page part name
        &xpsPage);                
    // Release this URI to reuse the interface pointer.
    if (NULL != opcPartUri) {opcPartUri->Release(); opcPartUri = NULL;}

    // Create a page reference for the page.
    hr = xpsFactory->CreatePageReference( &pageSize, &xpsPageRef );

    // Add the fixed document sequence to the package.
    hr = xpsPackage->SetDocumentSequence( xpsFDS );

    // Get the document collection of the fixed document sequence
    //  and then add the document to the collection.
    hr = xpsFDS->GetDocuments( &fixedDocuments );
    hr = fixedDocuments->Append( xpsFD );

    // Get the page reference collection from the document
    //  and add the page reference and blank page.
    hr = xpsFD->GetPageReferences( &pageRefs );
    hr = pageRefs->Append( xpsPageRef );
    hr = xpsPageRef->SetPage( xpsPage );

    // Release interface pointer
    if (NULL != xpsPage) xpsPage->Release();
    if (NULL != pageRefs) pageRefs->Release();
    if (NULL != fixedDocuments) fixedDocuments->Release();
    if (NULL != xpsPageRef) xpsPageRef->Release();
    if (NULL != xpsFD) xpsFD->Release();
    if (NULL != xpsFDS) xpsFDS->Release();
    if (NULL != xpsPackage) xpsPackage->Release();

```



## <a name="best-practices"></a><span data-ttu-id="9463a-117">Bonnes pratiques</span><span class="sxs-lookup"><span data-stu-id="9463a-117">Best Practices</span></span>

<span data-ttu-id="9463a-118">Une fois que vous avez utilisé une interface [**IOpcPartUri**](/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi) pour créer un composant (par exemple, après avoir appelé la méthode **createDocument** dans l’exemple de code), libérez le pointeur vers cette interface, sauf si vous en avez besoin pour un autre appel.</span><span class="sxs-lookup"><span data-stu-id="9463a-118">After you have used an [**IOpcPartUri**](/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi) interface to create a component (such as after calling the **CreateDocument** method in the code example), release the pointer to that interface—unless you need it for another call.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9463a-119">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="9463a-119">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="9463a-120">**Next Steps**</span><span class="sxs-lookup"><span data-stu-id="9463a-120">**Next Steps**</span></span>
</dt> <dt>

[<span data-ttu-id="9463a-121">Naviguer dans le modèle d’objet XPS</span><span class="sxs-lookup"><span data-stu-id="9463a-121">Navigate the XPS OM</span></span>](navigate-the-xps-om.md)
</dt> <dt>

[<span data-ttu-id="9463a-122">Écrire du texte dans un modèle d’objet XPS</span><span class="sxs-lookup"><span data-stu-id="9463a-122">Write Text to an XPS OM</span></span>](write-text-to-an-xps-om.md)
</dt> <dt>

[<span data-ttu-id="9463a-123">Dessiner des graphiques dans un modèle d’objet XPS</span><span class="sxs-lookup"><span data-stu-id="9463a-123">Draw Graphics in an XPS OM</span></span>](draw-graphics-in-an-xps-om.md)
</dt> <dt>

[<span data-ttu-id="9463a-124">Placer des images dans un modèle d’objet XPS</span><span class="sxs-lookup"><span data-stu-id="9463a-124">Place Images in an XPS OM</span></span>](place-images-in-an-xps-om.md)
</dt> <dt>

<span data-ttu-id="9463a-125">**Utilisé dans cette page**</span><span class="sxs-lookup"><span data-stu-id="9463a-125">**Used in This Page**</span></span>
</dt> <dt>

[<span data-ttu-id="9463a-126">**IOpcPartUri**</span><span class="sxs-lookup"><span data-stu-id="9463a-126">**IOpcPartUri**</span></span>](/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi)
</dt> <dt>

[<span data-ttu-id="9463a-127">**IXpsOMObjectFactory**</span><span class="sxs-lookup"><span data-stu-id="9463a-127">**IXpsOMObjectFactory**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomobjectfactory)
</dt> <dt>

[<span data-ttu-id="9463a-128">**IXpsOMPackage**</span><span class="sxs-lookup"><span data-stu-id="9463a-128">**IXpsOMPackage**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage)
</dt> <dt>

[<span data-ttu-id="9463a-129">**IXpsOMDocumentSequence**</span><span class="sxs-lookup"><span data-stu-id="9463a-129">**IXpsOMDocumentSequence**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence)
</dt> <dt>

[<span data-ttu-id="9463a-130">**IXpsOMDocumentCollection**</span><span class="sxs-lookup"><span data-stu-id="9463a-130">**IXpsOMDocumentCollection**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentcollection)
</dt> <dt>

[<span data-ttu-id="9463a-131">**IXpsOMDocument**</span><span class="sxs-lookup"><span data-stu-id="9463a-131">**IXpsOMDocument**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocument)
</dt> <dt>

[<span data-ttu-id="9463a-132">**IXpsOMPage**</span><span class="sxs-lookup"><span data-stu-id="9463a-132">**IXpsOMPage**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage)
</dt> <dt>

[<span data-ttu-id="9463a-133">**IXpsOMPageReference**</span><span class="sxs-lookup"><span data-stu-id="9463a-133">**IXpsOMPageReference**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference)
</dt> <dt>

[<span data-ttu-id="9463a-134">**IXpsOMPageReferenceCollection**</span><span class="sxs-lookup"><span data-stu-id="9463a-134">**IXpsOMPageReferenceCollection**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereferencecollection)
</dt> <dt>

[<span data-ttu-id="9463a-135">**\_taille XPS**</span><span class="sxs-lookup"><span data-stu-id="9463a-135">**XPS\_SIZE**</span></span>](/windows/win32/api/xpsobjectmodel/ns-xpsobjectmodel-xps_size)
</dt> <dt>

<span data-ttu-id="9463a-136">**Pour plus d’informations**</span><span class="sxs-lookup"><span data-stu-id="9463a-136">**For More Information**</span></span>
</dt> <dt>

[<span data-ttu-id="9463a-137">Initialiser un modèle d’objet XPS</span><span class="sxs-lookup"><span data-stu-id="9463a-137">Initialize an XPS OM</span></span>](xps-object-model-initialization.md)
</dt> <dt>

[<span data-ttu-id="9463a-138">API d’empaquetage</span><span class="sxs-lookup"><span data-stu-id="9463a-138">Packaging API</span></span>](/previous-versions/windows/desktop/opc/packaging)
</dt> <dt>

[<span data-ttu-id="9463a-139">Informations de référence sur l’API de document XPS</span><span class="sxs-lookup"><span data-stu-id="9463a-139">XPS Document API Reference</span></span>](xps-programming-reference.md)
</dt> <dt>

[<span data-ttu-id="9463a-140">XML Paper Specification</span><span class="sxs-lookup"><span data-stu-id="9463a-140">XML Paper Specification</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
