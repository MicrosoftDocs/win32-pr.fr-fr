---
title: Pixellisation de Direct3D 11,3
description: La pixellisation conservatrice apporte une certaine certitude au rendu des pixels, ce qui est utile en particulier pour les algorithmes de détection des collisions.
ms.assetid: 83F223C0-9282-4149-86CF-471B88829F76
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd33b7c7d237fc30adb349f1c1b24ce16c2740ce93fc97445a6e3f69d0949aeb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119408569"
---
# <a name="direct3d-113-conservative-rasterization"></a>Pixellisation de Direct3D 11,3

La pixellisation conservatrice apporte une certaine certitude au rendu des pixels, ce qui est utile en particulier pour les algorithmes de détection des collisions.

-   [Vue d'ensemble](#overview)
-   [Interactions avec le pipeline](#interactions-with-the-pipeline)
-   [Informations d’implémentation](#implementation-details)
-   [API summary](#api-summary)
-   [Rubriques connexes](#related-topics)

## <a name="overview"></a>Vue d’ensemble

La pixellisation conservatrice signifie que tous les pixels qui sont au moins partiellement couverts par une primitive rendue sont pixellisés, ce qui signifie que le nuanceur de pixels est appelé. Le comportement normal est l’échantillonnage, qui n’est pas utilisé si la pixellisation conservatrice est activée.

La pixellisation conservatrice est utile dans un certain nombre de situations, notamment pour garantir la détection des collisions, l’élimination des occlusions et la détection de la visibilité.

Par exemple, l’illustration suivante montre un triangle vert rendu à l’aide d’une pixellisation conservatrice. La zone brune est connue sous le nom de « région d’incertitude » : une région dans laquelle les erreurs d’arrondi et autres problèmes ajoutent de l’incertitude aux dimensions exactes du triangle. Les triangles rouges de chaque vertex montrent comment la région d’incertitude est calculée. Les grands carrés gris affichent les pixels qui seront rendus. Les carrés roses affichent les pixels affichés à l’aide de la « règle de haut en bas », qui entre en lecture lorsque le bord du triangle traverse le bord des pixels. Il peut y avoir des faux positifs (pixels définis qui ne devraient pas avoir été) que le système va normalement, mais pas toujours.

![affiche la règle en haut à gauche](images/conservative-rasterization-0.png)

## <a name="interactions-with-the-pipeline"></a>Interactions avec le pipeline

Pour de nombreux détails sur la façon dont la pixellisation conservatrice interagit avec le pipeline Graphics, reportez-vous à la [pixellisation conservatrice D3D12](/windows/desktop/direct3d12/conservative-rasterization).

## <a name="implementation-details"></a>Informations d’implémentation

Le type de pixellisation pris en charge dans Direct3D 12 est parfois appelé « pixellisation conservatrice préestimée ». Il existe également le concept de « pixellisation conservatrice sous-estimée », ce qui signifie que seuls les pixels entièrement couverts par une primitive rendue sont pixellisés. Les informations de pixellisation conservatrice sous-estimée sont disponibles via le nuanceur de pixels par le biais de l’utilisation de données de couverture d’entrée, et seule une pixellisation conservatrice surestimée est disponible en mode de pixellisation.

Si une partie d’une primitive chevauche un pixel, ce pixel est considéré comme couvert et est ensuite pixellisé. Lorsqu’un bord ou un angle d’une primitive se trouve le long du bord ou de l’angle d’un pixel, l’application de la « règle de haut en bas » est spécifique à l’implémentation. Toutefois, pour les implémentations qui prennent en charge les triangles dégénérées, un triangle dégenerate sur un bord ou un angle doit couvrir au moins un pixel.

Les implémentations de pixellisation conservatrices peuvent varier sur un matériel différent et produisent des faux positifs, ce qui signifie qu’ils peuvent incorrectement décider que les pixels sont couverts. Cela peut être dû à des détails spécifiques à l’implémentation, tels que des erreurs de culture ou d’accrochage primitives inhérentes aux coordonnées de vertex à virgule fixe utilisées dans la pixellisation. La raison pour laquelle les faux positifs (en ce qui concerne les coordonnées de vertex à virgule fixe) sont valides est parce qu’une certaine quantité de faux positifs sont nécessaires pour permettre à une implémentation d’effectuer une évaluation de la couverture sur des sommets postérieurs à l’alignement (c’est-à-dire des coordonnées de vertex qui ont été converties de la virgule flottante en virgule flottante de 16,8

Les implémentations de pixellisation conservatrice ne produisent pas de faux négatifs en ce qui concerne les coordonnées de vertex à virgule flottante pour les primitives postérieures à la dégénération : si une partie d’une primitive chevauche une partie d’un pixel, ce pixel est pixellisé.

Les triangles dégénérées (doublons d’index dans une mémoire tampon d’index ou colinéaire en 3D) ou dégénérées après la conversion à virgule fixe (vertex colinéaires dans le rastériseur) peuvent être éliminés ou non ; les deux sont des comportements valides. Les triangles dégénérées doivent être considérés comme étant en arrière. ainsi, si un comportement spécifique est requis par une application, il peut utiliser l’élimination des faces arrière ou les tests pour les faces avant. Les triangles dégénérées utilisent les valeurs affectées au vertex 0 pour toutes les valeurs interpolées.

Il existe trois niveaux de prise en charge matérielle, en plus de la possibilité que le matériel ne prenne pas en charge cette fonctionnalité.

-   Le niveau 1 prend en charge les régions d’incertitude de 1/2 pixels et aucune dégénération de l’instantané. Cela est utile pour le rendu en mosaïque, un Atlas de textures, la génération de cartes de lumière et les mappages d’ombre sous-pixel.
-   Le niveau 2 ajoute des dégénérations postérieures au Snap et 1/256 régions d’incertitude. Elle ajoute également la prise en charge de l’accélération de l’algorithme basée sur le processeur (telle que voxelization).
-   Le niveau 3 ajoute 1/512 régions d’incertitude, la couverture d’entrée interne et prend en charge l’élimination des occlusions. La couverture d’entrée ajoute la nouvelle valeur `SV_InnerCoverage` au langage HLSL (High Level Shading Language). Il s’agit d’un entier scalaire 32 bits qui peut être spécifié à l’entrée d’un nuanceur de pixels, et représente les informations de pixellisation conservatrice sous-estimées (autrement dit, si un pixel est garanti comme étant entièrement couvert).

## <a name="api-summary"></a>Résumé des API

Les méthodes, structures, énumérations et classes d’assistance suivantes font référence à la pixellisation conservatrice :

-   [**D3d11 \_ RASTÉRISEUR \_ DESC2**](/windows/desktop/api/D3D11_3/ns-d3d11_3-cd3d11_rasterizer_desc2) : structure contenant la description du rastériseur, en notant la \_ \_ classe d’assistance CD3D12 rastériseur DESC2 pour la création de descriptions de rastériseur.
-   [**D3d11 \_ \_ \_ Mode de pixellisation conservateur**](/windows/desktop/api/D3D11_3/ne-d3d11_3-d3d11_conservative_rasterization_mode) : valeurs enum pour le mode (on ou OFF).
-   [**D3d11 \_ Données de fonctionnalités \_ \_ d3d11 \_ OPTIONS2**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options2) : structure détenant le niveau de prise en charge.
-   [**D3d11 \_ \_ \_ Niveau de pixellisation conservateur**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_conservative_rasterization_tier) : valeurs d’énumération pour chaque niveau de prise en charge par le matériel.
-   [**ID3D11Device :: CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) : méthode permettant d’accéder aux fonctionnalités prises en charge.

## <a name="related-topics"></a>Rubriques connexes
* [Fonctionnalités Direct3D 11,3](direct3d-11-3-features.md)