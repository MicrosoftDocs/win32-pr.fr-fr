---
description: Les interfaces de package représentent le niveau supérieur du modèle d’objet XPS, qui correspond à un fichier de document XPS.
ms.assetid: 9e269b18-e5b1-4801-b8e7-473750443c6d
title: Interfaces du package OM XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1465f5d6782e29f9c37f899b59790302e21ebf1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127117970"
---
# <a name="xps-om-package-interfaces"></a>Interfaces du package OM XPS

Les interfaces de package représentent le niveau supérieur du modèle d’objet XPS, qui correspond à un fichier de document XPS. Ces interfaces contiennent des méthodes qui sérialisent un modèle d’objet XPS dans un document ou un flux XPS, et désérialisent un package XPS pour créer un modèle d’objet XPS qui permet à un programme d’accéder au contenu d’un document.



| Nom de l’interface                                                  | Interfaces enfants logiques                                                                                                            | Description                                                                                    |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [**IXpsOMPackage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage)<br/>               | [**IXpsOMDocumentSequence**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence)<br/> [**IXpsOMCoreProperties**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcoreproperties)<br/> | Modèle d’objet XPS complet qui correspond au package qui contient le document XPS.<br/> |
| [**IXpsOMPackageWriter**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter)<br/>   | None<br/>                                                                                                                     | Active la sérialisation incrémentielle des pages de document dans un package.<br/>                   |
| [**IXpsOMCoreProperties**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcoreproperties)<br/> | None<br/>                                                                                                                     | Accède aux métadonnées du document. <br/>                                                    |



 

## <a name="code-examples"></a>Exemples de code

Les exemples de code qui suivent illustrent la façon dont certaines interfaces de package sont utilisées par un programme. Sauf indication contraire, tous les éléments en italique sont des noms de paramètres.

-   [Lire un document XPS dans un modèle d’objet XPS](#read-an-xps-document-into-an-xps-om)
-   [Écrire un modèle OM XPS dans un fichier de document XPS](#write-an-xps-om-to-an-xps-document-file)
-   [Accéder à la séquence de documents du modèle d’objet XPS](#access-the-document-sequence-of-the-xps-om)
-   [Accéder au CoreProperties du document](#access-the-documents-coreproperties)

### <a name="read-an-xps-document-into-an-xps-om"></a>Lire un document XPS dans un modèle d’objet XPS

À partir d’un document XPS existant dont le nom de fichier est stocké dans *xpsDocumentFilename*, cet exemple de code crée un modèle d’objet XPS référencé par *xpsPackage*.


```C++
    HRESULT                 hr = S_OK;
    IXpsOMPackage           *xpsPackage;

    hr = xpsFactory->CreatePackageFromFile(
        xpsDocumentFilename,
        FALSE,
        &xpsPackage);

    // xpsPackage now contains a pointer to the IXpsOMPackage
    // object that has been populated with the contents
    // of the XPS document in xpsDocumentFilename.
```



### <a name="write-an-xps-om-to-an-xps-document-file"></a>Écrire un modèle OM XPS dans un fichier de document XPS

L’exemple de code suivant écrit le modèle d’objet XPS qui est référencé par *xpsPackage*. L’exemple crée un document XPS dans le fichier dont le nom est stocké dans *filename*.


```C++
    HRESULT hr = S_OK;

    hr = xpsPackage->WriteToFile(
        xpsDocumentFilename,
        NULL,                    // LPSECURITY_ATTRIBUTES
        FILE_ATTRIBUTE_NORMAL,
        FALSE);                  // optimizeMarkupSize
```



### <a name="access-the-document-sequence-of-the-xps-om"></a>Accéder à la séquence de documents du modèle d’objet XPS

L’exemple de code suivant obtient un pointeur vers l’interface [**IXpsOMDocumentSequence**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence) , qui contient la séquence de documents du modèle d’objet XPS qui est représenté par *xpsPackage*.


```C++
    HRESULT                         hr = S_OK;
    IXpsOMDocumentSequence          *docSeq;
    IXpsOMDocumentCollection        *docs;

    // get the fixed document sequence of the package
    hr = xpsPackage->GetDocumentSequence(&docSeq);

    // get the collection of fixed documents in 
    //  the fixed document sequence
    hr = docSeq->GetDocuments(&docs);
```



### <a name="access-the-documents-coreproperties"></a>Accéder au CoreProperties du document

L’exemple de code suivant obtient un pointeur vers l’interface [**IXpsOMCoreProperties**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcoreproperties) , ce qui permet au programme d’accéder au contenu de la partie CoreProperties. Dans l’exemple, le document est supposé avoir été lu dans un modèle d’objet XPS qui est représenté par *xpsPackage*.


```C++
    HRESULT                         hr = S_OK;
    IXpsOMCoreProperties            *coreProps;
    LPWSTR                          title;

    // get the fixed document sequence of the package
    hr = xpsPackage->GetCoreProperties(&coreProps);

    // get the title property 
    hr = coreProps->GetTitle(&title);

    // do something with the title property here...

    // free the string when finished with it
    CoTaskMemFree ( title );
    coreProps->Release();
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation de l’interface IXpsOMPackageWriter](using-the-ixpsompackagewriter-interface.md)
</dt> <dt>

[Naviguer dans le modèle d’objet XPS](navigate-the-xps-om.md)
</dt> <dt>

[**Interface IXpsOMDocumentSequence**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence)
</dt> <dt>

[**Interface IXpsOMPackage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage)
</dt> <dt>

[**Interface IXpsOMPackageWriter**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter)
</dt> <dt>

[**Interface IXpsOMCoreProperties**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcoreproperties)
</dt> </dl>

 

 




