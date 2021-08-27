---
title: Niveaux de fonctionnalités Direct3D
description: Cette rubrique traite des niveaux de fonctionnalité Direct3D.
ms.assetid: 5ad0525c-249f-452d-950b-df8fa2addde2
keywords:
- Niveau de fonctionnalité DX
- Niveau de fonctionnalité DirectX
- niveau de fonctionnalité, DX
- niveau de fonctionnalité, DirectX
ms.topic: article
ms.date: 09/01/2020
ms.openlocfilehash: e1ca80faa816ff7601f0a33893a708fafa7f2d3f
ms.sourcegitcommit: 0dec0044816af3f2b2e6403659e1cf11138c90cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/13/2021
ms.locfileid: "121812045"
---
# <a name="direct3d-feature-levels"></a>Niveaux de fonctionnalités Direct3D

> [!NOTE]
> **Certaines informations portent sur la préversion du produit, qui est susceptible d’être en grande partie modifié avant sa commercialisation. Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.**

Pour gérer la diversité des cartes vidéo dans les machines nouvelles et existantes, Microsoft Direct3D 11 introduit le concept de niveaux de fonctionnalité. Cette rubrique traite des niveaux de fonctionnalité Direct3D.

Chaque carte vidéo implémente un certain niveau de fonctionnalité Microsoft DirectX (DX) en fonction des unités de traitement graphique (GPU) installées. Dans les versions antérieures de Microsoft Direct3D, vous pouviez découvrir la version de Direct3D mise en œuvre par la carte vidéo, puis programmer votre application en conséquence.

Avec Direct3D 11, un nouveau paradigme est présenté sous le nom des niveaux de fonctionnalité. Un niveau de fonctionnalité est un ensemble de fonctionnalités GPU définies. Par exemple, le \_ niveau de fonctionnalité 9 1 implémente les fonctionnalités qui ont été implémentées dans Microsoft Direct3D 9, qui expose les fonctionnalités des modèles de nuanceur [PS \_ 2 \_ x](../direct3dhlsl/dx9-graphics-reference-asm-ps-2-x.md) et [vs \_ 2 \_ x](../direct3dhlsl/dx9-graphics-reference-asm-vs-2-x.md), tandis que le \_ niveau de fonctionnalité 11 0 implémente les fonctionnalités qui ont été implémentées dans Direct3D 11.

Désormais, lorsque vous créez un appareil, vous pouvez essayer de créer un appareil pour le niveau de fonctionnalité que vous souhaitez demander. Si la création de l’appareil fonctionne, ce niveau de fonctionnalité existe. si ce n’est pas le cas, le matériel ne prend pas en charge ce niveau de fonctionnalité. Vous pouvez essayer de recréer un appareil à un niveau de fonctionnalité inférieur, ou vous pouvez choisir de quitter l’application. Pour plus d’informations sur la création d’un appareil, consultez la fonction [**D3D11CreateDevice**](/windows/win32/api/D3D11/nf-d3d11-d3d11createdevice) .

À l’aide des niveaux de fonctionnalité, vous pouvez développer une application pour Direct3D 9, Microsoft Direct3D 10 ou Direct3D 11, puis l’exécuter sur du matériel 9, 10 ou 11 (à quelques exceptions près, par exemple, les nouvelles fonctionnalités de 11 ne seront pas exécutées sur une carte 9 existante). Voici quelques autres propriétés de base des niveaux de fonctionnalité :

- Un GPU qui autorise la création d’un périphérique atteint ou dépasse les fonctionnalités de ce niveau de fonctionnalité.
- Un niveau de fonctionnalité comprend toujours les fonctionnalités des niveaux de fonctionnalité précédents ou inférieurs.
- Un niveau de fonctionnalité n’implique pas les performances, mais uniquement les fonctionnalités. Les performances dépendent de l’implémentation matérielle.
- Choisissez un niveau de fonctionnalité lorsque vous créez un appareil Direct3D 11.

Pour plus d’informations sur les limitations de la création d’appareils de type non-dur sur certains niveaux de fonctionnalité, consultez [limitations création de périphériques de déformation et de référence](overviews-direct3d-11-devices-limitations.md).

Pour vous aider à choisir le niveau de fonctionnalité à utiliser pour la conception, comparez les fonctionnalités de chaque niveau de fonctionnalité.

La section de [référence 10Level9](d3d11-graphics-reference-10level9.md) répertorie les différences entre la façon dont les différentes méthodes [**ID3D11Device**](/windows/win32/api/D3D11/nn-d3d11-id3d11device) et [**ID3D11DeviceContext**](/windows/win32/api/D3D11/nn-d3d11-id3d11devicecontext) se comportent à différents niveaux de fonctionnalités 10Level9.

## <a name="formats-of-version-numbers"></a>Formats des numéros de version

Il existe trois formats pour les versions Direct3D, les modèles de nuanceur et les niveaux de fonctionnalité.

- Les versions Direct3D utilisent un point ; par exemple, Direct3D 12,0.
- Les modèles de nuanceur utilisent une période ; par exemple, le modèle de nuanceur 5,1.
- Les niveaux de fonctionnalité utilisent un trait de soulignement ; par exemple, le niveau de fonctionnalité est 12 \_ 0.

## <a name="feature-support-for-feature-levels-12_2-through-9_3"></a>Prise en charge des fonctionnalités des niveaux de fonctionnalité 12_2 à 9_3

Les fonctionnalités suivantes sont disponibles pour les niveaux de fonctionnalités répertoriés. Les en-têtes sur la ligne supérieure sont des niveaux de fonctionnalité Direct3D. Les en-têtes de la colonne de gauche sont des fonctionnalités. Consultez également [les notes de bas de page pour les tables](#footnotes-for-the-tables).

| Niveau de fonctionnalité de fonctionnalité \\ | 12 \_ 2<sup>8</sup> | 12 \_ 1<sup>0</sup> | 12 \_ 0<sup>0</sup> | 11 \_ 1<sup>1</sup> | 11 \_ 0 | 10 \_ 1 | 10 \_ 0 | 9 \_ 3<sup>7</sup> |
|-|-|-|-|-|-|-|-|-|
| Modèle de nuanceur (D3D11) | N/A | 5,0<sup>2</sup> | 5,0<sup>2</sup> | 5,0<sup>2</sup> | 5,0<sup>2</sup> | 4.x | 4.0 | 2,0 (4 \_ 0 \_ niveau \_ 9 \_ 3) \[ vs \_ 2 \_ a/PS \_ 2 \_ x \] <sup>5</sup> |
| Modèle de nuanceur (D3D12) | 6.5 | 5,1<sup>2</sup> | 5,1<sup>2</sup> | 5,1<sup>2</sup> | 5,1<sup>2</sup> | N/A | N/A | N/A |
| [Ressources en mosaïque](tiled-resources.md) | Niveau3 | Niveau2<sup>6</sup> | Niveau2<sup>6</sup> | Facultatif | Facultatif | Non | Non | Non |
| [Pixellisation conservatrice](conservative-rasterization.md) | Niveau3 | Niveau1<sup>6</sup> | Facultatif | Facultatif | Non | Non | Non | Non |
| [Vues de l’ordre du rastériseur](rasterizer-order-views.md) | Oui | Oui | Facultatif | Facultatif | Non | Non | Non | Non |
| [Filtres min/max](/windows/win32/api/D3D11/ne-d3d11-d3d11_filter) | Oui | Oui | Oui | Facultatif | Non | Non | Non | Non |
| Mapper la mémoire tampon par défaut | N/A | Facultatif | Facultatif | Facultatif | Facultatif | Non | Non | Non |
| [Valeur de référence du stencil spécifié par le nuanceur](shader-specified-stencil-reference-value.md) | Facultatif | Facultatif | Facultatif | Facultatif | Non | Non | Non | Non |
| Chargements de vues d’accès non ordonnées typées | 18 formats, plus facultatif | 18 formats, plus facultatif | 18 formats, plus facultatif | 3 formats, plus facultatifs | 3 formats, plus facultatifs | Non | Non | Non |
| [Nuanceur de géométrie](/previous-versions/bb205146(v=vs.85)) | Oui | Oui | Oui | Oui | Oui | Oui | Oui | Non |
| [Diffuser en continu](./d3d10-graphics-programming-guide-output-stream-stage.md) | Oui | Oui | Oui | Oui | Oui | Oui | Oui | Non |
| [Nuanceur de DirectCompute/Compute](direct3d-11-advanced-stages-compute-shader.md) | Oui | Oui | Oui | Oui | Oui | Facultatif | Facultatif | N/A |
| <b>Niveau de fonctionnalité de fonctionnalité \\</b> | <b>12 \_ 2<sup>8</sup></b> | <b>12 \_ 1<sup>0</sup></b> | <b>12 \_ 0<sup>0</sup></b> | <b>11 \_ 1<sup>1</sup></b> | <b>11 \_ 0</b> | <b>10 \_ 1</b> | <b>10 \_ 0</b> | <b>9 \_ 3<sup>7</sup></b> |
| [Nuanciers de la coque et du domaine](direct3d-11-advanced-stages-tessellation.md) | Oui | Oui | Oui | Oui | Oui | Non | Non | Non |
| [Tableaux de ressources de texture](overviews-direct3d-11-resources-textures-intro.md) | Oui | Oui | Oui | Oui | Oui | Oui | Oui | Non |
| [Carte cubique des groupes de ressources](overviews-direct3d-11-resources-textures-intro.md) | Oui | Oui | Oui | Oui | Oui | Oui | Non | Non |
| [Compression textures BC4/BC5](../direct3d10/d3d10-graphics-programming-guide-resources-block-compression.md) | Oui | Oui | Oui | Oui | Oui | Oui | Oui | Non |
| [Compression BC6H/BC7](texture-block-compression-in-direct3d-11.md) | Oui | Oui | Oui | Oui | Oui | Non | Non | Non |
| [Alpha-à-couverture](./d3d10-graphics-programming-guide-blend-state.md) | Oui | Oui | Oui | Oui | Oui | Oui | Oui | Non |
| [Formats étendus (BGRA, etc.)](overviews-direct3d-11-devices-downlevel-exceptions.md) | Oui | Oui | Oui | Oui | Oui | Facultatif | Facultatif | Oui |
| [Format de couleur XR 10 bits](overviews-direct3d-11-devices-downlevel-exceptions.md) | Oui | Oui | Oui | Oui | Oui | Facultatif | Facultatif | N/A |
| [Opérations logiques (fusion de sortie)](/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options) | Oui | Oui | Oui | Oui | Facultatif<sup>1</sup> | Facultatif<sup>1</sup> | Facultatif<sup>1</sup> | Non |
| Pixellisation indépendante de la cible | Oui | Oui | Oui | Oui | Non | Non | Non | Non |
| [Plusieurs cibles de rendu (MRT) avec ForcedSampleCount 1](/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options) | Oui | Oui | Oui | Oui | Facultatif<sup>1</sup> | Facultatif<sup>1</sup> | Facultatif<sup>1</sup> | Non |
| Emplacements UAV | <sup>9</sup> niveaux | 64 | 64 | 64 | 8 | 1 | 1 | N/A |
| <b>Niveau de fonctionnalité de fonctionnalité \\</b> | <b>12 \_ 2<sup>8</sup></b> | <b>12 \_ 1<sup>0</sup></b> | <b>12 \_ 0<sup>0</sup></b> | <b>11 \_ 1<sup>1</sup></b> | <b>11 \_ 0</b> | <b>10 \_ 1</b> | <b>10 \_ 0</b> | <b>9 \_ 3<sup>7</sup></b> |
| UAVs à chaque étape | Oui | Oui | Oui | Oui | Non | Non | Non | N/A |
| [Nombre maximal d’échantillons forcés pour le rendu UAV uniquement](/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options) | 16 | 16 | 16 | 16 | 8 | N/A | N/A | N/A |
| Décalage de la mémoire tampon constante et mises à jour partielles | Oui | Oui | Oui | Oui | Facultatif<sup>1</sup> | Facultatif<sup>1</sup> | Facultatif<sup>1</sup> | Oui<sup>1</sup> |
| formats 16 bits par pixel (BPP) | Oui | Oui | Oui | Oui | Facultatif<sup>1</sup> | Facultatif<sup>1</sup> | Facultatif<sup>1</sup> | Facultatif<sup>1</sup> |
| Dimension de texture max. | 16384 | 16384 | 16384 | 16384 | 16384 | 8 192 | 8 192 | 4096 |
| Dimension carte cubique max. | 16384 | 16384 | 16384 | 16384 | 16384 | 8 192 | 8 192 | 4096 |
| Étendue de volume max. | 2 048 | 2 048 | 2 048 | 2 048 | 2 048 | 2 048 | 2 048 | 256 |
| Répétition de la texture max. | 16384 | 16384 | 16384 | 16384 | 16384 | 8 192 | 8 192 | 8 192 |
| Anisotrope max. | 16 | 16 | 16 | 16 | 16 | 16 | 16 | 16 |
| Nombre maximal de primitives | 2 ^ 32 – 1 | 2 ^ 32 – 1 | 2 ^ 32 – 1 | 2 ^ 32 – 1 | 2 ^ 32 – 1 | 2 ^ 32 – 1 | 2 ^ 32 – 1 | 1048575 |
| Index de vertex max. | 2 ^ 32 – 1 | 2 ^ 32 – 1 | 2 ^ 32 – 1 | 2 ^ 32 – 1 | 2 ^ 32 – 1 | 2 ^ 32 – 1 | 2 ^ 32 – 1 | 1048575 |
| Nombre maximal d’emplacements d’entrée | 32 | 32 | 32 | 32 | 32 | 32 | 16 | 16 |
| Cibles de rendu simultanées | 8 | 8 | 8 | 8 | 8 | 8 | 8 | 4 |
| Requêtes d’occlusion | Oui | Oui | Oui | Oui | Oui | Oui | Oui | Oui |
| <b>Niveau de fonctionnalité de fonctionnalité \\</b> | <b>12 \_ 2<sup>8</sup></b> | <b>12 \_ 1<sup>0</sup></b> | <b>12 \_ 0<sup>0</sup></b> | <b>11 \_ 1<sup>1</sup></b> | <b>11 \_ 0</b> | <b>10 \_ 1</b> | <b>10 \_ 0</b> | <b>9 \_ 3<sup>7</sup></b> |
| Fusion alpha distincte | Oui | Oui | Oui | Oui | Oui | Oui | Oui | Oui |
| Miroir une seule fois | Oui | Oui | Oui | Oui | Oui | Oui | Oui | Oui |
| Chevauchement d’éléments vertex | Oui | Oui | Oui | Oui | Oui | Oui | Oui | Oui |
| Masques d’écriture indépendants | Oui | Oui | Oui | Oui | Oui | Oui | Oui | Oui |
| Instancing | Oui | Oui | Oui | Oui | Oui | Oui | Oui | Oui<sup>7</sup> |
| Non-puissance-de-2 conditionnelle-<sup>3</sup> | Non | Non | Non | Non | Non | Non | Non | Oui |
| Non-puissance-de-2 non conditionnelle<sup>4</sup> | Oui | Oui | Oui | Oui | Oui | Oui | Oui | Non |

## <a name="feature-support-for-feature-levels-9_2-and-9_1"></a>Prise en charge des fonctionnalités pour les niveaux de fonctionnalités 9_2 et 9_1

Les fonctionnalités suivantes sont disponibles pour les niveaux de fonctionnalités répertoriés. Les en-têtes sur la ligne supérieure sont des niveaux de fonctionnalité Direct3D. Les en-têtes de la colonne de gauche sont des fonctionnalités. Consultez également [les notes de bas de page pour les tables](#footnotes-for-the-tables).

| Niveau de fonctionnalité de fonctionnalité \\ | 9 \_ 2 | 9 \_ 1 |
|-|-|-|
| Modèle de nuanceur (D3D11) | 2,0 (4 \_ 0 \_ niveau \_ 9 \_ 1) | 2,0 (4 \_ 0 \_ niveau \_ 9 \_ 1) |
| Modèle de nuanceur (D3D12) | N/A | N/A |
| [Ressources en mosaïque](tiled-resources.md) | Non | Non |
| [Pixellisation conservatrice](conservative-rasterization.md) | Non | Non |
| [Vues de l’ordre du rastériseur](rasterizer-order-views.md) | Non | Non |
| [Filtres min/max](/windows/win32/api/D3D11/ne-d3d11-d3d11_filter) | Non | Non |
| Mapper la mémoire tampon par défaut | Non | Non |
| [Valeur de référence du stencil spécifié par le nuanceur](shader-specified-stencil-reference-value.md) | Non | Non |
| Chargements de vues d’accès non ordonnées typées | Non | Non |
| [Nuanceur de géométrie](/previous-versions/bb205146(v=vs.85)) | Non | Non |
| [Diffuser en continu](./d3d10-graphics-programming-guide-output-stream-stage.md) | Non | Non |
| [Nuanceur de DirectCompute/Compute](direct3d-11-advanced-stages-compute-shader.md) | N/A | N/A |
| [Nuanciers de la coque et du domaine](direct3d-11-advanced-stages-tessellation.md) | Non | Non |
| [Tableaux de ressources de texture](overviews-direct3d-11-resources-textures-intro.md) | Non | Non |
| [Carte cubique des groupes de ressources](overviews-direct3d-11-resources-textures-intro.md) | Non | Non |
| [Compression textures BC4/BC5](../direct3d10/d3d10-graphics-programming-guide-resources-block-compression.md) | Non | Non |
| <b>Niveau de fonctionnalité de fonctionnalité \\</b> | <b>9 \_ 2</b> | <b>9 \_ 1</b> |
| [Compression BC6H/BC7](texture-block-compression-in-direct3d-11.md) | Non | Non |
| [Alpha-à-couverture](./d3d10-graphics-programming-guide-blend-state.md) | Non | Non |
| [Formats étendus (BGRA, etc.)](overviews-direct3d-11-devices-downlevel-exceptions.md) | Oui | Oui |
| [Format de couleur XR 10 bits](overviews-direct3d-11-devices-downlevel-exceptions.md) | N/A | N/A |
| [Opérations logiques (fusion de sortie)](/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options) | Non | Non |
| Pixellisation indépendante de la cible | Non | Non |
| [Plusieurs cibles de rendu (MRT) avec ForcedSampleCount 1](/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options) | Non | Non |
| Emplacements UAV | N/A | N/A |
| UAVs à chaque étape | N/A | N/A |
| [Nombre maximal d’échantillons forcés pour le rendu UAV uniquement](/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options) | N/A | N/A |
| Décalage de la mémoire tampon constante et mises à jour partielles | Oui<sup>1</sup> | Oui<sup>1</sup> |
| formats 16 bits par pixel (BPP) | Facultatif<sup>1</sup> | Facultatif<sup>1</sup> |
| Dimension de texture max. | 2 048 | 2 048 |
| Dimension carte cubique max. | 512 | 512 |
| Étendue de volume max. | 256 | 256 |
| Répétition de la texture max. | 2 048 | 128 |
| <b>Niveau de fonctionnalité de fonctionnalité \\</b> | <b>9 \_ 2</b> | <b>9 \_ 1</b> |
| Anisotrope max. | 16 | 2 |
| Nombre maximal de primitives | 1048575 | 65535 |
| Index de vertex max. | 1048575 | 65534 |
| Nombre maximal d’emplacements d’entrée | 16 | 16 |
| Cibles de rendu simultanées | 1 | 1 |
| Requêtes d’occlusion | Oui | Non |
| Fusion alpha distincte | Oui | Non |
| Miroir une seule fois | Oui | Non |
| Chevauchement d’éléments vertex | Oui | Non |
| Masques d’écriture indépendants | Non | Non |
| Instancing | Non | Non |
| Non-puissance-de-2 conditionnelle-<sup>3</sup> | Oui | Oui |
| Non-puissance-de-2 non conditionnelle<sup>4</sup> | Non | Non |

## <a name="footnotes-for-the-tables"></a>Notes de bas de page pour les tables

<sup>0</sup> requiert le runtime Direct3D 11,3 ou Direct3D 12.

<sup>1</sup> nécessite le runtime Direct3D 11,1.

<sup>2</sup> le modèle de nuanceur 5,0 et versions ultérieures peuvent éventuellement prendre en charge des nuanceurs à double précision, des nuanceurs à double précision étendus, l’instruction de nuanceur **SAD4** et des nuanceurs de précision partielle. Pour déterminer les options du modèle de nuanceur 5,0 disponibles pour DirectX 11, appelez [**ID3D11Device :: CheckFeatureSupport**](/windows/win32/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport). Une certaine compatibilité dépend du matériel sur lequel vous exécutez. Le modèle de nuanceur 5,1 et versions ultérieures sont uniquement pris en charge via l’API DirectX 12, quel que soit le niveau de fonctionnalité utilisé. DirectX 11 prend uniquement en charge le modèle de nuanceur 5,0. L’API DirectX 12 ne descend que jusqu’au niveau de la fonctionnalité 11 \_ 0.

<sup>3</sup> au niveau des fonctionnalités 9 \_ 1, 9 \_ 2 et 9 \_ 3, le périphérique d’affichage prend en charge l’utilisation de textures 2D avec des dimensions qui ne sont pas des puissances de deux sous deux conditions. Tout d’abord, un seul niveau MIP-Map pour chaque texture peut être créé, et en second lieu, aucun mode d’échantillonnage de retour pour les textures n’est autorisé (autrement dit, les membres **addresse**, **AddressV** et **AddressW** de l' [**\_ échantillonneur d3d11 \_ desc**](/windows/win32/api/D3D11/ns-d3d11-d3d11_sampler_desc) ne peuvent pas être définis sur [**d3d11 \_ \_ Address texture \_ Wrap**](/windows/win32/api/D3D11/ne-d3d11-d3d11_texture_address_mode)).

<sup>4</sup> au niveau de la fonctionnalité 10 \_ 0, 10 \_ 1 et 11 \_ 0, le périphérique d’affichage prend en charge de manière inconditionnelle l’utilisation de textures 2D avec des dimensions qui ne sont pas des puissances de deux.

<sup>5</sup> vertex shader 2a avec 256 instructions, 32 registres temporaires, contrôle de workflow statique de profondeur 4, contrôle de workflow dynamique des prédicats de profondeur 24 et D3DVS20CAPS \_ . Nuanceur de pixels 2x avec 512 instructions, 32 registres temporaires, contrôle de workflow statique de profondeur 4, contrôle de workflow dynamique de profondeur 24, D3DPS20CAPS \_ ARBITRARYSWIZZLE, D3DPS20CAPS \_ GRADIENTINSTRUCTIONS, \_ prédicat D3DPS20CAPS, D3DPS20CAPS \_ NODEPENDENTREADLIMIT et D3DPS20CAPS NOTEXINSTRUCTIONLIMIT \_ .

<sup>6</sup> niveaux supérieurs facultatifs.

<sup>7</sup> pour les 9_3 au niveau des fonctionnalités, les seules méthodes de rendu prises en charge sont **Draw**, **DrawIndexed** et **DrawIndexInstanced**. De même, pour le niveau de fonctionnalité 9_3, le rendu de liste de points est pris en charge uniquement pour le rendu via **Draw**.

<sup>8</sup> requiert le runtime Direct3D 12.

<sup>9</sup> dans l’API Direct3D 12, il existe des limites sur le nombre de descripteurs dans un segment de mémoire CBV/SRV/UAV. Pour plus d’informations, consultez [niveaux matériels](../direct3d12/hardware-support.md) . Séparément, le nombre de UAVs dans toutes les tables de descripteurs est limité à travers toutes les étapes, qui est basé sur le [niveau de liaison de ressources](https://microsoft.github.io/DirectX-Specs/d3d/ResourceBinding.html#levels-of-hardware-support).

Pour plus d’informations sur la prise en charge des formats à différents niveaux de fonctionnalités matérielles, consultez :

- [Prise en charge du format DXGI pour le matériel de niveau de fonctionnalité Direct3D 12,1](../direct3ddxgi/hardware-support-for-direct3d-12-1-formats.md)
- [Prise en charge du format DXGI pour le matériel de niveau de fonctionnalité Direct3D 12,0](../direct3ddxgi/hardware-support-for-direct3d-12-0-formats.md)
- [Prise en charge du format DXGI pour le matériel de niveau de fonctionnalité Direct3D 11,1](../direct3ddxgi/format-support-for-direct3d-11-1-feature-level-hardware.md)
- [Prise en charge du format DXGI pour le matériel de niveau de fonctionnalité Direct3D 11,0](../direct3ddxgi/format-support-for-direct3d-11-0-feature-level-hardware.md)
- [Prise en charge matérielle pour les formats Direct3D 10Level9](/previous-versions/ff471324(v=vs.85))
- [Prise en charge du matériel pour les formats Direct3D 10,1](/previous-versions/cc627091(v=vs.85))
- [Prise en charge matérielle pour les formats Direct3D 10](/previous-versions/cc627090(v=vs.85))

## <a name="related-topics"></a>Rubriques connexes

* [Direct3D 11 sur du matériel de niveau inférieur](overviews-direct3d-11-devices-downlevel.md)
* [Niveaux de fonctionnalité matérielle (Direct3D 12)](../direct3d12/hardware-feature-levels.md)