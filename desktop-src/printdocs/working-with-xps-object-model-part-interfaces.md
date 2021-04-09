---
description: Cette rubrique explique comment utiliser les interfaces qui fournissent l’accès aux parties de document XPS dans un modèle d’objet XPS.
ms.assetid: c52f7044-890d-47d1-83f8-bae1f8d83139
title: Interfaces du composant XPS OM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d81cbf17c26e4ba6c80199ee787b1ee11b28d260
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951870"
---
# <a name="xps-om-part-interfaces"></a><span data-ttu-id="58cde-103">Interfaces du composant XPS OM</span><span class="sxs-lookup"><span data-stu-id="58cde-103">XPS OM Part Interfaces</span></span>

<span data-ttu-id="58cde-104">Cette rubrique explique comment utiliser les interfaces qui fournissent l’accès aux parties de document XPS dans un modèle d’objet XPS.</span><span class="sxs-lookup"><span data-stu-id="58cde-104">This topic describes how to use the interfaces that provide access to XPS document parts in an XPS OM.</span></span>



| <span data-ttu-id="58cde-105">Nom de l’interface</span><span class="sxs-lookup"><span data-stu-id="58cde-105">Interface name</span></span>                                                                                                    | <span data-ttu-id="58cde-106">Interfaces enfants logiques</span><span class="sxs-lookup"><span data-stu-id="58cde-106">Logical child interfaces</span></span>                                                                                                                                                                                                                                                                                     | <span data-ttu-id="58cde-107">Description</span><span class="sxs-lookup"><span data-stu-id="58cde-107">Description</span></span>                                                                                                  |
|-------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="58cde-108">**IXpsOMPart**</span><span class="sxs-lookup"><span data-stu-id="58cde-108">**IXpsOMPart**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompart)<br/>                                                                       | [<span data-ttu-id="58cde-109">**IXpsOMDocumentSequence**</span><span class="sxs-lookup"><span data-stu-id="58cde-109">**IXpsOMDocumentSequence**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence)<br/> [<span data-ttu-id="58cde-110">**IXpsOMDocument**</span><span class="sxs-lookup"><span data-stu-id="58cde-110">**IXpsOMDocument**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocument)<br/> [<span data-ttu-id="58cde-111">**IXpsOMPageReference**</span><span class="sxs-lookup"><span data-stu-id="58cde-111">**IXpsOMPageReference**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference)<br/> [<span data-ttu-id="58cde-112">**IXpsOMCoreProperties**</span><span class="sxs-lookup"><span data-stu-id="58cde-112">**IXpsOMCoreProperties**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcoreproperties)<br/> [<span data-ttu-id="58cde-113">**IXpsOMResource**</span><span class="sxs-lookup"><span data-stu-id="58cde-113">**IXpsOMResource**</span></span>](/windows/win32/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomresource)<br/>    | <span data-ttu-id="58cde-114">Documentez les composants qui composent la structure du document.</span><span class="sxs-lookup"><span data-stu-id="58cde-114">Document components that make up the document structure.</span></span><br/>                                          |
| [<span data-ttu-id="58cde-115">**IXpsOMResource**</span><span class="sxs-lookup"><span data-stu-id="58cde-115">**IXpsOMResource**</span></span>](/windows/win32/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomresource)<br/> [<span data-ttu-id="58cde-116">**IXpsOMPartResources**</span><span class="sxs-lookup"><span data-stu-id="58cde-116">**IXpsOMPartResources**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompartresources)<br/> | <span data-ttu-id="58cde-117">IXpsOMFontResource</span><span class="sxs-lookup"><span data-stu-id="58cde-117">IXpsOMFontResource</span></span><br/> <span data-ttu-id="58cde-118">IXpsOMImageResource</span><span class="sxs-lookup"><span data-stu-id="58cde-118">IXpsOMImageResource</span></span><br/> <span data-ttu-id="58cde-119">IXpsOMColorProfileResource</span><span class="sxs-lookup"><span data-stu-id="58cde-119">IXpsOMColorProfileResource</span></span><br/> <span data-ttu-id="58cde-120">IXpsOMPrintTicketResource</span><span class="sxs-lookup"><span data-stu-id="58cde-120">IXpsOMPrintTicketResource</span></span><br/> <span data-ttu-id="58cde-121">IXpsOMRemoteDictionaryResource</span><span class="sxs-lookup"><span data-stu-id="58cde-121">IXpsOMRemoteDictionaryResource</span></span><br/> <span data-ttu-id="58cde-122">IXpsOMDocumentStructureResource</span><span class="sxs-lookup"><span data-stu-id="58cde-122">IXpsOMDocumentStructureResource</span></span><br/> <span data-ttu-id="58cde-123">IXpsOMStoryFragmentsResource</span><span class="sxs-lookup"><span data-stu-id="58cde-123">IXpsOMStoryFragmentsResource</span></span><br/> <span data-ttu-id="58cde-124">IXpsOMSignatureBlockResource</span><span class="sxs-lookup"><span data-stu-id="58cde-124">IXpsOMSignatureBlockResource</span></span><br/> | <span data-ttu-id="58cde-125">Les composants de document qui contiennent des éléments qui sont utilisés dans ou référencés par une page ou un document.</span><span class="sxs-lookup"><span data-stu-id="58cde-125">Document components that contain elements that are used in or referenced by a page or a document.</span></span><br/> |
| [<span data-ttu-id="58cde-126">**IXpsOMPartUriCollection**</span><span class="sxs-lookup"><span data-stu-id="58cde-126">**IXpsOMPartUriCollection**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomparturicollection)<br/>                                             | <span data-ttu-id="58cde-127">Aucun</span><span class="sxs-lookup"><span data-stu-id="58cde-127">None</span></span><br/>                                                                                                                                                                                                                                                                                              | <span data-ttu-id="58cde-128">Collection d’URI de composant.</span><span class="sxs-lookup"><span data-stu-id="58cde-128">A collection of part URIs.</span></span><br/>                                                                        |



 

## <a name="code-examples"></a><span data-ttu-id="58cde-129">Exemples de code</span><span class="sxs-lookup"><span data-stu-id="58cde-129">Code Examples</span></span>

<span data-ttu-id="58cde-130">Les exemples de code suivants montrent deux exemples d’utilisation des interfaces de composant pour accéder au contenu du modèle d’objet XPS.</span><span class="sxs-lookup"><span data-stu-id="58cde-130">The code examples that follow show two examples of how to use the part interfaces to access XPS OM content.</span></span>

### <a name="get-the-name-of-a-document-part"></a><span data-ttu-id="58cde-131">Obtenir le nom d’une partie de document</span><span class="sxs-lookup"><span data-stu-id="58cde-131">Get the name of a document part</span></span>

<span data-ttu-id="58cde-132">L’exemple de code suivant permet d’accéder à une partie de document et d’obtenir le nom de la partie.</span><span class="sxs-lookup"><span data-stu-id="58cde-132">The following code example navigates to a document part and gets the part's name.</span></span>


```C++
    HRESULT                         hr = S_OK;
    
    IXpsOMDocumentSequence          *docSeq;
    IXpsOMDocumentCollection        *docs;
    IXpsOMDocument                  *doc;
    IXpsOMPageReferenceCollection   *pages;
    IXpsOMPageReference             *pageRef;
    IXpsOMPage                      *page;

    IOpcPartUri                     *thisDocPartUri;
    IOpcPartUri                     *thisPagePartUri;

    UINT32  numDocs = 0;
    UINT32  thisDoc = 0;

    UINT32  numPageRefs = 0;
    UINT32  thisPageRef = 0;

    // package points to the IXpsOMPackage interface to walk.

    // get the fixed document sequence of the package
    hr = package->GetDocumentSequence(&docSeq);

    // get the fixed documents in the fixed document sequence
    hr = docSeq->GetDocuments(&docs);

    // walk the collection of documents;
    hr = docs->GetCount(&numDocs);
    thisDoc = 0;
    while (thisDoc < numDocs) {
        hr = docs->GetAt(thisDoc, &doc);
        
        // get the part name (URI) of this document
        hr = doc->GetPartName ( &thisDocPartUri );

        // get the doc contents
        hr = doc->GetPageReferences(&pages);
        
        // walk the collection of page references
        hr = pages->GetCount(&numPageRefs);
        thisPageRef = 0;
        while (thisPageRef < numPageRefs) {
            // get this page reference
            hr = pages->GetAt(thisPageRef, &pageRef );

            // get the part name (URI) of this page
            hr = pageRef->GetPage (&page);
            hr = page->GetPartName ( &thisPagePartUri );

            // do something with the part name
 
            thisPagePartUri->Release();
            page->Release();
            pageRef->Release();

            thisPageRef++;
        }
        pages->Release();
        thisDocPartUri->Release();
        doc->Release();
        thisDoc++;
    }

    docs->Release();
    docSeq->Release();

```



### <a name="get-the-part-resources-that-are-associated-with-this-page"></a><span data-ttu-id="58cde-133">Obtient les ressources de composant associées à cette page</span><span class="sxs-lookup"><span data-stu-id="58cde-133">Get the part resources that are associated with this page</span></span>

<span data-ttu-id="58cde-134">L’exemple de code suivant obtient les listes des différentes ressources utilisées par cette page.</span><span class="sxs-lookup"><span data-stu-id="58cde-134">The following code example gets the lists of the different resources that are used by this page.</span></span>


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

    // use resources

    dictionaryResources->Release();
    imageResources->Release();
    fontResources->Release();
    colorProfileResources->Release();
    resources->Release();
```



 

