---
title: Qu’est-ce que Direct3D 12 ?
description: DirectX 12 introduit la prochaine version de Direct3D. l’API graphique 3D au cœur de DirectX.
ms.assetid: 09C586BF-11CE-4392-9BFD-A40B05DD0624
ms.localizationpriority: high
ms.topic: article
ms.date: 11/19/2018
ms.openlocfilehash: f82b01ba33cfa6660f266a481b2eaaab20ade236
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127292751"
---
# <a name="what-is-direct3d-12"></a>Qu’est-ce que Direct3D 12?

DirectX 12 introduit la prochaine version de Direct3D &mdash; l’API graphique 3D au cœur de DirectX. Direct3D 12 est plus rapide et plus efficace que les versions précédentes. Direct3D 12 offre des scènes plus riches, des objets plus complexes, des effets plus complexes et une utilisation complète du matériel du GPU moderne.

## <a name="how-can-direct3d-12-be-so-much-faster-and-more-efficient"></a>Comment Direct3D 12 peut-il être tellement plus rapide et plus efficace ?

Direct3D 12 est unique dans la limite du fait qu’il offre un niveau inférieur d’abstraction matérielle par rapport aux versions précédentes, ce qui vous permet d’améliorer considérablement la mise à l’échelle de l’UC multicœur de votre titre (ou d’une autre application). Pour une chose, avec Direct3D 12, votre titre est responsable de sa propre [gestion](memory-management.md)de la mémoire. En outre, en utilisant Direct3D 12, vos titres et vos applications tirent parti de la surcharge du GPU par le biais de fonctionnalités telles que les [listes et les files d’attente de commandes](command-queues-and-command-lists.md), les [tables de descripteurs](descriptor-tables.md)et les [objets d’état de pipeline](managing-graphics-pipeline-state-in-direct3d-12.md)concis.

Direct3D 12 et Direct3D 11,3 introduisent un ensemble de nouvelles fonctionnalités pour le pipeline de rendu.

- [Pixellisation conservatrice](../direct3d11/conservative-rasterization.md) pour activer la détection d’accès fiable.
- Les [ressources en mosaïque de volume](../direct3d11/volume-tiled-resources.md) pour permettre le traitement des ressources tridimensionnelles transmises en continu comme si elles étaient toutes dans la mémoire vidéo.
- [Vues triées par le rastériseur](../direct3d11/rasterizer-order-views.md) pour activer le rendu de transparence fiable.
- Définition de la référence de stencil dans un nuanceur pour activer l’occultation spéciale et d’autres effets.
- Amélioration du mappage de texture et des charges de vue d’accès non ordonnées typées (UAV).

## <a name="how-deeply-should-i-invest-in-direct3d-12"></a>En quoi dois-je investir dans Direct3D 12 ?

Direct3D 12 offre quatre principaux avantages pour les développeurs de graphiques (par rapport à Direct3D 11).

- La surcharge du processeur est considérablement réduite.
- Réduction significative de la consommation énergétique.
- Amélioration jusqu’à 20% de l’efficacité du GPU.
- développement multiplateforme pour un appareil Windows 10 (pc, tablette, console, mobile).

Direct3D 12 est conçu pour les programmeurs graphiques avancés à utiliser. Il appelle une expertise graphique importante et un niveau élevé de réglage précis. Direct3D 12 est conçu pour tirer pleinement parti de l’utilisation de plusieurs threads, de la synchronisation de l’UC/GPU, ainsi que de la transition et de la réutilisation des ressources d’un objectif à un autre. Il s’agit de techniques qui requièrent une quantité considérable de compétences en programmation au niveau de la mémoire.

Direct3D 12 présente un autre avantage. Il existe environ 200 fonctions ; et environ un tiers de ceux-ci font tout le lourd. Cela signifie que vous, en tant que développeur graphique, devez être en mesure de vous éduquer sur &mdash; &mdash; l’ensemble d’API complet sans avoir à mémoriser un trop grand nombre de noms d’API.

Direct3D 11 est toujours une option viable avec Direct3D 12. La plupart des nouvelles fonctionnalités de rendu de Direct3D 12 sont disponibles dans [direct3d 11,3](../direct3d11/direct3d-11-3-features.md). Direct3D 11,3 est une API de moteur graphique de bas niveau ; Direct3D 12 va encore plus loin.

Votre équipe de développement peut s’approcher d’un titre Direct3D 12 au moins deux façons.

### <a name="use-direct3d-12-exclusively"></a>Utiliser Direct3D 12 exclusivement

Pour un projet qui tire le meilleur parti de tous les avantages de Direct3D 12, vous devez développer un moteur Direct3D 12 hautement personnalisé dès le départ.

Si vous, en tant que développeur de graphismes, comprenez l’utilisation et la réutilisation des ressources au sein de vos titres, et que vous pouvez tirer parti de cela en minimisant le chargement et la copie, vous pouvez développer et personnaliser un moteur très efficace pour ces titres. Les améliorations des performances peuvent être très considérables, ce qui permet de libérer du temps processeur pour augmenter le nombre d’appels de dessin et d’ajouter des cluster à vos graphiques.

L’investissement en programmation est significatif et vous devez envisager le débogage et l’instrumentation du projet à partir du début. Le Threading, la synchronisation et d’autres bogues de minutage peuvent être difficiles.

### <a name="use-direct3d-12-in-concert-with-direct3d-11"></a>Utiliser Direct3D 12 conjointement avec Direct3D 11

Une approche plus rapide consiste à traiter les goulots d’étranglement connus dans votre titre Direct3D 11. Vous pouvez les traiter à l’aide des techniques [Direct3D 12 Interop et/ou D3D11On12](direct3d-12-interop.md) , qui permettent aux deux versions de l’API de fonctionner ensemble. Cette approche réduit les modifications nécessaires à un moteur graphique Direct3D 11 existant. Toutefois, les gains de performances sont limités à l’allègement du goulot d’étranglement que le code Direct3D 12.

## <a name="microsoft-directx-12-and-graphics-education-videos"></a>Vidéos sur Microsoft DirectX 12 (et Graphics Education)

[Enseignement amélioré pour les développeurs de graphiques](https://www.youtube.com/channel/UCiaX2B8XiXR70jaN7NK-FpA). Ces vidéos couvrent des sujets tels que les modes de présentation, le portage vers DirectX 12, la pixellisation conservatrice, les outils graphiques, l’angle, Win2D et les événements tels que GDC, Build, etc. Le contenu DirectX 12 technique est précédé de *DirectX 12*. Venez ici pour découvrir des conseils et astuces directement à partir de l’équipe de la fonctionnalité Direct3D 12. Nous souhaitons vous aider à utiliser nos dernières versions et outils pour rendre votre jeu le mieux possible !

## <a name="conclusion"></a>Conclusion

Direct3D 12 s’intéresse à la performance des moteurs graphiques spectaculaires. La facilité de développement, les constructions de niveau supérieur et la prise en charge du compilateur ont été mises à l’échelle pour permettre cela. La prise en charge des pilotes et la facilité de débogage sont conservées avec Direct3D 11.

Direct3D 12 est un nouveau secteur. Secteur qui attend que l’expert Inquisitive provienne et explore.
