---
description: Cette section décrit comment utiliser les interfaces relatives au chemin d’accès de l’API de document XPS dans un modèle d’objet XPS.
ms.assetid: 4e76355a-ad53-4177-b8c7-3e768a1d4e3f
title: Utilisation des interfaces de chemin d’accès OM XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 136d742db0b176875715b3b715c4401bb8131323ceeb9f8d2a77311fb75a0672
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119460329"
---
# <a name="working-with-xps-om-path-interfaces"></a>Utilisation des interfaces de chemin d’accès OM XPS

Cette section décrit comment utiliser les interfaces relatives au chemin d’accès de l’API de document XPS dans un modèle d’objet XPS.



| Nom de l’interface                                                            | Enfants conceptuels                                                                                                                                                                                                                                                                                                                                                                                                                                         | Description                                                                                                                                                                                       |
|---------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IXpsOMPath**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompath)<br/>                               | Aucun<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                             | Décrit un élément de chemin d’accès graphique.<br/>                                                                                                                                                    |
| [**IXpsOMBrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsombrush)<br/>                             | [**IXpsOMSolidColorBrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomsolidcolorbrush)<br/> [**IXpsOMTileBrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomtilebrush)<br/> [**IXpsOMVisualBrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisualbrush)<br/> [**IXpsOMImageBrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomimagebrush)<br/> [**IXpsOMGradientBrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgradientbrush)<br/> [**IXpsOMLinearGradientBrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomlineargradientbrush)<br/> [**IXpsOMRadialGradientBrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomradialgradientbrush)<br/> | Un pinceau est utilisé pour remplir une zone ou une ligne.<br/>                                                                                                                                             |
| [**IXpsOMSolidColorBrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomsolidcolorbrush)<br/>         | Aucun<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                             | Fournit des fonds de couleur unie ou des traits. <br/>                                                                                                                                                |
| [**IXpsOMVisualBrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisualbrush)<br/>                 | Aucun<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                             | Fournit un objet visuel, tel qu’un chemin d’accès, un glyphe ou un canevas, ou un visuel partiel à utiliser comme remplissage ou trait en mosaïque. <br/>                                                                  |
| [**IXpsOMImageBrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomimagebrush)<br/>                   | Aucun<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                             | Fournit une image (ou une image partielle) à utiliser comme remplissage ou trait en mosaïque. <br/>                                                                                                           |
| [**IXpsOMLinearGradientBrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomlineargradientbrush)<br/> | Aucun<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                             | Fournit un dégradé linéaire à utiliser comme remplissage ou trait. <br/>                                                                                                                            |
| [**IXpsOMRadialGradientBrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomradialgradientbrush)<br/> | Aucun<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                             | Fournit un dégradé radial à utiliser comme remplissage ou trait. <br/>                                                                                                                            |
| [**IXpsOMGradientStop**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgradientstop)<br/>               | Aucun<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                             | Définit un point d’inflexion de valeur de couleur unique dans un dégradé linéaire ou radial. <br/>                                                                                                     |
| [**IXpsOMGeometry**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometry)<br/>                       | [**IXpsOMGeometryFigure**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometryfigure)<br/>                                                                                                                                                                                                                                                                                                                                                                                             | Fournit une définition d’une région vectorielle à utiliser comme zone de découpage ou définition de chemin d’accès. Se compose d’une ou de plusieurs interfaces [**IXpsOMGeometryFigure**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometryfigure) . <br/> |
| [**IXpsOMGeometryFigure**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometryfigure)<br/>           | Aucun<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                             | Partie d’une définition de région qui est référencée par une interface [**IXpsOMGeometry**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometry) et qui se compose d’un ou de plusieurs segments. <br/>                                    |
| [**IXpsOMMatrixTransform**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsommatrixtransform)<br/>         | Aucun<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                             | Spécifie la transformation de matrice affine à appliquer à l’objet lors du rendu. <br/>                                                                                              |



 

## <a name="contents"></a>Contenu

-   [Pinceaux OM XPS](xps-object-model-brushes.md)
-   [Dégradés du modèle d’objet XPS](xps-object-model-gradients.md)
-   [Objets géométriques du modèle d’objet XPS](xps-object-model-geometry-objects.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Interface IXpsOMPath**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompath)
</dt> <dt>

[**Interface IXpsOMDashCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdashcollection)
</dt> <dt>

[**Interface IXpsOMMatrixTransform**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsommatrixtransform)
</dt> </dl>

 

 




