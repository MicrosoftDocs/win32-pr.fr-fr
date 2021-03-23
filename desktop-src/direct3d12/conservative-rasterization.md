---
title: Pixellisation de Direct3D 12
description: La pixellisation conservatrice apporte une certaine certitude au rendu des pixels, ce qui est utile en particulier pour les algorithmes de détection des collisions.
ms.assetid: 081199AD-1702-4EC8-95AD-B1148C676199
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e4fae3489d54ab7b6b7abfda56f54dd8d970962
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/23/2019
ms.locfileid: "104548611"
---
# <a name="direct3d-12-conservative-rasterization"></a>Pixellisation de Direct3D 12

La pixellisation conservatrice apporte une certaine certitude au rendu des pixels, ce qui est utile en particulier pour les algorithmes de détection des collisions.

-   [Vue d'ensemble](#overview)
-   [Interactions avec le pipeline](#interactions-with-the-pipeline)
    -   [Interaction des règles de pixellisation](#rasterization-rules-interaction)
    -   [Interaction d’échantillonnage multiple](#multisampling-interaction)
    -   [Interaction SampleMask](#samplemask-interaction)
    -   [Interaction de test de profondeur/stencil](#depthstencil-test-interaction)
    -   [Interaction des pixels d’assistance](#helper-pixel-interaction)
    -   [Interaction de couverture de sortie](#output-coverage-interaction)
    -   [Interaction InputCoverage](#inputcoverage-interaction)
    -   [Interaction InnerCoverage](#innercoverage-interaction)
    -   [Interaction d’interpolation d’attribut](#attribute-interpolation-interaction)
    -   [Interaction du découpage](#clipping-interaction)
    -   [Interaction de la distance du clip](#clip-distance-interaction)
    -   [Interaction de pixellisation indépendante cible](#target-independent-rasterization-interaction)
    -   [Interaction de la topologie de la primitive IA](#ia-primitive-topology-interaction)
    -   [Interroger l’interaction](#query-interaction)
    -   [Élimination de l’interaction de l’État](#cull-state-interaction)
    -   [Interaction IsFrontFace](#isfrontface-interaction)
    -   [Interaction des modes de remplissage](#fill-modes-interaction)
-   [Détails de l’implémentation](#implementation-details)
-   [API summary](#api-summary)
-   [Rubriques connexes](#related-topics)

## <a name="overview"></a>Vue d’ensemble

La pixellisation conservatrice signifie que tous les pixels qui sont au moins partiellement couverts par une primitive rendue sont pixellisés, ce qui signifie que le nuanceur de pixels est appelé. Le comportement normal est l’échantillonnage, qui n’est pas utilisé si la pixellisation conservatrice est activée.

La pixellisation conservatrice est utile dans un certain nombre de situations, notamment pour garantir la détection des collisions, l’élimination des occlusions et le rendu en mosaïque.

Par exemple, l’illustration suivante montre un triangle vert rendu à l’aide de la pixellisation conservatrice, tel qu’il apparaîtrait dans le rastériseur (autrement dit, en utilisant des coordonnées de sommets à virgule fixe 16,8). La zone brune est connue sous le nom de « région d’incertitude », une région conceptuelle qui représente les limites étendues du triangle, nécessaires pour garantir que la primitive dans le rastériseur est conservatrice en ce qui concerne les coordonnées de vertex à virgule flottante d’origine. Les carrés rouges à chaque vertex montrent comment la région d’incertitude est calculée : sous la forme d’un carré balayé.

Les grands carrés gris affichent les pixels qui seront rendus. Les carrés roses affichent les pixels affichés à l’aide de la « règle de haut en bas », qui entre en lecture lorsque le bord du triangle traverse le bord des pixels. Il peut y avoir des faux positifs (pixels définis qui ne devraient pas avoir été) que le système va normalement, mais pas toujours.

![règle en haut à gauche](images/conservative-rasterization-0.png)

## <a name="interactions-with-the-pipeline"></a>Interactions avec le pipeline

### <a name="rasterization-rules-interaction"></a>Interaction des règles de pixellisation

En mode de pixellisation conservateur, les règles de pixellisation s’appliquent de la même façon que lorsque le mode de pixellisation conservateur n’est pas activé avec des exceptions pour la règle de Top-Left, décrite ci-dessus et la couverture des pixels. 16,8 Fixed-Point la précision du rastériseur doit être utilisée.

Les pixels qui ne seraient pas couverts si le matériel utilisait des coordonnées de vertex à virgule flottante complètes ne peuvent être inclus que s’ils se trouvent dans une région d’incertitude ne dépassant pas la moitié d’un pixel dans le domaine à virgule fixe. Le matériel futur devrait atteindre la région d’incertitude renforcée spécifiée dans le niveau 2. Notez que cette exigence empêche les triangles d’éclats de s’étendre davantage que nécessaire.

Une région d’incertitude valide similaire s’applique `InnerCoverage` également à, mais elle est plus stricte, car aucune implémentation ne nécessite une région d’incertitude plus importante pour ce cas. Pour plus d’informations, consultez [interaction InnerCoverage](#innercoverage-interaction) .

Les régions d’incertitude interne et externe doivent être supérieures ou égales à la taille de la moitié de la grille de sous-pixel, ou 1/512 d’un pixel, dans le domaine à virgule fixe. Il s’agit de la région d’incertitude minimale valide. 1/512 provient de la représentation de la coordonnée du rastériseur à virgule fixe 16,8 et de la règle d’arrondi à la valeur la plus proche qui s’applique lors de la conversion de coordonnées de vertex à virgule flottante à 16,8 coordonnées en virgule fixe. 1/512 peut changer si la précision du rastériseur change. Si une implémentation implémente cette zone d’incertitude minimale, elle doit suivre la règle Top-Left lorsqu’un bord ou un angle de la région d’incertitude se situe le long du bord ou de l’angle d’un pixel. Les bords détourés de la région d’incertitude doivent être traités comme le sommet le plus proche, ce qui signifie qu’elle est comptabilisée comme deux arêtes : les deux qui se joignent au vertex associé. Top-Left règle est nécessaire lorsque la région d’incertitude minimale est utilisée car si elle ne l’est pas, une implémentation de pixellisation conservatrice ne parviendrait pas à pixelliser les pixels qui pourraient être couverts lorsque le mode de pixellisation conservateur est désactivé.

Le diagramme suivant illustre une région d’incertitude externe valide produite en balayant un carré autour des bords de la primitive dans le domaine à virgule fixe (c’est-à-dire que les vertex ont été quantifiés par la représentation à virgule fixe 16,8). Les dimensions de ce carré sont basées sur la taille de la région d’incertitude externe valide : pour le 1/2 d’un pixel, le carré est de 1 pixel en largeur et en hauteur, pour 1/512 de pixel, le carré est 1/256 d’un pixel en largeur et en hauteur. Le triangle vert représente une primitive donnée, la ligne en pointillés rouge représente la limite d’une pixellisation conservatrice surestimée, les carrés noirs pleins représentent le carré qui est balayé le long des arêtes primitives, et la zone de vérification bleue représente la région d’incertitude externe :

![région d’incertitude externe.](images/outercoverage.jpg)

### <a name="multisampling-interaction"></a>Interaction d’échantillonnage multiple

Quel que soit le nombre d’échantillons dans / les surfaces renderTarget **DepthStencil** (ou si *ForcedSampleCount* est utilisé ou non), tous les échantillons sont couverts par des pixels pixellisés par une pixellisation conservatrice. Les exemples d’emplacements individuels ne sont pas testés pour déterminer s’ils sont dans la primitive ou non.

### <a name="samplemask-interaction"></a>Interaction SampleMask

L’état du rastériseur *SampleMask* s’applique de la même façon que lorsque la pixellisation conservatrice n’est pas activée pour `InputCoverage` , mais n’affecte pas `InnerCoverage` (c’est-à-dire qu’elle n’est pas AND’ed dans une entrée déclarée avec `InnerCoverage` ). Cela est dû `InnerCoverage` au fait que n’est pas lié au fait que les exemples MSAA sont masqués : 0 `InnerCoverage` signifie que le pixel n’est pas garanti être entièrement couvert, pas qu’aucun échantillon ne sera mis à jour.

### <a name="depthstencil-test-interaction"></a>Interaction de test de profondeur/stencil

Le test de profondeur/gabarit se poursuit par un pixel pixellisé de la même façon que si tous les échantillons sont couverts lorsque la pixellisation conservatrice n’est pas activée.

La poursuite de tous les exemples couverts peut entraîner une extrapolation de profondeur, qui est valide et doit être ancrée dans la fenêtre d’affichage comme spécifié lorsque la pixellisation conservatrice n’est pas activée. Cela est similaire au moment où les modes d’interpolation de fréquence en pixels sont utilisés sur un **renderTarget** avec un nombre d’échantillons supérieur à 1, bien que dans le cas d’une pixellisation conservatrice, il s’agit de la valeur de profondeur entrant dans le test de profondeur de fonction fixe qui peut être extrapolée.

Le comportement d’élimination des détails précoces avec l’extrapolation de profondeur n’est pas défini. Cela est dû au fait que certains matériels de réforme de profondeur précoce ne peuvent pas prendre en charge correctement les valeurs de profondeur extrapolées. Toutefois, le comportement de l’élimination précoce des détails en présence d’une extrapolation de profondeur est problématique même avec le matériel capable de prendre en charge des valeurs de profondeur extrapolées. Ce problème peut être contourné en conservant la profondeur d’entrée de nuanceur de pixels aux valeurs de profondeur minimale et maximale de la primitive en cours de pixellisation et en écrivant cette valeur sur `oDepth` (registre de profondeur de sortie du nuanceur de pixels). Les implémentations sont nécessaires pour désactiver l’élimination des détails précoces dans ce cas, en raison de l' `oDepth` écriture.

### <a name="helper-pixel-interaction"></a>Interaction des pixels d’assistance

Les règles de pixels d’assistance s’appliquent de la même façon que lorsque la pixellisation conservatrice n’est pas activée. Dans ce cas, tous les pixels, y compris les pixels d’assistance, doivent signaler `InputCoverage` correctement comme indiqué dans la `InputCoverage` section interaction. Par conséquent, les pixels entièrement non couverts sont couverts par le rapport 0.

### <a name="output-coverage-interaction"></a>Interaction de couverture de sortie

La couverture de sortie ( `oMask` ) se comporte pour un pixel pixellisé de manière conservatrice comme c’est le cas lorsque la pixellisation conservatrice n’est pas activée avec tous les exemples couverts.

### <a name="inputcoverage-interaction"></a>Interaction InputCoverage

En mode de pixellisation conservateur, ce registre d’entrée est rempli comme si tous les échantillons étaient couverts lorsque la pixellisation conservatrice n’est pas activée pour un pixel pixellisé de manière conservatrice. Autrement dit, toutes les interactions existantes s’appliquent (par exemple, *SampleMask* est appliqué), et les n premiers bits dans `InputCoverage` à partir du LSB sont définis sur 1 pour un pixel pixellisé de manière conservatrice, à partir d’un échantillon n par pixel **renderTarget** et/ou de la mémoire tampon **DepthStencil** liée à la **fusion de sortie**, ou d’un exemple n *ForcedSampleCount*. Le reste des bits est 0.

Cette entrée est disponible dans un nuanceur, indépendamment de l’utilisation de la pixellisation conservatrice, bien que la pixellisation conservatrice modifie son comportement pour afficher uniquement tous les échantillons couverts (ou aucun pour les pixels d’assistance).

### <a name="innercoverage-interaction"></a>Interaction InnerCoverage

Cette fonctionnalité est requise par et uniquement disponible dans le niveau 3. Le runtime ne peut pas créer de nuanceur pour les nuanceurs qui utilisent ce mode lorsqu’une implémentation prend en charge un niveau inférieur au niveau 3.

Le nuanceur de pixels a un système entier scalaire 32 bits générer une valeur disponible : `InnerCoverage` . Il s’agit d’un champ de bits dont le bit 0 de la LSB a la valeur 1 pour un pixel pixellisé de façon conservatrice, uniquement lorsque ce pixel est garanti être entièrement à l’intérieur de la primitive actuelle. Tous les autres bits de registre d’entrée doivent avoir la valeur 0 lorsque le bit 0 n’est pas défini, mais qu’ils ne sont pas définis lorsque le bit 0 a la valeur 1 (fondamentalement, ce champ de bits représente une valeur booléenne où false doit être exactement 0, mais true peut être n’importe quelle valeur non nulle). Cette entrée est utilisée pour les informations de pixellisation conservatrice sous-estimées. Il informe le nuanceur de pixels si le pixel actuel se trouve entièrement à l’intérieur de la géométrie.

Cela doit tenir compte de l’erreur d’alignement au niveau de la résolution supérieure ou égale à celle du dessin actuel. Il ne doit pas y avoir de faux positifs (en définissant `InnerCoverage` les bits lorsque le pixel n’est pas entièrement couvert par une erreur d’alignement au niveau de la résolution supérieure ou égale à la résolution à laquelle le dessin actuel fonctionne), mais les faux négatifs sont autorisés. En résumé, l’implémentation ne doit pas identifier de manière incorrecte les pixels comme étant entièrement couverts, ce qui ne serait pas le cas des coordonnées de vertex à virgule flottante complètes dans le rastériseur.

Les pixels qui seraient entièrement couverts si le matériel utilisait des coordonnées de vertex à virgule flottante complètes ne peuvent être omis que s’ils croisent la région d’incertitude interne, qui ne doit pas être supérieure à la taille de la grille de sous-pixel, ou 1/256 d’un pixel, dans le domaine à virgule fixe. Autrement dit, les pixels entièrement situés à l’intérieur de la limite interne de la région d’incertitude interne doivent être marqués comme étant entièrement couverts. La limite interne de la région d’incertitude est illustrée dans le diagramme ci-dessous par la ligne en pointillés noires en gras. 1/256 provient de la représentation de coordonnées de rastériseur à virgule fixe 16,8, qui peut changer si la précision du rastériseur change. Cette région d’incertitude est suffisante pour tenir compte de l’erreur d’alignement provoquée par la conversion de coordonnées de vertex à virgule flottante en coordonnées de vertex point fixe dans le rastériseur.

Les mêmes exigences de région d’incertitude minimale 1/512 définies dans l’interaction des règles de pixellisation s’appliquent également ici.

Le diagramme suivant illustre une région d’incertitude interne valide produite en balayant un carré autour des bords de la primitive dans le domaine à virgule fixe (c’est-à-dire que les vertex ont été quantifiés par la représentation à virgule fixe 16,8). Les dimensions de ce carré sont basées sur la taille de la région d’incertitude interne valide : pour 1/256 d’un pixel, le carré est 1/128 d’un pixel en largeur et en hauteur. Le triangle vert représente une primitive donnée, la ligne en pointillés noires en gras représente la limite de la région d’incertitude interne, les carrés noirs pleins représentent le carré qui est balayé le long des arêtes primitives, et la zone de vérification orange est la région d’incertitude interne :

![incertitude interne reqion.](images/innercoverage.jpg)

L’utilisation de `InnerCoverage` n’a pas d’incidence sur la pixellisation prudente d’un pixel, c’est-à-dire que l’utilisation de l’un de ces `InputCoverage` modes n’affecte pas les pixels pixellisés lorsque le mode de pixellisation conservateur est activé. Par conséquent, lorsque `InnerCoverage` est utilisé et que le nuanceur de pixels traite un pixel qui n’est pas entièrement couvert par la géométrie, sa valeur est 0, mais l’appel du nuanceur de pixels aura des exemples mis à jour. Cela diffère de lorsque `InputCoverage` a la valeur 0, ce qui signifie qu’aucun échantillon ne sera mis à jour.

Cette entrée s’exclut mutuellement avec `InputCoverage` : les deux ne peuvent pas être utilisés.

Pour accéder à `InnerCoverage` , il doit être déclaré en tant que composant unique de l’un des registres d’entrée de nuanceur de pixels. Le mode d’interpolation sur la déclaration doit être constant (l’interpolation ne s’applique pas).

Le `InnerCoverage` champ de bits n’est pas affecté par les tests de profondeur/stencil et n’est pas non plus liés avec l’état du rastériseur *SampleMask* .

Cette entrée est valide uniquement en mode de pixellisation conservateur. Lorsque la pixellisation conservatrice n’est pas activée, `InnerCoverage` produit une valeur non définie.

Les appels de nuanceur de pixels provoqués par le besoin de pixels d’assistance, mais non couverts par la primitive, doivent avoir le `InnerCoverage` Registre défini sur 0.

### <a name="attribute-interpolation-interaction"></a>Interaction d’interpolation d’attribut

Les modes d’interpolation d’attribut sont inchangés et se poursuivent de la même façon que lorsque la pixellisation conservatrice n’est pas activée, où les sommets de la fenêtre d’affichage et les vertex convertis à virgule fixe sont utilisés. Étant donné que tous les échantillons dans un pixel pixellisé de manière conservatrice sont considérés comme couverts, il est valide pour les valeurs qui sont extrapolées, comme lorsque les modes d’interpolation de fréquence des pixels sont utilisés sur un **renderTarget** avec un nombre d’échantillons supérieur à 1. Les modes d’interpolation de l’un de ces types produisent des résultats identiques au mode d’interpolation non-Centre de gravité correspondant. la notion de centre de gravité n’a pas de sens dans ce scénario, où la couverture de l’échantillon est uniquement complète ou 0.

La pixellisation conservatrice permet de dégénérer des triangles pour produire des appels de nuanceur de pixels. par conséquent, les triangles dégénérées doivent utiliser les valeurs assignées au vertex 0 pour toutes les valeurs interpolées.

### <a name="clipping-interaction"></a>Interaction du découpage

Lorsque le mode de pixellisation conservateur est activé et que le clip de profondeur est désactivé (lorsque l’état du rastériseur *DepthClipEnable* est défini sur false), il peut y avoir des variances dans l’interpolation d’attribut pour les segments d’une primitive qui se trouvent en dehors de la plage 0 <= z <= w, en fonction de l’implémentation : les valeurs constantes sont utilisées à partir d’un point où la primitive croise le plan approprié (proche ou loin), ou l’interpolation d’attribut se comporte comme lorsque le mode de pixellisation conservateur est désactivé Toutefois, le comportement de la valeur de profondeur est le même quel que soit le mode de pixellisation conservateur, c’est-à-dire que les primitives qui se trouvent en dehors de la plage de profondeur doivent toujours recevoir la valeur de la limite la plus proche de la plage de profondeur de la fenêtre d’affichage. Le comportement d’interpolation d’attribut à l’intérieur de la plage 0 <= z <= w doit rester inchangé.

### <a name="clip-distance-interaction"></a>Interaction de la distance du clip

La distance du clip est valide lorsque le mode de pixellisation conservateur est activé et qu’il se comporte pour un pixel pixellisé de manière conservatrice, comme c’est le cas lorsque la pixellisation conservatrice n’est pas activée avec tous les exemples couverts.

Notez que la pixellisation conservatrice peut entraîner l’extrapolation de la coordonnée de sommet W, ce qui peut entraîner une <= 0. Cela peut entraîner des implémentations de distance par point par pixel sur une distance de découpage qui a été divisée par une valeur W non valide. Les implémentations de distance de découpage doivent empêcher l’appel de la pixellisation pour les pixels où la coordonnée de vertex W <= 0 (par exemple, en raison de l’extrapolation en mode de pixellisation conservateur).

### <a name="target-independent-rasterization-interaction"></a>Interaction de pixellisation indépendante cible

Le mode de pixellisation conservateur est compatible avec le mode de rastérisation cible (TIR). Les règles et restrictions TIR s’appliquent à un pixel pixellisé de manière conservatrice comme si tous les échantillons sont couverts.

### <a name="ia-primitive-topology-interaction"></a>Interaction de la topologie de la primitive IA

La pixellisation conservatrice n’est pas définie pour les primitives de ligne ou de point. Par conséquent, les topologies de primitive qui spécifient des points ou des lignes produisent un comportement indéfini s’ils sont acheminés vers l’unité de rastérisation lorsque la pixellisation conservatrice est activée.

La validation de la couche de débogage vérifie que les applications n’utilisent pas ces topologies de Primitives.

### <a name="query-interaction"></a>Interroger l’interaction

Pour un pixel pixellisé de manière conservatrice, les requêtes se comportent comme elles le font quand la pixellisation conservatrice n’est pas activée lorsque tous les échantillons sont couverts. Par exemple, pour un pixel pixellisé, le \_ type de requête D3D12 \_ \_ occlusion et les \_ \_ \_ statistiques de pipeline \_ de type de requête D3D12 (à partir du [**\_ \_ type de requête D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_query_type)) doivent se comporter comme lorsque la pixellisation conservatrice n’est pas activée lorsque tous les échantillons sont couverts.

Les appels de nuanceur de pixels doivent être incrémentés pour chaque pixel pixellisé de manière conservatrice en mode de pixellisation conservateur.

### <a name="cull-state-interaction"></a>Élimination de l’interaction de l’État

Tous les États de réforme sont valides en mode de pixellisation prudent et suivent les mêmes règles que lorsque la pixellisation conservatrice n’est pas activée.

Lorsque vous comparez la pixellisation conservatrice entre les résolutions à elle-même ou si la pixellisation conservatrice n’est pas activée, il est possible que certaines primitives soient incompatibles (c’est-à-dire une face arrière, l’autre face avant). Les applications peuvent éviter cette incertitude en utilisant \_ \_ le mode \_ d’élimination D3D12 aucun ( [**\_ \_ en mode d’élimination D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_cull_mode)) et sans utiliser la valeur générée par le `IsFrontFace` système.

### <a name="isfrontface-interaction"></a>Interaction IsFrontFace

La `IsFrontFace` valeur générée par le système est valide pour une utilisation en mode de pixellisation prudent et suit le comportement défini lorsque la pixellisation conservatrice n’est pas activée.

### <a name="fill-modes-interaction"></a>Interaction des modes de remplissage

Le seul [**mode de \_ remplissage \_ D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_fill_mode) valide pour la pixellisation conservatrice est D3D12 \_ Fill \_ Solid, tout autre mode de remplissage est un paramètre non valide pour l’état du rastériseur.

Cela est dû au fait que la spécification fonctionnelle D3D12 spécifie que le mode de remplissage filaire doit convertir les bords de triangle en lignes et suivre les règles de pixellisation de ligne et le comportement de pixellisation de ligne conservateur n’a pas été défini.

## <a name="implementation-details"></a>Informations d’implémentation

Le type de pixellisation pris en charge dans Direct3D 12 est parfois appelé « pixellisation conservatrice préestimée ». Il existe également le concept de « pixellisation conservatrice sous-estimée », ce qui signifie que seuls les pixels entièrement couverts par une primitive rendue sont pixellisés. Les informations de pixellisation conservatrice sous-estimée sont disponibles via le nuanceur de pixels par le biais de l’utilisation de données de couverture d’entrée, et seule une pixellisation conservatrice surestimée est disponible en mode de pixellisation.

Si une partie d’une primitive chevauche un pixel, ce pixel est considéré comme couvert et est ensuite pixellisé. Lorsqu’un bord ou un angle d’une primitive se trouve le long du bord ou de l’angle d’un pixel, l’application de la « règle de haut en bas » est spécifique à l’implémentation. Toutefois, pour les implémentations qui prennent en charge les triangles dégénérées, un triangle dégenerate sur un bord ou un angle doit couvrir au moins un pixel.

Les implémentations de pixellisation conservatrices peuvent varier sur un matériel différent et produisent des faux positifs, ce qui signifie qu’ils peuvent incorrectement décider que les pixels sont couverts. Cela peut être dû à des détails spécifiques à l’implémentation, tels que des erreurs de culture ou d’accrochage primitives inhérentes aux coordonnées de vertex à virgule fixe utilisées dans la pixellisation. La raison pour laquelle les faux positifs (en ce qui concerne les coordonnées de vertex à virgule fixe) sont valides est parce qu’une certaine quantité de faux positifs sont nécessaires pour permettre à une implémentation d’effectuer une évaluation de la couverture sur des sommets postérieurs à l’alignement (c’est-à-dire des coordonnées de vertex qui ont été converties de la virgule flottante en virgule flottante de 16,8

Les implémentations de pixellisation conservatrice ne produisent pas de faux négatifs en ce qui concerne les coordonnées de vertex à virgule flottante pour les primitives postérieures à la dégénération : si une partie d’une primitive chevauche une partie d’un pixel, ce pixel est pixellisé.

Les triangles dégénérées (doublons d’index dans une mémoire tampon d’index ou colinéaire en 3D) ou dégénérées après la conversion à virgule fixe (vertex colinéaires dans le rastériseur) peuvent être éliminés ou non ; les deux sont des comportements valides. Les triangles dégénérées doivent être considérés comme étant en arrière. ainsi, si un comportement spécifique est requis par une application, il peut utiliser l’élimination des faces arrière ou les tests pour les faces avant. Les triangles dégénérées utilisent les valeurs affectées au vertex 0 pour toutes les valeurs interpolées.

Il existe trois niveaux de prise en charge matérielle, en plus de la possibilité que le matériel ne prenne pas en charge cette fonctionnalité.

-   Le niveau 1 applique une région d’incertitude maximale de 1/2 pixels et ne prend pas en charge les Dégénérations postérieures à l’accrochage. Cela est utile pour le rendu en mosaïque, un Atlas de textures, la génération de cartes de lumière et les mappages d’ombre sous-pixel.
-   Le niveau 2 réduit la zone d’incertitude maximale à 1/256 et nécessite que les Dégénérations postérieures à l’accrochage ne soient pas éliminées. Ce niveau est utile pour l’accélération de l’algorithme basé sur le processeur (par exemple, voxelization).
-   Le niveau 3 conserve une région d’incertitude maximale de 1/256 et ajoute la prise en charge de la couverture d’entrée interne. La couverture d’entrée interne ajoute la nouvelle valeur `SV_InnerCoverage` au langage HLSL (High Level Shading Language). Il s’agit d’un entier scalaire 32 bits qui peut être spécifié à l’entrée d’un nuanceur de pixels, et représente les informations de pixellisation conservatrice sous-estimées (autrement dit, si un pixel est garanti comme étant entièrement couvert). Ce niveau est utile pour l’élimination des occlusions.

## <a name="api-summary"></a>Résumé des API

Les méthodes, structures, énumérations et classes d’assistance suivantes font référence à la pixellisation conservatrice :

-   [**D3D12 \_ RASTÉRISEUR \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rasterizer_desc) : structure contenant la description du rastériseur.
-   [**D3D12 \_ \_ \_ Mode de pixellisation conservateur**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_conservative_rasterization_mode) : valeurs enum pour le mode (on ou OFF).
-   [**D3D12 \_ \_ \_ \_ Options D3D12 données**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options) de la fonctionnalité : structure contenant le niveau de prise en charge.
-   [**D3D12 \_ \_ \_ Niveau de pixellisation conservateur**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_conservative_rasterization_tier) : valeurs d’énumération pour chaque niveau de prise en charge par le matériel.
-   [**CheckFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport) : méthode permettant d’accéder aux fonctionnalités prises en charge.
-   [**CD3DX12 \_ RASTÉRISEUR \_ desc**](cd3dx12-rasterizer-desc.md) : classe d’assistance pour la création de descriptions de rastériseur.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Didacticiels vidéo sur DirectX Advanced Learning : pixellisation conservatrice](https://www.youtube.com/watch?v=zL0oSY_YmDY)
</dt> <dt>

[Affichages ordonnés du rastériseur](rasterizer-order-views.md)
</dt> <dt>

[Rendu](rendering.md)
</dt> </dl>

 

 




