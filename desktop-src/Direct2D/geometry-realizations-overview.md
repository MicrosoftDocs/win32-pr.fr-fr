---
title: Vue d’ensemble des réalisations géométriques
description: Cette rubrique explique comment utiliser la réalisation de la géométrie de Direct2D pour améliorer les performances de rendu de géométrie de votre application dans certains scénarios.
ms.assetid: E8C4C4E5-3102-4F53-847E-A4C2D12A6921
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5108537e9ea9b38bebaab590178d990b44e611e56e82690e9d91ad9b56c19372
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119260132"
---
# <a name="geometry-realizations-overview"></a>Vue d’ensemble des réalisations géométriques

Cette rubrique explique comment utiliser la réalisation de la géométrie de [Direct2D](direct2d-portal.md) pour améliorer les performances de rendu de géométrie de votre application dans certains scénarios.

Il contient les sections suivantes :

-   [Qu’est-ce que la réalisation de géométrie ?](#what-are-geometry-realizations)
-   [Pourquoi utiliser des réalisations géométriques ?](#why-use-geometry-realizations)
-   [Quand utiliser des réalisations géométriques](#when-to-use-geometry-realizations)
-   [Création de réalisations géométriques](#creating-geometry-realizations)
-   [Dessin des réalisations géométriques](#drawing-geometry-realizations)
-   [Mise à l’échelle des réalisations géométriques](#scaling-geometry-realizations)
    -   [Utilisation des réalisations géométriques dans des applications qui ne sont pas mises à l’échelle](#using-geometry-realizations-in-apps-that-do-not-scale)
    -   [Utilisation des réalisations géométriques dans les applications qui sont mises à l’échelle d’une petite quantité](#using-geometry-realizations-in-apps-that-scale-by-a-small-amount)
    -   [Utilisation des réalisations géométriques dans les applications qui sont mises à l’échelle d’une grande quantité](#using-geometry-realizations-in-apps-that-scale-by-a-large-amount)
-   [Rubriques connexes](#related-topics)

## <a name="what-are-geometry-realizations"></a>Qu’est-ce que la réalisation de géométrie ?

les réalisations géométriques, introduites dans Windows 8.1, sont un nouveau type de primitive de dessin qui permet aux applications [Direct2D](direct2d-portal.md) d’améliorer les performances de rendu de géométrie dans certains cas. Les réalisations géométriques sont représentées par l’interface [**ID2D1GeometryRealization**](/windows/win32/api/d2d1_2/nn-d2d1_2-id2d1geometryrealization) .

## <a name="why-use-geometry-realizations"></a>Pourquoi utiliser des réalisations géométriques ?

Lorsque [Direct2D](direct2d-portal.md) rend un objet [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) , il doit convertir cette géométrie en une forme que le matériel graphique comprend à travers un processus appelé pavage. En règle générale, Direct2D doit paver Geometry chaque frame qu’il dessine, même si la géométrie ne change pas. Si votre application restitue la même géométrie à chaque trame, le repavage répété représente un effort de calcul gaspillé. Il est plus efficace en termes de calcul pour mettre en cache le pavage, ou même la pixellisation complète, de la géométrie, et de dessiner cette représentation en cache de chaque image au lieu de rele pavage à plusieurs reprises.

Un moyen courant pour les développeurs de résoudre ce problème consiste à mettre en cache la pixellisation complète de la géométrie. En particulier, il est courant de créer une nouvelle bitmap, de pixelliser la géométrie sur cette bitmap, puis de la dessiner sur la scène en fonction des besoins. (Cette approche est décrite dans la section de [rendu Geometry](improving-direct2d-performance.md) qui améliore les performances des applications Direct2D.) Bien que cette approche soit très efficace en termes de calcul, elle présente certains inconvénients :

-   La bitmap mise en cache est sensible aux modifications apportées à la transformation appliquée à la scène. Par exemple, la mise à l’échelle de la pixellisation peut entraîner des artefacts de mise à l’échelle perceptibles. L’atténuation de ces artefacts avec des algorithmes de mise à l’échelle de haute qualité peut être coûteuse en ressources informatiques.
-   La bitmap mise en cache consomme une quantité importante de mémoire, surtout si elle est pixellisée à une résolution élevée.

Les réalisations de géométrie offrent un autre moyen de mettre en cache la géométrie qui évite les inconvénients ci-dessus. Les réalisations géométriques ne sont pas représentées par des pixels (comme c’est le cas avec une pixellisation complète), mais plutôt par des points sur un plan mathématique. Pour cette raison, elles sont moins sensibles que les pixellisations complètes pour la mise à l’échelle et d’autres manipulations, et elles consomment beaucoup moins de mémoire.

## <a name="when-to-use-geometry-realizations"></a>Quand utiliser des réalisations géométriques

Envisagez d’utiliser des réalisations géométriques lorsque votre application restitue des géométries complexes dont les formes changent rarement, mais qui peuvent être sujettes à des transformations modifiées.

Par exemple, Imaginez une application de mappage qui montre un mappage statique, mais qui permet à l’utilisateur d’effectuer un zoom avant ou arrière. Cette application peut tirer parti de l’utilisation des réalisations géométriques. Étant donné que les géométries rendues restent statiques, il est utile de les mettre en cache pour enregistrer le travail de pavage. Toutefois, étant donné que les mappages sont mis à l’échelle lorsque l’utilisateur effectue un zoom, la mise en cache d’une pixellisation complète n’est pas idéale, en raison des artefacts de mise à l’échelle. La mise en cache des réalisations géométriques permet à l’application d’éviter la refacettisation du travail tout en conservant une haute qualité visuelle pendant la mise à l’échelle.

En revanche, Imaginez une application Kaléidoscope avec une géométrie animée qui change continuellement. Cette application n’a probablement pas intérêt à utiliser des réalisations géométriques. Étant donné que les formes changent d’une image à l’autres, il n’est pas utile de mettre en cache leur pavages. La meilleure approche pour cette application est de dessiner des objets [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) directement.

## <a name="creating-geometry-realizations"></a>Création de réalisations géométriques

Un objet [**ID2D1GeometryRealization**](/windows/win32/api/d2d1_2/nn-d2d1_2-id2d1geometryrealization) doit être créé à partir d’un objet [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) existant. Pour créer une réalisation géométrique, appelez la méthode [**CreateFilledGeometryRealization**](/windows/win32/api/d2d1_2/nf-d2d1_2-id2d1devicecontext1-createfilledgeometryrealization) ou la méthode [**CreateStrokedGeometryRealization**](/windows/win32/api/d2d1_2/nf-d2d1_2-id2d1devicecontext1-createstrokedgeometryrealization) et transmettez le **ID2D1Geometry** à réaliser.

-   [**CreateFilledGeometryRealization**](/windows/win32/api/d2d1_2/nf-d2d1_2-id2d1devicecontext1-createfilledgeometryrealization) crée une réalisation de l’intérieur de la forme : la région qui serait dessinée en appelant [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry).
-   [**CreateStrokedGeometryRealization**](/windows/win32/api/d2d1_2/nf-d2d1_2-id2d1devicecontext1-createstrokedgeometryrealization) crée une réalisation du trait de la forme : la région qui serait dessinée en appelant [**DrawGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry).

Les deux types de réalisation géométrique sont représentés par l’interface [**ID2D1GeometryRealization**](/windows/win32/api/d2d1_2/nn-d2d1_2-id2d1geometryrealization) .

Lors de la création d’une réalisation géométrique, [Direct2D](direct2d-portal.md) doit aplatir les courbes de la géométrie fournie en approximations polygonales. Vous devez fournir un paramètre de tolérance de aplatissement à la méthode de création, qui spécifie la distance maximale, en pixels indépendants du périphérique (DIP), entre la courbe vraie de la géométrie et son approximation polygonale. Plus la tolérance d’aplatissement que vous fournissez est faible, plus la fidélité de l’objet de réalisation géométrique résultant est élevée. De même, si vous fournissez une tolérance plus élevée, la réalisation de la géométrie est plus faible. Notez que les réalisations de géométrie à fidélité élevée sont plus coûteuses que les plus faibles, mais elles peuvent être mises à l’échelle avant d’introduire des artefacts visibles. Pour obtenir des conseils sur l’utilisation des tolérances de mise à plat, consultez [mise à l’échelle des réalisations géométriques](#scaling-geometry-realizations) ci-dessous.

> [!Note]  
> Les objets de réalisation Geometry sont associés à un appareil graphique particulier : il s’agit de ressources dépendantes de l’appareil.

 

## <a name="drawing-geometry-realizations"></a>Dessin des réalisations géométriques

Le dessin des réalisations géométriques est similaire au dessin d’autres primitives [Direct2D](direct2d-portal.md) , comme les bitmaps. Pour ce faire, appelez la méthode [**DrawGeometryRealization**](/windows/win32/api/d2d1_2/nf-d2d1_2-id2d1devicecontext1-drawgeometryrealization) et transmettez-lui l’objet de réalisation géométrique à dessiner et le pinceau à utiliser. Comme pour les autres méthodes de dessin Direct2D, vous devez appeler **DrawGeometryRealization** entre les appels à [**BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) et [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw).

## <a name="scaling-geometry-realizations"></a>Mise à l’échelle des réalisations géométriques

Les réalisations géométriques, comme d’autres primitives [Direct2D](direct2d-portal.md) , respectent le jeu de transformations sur le contexte de périphérique. Bien que les transformations de translation et de rotation n’aient aucun effet sur la qualité visuelle des réalisations géométriques, les transformations de mise à l’échelle peuvent produire des artefacts visuels.

En particulier, l’application d’une mise à l’échelle suffisamment importante à toute réalisation géométrique peut révéler la approximation polygonale des courbes vraies. L’image ci-dessous montre une paire de réalisations de géométries elliptiques (remplissage et trait) qui ont été mises à l’échelle trop loin. Les artefacts de mise à plat des courbes sont visibles.

![paire de réalisations de géométries elliptiques (remplissage et trait) qui ont été mises à l’échelle trop loin. les artefacts de mise à plat des courbes sont visibles.](images/zoomed-in.png)

Les applications qui sont sensibles à la qualité visuelle doivent prendre des mesures pour s’assurer que cela ne se produit pas. La façon dont vous gérez la mise à l’échelle dépend des besoins de votre application. Voici plusieurs approches recommandées pour plusieurs types d’application différents.

### <a name="using-geometry-realizations-in-apps-that-do-not-scale"></a>Utilisation des réalisations géométriques dans des applications qui ne sont pas mises à l’échelle

Si votre application n’effectue pas de mise à l’échelle sur les réalisations géométriques, il est possible de créer des réalisations une seule fois à l’aide d’une seule tolérance d’aplatissement. (Les transformations sans mise à l’échelle n’affectent pas la qualité visuelle des réalisations de géométries rendues.) Utilisez la fonction [**ComputeFlatteningTolerance**](/previous-versions/windows/desktop/legacy/dn280327(v=vs.85)) pour calculer la tolérance d’aplatissement appropriée pour le PPP :


```C++
    float dpiX, dpiY;
    deviceContext->GetDpi(&dpiX, &dpiY);

    float flatteningTolerance = D2D1::ComputeFlatteningTolerance(
        D2D1::Matrix3x2F::Identity(),   // apply no additional scaling transform
        dpiX,                           // horizontal DPI
        dpiY                            // vertical DPI
        );
```



### <a name="using-geometry-realizations-in-apps-that-scale-by-a-small-amount"></a>Utilisation des réalisations géométriques dans les applications qui sont mises à l’échelle d’une petite quantité

Si votre application peut mettre à l’échelle une géométrie qui ne se trouve que sur une petite quantité (par exemple, jusqu’à 2x ou 3 fois), il peut être approprié de créer la réalisation de la géométrie une seule fois, à une tolérance d’aplatissement proportionnellement inférieure à la valeur par défaut. Cela crée une réalisation plus fidèle qui peut être mise à l’échelle de façon significative avant de générer des artefacts de mise à l’échelle ; le compromis est que la réalisation d’une plus haute fidélité nécessite davantage de travail.

Par exemple, supposons que vous savez que votre application ne mettra jamais à l’échelle une réalisation géométrique de plus de 2x. Votre application peut créer la réalisation géométrique à l’aide d’une tolérance de aplatissement qui est la moitié de la valeur par défaut et faire simplement évoluer la réalisation en fonction des besoins, jusqu’à 2x. Utilisez la fonction [**ComputeFlatteningTolerance**](/previous-versions/windows/desktop/legacy/dn280327(v=vs.85)) pour calculer la tolérance d’aplatissement appropriée en passant 2,0 comme paramètre *maxZoomFactor* :


```C++
    float dpiX, dpiY;
    deviceContext->GetDpi(&dpiX, &dpiY);
    
    float flatteningTolerance = D2D1::ComputeFlatteningTolerance(
        D2D1::Matrix3x2F::Identity(),   // apply no additional scaling transform
        dpiX,                           // horizontal DPI
        dpiY,                           // vertical DPI
        2.0f                            // realization can be scaled by an additional 2x
        );
```



### <a name="using-geometry-realizations-in-apps-that-scale-by-a-large-amount"></a>Utilisation des réalisations géométriques dans les applications qui sont mises à l’échelle d’une grande quantité

Si votre application peut mettre à l’échelle une réalisation géométrique vers le haut ou vers le haut (par exemple, d’une taille de 10 ou plus), la gestion de la mise à l’échelle appropriée est plus compliquée.

Pour la plupart de ces applications, l’approche recommandée consiste à recréer la réalisation de la géométrie à des tolérances de aplatissement progressivement plus basses à mesure que la scène est montée en puissance, afin de préserver la fidélité visuelle et d’éviter la mise à l’échelle des artefacts. De même, à mesure que la scène est mise à l’échelle, l’application doit recréer les réalisations géométriques à des tolérances de mise à plat progressive, afin d’éviter un rendu plus lent des détails qui ne sont pas visibles. L’application ne doit pas recréer les exécutions géométriques à chaque modification de l’échelle, car cette opération a pour effet de mettre en cache le travail de pavage. Au lieu de cela, l’application doit recréer les réalisations géométriques moins fréquemment : par exemple, après chaque augmentation ou baisse de l’échelle.

Chaque fois que la mise à l’échelle change dans une application en réponse à l’interaction de l’utilisateur, l’application peut comparer la nouvelle échelle à l’échelle à laquelle les réalisations de la géométrie ont été créées (stockées, par exemple, dans un membre **m \_ lastScale** ). Si les deux valeurs sont proches (dans ce cas, dans le cas d’un facteur de 2), aucune action supplémentaire n’est effectuée. Toutefois, si les deux valeurs ne sont pas proches, les réalisations de géométrie sont recréées. La fonction [**ComputeFlatteningTolerance**](/previous-versions/windows/desktop/legacy/dn280327(v=vs.85)) est utilisée pour calculer une tolérance d’aplatissement appropriée pour la nouvelle échelle, et **m \_ lastScale** est mis à jour avec la nouvelle échelle.

En outre, l’application crée toujours des réalisations à l’aide d’une tolérance plus petite que ce qui serait normalement utilisé pour la nouvelle échelle, en passant une valeur de 2 comme paramètre *maxZoomFactor* à [**ComputeFlatteningTolerance**](/previous-versions/windows/desktop/legacy/dn280327(v=vs.85)). Cela permet de mettre à l’échelle les nouvelles réalisations géométriques par un facteur supplémentaire de 2 sans générer d’artefacts de mise à l’échelle.

> [!Note]  
> L’approche décrite ici peut ne pas convenir à toutes les applications. Par exemple, si votre application permet la mise à l’échelle de la scène par de très grands facteurs très rapidement (par exemple, si elle contient un curseur « Zoom » qui peut être déplacé de 100% à 1 million% dans l’étendue de quelques frames), cette approche peut entraîner un excès de travail en recréant la géométrie qui effectue chaque trame. Une autre approche consiste à recréer les réalisations géométriques uniquement après que chaque manipulation de l’échelle de la scène est terminée (par exemple, une fois que l’utilisateur a terminé un geste de pincement).

 

## <a name="related-topics"></a>Rubriques connexes

[Vue d’ensemble des géométries](direct2d-geometries-overview.md)

[Amélioration des performances des applications Direct2D](improving-direct2d-performance.md)

[Instructions générales pour le rendu de contenu statique complexe](improving-direct2d-performance.md)

[**ID2D1DeviceContext1**](/windows/win32/api/d2d1_2/nn-d2d1_2-id2d1devicecontext1)

[**ID2D1GeometryRealization**](/windows/win32/api/d2d1_2/nn-d2d1_2-id2d1geometryrealization)

[**ComputeFlatteningTolerance fonction)**](/previous-versions/windows/desktop/legacy/dn280327(v=vs.85))