---
title: Canevas et interfaces visuels du modèle XPS OM
description: Cette rubrique explique comment utiliser les interfaces de canevas de l’API de document XPS dans un modèle d’objet XPS.
ms.assetid: 368b8c47-9803-42ee-a3a8-681bf55315ad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93a3acc8fbc85298e21d039898d4ae7d38fbb272
ms.sourcegitcommit: 78b64f3865e64768b5319d4f010032ee68924a98
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/13/2021
ms.locfileid: "107314752"
---
# <a name="working-with-xps-om-canvas-and-visual-interfaces"></a><span data-ttu-id="b86f9-103">Utilisation d’une zone de dessin et d’interfaces visuels XPS OM</span><span class="sxs-lookup"><span data-stu-id="b86f9-103">Working with XPS OM Canvas and Visual Interfaces</span></span>

<span data-ttu-id="b86f9-104">Cette rubrique explique comment utiliser les interfaces de canevas de l’API de document XPS dans un modèle d’objet XPS.</span><span class="sxs-lookup"><span data-stu-id="b86f9-104">This topic describes how to use the canvas-related interfaces of the XPS Document API in an XPS OM.</span></span>

| <span data-ttu-id="b86f9-105">Nom de l’interface</span><span class="sxs-lookup"><span data-stu-id="b86f9-105">Interface name</span></span>                                  | <span data-ttu-id="b86f9-106">Interfaces enfants logiques</span><span class="sxs-lookup"><span data-stu-id="b86f9-106">Logical child interfaces</span></span>                                                                                                                    | <span data-ttu-id="b86f9-107">Description</span><span class="sxs-lookup"><span data-stu-id="b86f9-107">Description</span></span>                                                                                                                                                                                                             |
|-------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b86f9-108">**IXpsOMVisual**</span><span class="sxs-lookup"><span data-stu-id="b86f9-108">**IXpsOMVisual**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisual)<br/> | [<span data-ttu-id="b86f9-109">**IXpsOMCanvas**</span><span class="sxs-lookup"><span data-stu-id="b86f9-109">**IXpsOMCanvas**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas)<br/> [<span data-ttu-id="b86f9-110">**IXpsOMGlyphs**</span><span class="sxs-lookup"><span data-stu-id="b86f9-110">**IXpsOMGlyphs**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphs)<br/> [<span data-ttu-id="b86f9-111">**IXpsOMPath**</span><span class="sxs-lookup"><span data-stu-id="b86f9-111">**IXpsOMPath**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompath)<br/> | <span data-ttu-id="b86f9-112">Classe de base des interfaces qui définissent des objets visuels, tels que du texte et des graphiques.</span><span class="sxs-lookup"><span data-stu-id="b86f9-112">The base class of the interfaces that define visual objects, such as text and graphics.</span></span><br/> <span data-ttu-id="b86f9-113">Les objets visuels peuvent être collectés dans une interface [**IXpsOMVisualCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisualcollection) .</span><span class="sxs-lookup"><span data-stu-id="b86f9-113">Visual objects can be collected in an [**IXpsOMVisualCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisualcollection) interface.</span></span><br/> |
| [<span data-ttu-id="b86f9-114">**IXpsOMCanvas**</span><span class="sxs-lookup"><span data-stu-id="b86f9-114">**IXpsOMCanvas**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas)<br/> | [<span data-ttu-id="b86f9-115">**IXpsOMCanvas**</span><span class="sxs-lookup"><span data-stu-id="b86f9-115">**IXpsOMCanvas**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas)<br/> [<span data-ttu-id="b86f9-116">**IXpsOMGlyphs**</span><span class="sxs-lookup"><span data-stu-id="b86f9-116">**IXpsOMGlyphs**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphs)<br/> [<span data-ttu-id="b86f9-117">**IXpsOMPath**</span><span class="sxs-lookup"><span data-stu-id="b86f9-117">**IXpsOMPath**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompath)<br/> | <span data-ttu-id="b86f9-118">Collection d’objets visuels qui peuvent être traités comme un objet visuel unique.</span><span class="sxs-lookup"><span data-stu-id="b86f9-118">A collection of visual objects that can be treated as a single visual object.</span></span><br/>                                                                                                                                |

<span data-ttu-id="b86f9-119">[**IXpsOMVisual**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisual) est l’interface de base ; les objets visibles d’une page héritent de celui-ci.</span><span class="sxs-lookup"><span data-stu-id="b86f9-119">[**IXpsOMVisual**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisual) is the base interface; the visible objects of a page inherit from it.</span></span> <span data-ttu-id="b86f9-120">[**IXpsOMCanvas**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas) hérite de [**IXpsOMVisual**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisual) et permet de regrouper de nombreux autres éléments visuels et d’agir en tant qu’élément visuel unique.</span><span class="sxs-lookup"><span data-stu-id="b86f9-120">[**IXpsOMCanvas**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas) inherits from [**IXpsOMVisual**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisual) and enables many other visual elements to be grouped and acted upon as a single visual element.</span></span> <span data-ttu-id="b86f9-121">Par exemple, vous pouvez utiliser une interface [**IXpsOMCanvas**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas) pour créer une bannière de page contenant une collection de texte et d’éléments graphiques.</span><span class="sxs-lookup"><span data-stu-id="b86f9-121">For example, you could use an [**IXpsOMCanvas**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas) interface to create a page banner that contains a collection of text and graphical elements.</span></span> <span data-ttu-id="b86f9-122">Une telle bannière peut contenir un logo, le slogan de l’entreprise et l’adresse de la société.</span><span class="sxs-lookup"><span data-stu-id="b86f9-122">Such a banner might contain a logo, the company slogan, and the company address.</span></span> <span data-ttu-id="b86f9-123">Vous pouvez placer tous ces éléments dans le [**IXpsOMVisualCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisualcollection) d’une interface [**IXpsOMCanvas**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas) , puis appliquer une transformation unique à l’objet [**IXpsOMCanvas**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas) pour le redimensionner sur une page particulière.</span><span class="sxs-lookup"><span data-stu-id="b86f9-123">You could place all these elements into the [**IXpsOMVisualCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisualcollection) of an [**IXpsOMCanvas**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas) interface, and then apply a single transform to the [**IXpsOMCanvas**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas) object to resize it to a particular page.</span></span> <span data-ttu-id="b86f9-124">C’est plus simple que le calcul et l’application d’une transformation à chaque composant visuel dans la bannière.</span><span class="sxs-lookup"><span data-stu-id="b86f9-124">This is much simpler than computing and applying a transform to each individual visual component in the banner.</span></span>

<span data-ttu-id="b86f9-125">Vous pouvez également utiliser un canevas pour redimensionner le contenu de la page en fonction de la taille de page actuelle.</span><span class="sxs-lookup"><span data-stu-id="b86f9-125">You can also use a canvas to resize the page contents to fit the current page size.</span></span> <span data-ttu-id="b86f9-126">Pour ce faire, placez tout le contenu de la page dans un canevas unique, puis appliquez la transformation appropriée pour ajuster la zone de dessin à la taille de page actuelle.</span><span class="sxs-lookup"><span data-stu-id="b86f9-126">To accomplish this, place all contents of the page into a single canvas, then apply the appropriate transform to fit the canvas to the current page size.</span></span> <span data-ttu-id="b86f9-127">Cela est également bien plus simple que d’essayer de redimensionner chaque élément visuel dans la collection d’éléments visuels de la page.</span><span class="sxs-lookup"><span data-stu-id="b86f9-127">This is also much simpler than trying to resize each visual element in the collection of visuals in the page.</span></span>

## <a name="move-page-contents-to-a-canvas"></a><span data-ttu-id="b86f9-128">Déplacer le contenu d’une page vers une zone de dessin</span><span class="sxs-lookup"><span data-stu-id="b86f9-128">Move page contents to a canvas</span></span>

<span data-ttu-id="b86f9-129">L’exemple de code suivant déplace le contenu d’une page vers un canevas.</span><span class="sxs-lookup"><span data-stu-id="b86f9-129">The following code example moves the contents of a page to a canvas.</span></span>

```C++
    HRESULT                   hr = S_OK;

    IXpsOMVisualCollection    *pageVisuals;
    IXpsOMVisualCollection    *canvasVisuals;
    IXpsOMVisual              *oneVisual;
    IXpsOMCanvas              *newPageCanvas;

    UINT32 numVisuals = 0;
    UINT32 thisVisual;

    // get the page's visual collection
    // and how many objects it contains
    hr = page->GetVisuals( &pageVisuals );
    hr = pageVisuals->GetCount ( &numVisuals );

    // create the new canvas object and
    // its (empty) visual collection
    hr = xpsFactory->CreateCanvas ( &newPageCanvas );
    hr = newPageCanvas->GetVisuals ( &canvasVisuals );

    // go through the page's list of visual objects,
    //  move each one from the page's list to the canvas' list
    //  release the local pointer
    //  remove it from the page's collection
    thisVisual = 0;
    while (thisVisual < numVisuals) {
        hr = pageVisuals->GetAt (0, &oneVisual);
        hr = canvasVisuals->Append (oneVisual);
        hr = pageVisuals->RemoveAt (0);
        thisVisual++;
    }
    // the page's visual collection should be empty
    hr = pageVisuals->GetCount (&numVisuals);
    _ASSERT (0 == numVisuals);

    // add the new canvas to the page's visual collection
    pageVisuals->Append ( newPageCanvas );

```

## <a name="related-topics"></a><span data-ttu-id="b86f9-130">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b86f9-130">Related topics</span></span>

<dl> 
  <span data-ttu-id="b86f9-131">Interface <dt>[**IXpsOMCanvas**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas)</dt>interface
  <dt>[**IXpsOMVisual**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisual)</dt>interface
  <dt>[**IXpsOMVisualCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisualcollection)</dt>
</span><span class="sxs-lookup"><span data-stu-id="b86f9-131"><dt>[**IXpsOMCanvas Interface**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas)</dt>
  <dt>[**IXpsOMVisual Interface**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisual)</dt>
  <dt>[**IXpsOMVisualCollection Interface**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisualcollection)</dt>
</span></span></dl>
