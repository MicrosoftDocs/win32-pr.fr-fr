---
description: Cette rubrique explique comment utiliser les interfaces qui fournissent l’accès à FixedDocumentSequence, qui est le niveau supérieur de la hiérarchie de documents dans un modèle d’objet XPS.
ms.assetid: e7d01f21-0b5d-4385-89e8-14021800e234
title: Utilisation des interfaces IXpsOMDocumentSequence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f108cbadf735b334f758102915abbda239a4e974
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106528166"
---
# <a name="working-with-ixpsomdocumentsequence-interfaces"></a><span data-ttu-id="2ad2d-103">Utilisation des interfaces IXpsOMDocumentSequence</span><span class="sxs-lookup"><span data-stu-id="2ad2d-103">Working with IXpsOMDocumentSequence Interfaces</span></span>

<span data-ttu-id="2ad2d-104">Cette rubrique explique comment utiliser les interfaces qui fournissent l’accès à FixedDocumentSequence, qui est le niveau supérieur de la hiérarchie de documents dans un modèle d’objet XPS.</span><span class="sxs-lookup"><span data-stu-id="2ad2d-104">This topic describes how to use the interfaces that provide access to the FixedDocumentSequence, which is the top level of the document hierarchy in an XPS OM.</span></span>



| <span data-ttu-id="2ad2d-105">Nom de l’interface</span><span class="sxs-lookup"><span data-stu-id="2ad2d-105">Interface name</span></span>                                                          | <span data-ttu-id="2ad2d-106">Interfaces enfants logiques</span><span class="sxs-lookup"><span data-stu-id="2ad2d-106">Logical child interfaces</span></span>                            | <span data-ttu-id="2ad2d-107">Description</span><span class="sxs-lookup"><span data-stu-id="2ad2d-107">Description</span></span>                                                              |
|-------------------------------------------------------------------------|-----------------------------------------------------|--------------------------------------------------------------------------|
| [<span data-ttu-id="2ad2d-108">**IXpsOMDocumentSequence**</span><span class="sxs-lookup"><span data-stu-id="2ad2d-108">**IXpsOMDocumentSequence**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence)<br/>     | [<span data-ttu-id="2ad2d-109">**IXpsOMDocument**</span><span class="sxs-lookup"><span data-stu-id="2ad2d-109">**IXpsOMDocument**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocument)<br/> | <span data-ttu-id="2ad2d-110">Regroupe un ensemble de FixedDocuments dans une liste ordonnée.</span><span class="sxs-lookup"><span data-stu-id="2ad2d-110">Groups a set of FixedDocuments into an ordered list.</span></span><br/>          |
| [<span data-ttu-id="2ad2d-111">**IXpsOMDocumentCollection**</span><span class="sxs-lookup"><span data-stu-id="2ad2d-111">**IXpsOMDocumentCollection**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentcollection)<br/> | <span data-ttu-id="2ad2d-112">Aucun</span><span class="sxs-lookup"><span data-stu-id="2ad2d-112">None</span></span><br/>                                     | <span data-ttu-id="2ad2d-113">Collection de FixedDocuments dans une séquence de documents XPS.</span><span class="sxs-lookup"><span data-stu-id="2ad2d-113">The collection of FixedDocuments in an XPS document sequence.</span></span><br/> |



 

## <a name="code-example"></a><span data-ttu-id="2ad2d-114">Exemple de code</span><span class="sxs-lookup"><span data-stu-id="2ad2d-114">Code Example</span></span>

<span data-ttu-id="2ad2d-115">L’exemple de code suivant obtient un pointeur vers l’interface [**IXpsOMDocumentSequence**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence) qui contient la séquence de documents du modèle d’objet XPS qui est représenté par *xpsPackage*.</span><span class="sxs-lookup"><span data-stu-id="2ad2d-115">The following code example obtains a pointer to the [**IXpsOMDocumentSequence**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence) interface that contains the document sequence of the XPS OM that is represented by *xpsPackage*.</span></span> <span data-ttu-id="2ad2d-116">L’exemple énumère ensuite les documents dans la collection.</span><span class="sxs-lookup"><span data-stu-id="2ad2d-116">The example then enumerates the documents in the collection.</span></span>


```C++
    HRESULT                         hr = S_OK;

    IXpsOMDocumentSequence          *docSeq;
    IXpsOMDocumentCollection        *docs;
    IXpsOMDocument                  *doc;

    UINT32  numDocs = 0;
    UINT32  thisDoc = 0;

    // get the fixed document sequence of the package
    hr = xpsPackage->GetDocumentSequence(&docSeq);

    // get the collection of fixed documents in 
    //  the fixed document sequence
    hr = docSeq->GetDocuments(&docs);

    // walk the collection of documents;
    hr = docs->GetCount(&numDocs);
    thisDoc = 0;
    while (thisDoc < numDocs) {
        hr = docs->GetAt(thisDoc, &doc);
 
        // use this doc for something

        // release this doc and then go to the next one
        doc->Release();
        thisDoc++;
    }
    // release the document collection and
    // the document sequence
    docs->Release();
    docSeq->Release();
```



 

 




