---
title: Chargements de vues d’accès non ordonnées typées
description: En savoir plus sur la charge typée de la vue d’accès non triée (UAV) dans Direct3D 11. La charge typée UAV est la capacité d’un nuanceur à lire à partir d’un UAV avec un DXGI_FORMAT spécifique.
ms.assetid: BA72BF21-8621-461D-8677-9DFB7D5BC6AA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c6d2cbfa51c8473dc3da51c5844c63bef944b50
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396284"
---
# <a name="typed-unordered-access-view-loads"></a>Chargements de vues d’accès non ordonnées typées

Le chargement typé de vue d’accès non triée (UAV) est la possibilité pour un nuanceur de lire à partir d’un UAV avec un format DXGI spécifique \_ .

-   [Vue d'ensemble](#overview)
-   [Formats et appels d’API pris en charge](#supported-formats-and-api-calls)
-   [Utilisation de chargements UAV typés à partir de HLSL](#using-typed-uav-loads-from-hlsl)
-   [Rubriques connexes](#related-topics)

## <a name="overview"></a>Vue d’ensemble

Une vue d’accès non triée (UAV) est une vue d’une ressource d’accès non ordonnée (qui peut inclure des mémoires tampons, des textures et des tableaux de texture, mais sans échantillonnage multiple). Un UAV autorise l’accès en lecture/écriture non ordonné de manière temporelle à partir de plusieurs threads. Cela signifie que ce type de ressource peut être lu/écrit simultanément par plusieurs threads sans générer de conflits de mémoire. Cet accès simultané est géré par le biais de l’utilisation de [fonctions atomiques](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-atomic-functions).

D3D12 et D3D 11.3 se développent dans la liste des formats qui peuvent être utilisés avec les charges UAV typées.

## <a name="supported-formats-and-api-calls"></a>Formats et appels d’API pris en charge

Auparavant, les trois formats suivants prenait en charge les chargements UAV typés, et étaient requis pour le matériel D3D 11.0. Ils sont pris en charge pour tous les matériels D3D 11.3 et D3D12.

-   R32 \_ float
-   R32 \_ uint
-   R32 \_ Saint-

Les formats suivants sont pris en charge en tant qu’ensemble sur le matériel D3D12 ou D3D 11,3. si l’un d’eux est pris en charge, tous sont pris en charge.

-   R32G32B32A32 \_ float
-   R32G32B32A32 \_ uint
-   R32G32B32A32 \_ Saint-
-   R16G16B16A16 \_ float
-   R16G16B16A16 \_ uint
-   R16G16B16A16 \_ Saint-
-   R8G8B8A8 \_ UNORM
-   R8G8B8A8 \_ uint
-   R8G8B8A8 \_ Saint-
-   R16 \_ float
-   R16 \_ uint
-   R16 \_ Saint-
-   R8 \_ UNORM
-   R8 \_ uint
-   R8 \_ Saint-

Les formats suivants sont facultatifs et individuellement pris en charge sur le matériel D3D12 et D3D 11.3. par conséquent, une seule requête doit être effectuée sur chaque format pour tester la prise en charge.

-   R16G16B16A16 \_ UNORM
-   R16G16B16A16 \_ ronfler
-   R32G32 \_ float
-   R32G32 \_ uint
-   R32G32 \_ Saint-
-   R10G10B10A2 \_ UNORM
-   R10G10B10A2 \_ uint
-   R11G11B10 \_ float
-   R8G8B8A8 \_ ronfler
-   R16G16 \_ float
-   R16G16 \_ UNORM
-   R16G16 \_ uint
-   R16G16 \_ ronfler
-   R16G16 \_ Saint-
-   R8G8 \_ UNORM
-   R8G8 \_ uint
-   R8G8 \_ ronfler
-   8G8 \_ Saint-
-   R16 \_ UNORM
-   R16 \_ ronfler
-   R8 \_ ronfler
-   A8 \_ UNORM
-   B5G6R5 \_ UNORM
-   B5G5R5A1 \_ UNORM
-   B4G4R4A4 \_ UNORM

Pour déterminer la prise en charge de tout autre format, appelez [**ID3D11Device :: CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) avec la structure [**\_ \_ \_ d3d11 \_ OPTIONS2 des données de la fonctionnalité d3d11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options2) en tant que premier paramètre. Le `TypedUAVLoadAdditionalFormats` bit est défini si la liste « pris en charge en tant que jeu » ci-dessus est prise en charge. Effectuez un deuxième appel à **CheckFeatureSupport**, à l’aide de la structure de données de la [**fonctionnalité d3d11, (vérification \_ \_ \_ \_**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_format_support2) de la structure retournée par rapport au D3D12 \_ format \_ de chargement de type d’élément \_ UAV \_ \_ de l’énumération de format d3d11) pour déterminer la prise en charge dans la liste des formats éventuellement pris en charge ci-dessus, par exemple : [**\_ \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_format_support2)

``` syntax
D3D11_FEATURE_DATA_D3D11_OPTIONS2 FeatureData;
ZeroMemory(&FeatureData, sizeof(FeatureData));
HRESULT hr = pDevice->CheckFeatureSupport(D3D11_FEATURE_D3D11_OPTIONS2, &FeatureData, sizeof(FeatureData));
if (SUCCEEDED(hr))
{
    // TypedUAVLoadAdditionalFormats contains a Boolean that tells you whether the feature is supported or not
    if (FeatureData.TypedUAVLoadAdditionalFormats)
    {
        // Can assume “all-or-nothing” subset is supported (e.g. R32G32B32A32_FLOAT)
        // Can not assume other formats are supported, so we check:
        D3D11_FEATURE_DATA_FORMAT_SUPPORT2 FormatSupport;
        ZeroMemory(&FormatSupport, sizeof(FormatSupport));
        FormatSupport.InFormat = DXGI_FORMAT_R32G32_FLOAT;
        hr = pDevice->CheckFeatureSupport(D3D11_FEATURE_FORMAT_SUPPORT2, &FormatSupport, sizeof(FormatSupport));
        if (SUCCEEDED(hr) && (FormatSupport.OutFormatSupport2 & D3D11_FORMAT_SUPPORT2_UAV_TYPED_LOAD) != 0)
        {
            // DXGI_FORMAT_R32G32_FLOAT supports UAV Typed Load!
        }
    }
}
```

## <a name="using-typed-uav-loads-from-hlsl"></a>Utilisation de chargements UAV typés à partir de HLSL

Pour les UAVs typés, l’indicateur HLSL est un \_ nuanceur D3D \_ nécessitant \_ \_ \_ \_ des formats supplémentaires de chargement UAV \_ .

Voici un exemple de code de nuanceur pour traiter une charge de UAV typée :

``` syntax
RWTexture2D<float4> uav1;
uint2 coord;
float4 main() : SV_Target
{
  return uav1.Load(coord);
}
```

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Fonctionnalités Direct3D 11,3](direct3d-11-3-features.md)
</dt> <dt>

[Modèle de nuanceur 5,1](/windows/desktop/direct3dhlsl/shader-model-5-1)
</dt> </dl>

 

 