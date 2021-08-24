---
description: Les applications C++ peuvent contrôler la façon dont le brouillard affecte la couleur des objets dans une scène en modifiant la façon dont Microsoft Direct3D calcule les effets de brouillard sur la distance.
ms.assetid: b7148ae8-45c7-4dbe-8295-0335c7fdeff0
title: Formules de brouillard (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac92b6d00ff5f4d4ec03dbe7bb40365917f8b835fd121cdc934c470c45c38814
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120026995"
---
# <a name="fog-formulas-direct3d-9"></a>Formules de brouillard (Direct3D 9)

Les applications C++ peuvent contrôler la façon dont le brouillard affecte la couleur des objets dans une scène en modifiant la façon dont Microsoft Direct3D calcule les effets de brouillard sur la distance. Le type énuméré [**D3DFOGMODE**](./d3dfogmode.md) contient des membres qui identifient les trois formules de brouillard. Toutes les formules calculent un facteur de brouillard comme fonction de distance, en fonction des paramètres définis par votre application.

## <a name="linear-fog"></a>Brouillard linéaire

Cette valeur est définie avec l' \_ équation linéaire D3DFOG suivante.

![équation du brouillard linéaire Direct3D](images/fogliner.png)

where

-   Start est la distance à laquelle les effets de brouillard commencent.
-   end est la distance à laquelle les effets de brouillard n’augmentent plus.
-   d représente la profondeur ou la distance à partir du point de vue. Pour le brouillard basé sur une plage, la valeur de d correspond à la distance entre la position de la caméra et un sommet. Pour un brouillard non basé sur une plage, la valeur pour d est la valeur absolue de la coordonnée Z dans l’espace de l’appareil photo.

## <a name="exponential-fog"></a>Brouillard exponentiel

Les formules linéaires et exponentielles sont prises en charge pour le brouillard de pixel et le brouillard de vertex.

Cela est défini avec l’équation D3DFOG \_ exp suivante.

![équation du brouillard exponentiel Direct3D](images/fogexp.png)

where

-   e est la base des logarithmes naturels (environ 2,71828).
-   la densité est une densité de brouillard arbitraire qui peut être comprise entre 0,0 et 1,0.
-   d représente la profondeur, ou la distance par rapport au point de vue, comme indiqué plus haut.

Cette valeur est définie avec l' \_ équation D3DFOG EXP2 suivante.

![équation du brouillard exponentielle 2 Direct3D](images/fogexp2.png)

where

-   e est la base des logarithmes naturels comme indiqué ci-dessus.
-   la densité est une densité de brouillard arbitraire qui peut être comprise entre 0,0 et 1,0, comme indiqué ci-dessus.
-   d représente la profondeur, ou la distance par rapport au point de vue, comme indiqué ci-dessus.

> [!Note]  
> Le système stocke le facteur de brouillard dans le composant alpha de la couleur spéculaire d’un vertex. Si votre application effectue sa propre transformation et éclairage, vous pouvez insérer des valeurs de facteur de brouillard manuellement, qui seront appliquées par le système lors du rendu.

 

Le graphique suivant présente ces formules, en utilisant des valeurs communes comme dans les paramètres de formule.

![graphique des formules de brouillard sur la distance et la quantité de couleur](images/foggraph.png)

D3DFOG \_ Linear est 1,0 au début et 0,0 à la fin. Il n’est pas mesuré par rapport aux plans near ou Far.

Lorsque Direct3D calcule des effets de brouillard, il utilise le facteur de brouillard de l’une des équations précédentes dans l’équation de fusion suivante.

![équation des effets de brouillard pour Direct3D](images/fogcalc.png)

Cette formule met effectivement à l’échelle la couleur du polygone actuel par le facteur de brouillard f, puis ajoute le produit à la couleur de brouillard C, mise à l’échelle par l’inverse de l’opération de bits du facteur de brouillard. La valeur de couleur résultante est un mélange de la couleur de brouillard et de la couleur d’origine, en tant que facteur de distance. La formule s’applique à tous les appareils pris en charge dans Microsoft DirectX 7,0 et versions ultérieures. Pour l’appareil rampe héritée, le facteur de brouillard met à l’échelle les composants de couleur diffuse et spéculaire, fixés à la plage 0,0 et 1,0, inclus. Le facteur de brouillard commence généralement à 1,0 pour le plan proche et diminue à 0,0 du plan lointain.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Types de brouillard](fog-types.md)
</dt> </dl>

 

 
