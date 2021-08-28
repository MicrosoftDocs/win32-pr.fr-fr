---
title: Le chargement de la vue d’accès non triée (UAV) typée
description: En savoir plus sur la charge typée de vue d’accès non ordonnée (UAV) dans Direct3D 12. La charge typée UAV est la capacité d’un nuanceur à lire à partir d’un UAV avec un DXGI_FORMAT spécifique.
ms.assetid: 6106D15E-EAF6-4583-B4F2-7CC7EE30DE15
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3bd45c1b2c14aa85ec9b9ab65cd6d6a9f33cb5e0995ac20b779b84aa7bed640
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119123476"
---
# <a name="typed-unordered-access-view-uav-loads"></a>Le chargement de la vue d’accès non triée (UAV) typée

Le chargement typé de vue d’accès non triée (UAV) est la possibilité pour un nuanceur de lire à partir d’un UAV avec un [**\_ format dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)spécifique.

-   [Vue d'ensemble](#overview)
-   [Formats et appels d’API pris en charge](#supported-formats-and-api-calls)
-   [Utilisation de chargements UAV typés à partir de HLSL](#using-typed-uav-loads-from-hlsl)
-   [Utilisation des charges UAV typées UNORM et RONFLEr à partir du langage HLSL](#using-unorm-and-snorm-typed-uav-loads-from-hlsl)
-   [Rubriques connexes](#related-topics)

## <a name="overview"></a>Vue d’ensemble

Une vue d’accès non triée (UAV) est une vue d’une ressource d’accès non ordonnée (qui peut inclure des mémoires tampons, des textures et des tableaux de texture, mais sans échantillonnage multiple). Un UAV autorise l’accès en lecture/écriture non ordonné de manière temporelle à partir de plusieurs threads. Cela signifie que ce type de ressource peut être lu/écrit simultanément par plusieurs threads sans générer de conflits de mémoire. Cet accès simultané est géré par le biais de l’utilisation de [fonctions atomiques](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-atomic-functions).

D3D12 (et D3D 11.3) s’étend sur la liste des formats qui peuvent être utilisés avec les charges UAV typées.

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
-   R8G8 \_ Saint-
-   R16 \_ UNORM
-   R16 \_ ronfler
-   R8 \_ ronfler
-   A8 \_ UNORM
-   B5G6R5 \_ UNORM
-   B5G5R5A1 \_ UNORM
-   B4G4R4A4 \_ UNORM

Pour déterminer la prise en charge de tout autre format, appelez [**CheckFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport) avec la structure d' [**\_ \_ \_ \_ options D3D12 des données de la fonctionnalité D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options) en tant que premier paramètre (reportez-vous à [fonctionnalité interrogation](capability-querying.md)). Le champ *TypedUAVLoadAdditionalFormats* est défini si la liste « pris en charge en tant que jeu » ci-dessus est prise en charge. Effectuer un deuxième appel à **CheckFeatureSupport**, à l’aide d’une structure de [**\_ \_ \_ \_ prise en charge du format de données de la fonctionnalité D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_format_support) (vérification de la structure retournée par rapport à la structure D3D12 membre de \_ \_ \_ \_ chargement de type d’élément UAV \_ de l’énumération de [**\_ format \_ de D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support2) ) pour déterminer la prise en charge dans la liste des formats éventuellement pris en charge, par exemple :

``` syntax
D3D12_FEATURE_DATA_D3D12_OPTIONS FeatureData;
ZeroMemory(&FeatureData, sizeof(FeatureData));
HRESULT hr = pDevice->CheckFeatureSupport(D3D12_FEATURE_D3D12_OPTIONS, &FeatureData, sizeof(FeatureData));
if (SUCCEEDED(hr))
{
    // TypedUAVLoadAdditionalFormats contains a Boolean that tells you whether the feature is supported or not
    if (FeatureData.TypedUAVLoadAdditionalFormats)
    {
        // Can assume “all-or-nothing” subset is supported (e.g. R32G32B32A32_FLOAT)
        // Cannot assume other formats are supported, so we check:
        D3D12_FEATURE_DATA_FORMAT_SUPPORT FormatSupport = {DXGI_FORMAT_R32G32_FLOAT, D3D12_FORMAT_SUPPORT1_NONE, D3D12_FORMAT_SUPPORT2_NONE};
        hr = pDevice->CheckFeatureSupport(D3D12_FEATURE_FORMAT_SUPPORT, &FormatSupport, sizeof(FormatSupport));
        if (SUCCEEDED(hr) && (FormatSupport.Support2 & D3D12_FORMAT_SUPPORT2_UAV_TYPED_LOAD) != 0)
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

## <a name="using-unorm-and-snorm-typed-uav-loads-from-hlsl"></a>Utilisation des charges UAV typées UNORM et RONFLEr à partir du langage HLSL

Lorsque vous utilisez des chargements UAV typés pour lire à partir d’une ressource UNORM ou RONFLEr, vous devez déclarer correctement le type d’élément de l’objet HLSL sur `unorm` ou `snorm` . Elle est spécifiée comme un comportement indéfini pour incompatibilité avec le type d’élément déclaré en HLSL avec le type de données de ressource sous-jacent. Par exemple, si vous utilisez des charges UAV typées sur une ressource de mémoire tampon avec des \_ données R8 UNORM, vous devez déclarer le type d’élément comme `unorm float` suit :

``` syntax
RWBuffer<unorm float> uav;
```

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Rendu](rendering.md)
</dt> <dt>

[Liaison de ressource](resource-binding.md)
</dt> <dt>

[Liaison de ressource dans HSL](resource-binding-in-hlsl.md)
</dt> <dt>

[Modèle de nuanceur 5,1](/windows/desktop/direct3dhlsl/shader-model-5-1)
</dt> <dt>

[Spécification de signatures racine en langage HLSL](specifying-root-signatures-in-hlsl.md)
</dt> </dl>

 

 