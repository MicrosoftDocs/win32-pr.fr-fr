---
title: Vues de l’ordre du rastériseur
description: Les vues triées du rastériseur (ROVs) autorisent le code du nuanceur de pixels à marquer des liaisons UAV avec une déclaration qui modifie les exigences normales pour l’ordre des résultats de la canalisation Graphics pour UAVs.
ms.assetid: 7FCFCD28-E68D-4594-8879-937F57245507
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d891701aeaadd6f4474aeed8303d9b0046d1b656
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127517056"
---
# <a name="rasterizer-order-views"></a>Vues de l’ordre du rastériseur

Les vues triées du rastériseur (ROVs) autorisent le code du nuanceur de pixels à marquer des liaisons UAV avec une déclaration qui modifie les exigences normales pour l’ordre des résultats de la canalisation Graphics pour UAVs. Cela permet l’utilisation d’algorithmes OIT (commande Independent transparent), ce qui donne de meilleurs résultats de rendu lorsque plusieurs objets transparents sont alignés les uns avec les autres dans une vue.

-   [Vue d'ensemble](#overview)
-   [Informations d’implémentation](#implementation-details)
-   [API summary](#api-summary)
-   [Rubriques connexes](#related-topics)

## <a name="overview"></a>Vue d’ensemble

Les pipelines graphiques standard peuvent avoir des difficultés à converser correctement ensemble plusieurs textures qui contiennent de la transparence. Les objets tels que les clôtures de câble, les fumées, les incendies, les végétations et les verres de couleur utilisent la transparence pour atteindre l’effet souhaité. Des problèmes surviennent lorsque plusieurs textures contenant de la transparence sont alignées les unes avec les autres (fumée devant une clôture devant une couche de verre contenant de la végétation, par exemple). Les vues triées du rastériseur (ROVs) permettent aux algorithmes OIT sous-jacents d’utiliser les fonctionnalités du matériel pour tenter de résoudre correctement l’ordre de transparence. La transparence est gérée par le nuanceur de pixels.

Les vues triées du rastériseur (ROVs) autorisent le code du nuanceur de pixels à marquer des liaisons UAV avec une déclaration qui modifie les exigences normales pour l’ordre des résultats de la canalisation Graphics pour UAVs.

ROVs garantissent l’ordre des accès à UAV pour toutes les paires d’appels de nuanceur de pixels qui se chevauchent. Dans ce cas, « se chevauchant » signifie que les appels sont générés par les mêmes appels de dessin et partagent la même coordonnée de pixels en mode d’exécution de fréquence en pixels, et les mêmes coordonnées et coordonnée de l’échantillon en mode échantillonnage-fréquence.

L’ordre dans lequel les accès ROV se chevauchant aux appels de nuanceur de pixels sont exécutés est identique à l’ordre dans lequel la géométrie est soumise. Cela signifie que, pour les appels de nuanceur de pixels qui se chevauchent, les écritures ROV effectuées par un appel de nuanceur de pixels doivent être disponibles pour être lues par un appel ultérieur et ne doivent pas affecter les lectures effectuées par un appel précédent. Les lectures ROV effectuées par un appel de nuanceur de pixels doivent refléter les écritures par un appel précédent et ne doivent pas refléter les écritures par un appel ultérieur. Cela est important pour UAVs, car ils sont explicitement omis des garanties de non-variance de sortie définies normalement par l’ordre fixe des résultats de la canalisation Graphics.

## <a name="implementation-details"></a>Informations d’implémentation

Les vues triées du rastériseur (ROVs) sont déclarées avec les nouveaux objets HLSL (High Level Shader Language) suivants, et sont uniquement disponibles pour le nuanceur de pixels :

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

-   [**D3d11 \_ RASTÉRISEUR \_ DESC2**](/windows/desktop/api/D3D11_3/ns-d3d11_3-cd3d11_rasterizer_desc2) : structure contenant la description du rastériseur, en notant la \_ \_ classe d’assistance CD3D12 rastériseur DESC2 pour la création de descriptions de rastériseur.
-   [**D3d11 \_ Données de fonctionnalités \_ \_ d3d11 \_ OPTIONS2**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options2) : structure contenant la valeur booléenne `ROVsSupported` , indiquant la prise en charge.
-   [**ID3D11Device :: CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) : méthode permettant d’accéder aux fonctionnalités prises en charge.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Fonctionnalités Direct3D 11,3](direct3d-11-3-features.md)
</dt> <dt>

[Modèle de nuanceur 5,1](/windows/desktop/direct3dhlsl/shader-model-5-1)
</dt> </dl>

 

 