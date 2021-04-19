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
# <a name="working-with-xps-om-canvas-and-visual-interfaces"></a>Utilisation d’une zone de dessin et d’interfaces visuels XPS OM

Cette rubrique explique comment utiliser les interfaces de canevas de l’API de document XPS dans un modèle d’objet XPS.

| Nom de l’interface                                  | Interfaces enfants logiques                                                                                                                    | Description                                                                                                                                                                                                             |
|-------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IXpsOMVisual**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisual)<br/> | [**IXpsOMCanvas**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas)<br/> [**IXpsOMGlyphs**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphs)<br/> [**IXpsOMPath**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompath)<br/> | Classe de base des interfaces qui définissent des objets visuels, tels que du texte et des graphiques.<br/> Les objets visuels peuvent être collectés dans une interface [**IXpsOMVisualCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisualcollection) .<br/> |
| [**IXpsOMCanvas**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas)<br/> | [**IXpsOMCanvas**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas)<br/> [**IXpsOMGlyphs**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphs)<br/> [**IXpsOMPath**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompath)<br/> | Collection d’objets visuels qui peuvent être traités comme un objet visuel unique.<br/>                                                                                                                                |

[**IXpsOMVisual**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisual) est l’interface de base ; les objets visibles d’une page héritent de celui-ci. [**IXpsOMCanvas**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas) hérite de [**IXpsOMVisual**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisual) et permet de regrouper de nombreux autres éléments visuels et d’agir en tant qu’élément visuel unique. Par exemple, vous pouvez utiliser une interface [**IXpsOMCanvas**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas) pour créer une bannière de page contenant une collection de texte et d’éléments graphiques. Une telle bannière peut contenir un logo, le slogan de l’entreprise et l’adresse de la société. Vous pouvez placer tous ces éléments dans le [**IXpsOMVisualCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisualcollection) d’une interface [**IXpsOMCanvas**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas) , puis appliquer une transformation unique à l’objet [**IXpsOMCanvas**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas) pour le redimensionner sur une page particulière. C’est plus simple que le calcul et l’application d’une transformation à chaque composant visuel dans la bannière.

Vous pouvez également utiliser un canevas pour redimensionner le contenu de la page en fonction de la taille de page actuelle. Pour ce faire, placez tout le contenu de la page dans un canevas unique, puis appliquez la transformation appropriée pour ajuster la zone de dessin à la taille de page actuelle. Cela est également bien plus simple que d’essayer de redimensionner chaque élément visuel dans la collection d’éléments visuels de la page.

## <a name="move-page-contents-to-a-canvas"></a>Déplacer le contenu d’une page vers une zone de dessin

L’exemple de code suivant déplace le contenu d’une page vers un canevas.

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

## <a name="related-topics"></a>Rubriques connexes

<dl> 
  Interface <dt>[**IXpsOMCanvas**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas)</dt>interface
  <dt>[**IXpsOMVisual**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisual)</dt>interface
  <dt>[**IXpsOMVisualCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisualcollection)</dt>
</dl>
