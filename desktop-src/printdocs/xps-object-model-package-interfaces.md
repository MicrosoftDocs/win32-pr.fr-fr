---
description: Les interfaces de package représentent le niveau supérieur du modèle d’objet XPS, qui correspond à un fichier de document XPS.
ms.assetid: 9e269b18-e5b1-4801-b8e7-473750443c6d
title: Interfaces du package OM XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1465f5d6782e29f9c37f899b59790302e21ebf1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863917"
---
# <a name="xps-om-package-interfaces"></a><span data-ttu-id="19497-103">Interfaces du package OM XPS</span><span class="sxs-lookup"><span data-stu-id="19497-103">XPS OM Package Interfaces</span></span>

<span data-ttu-id="19497-104">Les interfaces de package représentent le niveau supérieur du modèle d’objet XPS, qui correspond à un fichier de document XPS.</span><span class="sxs-lookup"><span data-stu-id="19497-104">The package interfaces represent the top level of the XPS OM, which corresponds to an XPS document file.</span></span> <span data-ttu-id="19497-105">Ces interfaces contiennent des méthodes qui sérialisent un modèle d’objet XPS dans un document ou un flux XPS, et désérialisent un package XPS pour créer un modèle d’objet XPS qui permet à un programme d’accéder au contenu d’un document.</span><span class="sxs-lookup"><span data-stu-id="19497-105">These interfaces contain methods that serialize an XPS OM to an XPS document or stream, and deserialize an XPS package to create an XPS OM that enables a program to access the contents of a document.</span></span>



| <span data-ttu-id="19497-106">Nom de l’interface</span><span class="sxs-lookup"><span data-stu-id="19497-106">Interface name</span></span>                                                  | <span data-ttu-id="19497-107">Interfaces enfants logiques</span><span class="sxs-lookup"><span data-stu-id="19497-107">Logical child interfaces</span></span>                                                                                                            | <span data-ttu-id="19497-108">Description</span><span class="sxs-lookup"><span data-stu-id="19497-108">Description</span></span>                                                                                    |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="19497-109">**IXpsOMPackage**</span><span class="sxs-lookup"><span data-stu-id="19497-109">**IXpsOMPackage**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage)<br/>               | [<span data-ttu-id="19497-110">**IXpsOMDocumentSequence**</span><span class="sxs-lookup"><span data-stu-id="19497-110">**IXpsOMDocumentSequence**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence)<br/> [<span data-ttu-id="19497-111">**IXpsOMCoreProperties**</span><span class="sxs-lookup"><span data-stu-id="19497-111">**IXpsOMCoreProperties**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcoreproperties)<br/> | <span data-ttu-id="19497-112">Modèle d’objet XPS complet qui correspond au package qui contient le document XPS.</span><span class="sxs-lookup"><span data-stu-id="19497-112">The complete XPS OM that corresponds to the package that contains the XPS document.</span></span><br/> |
| [<span data-ttu-id="19497-113">**IXpsOMPackageWriter**</span><span class="sxs-lookup"><span data-stu-id="19497-113">**IXpsOMPackageWriter**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter)<br/>   | <span data-ttu-id="19497-114">Aucun</span><span class="sxs-lookup"><span data-stu-id="19497-114">None</span></span><br/>                                                                                                                     | <span data-ttu-id="19497-115">Active la sérialisation incrémentielle des pages de document dans un package.</span><span class="sxs-lookup"><span data-stu-id="19497-115">Enables incremental serialization of document pages to a package.</span></span><br/>                   |
| [<span data-ttu-id="19497-116">**IXpsOMCoreProperties**</span><span class="sxs-lookup"><span data-stu-id="19497-116">**IXpsOMCoreProperties**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcoreproperties)<br/> | <span data-ttu-id="19497-117">Aucun</span><span class="sxs-lookup"><span data-stu-id="19497-117">None</span></span><br/>                                                                                                                     | <span data-ttu-id="19497-118">Accède aux métadonnées du document.</span><span class="sxs-lookup"><span data-stu-id="19497-118">Accesses the document metadata.</span></span> <br/>                                                    |



 

## <a name="code-examples"></a><span data-ttu-id="19497-119">Exemples de code</span><span class="sxs-lookup"><span data-stu-id="19497-119">Code Examples</span></span>

<span data-ttu-id="19497-120">Les exemples de code qui suivent illustrent la façon dont certaines interfaces de package sont utilisées par un programme.</span><span class="sxs-lookup"><span data-stu-id="19497-120">The code examples that follow illustrate how some of the package interfaces are used by a program.</span></span> <span data-ttu-id="19497-121">Sauf indication contraire, tous les éléments en italique sont des noms de paramètres.</span><span class="sxs-lookup"><span data-stu-id="19497-121">Unless noted otherwise, all italicized items are parameter names.</span></span>

-   [<span data-ttu-id="19497-122">Lire un document XPS dans un modèle d’objet XPS</span><span class="sxs-lookup"><span data-stu-id="19497-122">Read an XPS document into an XPS OM</span></span>](#read-an-xps-document-into-an-xps-om)
-   [<span data-ttu-id="19497-123">Écrire un modèle OM XPS dans un fichier de document XPS</span><span class="sxs-lookup"><span data-stu-id="19497-123">Write an XPS OM to an XPS document file</span></span>](#write-an-xps-om-to-an-xps-document-file)
-   [<span data-ttu-id="19497-124">Accéder à la séquence de documents du modèle d’objet XPS</span><span class="sxs-lookup"><span data-stu-id="19497-124">Access the document sequence of the XPS OM</span></span>](#access-the-document-sequence-of-the-xps-om)
-   [<span data-ttu-id="19497-125">Accéder au CoreProperties du document</span><span class="sxs-lookup"><span data-stu-id="19497-125">Access the document's CoreProperties</span></span>](#access-the-documents-coreproperties)

### <a name="read-an-xps-document-into-an-xps-om"></a><span data-ttu-id="19497-126">Lire un document XPS dans un modèle d’objet XPS</span><span class="sxs-lookup"><span data-stu-id="19497-126">Read an XPS document into an XPS OM</span></span>

<span data-ttu-id="19497-127">À partir d’un document XPS existant dont le nom de fichier est stocké dans *xpsDocumentFilename*, cet exemple de code crée un modèle d’objet XPS référencé par *xpsPackage*.</span><span class="sxs-lookup"><span data-stu-id="19497-127">From an existing XPS document whose file name is stored in *xpsDocumentFilename*, this code example creates an XPS OM that is referenced by *xpsPackage*.</span></span>


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



### <a name="write-an-xps-om-to-an-xps-document-file"></a><span data-ttu-id="19497-128">Écrire un modèle OM XPS dans un fichier de document XPS</span><span class="sxs-lookup"><span data-stu-id="19497-128">Write an XPS OM to an XPS document file</span></span>

<span data-ttu-id="19497-129">L’exemple de code suivant écrit le modèle d’objet XPS qui est référencé par *xpsPackage*.</span><span class="sxs-lookup"><span data-stu-id="19497-129">The following code example writes the XPS OM that is referenced by *xpsPackage*.</span></span> <span data-ttu-id="19497-130">L’exemple crée un document XPS dans le fichier dont le nom est stocké dans *filename*.</span><span class="sxs-lookup"><span data-stu-id="19497-130">The example creates an XPS document in the file whose name is stored in *fileName*.</span></span>


```C++
    HRESULT hr = S_OK;

    hr = xpsPackage->WriteToFile(
        xpsDocumentFilename,
        NULL,                    // LPSECURITY_ATTRIBUTES
        FILE_ATTRIBUTE_NORMAL,
        FALSE);                  // optimizeMarkupSize
```



### <a name="access-the-document-sequence-of-the-xps-om"></a><span data-ttu-id="19497-131">Accéder à la séquence de documents du modèle d’objet XPS</span><span class="sxs-lookup"><span data-stu-id="19497-131">Access the document sequence of the XPS OM</span></span>

<span data-ttu-id="19497-132">L’exemple de code suivant obtient un pointeur vers l’interface [**IXpsOMDocumentSequence**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence) , qui contient la séquence de documents du modèle d’objet XPS qui est représenté par *xpsPackage*.</span><span class="sxs-lookup"><span data-stu-id="19497-132">The following code example obtains a pointer to the [**IXpsOMDocumentSequence**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence) interface, which contains the document sequence of the XPS OM that is represented by *xpsPackage*.</span></span>


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



### <a name="access-the-documents-coreproperties"></a><span data-ttu-id="19497-133">Accéder au CoreProperties du document</span><span class="sxs-lookup"><span data-stu-id="19497-133">Access the document's CoreProperties</span></span>

<span data-ttu-id="19497-134">L’exemple de code suivant obtient un pointeur vers l’interface [**IXpsOMCoreProperties**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcoreproperties) , ce qui permet au programme d’accéder au contenu de la partie CoreProperties.</span><span class="sxs-lookup"><span data-stu-id="19497-134">The following is code example obtains a pointer to the [**IXpsOMCoreProperties**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcoreproperties) interface, allowing the program to access the contents of the CoreProperties part.</span></span> <span data-ttu-id="19497-135">Dans l’exemple, le document est supposé avoir été lu dans un modèle d’objet XPS qui est représenté par *xpsPackage*.</span><span class="sxs-lookup"><span data-stu-id="19497-135">In the example, the document is assumed to have been read into an XPS OM that is represented by *xpsPackage*.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="19497-136">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="19497-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="19497-137">Utilisation de l’interface IXpsOMPackageWriter</span><span class="sxs-lookup"><span data-stu-id="19497-137">Using the IXpsOMPackageWriter Interface</span></span>](using-the-ixpsompackagewriter-interface.md)
</dt> <dt>

[<span data-ttu-id="19497-138">Naviguer dans le modèle d’objet XPS</span><span class="sxs-lookup"><span data-stu-id="19497-138">Navigate the XPS OM</span></span>](navigate-the-xps-om.md)
</dt> <dt>

[<span data-ttu-id="19497-139">**Interface IXpsOMDocumentSequence**</span><span class="sxs-lookup"><span data-stu-id="19497-139">**IXpsOMDocumentSequence Interface**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence)
</dt> <dt>

[<span data-ttu-id="19497-140">**Interface IXpsOMPackage**</span><span class="sxs-lookup"><span data-stu-id="19497-140">**IXpsOMPackage Interface**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage)
</dt> <dt>

[<span data-ttu-id="19497-141">**Interface IXpsOMPackageWriter**</span><span class="sxs-lookup"><span data-stu-id="19497-141">**IXpsOMPackageWriter Interface**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter)
</dt> <dt>

[<span data-ttu-id="19497-142">**Interface IXpsOMCoreProperties**</span><span class="sxs-lookup"><span data-stu-id="19497-142">**IXpsOMCoreProperties Interface**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcoreproperties)
</dt> </dl>

 

 




