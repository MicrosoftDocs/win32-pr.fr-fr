---
description: Décrit comment lire un document XPS existant à partir d’un fichier dans un modèle d’objet XPS.
ms.assetid: 92a8d19f-1c9e-4e02-a3d4-f2869ec871df
title: Lire un document XPS dans un modèle d’objet XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5c3b703de24be58db875618b575cebf9c1c0b27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320265"
---
# <a name="read-an-xps-document-into-an-xps-om"></a><span data-ttu-id="a136f-103">Lire un document XPS dans un modèle d’objet XPS</span><span class="sxs-lookup"><span data-stu-id="a136f-103">Read an XPS Document into an XPS OM</span></span>

<span data-ttu-id="a136f-104">Décrit comment lire un document XPS existant à partir d’un fichier dans un modèle d’objet XPS.</span><span class="sxs-lookup"><span data-stu-id="a136f-104">Describes how to read an existing XPS document from a file into an XPS OM.</span></span>

<span data-ttu-id="a136f-105">Pour créer un modèle d’objet XPS à partir d’un document XPS, appelez la méthode [**IXpsOMObjectFactory :: CreatePackageFromFile**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createpackagefromfile) .</span><span class="sxs-lookup"><span data-stu-id="a136f-105">To create an XPS OM from an XPS document, call the [**IXpsOMObjectFactory::CreatePackageFromFile**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createpackagefromfile) method.</span></span>

<span data-ttu-id="a136f-106">Avant d’utiliser ces exemples de code dans votre programme, lisez l’exclusion de responsabilité dans les [tâches de programmation de document XPS courantes](common-xps-document-tasks.md).</span><span class="sxs-lookup"><span data-stu-id="a136f-106">Before using these code examples in your program, read the disclaimer in [Common XPS Document Programming Tasks](common-xps-document-tasks.md).</span></span>

## <a name="code-example"></a><span data-ttu-id="a136f-107">Exemple de code</span><span class="sxs-lookup"><span data-stu-id="a136f-107">Code Example</span></span>

<span data-ttu-id="a136f-108">L’exemple de code suivant suppose que l’initialisation décrite dans [initialiser un modèle d’objet XPS](xps-object-model-initialization.md) a réussi.</span><span class="sxs-lookup"><span data-stu-id="a136f-108">The following code example assumes that the initialization described in [Initialize an XPS OM](xps-object-model-initialization.md) has succeeded.</span></span>


```C++
    IXpsOMPackage *package = NULL;

    hr = xpsFactory->CreatePackageFromFile(
        xpsDocumentFilename,
        FALSE,
        &package);

    // package now contains a pointer to the IXpsOMPackage
    // object that has been populated with the contents
    // of the XPS document in xpsDocumentFilename.

    // When finished with the package, release the object.
    if (NULL != package) package->Release();
```



<span data-ttu-id="a136f-109">Pour créer un modèle d’objet XPS à partir d’un document XPS stocké sous forme de flux, appelez [**IXpsOMObjectFactory :: CreatePackageFromStream**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createpackagefromstream).</span><span class="sxs-lookup"><span data-stu-id="a136f-109">To create an XPS OM from an XPS document that is stored as a stream, call [**IXpsOMObjectFactory::CreatePackageFromStream**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createpackagefromstream).</span></span>

## <a name="remarks"></a><span data-ttu-id="a136f-110">Notes</span><span class="sxs-lookup"><span data-stu-id="a136f-110">Remarks</span></span>

<span data-ttu-id="a136f-111">Si vous écrivez un modèle d’objet XPS immédiatement après y avoir lu un package XPS, une partie du contenu d’origine peut être perdue ou modifiée.</span><span class="sxs-lookup"><span data-stu-id="a136f-111">If you write an XPS OM immediately after you have read an XPS package into it, some of the original content might be lost or changed.</span></span>

<span data-ttu-id="a136f-112">Certaines des modifications qui peuvent se produire dans ce cas sont répertoriées dans le tableau suivant :</span><span class="sxs-lookup"><span data-stu-id="a136f-112">Some of the changes that can occur in such case are listed in the table that follows:</span></span>

| <span data-ttu-id="a136f-113">Fonctionnalité de document</span><span class="sxs-lookup"><span data-stu-id="a136f-113">Document feature</span></span>                      | <span data-ttu-id="a136f-114">Action</span><span class="sxs-lookup"><span data-stu-id="a136f-114">Action</span></span>                                                             |
|---------------------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="a136f-115">Signatures numériques</span><span class="sxs-lookup"><span data-stu-id="a136f-115">Digital signatures</span></span><br/>         | <span data-ttu-id="a136f-116">Supprimé du document</span><span class="sxs-lookup"><span data-stu-id="a136f-116">Removed from the document</span></span><br/>                               |
| <span data-ttu-id="a136f-117">Partie DiscardControl</span><span class="sxs-lookup"><span data-stu-id="a136f-117">DiscardControl part</span></span><br/>        | <span data-ttu-id="a136f-118">Supprimé du document</span><span class="sxs-lookup"><span data-stu-id="a136f-118">Removed from the document</span></span><br/>                               |
| <span data-ttu-id="a136f-119">Parties de documents étrangers</span><span class="sxs-lookup"><span data-stu-id="a136f-119">Foreign document parts</span></span><br/>     | <span data-ttu-id="a136f-120">Supprimé du document</span><span class="sxs-lookup"><span data-stu-id="a136f-120">Removed from the document</span></span><br/>                               |
| <span data-ttu-id="a136f-121">FixedPage, balisage</span><span class="sxs-lookup"><span data-stu-id="a136f-121">FixedPage markup</span></span><br/>           | <span data-ttu-id="a136f-122">Modifié à partir de l’original</span><span class="sxs-lookup"><span data-stu-id="a136f-122">Modified from the original</span></span><br/>                              |
| <span data-ttu-id="a136f-123">Balisage du dictionnaire de ressources</span><span class="sxs-lookup"><span data-stu-id="a136f-123">Resource dictionary markup</span></span><br/> | <span data-ttu-id="a136f-124">Modifié à partir de l’original, si l’indicateur d’optimisation est défini</span><span class="sxs-lookup"><span data-stu-id="a136f-124">Modified from the original, if Optimization flag is set</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="a136f-125">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a136f-125">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="a136f-126">**Next Steps**</span><span class="sxs-lookup"><span data-stu-id="a136f-126">**Next Steps**</span></span>
</dt> <dt>

[<span data-ttu-id="a136f-127">Naviguer dans le modèle d’objet XPS</span><span class="sxs-lookup"><span data-stu-id="a136f-127">Navigate the XPS OM</span></span>](navigate-the-xps-om.md)
</dt> <dt>

[<span data-ttu-id="a136f-128">Écrire du texte dans un modèle d’objet XPS</span><span class="sxs-lookup"><span data-stu-id="a136f-128">Write Text to an XPS OM</span></span>](write-text-to-an-xps-om.md)
</dt> <dt>

[<span data-ttu-id="a136f-129">Dessiner des graphiques dans un modèle d’objet XPS</span><span class="sxs-lookup"><span data-stu-id="a136f-129">Draw Graphics in an XPS OM</span></span>](draw-graphics-in-an-xps-om.md)
</dt> <dt>

[<span data-ttu-id="a136f-130">Placer des images dans un modèle d’objet XPS</span><span class="sxs-lookup"><span data-stu-id="a136f-130">Place Images in an XPS OM</span></span>](place-images-in-an-xps-om.md)
</dt> <dt>

<span data-ttu-id="a136f-131">**Utilisé dans cette section**</span><span class="sxs-lookup"><span data-stu-id="a136f-131">**Used in This Section**</span></span>
</dt> <dt>

[<span data-ttu-id="a136f-132">**IXpsOMObjectFactory**</span><span class="sxs-lookup"><span data-stu-id="a136f-132">**IXpsOMObjectFactory**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomobjectfactory)
</dt> <dt>

[<span data-ttu-id="a136f-133">**IXpsOMPackage**</span><span class="sxs-lookup"><span data-stu-id="a136f-133">**IXpsOMPackage**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage)
</dt> <dt>

<span data-ttu-id="a136f-134">**Pour plus d’informations**</span><span class="sxs-lookup"><span data-stu-id="a136f-134">**For More Information**</span></span>
</dt> <dt>

[<span data-ttu-id="a136f-135">Initialiser un modèle d’objet XPS</span><span class="sxs-lookup"><span data-stu-id="a136f-135">Initialize an XPS OM</span></span>](xps-object-model-initialization.md)
</dt> <dt>

[<span data-ttu-id="a136f-136">API d’empaquetage</span><span class="sxs-lookup"><span data-stu-id="a136f-136">Packaging API</span></span>](/previous-versions/windows/desktop/opc/packaging)
</dt> <dt>

[<span data-ttu-id="a136f-137">Informations de référence sur l’API de document XPS</span><span class="sxs-lookup"><span data-stu-id="a136f-137">XPS Document API Reference</span></span>](xps-programming-reference.md)
</dt> <dt>

[<span data-ttu-id="a136f-138">XML Paper Specification</span><span class="sxs-lookup"><span data-stu-id="a136f-138">XML Paper Specification</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

