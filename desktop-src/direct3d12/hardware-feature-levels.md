---
title: Niveaux de fonctionnalité matérielle
description: Décrit les fonctionnalités des niveaux de \_ fonctionnalité matérielle de 11 0 à 12 \_ 1.
ms.assetid: B8304E29-A532-464E-8FAF-075228D8FB73
keywords:
- Niveau de fonctionnalité DX
- Niveau de fonctionnalité DirectX
- niveau de fonctionnalité, DX
- niveau de fonctionnalité, DirectX
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d464f6cc52539e31fee5e234af2c045dfff7e413
ms.sourcegitcommit: 218b1ff779402c3ebe1786679e1aa80a5c0d6c95
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/01/2020
ms.locfileid: "104548493"
---
# <a name="hardware-feature-levels"></a>Niveaux de fonctionnalité matérielle

Décrit les fonctionnalités des niveaux de \_ fonctionnalité matérielle de 11 0 à 12 \_ 1.

-   [Systèmes de numérotation](#numbering-systems)
-   [Support au niveau des fonctionnalités](#feature-level-support)
-   [Prise en charge du matériel pour les formats DXGI](#hardware-support-for-dxgi-formats)
-   [Rubriques connexes](#related-topics)

Pour gérer la diversité des cartes vidéo dans les machines nouvelles et existantes, Microsoft Direct3D 11 a introduit le concept de niveaux de fonctionnalité. Chaque carte vidéo implémente un certain niveau de fonctionnalité Microsoft DirectX (DX) en fonction des unités de traitement graphique (GPU) installées. Un niveau de fonctionnalité est un ensemble bien défini de fonctionnalités GPU. Par exemple, le \_ niveau de fonctionnalité 11 0 implémente les fonctionnalités qui ont été implémentées dans Direct3D 11.

Désormais, lorsque vous créez un appareil, vous pouvez essayer de créer un appareil pour le niveau de fonctionnalité que vous souhaitez demander. Si la création de l’appareil fonctionne, ce niveau de fonctionnalité existe. si ce n’est pas le cas, le matériel ne prend pas en charge ce niveau de fonctionnalité. Vous pouvez essayer de recréer un appareil à un niveau de fonctionnalité inférieur, ou vous pouvez choisir de quitter l’application.

Les propriétés de base des niveaux de fonctionnalité sont les suivantes :

-   Tous les pilotes Direct3D 12 seront de niveau fonctionnalité 11 \_ 0 ou plus.
-   Un GPU qui autorise la création d’un périphérique atteint ou dépasse les fonctionnalités de ce niveau de fonctionnalité.
-   Un niveau de fonctionnalité comprend toujours les fonctionnalités des niveaux de fonctionnalité précédents ou inférieurs.
-   Un niveau de fonctionnalité n’implique pas les performances, mais uniquement les fonctionnalités. Les performances dépendent de l’implémentation matérielle.
-   Un niveau de fonctionnalité est choisi quand vous appelez [**D3D12CreateDevice**](/windows/desktop/api/d3d12/nf-d3d12-d3d12createdevice).
-   Pour plus d’informations sur les fonctionnalités prises en charge (notamment celles marquées comme étant *facultatives* dans le tableau ci-dessous, ce qui signifie que le matériel peut prendre en charge la fonctionnalité mais n’est pas obligatoire) appeler [**CheckFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport).

Pour plus d’informations sur les limitations de la création d’appareils de type non-matériel sur certains niveaux de fonctionnalité, consultez [limitations création de périphériques de déformation et de référence](/windows/desktop/direct3d11/overviews-direct3d-11-devices-limitations). Pour plus d’informations sur l’introduction des niveaux de fonctionnalités, reportez-vous à la documentation de Direct3D 11 sur les [niveaux de fonctionnalité Direct3D](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro).

## <a name="numbering-systems"></a>Systèmes de numérotation

Les niveaux de fonctionnalité matérielle ne sont *pas* les mêmes que les versions d’API. Par exemple, il existe une API D3D 11.3, mais il n’existe pas de \_ niveau de fonctionnalité matérielle 11 3. Les niveaux de fonctionnalité sont définis dans l’énumération de [**\_ \_ niveau de fonctionnalité D3D**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_feature_level) .

Il existe trois systèmes de numérotation distincts :

-   Les versions Direct3D utilisent un point ; par exemple, Direct3D 12,0.
-   Les modèles de nuanceur utilisent une période ; par exemple, le modèle de nuanceur 5,1.
-   Les niveaux de fonctionnalité utilisent un trait de soulignement ; par exemple, le niveau de fonctionnalité est 12 \_ 0.

## <a name="feature-level-support"></a>Support au niveau des fonctionnalités

Les fonctionnalités suivantes sont disponibles pour chaque niveau de fonctionnalité Direct3D.

Les en-têtes sur la ligne supérieure sont des niveaux de fonctionnalité Direct3D. Les en-têtes de la colonne de gauche sont des fonctionnalités.



| Niveau de fonctionnalité de fonctionnalité \\                                                                                                 | 12 \_ 1 ⁰                    | 12 \_ 0 ⁰                    | 11 \_ 1 ¹                   | 11 \_ 0                    |
|--------------------------------------------------------------------------------------------------------------------------|---------------------------|---------------------------|--------------------------|--------------------------|
| Modèle de nuanceur                                                                                                             | 5,1                       | 5,1                       | 5,1 ²                     | 5,1 ²                     |
| [Niveau de liaison des ressources](hardware-support.md)                                                                            | Niveau2 ³                    | Niveau2 ³                    | 1 to ³                   | 1 to ³                   |
| [Ressources en mosaïque](/windows/desktop/api/d3d12/ne-d3d12-d3d12_tiled_resources_tier)                                                                        | Niveau2 ³                    | Niveau2 ³                    | Facultatif                 | Facultatif                 |
| [Pixellisation conservatrice](conservative-rasterization.md)                                                             | 1 to ³                    | Facultatif                  | Facultatif                 | Non                       |
| [Affichages ordonnés du rastériseur](rasterizer-order-views.md)                                                                   | Oui                       | Facultatif                  | Facultatif                 | Non                       |
| [Filtres min/max](/windows/desktop/api/d3d12/ne-d3d12-d3d12_filter)                                                                                      | Oui                       | Oui                       | Facultatif                 | Non                       |
| Mapper la mémoire tampon par défaut                                                                                                       | Facultatif                  | Facultatif                  | Facultatif                 | Facultatif                 |
| [Valeur de référence du stencil spécifié par le nuanceur](shader-specified-stencil-reference-value.md)                                 | Facultatif                  | Facultatif                  | Facultatif                 | Non                       |
| [Chargements de vues d’accès non ordonnées typées](typed-unordered-access-view-loads.md)                                               | 18 formats, plus facultatif | 18 formats, plus facultatif | 3 formats, plus facultatifs | 3 formats, plus facultatifs |
| [Nuanceur de géométrie](/previous-versions//bb205146(v=vs.85)) | Oui                       | Oui                       | Oui                      | Oui                      |
| [Diffuser en continu](/windows/desktop/direct3d11/d3d10-graphics-programming-guide-output-stream-stage)                                            | Oui                       | Oui                       | Oui                      | Oui                      |
| [Nuanceur de DirectCompute/Compute](/windows/desktop/direct3d11/direct3d-11-advanced-stages-compute-shader)                                  | Oui                       | Oui                       | Oui                      | Oui                      |
| [Nuanciers de la coque et du domaine](/windows/desktop/direct3d11/direct3d-11-advanced-stages-tessellation)                                           | Oui                       | Oui                       | Oui                      | Oui                      |
| [Tableaux de ressources de texture](/windows/desktop/direct3d11/overviews-direct3d-11-resources-textures-intro)                                     | Oui                       | Oui                       | Oui                      | Oui                      |
| [Carte cubique des groupes de ressources](/windows/desktop/direct3d11/overviews-direct3d-11-resources-textures-intro)                                     | Oui                       | Oui                       | Oui                      | Oui                      |
| [Compression BC1 à BC7](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-block-compression)                        | Oui                       | Oui                       | Oui                      | Oui                      |
| [Alpha-à-couverture](/windows/desktop/direct3d11/d3d10-graphics-programming-guide-blend-state)         | Oui                       | Oui                       | Oui                      | Oui                      |
| [Opérations logiques (fusion de sortie)](/windows/desktop/api/d3d11/ns-d3d11-d3d11_feature_data_d3d11_options)                                          | Oui                       | Oui                       | Oui                      | Facultatif                 |
| Pixellisation indépendante de la cible                                                                                         | Oui                       | Oui                       | Oui                      | Non                       |
| [Plusieurs cibles de rendu (MRT) avec ForcedSampleCount 1](/windows/desktop/api/d3d11/ns-d3d11-d3d11_feature_data_d3d11_options)                      | Oui                       | Oui                       | Oui                      | Facultatif                 |
| [Nombre maximal d’échantillons forcés pour le rendu UAV uniquement](/windows/desktop/api/d3d11/ns-d3d11-d3d11_feature_data_d3d11_options)                            | 16                        | 16                        | 16                       | 8                        |
| Dimension de texture max.                                                                                                    | 16384                     | 16384                     | 16384                    | 16384                    |
| Dimension carte cubique max.                                                                                                    | 16384                     | 16384                     | 16384                    | 16384                    |
| Étendue de volume max.                                                                                                        | 2 048                      | 2 048                      | 2 048                     | 2 048                     |
| Répétition de la texture max.                                                                                                       | 16384                     | 16384                     | 16384                    | 16384                    |
| Anisotrope max.                                                                                                           | 16                        | 16                        | 16                       | 16                       |
| Nombre maximal de primitives                                                                                                      | 2 ^ 32 – 1                  | 2 ^ 32 – 1                  | 2 ^ 32 – 1                 | 2 ^ 32 – 1                 |
| Index de vertex max.                                                                                                         | 2 ^ 32 – 1                  | 2 ^ 32 – 1                  | 2 ^ 32 – 1                 | 2 ^ 32 – 1                 |
| Nombre maximal d’emplacements d’entrée                                                                                                          | 32                        | 32                        | 32                       | 32                       |
| Cibles de rendu simultanées                                                                                              | 8                         | 8                         | 8                        | 8                        |
| Requêtes d’occlusion                                                                                                        | Oui                       | Oui                       | Oui                      | Oui                      |
| Fusion alpha distincte                                                                                                     | Oui                       | Oui                       | Oui                      | Oui                      |
| Miroir une seule fois                                                                                                              | Oui                       | Oui                       | Oui                      | Oui                      |
| Chevauchement d’éléments vertex                                                                                              | Oui                       | Oui                       | Oui                      | Oui                      |
| Masques d’écriture indépendants                                                                                                  | Oui                       | Oui                       | Oui                      | Oui                      |
| Instancing                                                                                                               | Oui                       | Oui                       | Oui                      | Oui                      |



 

-   ⁰ requiert le runtime Direct3D 11,3 ou Direct3D 12.
-   ¹ requiert le runtime Direct3D 11,1.
-   le modèle de nuanceur ² 5,0 peut éventuellement prendre en charge les nuanceurs à double précision, les nuanceurs à double précision étendus, l’instruction de nuanceur **SAD4** et les nuanceurs de précision partielle. Pour déterminer les options du modèle de nuanceur 5,0 disponibles, appelez [**ID3D12Device :: CheckFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport). Une certaine compatibilité dépend du matériel sur lequel vous exécutez : le modèle de nuanceur 5,1 est uniquement pris en charge sur le matériel qui prend en charge l’API DirectX 12, quel que soit le niveau de fonctionnalité utilisé. Le matériel DirectX 11 ne prend en charge que le modèle de nuanceur 5,0. L’API DirectX 12 ne descend que jusqu’au niveau de la fonctionnalité 11 \_ 0.
-   ³ les niveaux supérieurs sont facultatifs.
-   Les niveaux de fonctionnalité 12 \_ 0 et 12 \_ 1 nécessitent le runtime Direct3D 11,3 ou Direct3D 12.
-   Le niveau de fonctionnalité 11 \_ 1 nécessite le runtime Direct3D 11,1.
-   Le niveau de fonctionnalité 11 \_ 0 requiert le runtime Direct3D 11,0.

## <a name="hardware-support-for-dxgi-formats"></a>Prise en charge du matériel pour les formats DXGI

Pour afficher les tables de formats DXGI et les fonctionnalités matérielles, consultez :

-   [Prise en charge du format DXGI pour le matériel de niveau de fonctionnalité Direct3D 12,1](/windows/desktop/direct3ddxgi/hardware-support-for-direct3d-12-1-formats)
-   [Prise en charge du format DXGI pour le matériel de niveau de fonctionnalité Direct3D 12,0](/windows/desktop/direct3ddxgi/hardware-support-for-direct3d-12-0-formats)
-   [Prise en charge du format DXGI pour le matériel de niveau de fonctionnalité Direct3D 11,1](/windows/desktop/direct3ddxgi/format-support-for-direct3d-11-1-feature-level-hardware)
-   [Prise en charge du format DXGI pour le matériel de niveau de fonctionnalité Direct3D 11,0](/windows/desktop/direct3ddxgi/format-support-for-direct3d-11-0-feature-level-hardware)
-   [Prise en charge matérielle pour les formats Direct3D 10Level9](/previous-versions//ff471324(v=vs.85))
-   [Prise en charge du matériel pour les formats Direct3D 10,1](/previous-versions//cc627091(v=vs.85))
-   [Prise en charge matérielle pour les formats Direct3D 10](/previous-versions//cc627090(v=vs.85))

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Interrogation des fonctionnalités](capability-querying.md)
</dt> <dt>

[Comprendre Direct3D 12](directx-12-getting-started.md)
</dt> </dl>

 

 
