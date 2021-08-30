---
description: Cette rubrique explique comment créer un modèle OM XPS vide.
ms.assetid: 5b6f12ba-9a41-4252-96c4-391bb8d75cd4
title: Créer un modèle d’objet XPS vide
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78a2d57810a9a8bb500c4d9392b362f4e41e12f7c1a7384c029953a48e77d9a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119950339"
---
# <a name="create-a-blank-xps-om"></a>Créer un modèle d’objet XPS vide

Cette rubrique explique comment créer un modèle OM XPS vide. Il présente les exemples de code qui illustrent l’utilisation d’un modèle d’objet XPS pour créer la structure de document d’un document XPS qui comporte une page vierge.

Pour être enregistré en tant que document XPS, le modèle d’objet XPS requiert au moins les composants suivants :

-   [**IXpsOMPackage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage) décrivant le package de documents XPS
-   [**IXpsOMDocumentSequence**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence) qui contient le Framework du contenu du package
-   [**IXpsOMDocument**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocument) qui contient l’infrastructure d’un document dans le package
-   [**IXpsOMPageReference**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference) qui contient la collection de pages dans le document
-   [**IXpsOMPage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage) qui contient une page vierge

Lorsque ces interfaces sont utilisées, le modèle d’objet XPS contient un document qui contient une page vierge. Pour créer ce document dans un modèle d’objet XPS, le programme doit d’abord créer les composants individuels, puis les lier ensemble.

Avant d’utiliser les exemples de code suivants, lisez l’exclusion de responsabilité dans les [tâches de programmation de document XPS courantes](common-xps-document-tasks.md).

## <a name="code-examples"></a>Exemples de code

L’exemple de code suivant suppose que l’initialisation, décrite dans [initialiser un modèle d’objet XPS](xps-object-model-initialization.md), a réussi.


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



## <a name="best-practices"></a>Meilleures pratiques

Une fois que vous avez utilisé une interface [**IOpcPartUri**](/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi) pour créer un composant (par exemple, après avoir appelé la méthode **createDocument** dans l’exemple de code), libérez le pointeur vers cette interface, sauf si vous en avez besoin pour un autre appel.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**Next Steps**
</dt> <dt>

[Naviguer dans le modèle d’objet XPS](navigate-the-xps-om.md)
</dt> <dt>

[Écrire du texte dans un modèle d’objet XPS](write-text-to-an-xps-om.md)
</dt> <dt>

[Dessiner des graphiques dans un modèle d’objet XPS](draw-graphics-in-an-xps-om.md)
</dt> <dt>

[Placer des images dans un modèle d’objet XPS](place-images-in-an-xps-om.md)
</dt> <dt>

**Utilisé dans cette page**
</dt> <dt>

[**IOpcPartUri**](/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi)
</dt> <dt>

[**IXpsOMObjectFactory**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomobjectfactory)
</dt> <dt>

[**IXpsOMPackage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage)
</dt> <dt>

[**IXpsOMDocumentSequence**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence)
</dt> <dt>

[**IXpsOMDocumentCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentcollection)
</dt> <dt>

[**IXpsOMDocument**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocument)
</dt> <dt>

[**IXpsOMPage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage)
</dt> <dt>

[**IXpsOMPageReference**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference)
</dt> <dt>

[**IXpsOMPageReferenceCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereferencecollection)
</dt> <dt>

[**\_taille XPS**](/windows/win32/api/xpsobjectmodel/ns-xpsobjectmodel-xps_size)
</dt> <dt>

**Pour plus d’informations**
</dt> <dt>

[Initialiser un modèle d’objet XPS](xps-object-model-initialization.md)
</dt> <dt>

[API d’empaquetage](/previous-versions/windows/desktop/opc/packaging)
</dt> <dt>

[Informations de référence sur l’API de document XPS](xps-programming-reference.md)
</dt> <dt>

[XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
