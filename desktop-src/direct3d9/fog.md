---
description: L’ajout de brouillard à une scène 3D peut améliorer le réalisme, fournir des ambiance ou définir une humeur, et obscurcir les artefacts provoqués lorsque la géométrie à distance entre en vue.
ms.assetid: 42045e96-43aa-4cec-82b5-0b46a7d5097b
title: Brouillard (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44b9ed234bef0f3dea76baa98390f25e9b2003a6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126916579"
---
# <a name="fog-direct3d-9"></a>Brouillard (Direct3D 9)

L’ajout de brouillard à une scène 3D peut améliorer le réalisme, fournir des ambiance ou définir une humeur, et obscurcir les artefacts provoqués lorsque la géométrie à distance entre en vue. Direct3D prend en charge deux modèles de brouillard, le brouillard de pixel et le brouillard de vertex, chacun avec ses propres fonctionnalités et interface de programmation.

Fondamentalement, le brouillard est implémenté en fusionnant la couleur des objets dans une scène avec une couleur de brouillard choisie en fonction de la profondeur d’un objet dans une scène ou de sa distance par rapport au point de vue. À mesure que les objets sont plus éloignés, leur couleur d’origine fusionne de plus en plus avec la couleur de brouillard choisie, créant ainsi l’illusion que l’objet est de plus en plus obscurci par de petites particules flottantes dans la scène. L’illustration suivante montre une scène rendue sans brouillard, et une scène similaire rendue avec Fog activé.

![illustration de la même scène avec et sans brouillard](images/fogcomp.png)

Dans cette illustration, la scène sur la gauche présente un horizon clair, au-delà duquel aucun décor n’est visible, même s’il est visible dans le monde réel. La scène sur la droite masque l’horizon en utilisant une couleur de brouillard identique à la couleur d’arrière-plan, ce qui fait apparaître les polygones dans la distance. En associant des effets de brouillard discrets à la conception de scènes créatives, vous pouvez ajouter de l’humeur et adoucir la couleur des objets dans une scène.

Direct3D offre deux façons d’ajouter un brouillard à une scène : le brouillard de pixel et le brouillard de vertex, nommés pour la façon dont les effets de brouillard sont appliqués. Pour plus d’informations, consultez [brouillard de pixel (Direct3D 9)](pixel-fog.md) et [brouillard de vertex (Direct3D 9)](vertex-fog.md). En bref, le brouillard de pixel, également appelé « brouillard de table », est implémenté dans le pilote de périphérique et le brouillard de vertex est implémenté dans le moteur d’éclairage Direct3D. Une application peut implémenter un brouillard avec un nuanceur de sommets et un brouillard de pixel simultanément, si vous le souhaitez.

> [!Note]  
> Que vous utilisiez le brouillard de pixel ou de vertex, votre application doit fournir une matrice de projection conforme pour s’assurer que les effets de brouillard sont correctement appliqués. Cette restriction s’applique même aux applications qui n’utilisent pas la transformation et le moteur d’éclairage Direct3D. Pour plus d’informations sur la façon dont vous pouvez fournir une matrice appropriée, consultez [projection Transform (Direct3D 9)](projection-transform.md).

 

Les rubriques suivantes présentent le brouillard et présentent des informations sur l’utilisation de diverses fonctionnalités de brouillard dans les applications Direct3D.

-   [Formules de brouillard (Direct3D 9)](fog-formulas.md)
-   [Paramètres de brouillard (Direct3D 9)](fog-parameters.md)
-   [Fusion de brouillard (Direct3D 9)](fog-blending.md)
-   [Couleur de brouillard (Direct3D 9)](fog-color.md)
-   [Brouillard du vertex (Direct3D 9)](vertex-fog.md)
-   [Brouillard de pixel (Direct3D 9)](pixel-fog.md)

La fusion de brouillard est contrôlée par les États de rendu ; il ne fait pas partie du pipeline de pixels programmable.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Rendu Direct3D](direct3d-rendering.md)
</dt> </dl>

 

 



