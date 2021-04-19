---
description: Cette rubrique décrit les interfaces qui fournissent l’accès aux composants au niveau du document d’un modèle d’objet XPS.
ms.assetid: 96b92480-cc28-4a57-a184-c52d3ddc9b05
title: Utilisation des interfaces IXpsOMDocument
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5299452195dc8f14ebd08508c3fd9a6e198781a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106531923"
---
# <a name="working-with-ixpsomdocument-interfaces"></a><span data-ttu-id="5983b-103">Utilisation des interfaces IXpsOMDocument</span><span class="sxs-lookup"><span data-stu-id="5983b-103">Working with IXpsOMDocument Interfaces</span></span>

<span data-ttu-id="5983b-104">Cette rubrique décrit les interfaces qui fournissent l’accès aux composants au niveau du document d’un modèle d’objet XPS.</span><span class="sxs-lookup"><span data-stu-id="5983b-104">This topic describes the interfaces that provide access to the document-level components of an XPS OM.</span></span>



| <span data-ttu-id="5983b-105">Nom de l’interface</span><span class="sxs-lookup"><span data-stu-id="5983b-105">Interface name</span></span>                                                                        | <span data-ttu-id="5983b-106">Interfaces enfants logiques</span><span class="sxs-lookup"><span data-stu-id="5983b-106">Logical child interfaces</span></span>                                      | <span data-ttu-id="5983b-107">Description</span><span class="sxs-lookup"><span data-stu-id="5983b-107">Description</span></span>                                                                                                                                                                                                                                                                                                                 |
|---------------------------------------------------------------------------------------|---------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5983b-108">**IXpsOMDocument**</span><span class="sxs-lookup"><span data-stu-id="5983b-108">**IXpsOMDocument**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocument)<br/>                                   | [<span data-ttu-id="5983b-109">**IXpsOMPageReference**</span><span class="sxs-lookup"><span data-stu-id="5983b-109">**IXpsOMPageReference**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference)<br/> | <span data-ttu-id="5983b-110">Représente un seul composant FixedDocument et lie une collection de références de page.</span><span class="sxs-lookup"><span data-stu-id="5983b-110">Represents a single FixedDocument part and binds a collection of page references.</span></span><br/> <span data-ttu-id="5983b-111">[**IXpsOMPageReferenceCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereferencecollection) est l’interface de collection qui est utilisée pour itérer au sein des interfaces [**IXpsOMPageReference**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference) dans un document.</span><span class="sxs-lookup"><span data-stu-id="5983b-111">[**IXpsOMPageReferenceCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereferencecollection) is the collection interface that is used to iterate through the [**IXpsOMPageReference**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference) interfaces in a document.</span></span><br/> |
| [<span data-ttu-id="5983b-112">**IXpsOMDocumentStructureResource**</span><span class="sxs-lookup"><span data-stu-id="5983b-112">**IXpsOMDocumentStructureResource**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentstructureresource)<br/> | <span data-ttu-id="5983b-113">Aucun</span><span class="sxs-lookup"><span data-stu-id="5983b-113">None</span></span><br/>                                               | <span data-ttu-id="5983b-114">Représente la partie DocumentStructure.</span><span class="sxs-lookup"><span data-stu-id="5983b-114">Represents the DocumentStructure part.</span></span><br/>                                                                                                                                                                                                                                                                           |



 

## <a name="code-examples"></a><span data-ttu-id="5983b-115">Exemples de code</span><span class="sxs-lookup"><span data-stu-id="5983b-115">Code Examples</span></span>

<span data-ttu-id="5983b-116">Les exemples de code de cette section illustrent l’utilisation de certaines des interfaces de document dans un programme.</span><span class="sxs-lookup"><span data-stu-id="5983b-116">The code examples in this section illustrate how some of the document interfaces are used in a program.</span></span>

### <a name="get-the-page-references-of-a-document"></a><span data-ttu-id="5983b-117">Obtenir les références de page d’un document</span><span class="sxs-lookup"><span data-stu-id="5983b-117">Get the page references of a document</span></span>

<span data-ttu-id="5983b-118">L’exemple de code suivant obtient un pointeur vers le [**IXpsOMPageReferenceCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereferencecollection) qui contient la liste des interfaces [**IXpsOMPageReference**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference) pour le document qui est référencé par le paramètre *doc* .</span><span class="sxs-lookup"><span data-stu-id="5983b-118">The following code example gets a pointer to the [**IXpsOMPageReferenceCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereferencecollection) that contains the list of [**IXpsOMPageReference**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference) interfaces for the document that is referenced by *doc* parameter.</span></span>


```C++
    HRESULT                               hr = S_OK;


    IXpsOMPageReferenceCollection         *pages;
    IXpsOMPageReference                   *pageRef;
    IXpsOMPage                            *page;

    UINT32  numPageRefs = 0;
    UINT32  thisPageRef = 0;

    // get the doc contents
    hr = doc->GetPageReferences(&pages);
        
    // walk the collection of page references
    hr = pages->GetCount(&numPageRefs);
    thisPageRef = 0;
    while (thisPageRef < numPageRefs) {
        // get this page reference
        hr = pages->GetAt(thisPageRef, &pageRef);

        // get the page content of this page reference
        hr = pageRef->GetPage (&page);

        // use the page

        // free this page & page reference and go to next
        page->Release();
        pageRef->Release();
        thisPageRef++;
    }

    pages->Release();
```



### <a name="get-the-document-structure-of-a-document"></a><span data-ttu-id="5983b-119">Obtenir la structure d’un document</span><span class="sxs-lookup"><span data-stu-id="5983b-119">Get the document structure of a document</span></span>

<span data-ttu-id="5983b-120">L’exemple de code suivant obtient la ressource qui contient la structure du document.</span><span class="sxs-lookup"><span data-stu-id="5983b-120">The following code example gets the resource that contains the document structure.</span></span>


```C++
    HRESULT                             hr = S_OK;
    
    IXpsOMDocumentStructureResource     *docStruct;
    IStream                             *docStructResStream;

    // doc is passed in as an argument
    // get the doc contents
    hr = doc->GetDocumentStructureResource(&docStruct);
   
    hr = docStruct->GetStream ( &docStructResStream );

    // access the document structure resource 
    //  contents by reading from the stream

    docStructResStream->Release();
    docStruct->Release();

```



 

 




