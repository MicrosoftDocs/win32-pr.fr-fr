---
description: Cette rubrique explique comment utiliser les interfaces qui fournissent l’accès à FixedDocumentSequence, qui est le niveau supérieur de la hiérarchie de documents dans un modèle d’objet XPS.
ms.assetid: e7d01f21-0b5d-4385-89e8-14021800e234
title: Utilisation des interfaces IXpsOMDocumentSequence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: edac74809de63c1ae4e688bb99214d11b091ee4e877c921e9280abc9c6868121
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119098661"
---
# <a name="working-with-ixpsomdocumentsequence-interfaces"></a>Utilisation des interfaces IXpsOMDocumentSequence

Cette rubrique explique comment utiliser les interfaces qui fournissent l’accès à FixedDocumentSequence, qui est le niveau supérieur de la hiérarchie de documents dans un modèle d’objet XPS.



| Nom de l’interface                                                          | Interfaces enfants logiques                            | Description                                                              |
|-------------------------------------------------------------------------|-----------------------------------------------------|--------------------------------------------------------------------------|
| [**IXpsOMDocumentSequence**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence)<br/>     | [**IXpsOMDocument**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocument)<br/> | Regroupe un ensemble de FixedDocuments dans une liste ordonnée.<br/>          |
| [**IXpsOMDocumentCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentcollection)<br/> | Aucun<br/>                                     | Collection de FixedDocuments dans une séquence de documents XPS.<br/> |



 

## <a name="code-example"></a>Exemple de code

L’exemple de code suivant obtient un pointeur vers l’interface [**IXpsOMDocumentSequence**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence) qui contient la séquence de documents du modèle d’objet XPS qui est représenté par *xpsPackage*. L’exemple énumère ensuite les documents dans la collection.


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



 

 




