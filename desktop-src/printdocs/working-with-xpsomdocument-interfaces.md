---
description: Cette rubrique décrit les interfaces qui fournissent l’accès aux composants au niveau du document d’un modèle d’objet XPS.
ms.assetid: 96b92480-cc28-4a57-a184-c52d3ddc9b05
title: Utilisation des interfaces IXpsOMDocument
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad7e8c0908382a731532f2697f03c8d67cb732ddf902f0c1ea181fe221d075fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119033757"
---
# <a name="working-with-ixpsomdocument-interfaces"></a>Utilisation des interfaces IXpsOMDocument

Cette rubrique décrit les interfaces qui fournissent l’accès aux composants au niveau du document d’un modèle d’objet XPS.



| Nom de l’interface                                                                        | Interfaces enfants logiques                                      | Description                                                                                                                                                                                                                                                                                                                 |
|---------------------------------------------------------------------------------------|---------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IXpsOMDocument**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocument)<br/>                                   | [**IXpsOMPageReference**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference)<br/> | Représente un seul composant FixedDocument et lie une collection de références de page.<br/> [**IXpsOMPageReferenceCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereferencecollection) est l’interface de collection qui est utilisée pour itérer au sein des interfaces [**IXpsOMPageReference**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference) dans un document.<br/> |
| [**IXpsOMDocumentStructureResource**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentstructureresource)<br/> | Aucun<br/>                                               | Représente la partie DocumentStructure.<br/>                                                                                                                                                                                                                                                                           |



 

## <a name="code-examples"></a>Exemples de code

Les exemples de code de cette section illustrent l’utilisation de certaines des interfaces de document dans un programme.

### <a name="get-the-page-references-of-a-document"></a>Obtenir les références de page d’un document

L’exemple de code suivant obtient un pointeur vers le [**IXpsOMPageReferenceCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereferencecollection) qui contient la liste des interfaces [**IXpsOMPageReference**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference) pour le document qui est référencé par le paramètre *doc* .


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



### <a name="get-the-document-structure-of-a-document"></a>Obtenir la structure d’un document

L’exemple de code suivant obtient la ressource qui contient la structure du document.


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



 

 




