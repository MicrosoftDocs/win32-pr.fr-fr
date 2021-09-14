---
title: Affichages triés par rastérisation
description: Les vues pixellisées (ROVs) permettent au code de nuanceur de pixels de marquer des liaisons de vue d’accès non ordonnées avec une déclaration qui modifie les exigences normales pour l’ordre des résultats de pipeline graphique pour UAVs.
ms.assetid: D308BF3E-8CBE-4DF0-B020-4D202E858D99
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a19988d3f3eec39e8fc298a2fc13031ecc29e3e8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127012918"
---
# <a name="rasterizer-ordered-views"></a>Affichages triés par rastérisation

Les vues pixellisées (ROVs) autorisent le code de nuanceur de pixels à marquer des liaisons de vue d’accès non triée (UAV) avec une déclaration qui modifie les exigences normales pour l’ordre des résultats de pipeline graphique pour UAVs. Cela permet l’utilisation d’algorithmes de transparence OIT (Order-Independent transparent), ce qui donne de meilleurs résultats de rendu lorsque plusieurs objets transparents sont alignés les uns avec les autres dans une vue.

-   [Vue d'ensemble](#overview)
-   [Informations d’implémentation](#implementation-details)
-   [API summary](#api-summary)
-   [Rubriques connexes](#related-topics)

## <a name="overview"></a>Vue d’ensemble

Les pipelines graphiques standard peuvent avoir des difficultés à converser correctement ensemble plusieurs textures qui contiennent de la transparence. Les objets tels que les clôtures de câble, les fumées, les incendies, les végétations et les verres de couleur utilisent la transparence pour atteindre l’effet souhaité. Des problèmes surviennent lorsque plusieurs textures contenant de la transparence sont alignées les unes avec les autres (fumée devant une clôture devant une couche de verre contenant de la végétation, par exemple). Les vues ROVs (rastériseur-ordered views) permettent aux algorithmes OIT sous-jacents d’utiliser les fonctionnalités du matériel pour tenter de résoudre correctement l’ordre de transparence. La transparence est gérée par le nuanceur de pixels.

Les vues ROVs (rastériseur-ordered views) autorisent le code du nuanceur de pixels à marquer des liaisons UAV avec une déclaration qui modifie les exigences normales pour l’ordre des résultats de la canalisation Graphics pour UAVs.

ROVs garantissent l’ordre des accès à UAV pour toutes les paires d’appels de nuanceur de pixels qui se chevauchent. Dans ce cas, « se chevauchant » signifie que les appels sont générés par les mêmes appels de dessin et partagent la même coordonnée de pixels en mode d’exécution de fréquence en pixels, et les mêmes coordonnées et coordonnée de l’échantillon en mode échantillonnage-fréquence.

L’ordre dans lequel les accès ROV se chevauchant aux appels de nuanceur de pixels sont exécutés est identique à l’ordre dans lequel la géométrie est soumise. Cela signifie que, pour les appels de nuanceur de pixels qui se chevauchent, les écritures ROV effectuées par un appel de nuanceur de pixels doivent être disponibles pour être lues par un appel ultérieur et ne doivent pas affecter les lectures effectuées par un appel précédent. Les lectures ROV effectuées par un appel de nuanceur de pixels doivent refléter les écritures par un appel précédent et ne doivent pas refléter les écritures par un appel ultérieur. Cela est important pour UAVs, car ils sont explicitement omis des garanties de non-variance de sortie définies normalement par l’ordre fixe des résultats de la canalisation Graphics.

## <a name="implementation-details"></a>Informations d’implémentation

Les vues ROVs (rastériseur-ordered views) sont déclarées avec les nouveaux objets HLSL (High Level Shader Language) suivants, et sont uniquement disponibles pour le nuanceur de pixels :

-   `RasterizerOrderedBuffer`
-   `RasterizerOrderedByteAddressBuffer`
-   `RasterizerOrderedStructuredBuffer`
-   `RasterizerOrderedTexture1D`
-   `RasterizerOrderedTexture1DArray`
-   `RasterizerOrderedTexture2D`
-   `RasterizerOrderedTexture2DArray`
-   `RasterizerOrderedTexture3D`

Utilisez ces objets de la même façon que les autres objets UAV (tels que `RWBuffer` etc.).

## <a name="api-summary"></a>Résumé des API

Les ROVs sont une construction en HLSL uniquement qui applique une sémantique de comportement différente à UAVs. Toutes les API relatives à UAVs sont également pertinentes pour ROVs. Notez que la méthode, les structures et la classe d’assistance suivantes référencent le rastériseur :

-   [**D3D12 \_ RASTÉRISEUR \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rasterizer_desc) : structure contenant la description du rastériseur.
-   [**D3D12 \_ \_ \_ \_ Options D3D12 données**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options) de la fonctionnalité : structure contenant un booléen, indiquant la prise en charge.
-   [**CheckFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport) : méthode permettant d’accéder aux fonctionnalités prises en charge.
-   [**CD3DX12 \_ RASTÉRISEUR \_ desc**](cd3dx12-rasterizer-desc.md) : classe d’assistance pour la création de descriptions de rastériseur.
-   [**D3D12 \_ Description de l' \_ \_ état \_ du pipeline Graphics**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc) : structure contenant l’état du pipeline.

## <a name="related-topics"></a>Rubriques connexes

* [Pixellisation conservatrice](conservative-rasterization.md)
* [Rendu](rendering.md)
* [Liaison de ressource dans HSL](resource-binding-in-hlsl.md)
* [Modèle de nuanceur 5,1](/windows/desktop/direct3dhlsl/shader-model-5-1)