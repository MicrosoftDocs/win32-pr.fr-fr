---
description: Décrit comment écrire le contenu d’un modèle d’objet XPS dans un programme dans un fichier de document XPS.
ms.assetid: 8bee8059-b901-4a99-a7e4-60dad831c239
title: Écrire un modèle OM XPS dans un document XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 811f773394ee9dbbcf77dc75d1429322bb733631
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203706"
---
# <a name="write-an-xps-om-to-an-xps-document"></a><span data-ttu-id="c2623-103">Écrire un modèle OM XPS dans un document XPS</span><span class="sxs-lookup"><span data-stu-id="c2623-103">Write an XPS OM to an XPS Document</span></span>

<span data-ttu-id="c2623-104">Décrit comment écrire le contenu d’un modèle d’objet XPS dans un programme dans un fichier de document XPS.</span><span class="sxs-lookup"><span data-stu-id="c2623-104">Describes how to write the contents of an XPS OM in a program to an XPS document file.</span></span>

<span data-ttu-id="c2623-105">Si un programme possède un modèle d’objet XPS qui contient un document complet, le programme peut écrire le modèle OM XPS dans un fichier en tant que document XPS, en appelant la méthode [**WritetoFile**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackage-writetofile) de l’interface [**IXpsOMPackage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage) .</span><span class="sxs-lookup"><span data-stu-id="c2623-105">If a program has an XPS OM that contains a complete document, the program can write the XPS OM to a file as an XPS document, by calling the [**WriteToFile**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackage-writetofile) method of the [**IXpsOMPackage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage) interface.</span></span>

<span data-ttu-id="c2623-106">Avant d’utiliser ces exemples de code dans un programme, lisez l’exclusion de responsabilité dans les [tâches de programmation de document XPS courantes](common-xps-document-tasks.md).</span><span class="sxs-lookup"><span data-stu-id="c2623-106">Before using these code examples in a program, read the disclaimer in [Common XPS Document Programming Tasks](common-xps-document-tasks.md).</span></span>

## <a name="writing-a-complete-xps-om-to-an-xps-document"></a><span data-ttu-id="c2623-107">Écriture d’un modèle d’objet XPS complet dans un document XPS</span><span class="sxs-lookup"><span data-stu-id="c2623-107">Writing a complete XPS OM to an XPS document</span></span>

<span data-ttu-id="c2623-108">Une fois que vous avez défini le contenu d’un modèle d’objet XPS, vous pouvez enregistrer le modèle d’objet XPS dans un fichier en tant que document XPS, en appelant la méthode [**WritetoFile**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackage-writetofile) de l’interface [**IXpsOMPackage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage) .</span><span class="sxs-lookup"><span data-stu-id="c2623-108">After you set the contents of an XPS OM, you can save the XPS OM to a file as an XPS document, by calling the [**WriteToFile**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackage-writetofile) method of the [**IXpsOMPackage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage) interface.</span></span>


```C++
    HRESULT hr = S_OK;

    hr = xpsPackage->WriteToFile(
        fileName,
        NULL,                    // LPSECURITY_ATTRIBUTES
        FILE_ATTRIBUTE_NORMAL,
        FALSE                    // Optimize Markup Size
        );

```



> [!Note]  
> <span data-ttu-id="c2623-109">L’écriture d’un modèle OM XPS dans un fichier ou un flux ne crée pas automatiquement une miniature pour le document XPS.</span><span class="sxs-lookup"><span data-stu-id="c2623-109">Writing an XPS OM to a file or stream does not automatically create a thumbnail for the XPS document.</span></span> <span data-ttu-id="c2623-110">Pour créer une miniature du document XPS, utilisez l’interface [**IXpsOMThumbnailGenerator**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomthumbnailgenerator) .</span><span class="sxs-lookup"><span data-stu-id="c2623-110">To create a thumbnail of the XPS document, use the [**IXpsOMThumbnailGenerator**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomthumbnailgenerator) interface.</span></span>

 

## <a name="incrementally-writing-an-xps-document"></a><span data-ttu-id="c2623-111">Écriture incrémentielle d’un document XPS</span><span class="sxs-lookup"><span data-stu-id="c2623-111">Incrementally writing an XPS document</span></span>

<span data-ttu-id="c2623-112">L’interface [**IXpsOMPackageWriter**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter) peut être utilisée pour écrire les parties d’un document XPS de manière incrémentielle. par exemple, lorsque les parties du document sont créées ou traitées dans l’ordre.</span><span class="sxs-lookup"><span data-stu-id="c2623-112">The [**IXpsOMPackageWriter**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter) interface can be used to write the parts of an XPS document incrementally; for example, when the document parts are created or processed in sequence.</span></span>

> [!Note]  
> <span data-ttu-id="c2623-113">L’écriture d’un modèle OM XPS dans un fichier ou un flux ne crée pas automatiquement une miniature pour le document XPS.</span><span class="sxs-lookup"><span data-stu-id="c2623-113">Writing an XPS OM to a file or stream does not automatically create a thumbnail for the XPS document.</span></span> <span data-ttu-id="c2623-114">Pour créer une miniature du document XPS, utilisez l’interface [**IXpsOMThumbnailGenerator**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomthumbnailgenerator) .</span><span class="sxs-lookup"><span data-stu-id="c2623-114">To create a thumbnail of the XPS document, use the [**IXpsOMThumbnailGenerator**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomthumbnailgenerator) interface.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="c2623-115">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c2623-115">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="c2623-116">**Next Steps**</span><span class="sxs-lookup"><span data-stu-id="c2623-116">**Next Steps**</span></span>
</dt> <dt>

[<span data-ttu-id="c2623-117">Imprimer un modèle OM XPS</span><span class="sxs-lookup"><span data-stu-id="c2623-117">Print an XPS OM</span></span>](print-an-xps-om.md)
</dt> <dt>

<span data-ttu-id="c2623-118">**Utilisé dans cette section**</span><span class="sxs-lookup"><span data-stu-id="c2623-118">**Used in This Section**</span></span>
</dt> <dt>

[<span data-ttu-id="c2623-119">**IOpcPartUri**</span><span class="sxs-lookup"><span data-stu-id="c2623-119">**IOpcPartUri**</span></span>](/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi)
</dt> <dt>

[<span data-ttu-id="c2623-120">**IXpsOMPackage**</span><span class="sxs-lookup"><span data-stu-id="c2623-120">**IXpsOMPackage**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage)
</dt> <dt>

[<span data-ttu-id="c2623-121">**IXpsOMThumbnailGenerator**</span><span class="sxs-lookup"><span data-stu-id="c2623-121">**IXpsOMThumbnailGenerator**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomthumbnailgenerator)
</dt> <dt>

<span data-ttu-id="c2623-122">**Pour plus d’informations**</span><span class="sxs-lookup"><span data-stu-id="c2623-122">**For More Information**</span></span>
</dt> <dt>

[<span data-ttu-id="c2623-123">Initialiser un modèle d’objet XPS</span><span class="sxs-lookup"><span data-stu-id="c2623-123">Initialize an XPS OM</span></span>](xps-object-model-initialization.md)
</dt> <dt>

[<span data-ttu-id="c2623-124">Informations de référence sur l’API de document XPS</span><span class="sxs-lookup"><span data-stu-id="c2623-124">XPS Document API Reference</span></span>](xps-programming-reference.md)
</dt> <dt>

[<span data-ttu-id="c2623-125">XML Paper Specification</span><span class="sxs-lookup"><span data-stu-id="c2623-125">XML Paper Specification</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
